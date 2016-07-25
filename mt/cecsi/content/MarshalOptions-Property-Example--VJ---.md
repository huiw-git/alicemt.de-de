---
title: "MarshalOptions Property Example (VJ++)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 9475c5f9-3a63-42cb-818c-4268e938a25c
caps.latest.revision: 9
caps.handback.revision: 9
manager: sonalm
translation.priority.ht: 
  - de-de
  - es-es
  - fr-fr
  - it-it
  - ja-jp
  - ko-kr
  - pt-br
  - ru-ru
  - zh-cn
  - zh-tw
---
# MarshalOptions Property Example (VJ++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c21547979ca9b20334bcdee5d7bc0267" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="390c8abf-133e-40da-8b99-8f748a983e4f">MarshalOptions</legacyLink> property to specify what rows are sent back to the server—All Rows or only Modified Rows.</caps:sentence>
        </para>
        <code>// BeginMarshalOptionsJ
import java.io.*;
import com.ms.wfc.data.*;

public class MarshalOptionsX
{
   // The main entry point for the application.
   public static void main (String[] args)
   {
      MarshalOptionsX();
      System.exit(0);
   }
   // MarshalX Function

   static void MarshalOptionsX()
   {
      // Define ADO Objects
      Recordset rstEmployees = null;

      // Declarations
      BufferedReader in = 
         new BufferedReader(new InputStreamReader(System.in));
      String line = null;

      try
      {

         // Open Recordset with names from Employees Table.
         String strCnn = " Provider='sqloledb';Data Source='MySqlServer';" +
                "Initial Catalog='Pubs';Integrated Security='SSPI';";

         rstEmployees = new Recordset();
         rstEmployees.setCursorType(AdoEnums.CursorType.KEYSET);
         rstEmployees.setLockType(AdoEnums.LockType.OPTIMISTIC);
         rstEmployees.setCursorLocation(AdoEnums.CursorLocation.CLIENT);

         rstEmployees.open(
            "SELECT fname,lname from Employee ORDER BY lname", 
            strCnn,AdoEnums.CursorType.KEYSET, 
            AdoEnums.LockType.OPTIMISTIC, AdoEnums.CommandType.TEXT);

         // Store original data
         String strOldFirst = rstEmployees.getField("fname").getString();
         String strOldLast = rstEmployees.getField("lname").getString();

         // Change data in edit buffer
         rstEmployees.getField("fname").setString("Linda");
         rstEmployees.getField("lname").setString("Kobara");

         // Show contents of buffer and get user input
         String strMessage = "Edit in progress: "+ "\n"+
                   "Original Data  = \t"+ strOldFirst +" "+
                   strOldLast + "\n" + "Data in Buffer = \t"+
                   rstEmployees.getField("fname").getString()+ " " +
                   rstEmployees.getField("lname").getString()+"\n"+"\n"+
                   "Use Update to replace the original data with " +
                   "the buffered data in the recordset";
         String strMarshalAll = "Would you like to send all the rows" +
                     " in the recordset back to the server";
         String strMarshalModified = "Would you like to send only "+
                         " modified rows back to the server";

         System.out.println(strMessage + "\nEnter (Y/N)...");

         if (in.readLine().equalsIgnoreCase("Y"))
         {
            System.out.println(strMarshalAll);
            System.out.println("\nEnter (Y/N)...");

            if(in.readLine().equalsIgnoreCase("Y"))
            {
               rstEmployees.setMarshalOptions(AdoEnums.MarshalOptions.ALL);
               rstEmployees.update();
            }
            else
            {
               System.out.println(strMarshalModified);
               System.out.println("\nEnter (Y/N)...");

               if (in.readLine().equalsIgnoreCase("Y"))
               {
                  rstEmployees.setMarshalOptions(
                     AdoEnums.MarshalOptions.MODIFIEDONLY);
                  rstEmployees.update();
               }
            }

         }

         // Show the resulting data
         System.out.println("\nData in recordset = " + 
            rstEmployees.getField("fname").getString() + 
            " " + rstEmployees.getField("lname").getString());

         // Restore original data because this is a demonstration
         if (!((strOldFirst.equals(rstEmployees.getField("fname")))
            &amp;&amp;(strOldLast.equals(rstEmployees.getField("lname")))))
         {
            rstEmployees.getField("fname").setString(strOldFirst);
            rstEmployees.getField("lname").setString(strOldLast);
            rstEmployees.update();
         }
         
         System.out.println("\n\nPress &lt;Enter&gt; to continue..");
         in.readLine();
      }

      catch(AdoException ae)
      {
         // Notify the user of any errors that result from ADO

         // As passing a connection, check for null pointer first
         if(rstEmployees!= null)
         {
            PrintProviderError(rstEmployees.getActiveConnection());
         }
         else
         {
            System.out.println("Exception: " + ae.getLocalizedMessage());
         }
      }

      // System Read requires this catch
      catch(java.io.IOException je)
      {
         PrintIOError(je);
      }   
      
      finally
      {
         // Cleanup objects before exit.   
         if (rstEmployees != null)
            if (rstEmployees.getState() == 1)
               rstEmployees.close();
      }
   }

   // PrintProviderError Function

   static void PrintProviderError( Connection Cnn1 )
   {
      // Print Provider errors from Connection object.
      // ErrItem is an item object in the Connections Errors collection.
      com.ms.wfc.data.Error  ErrItem = null;
      long nCount = 0;
      int  i      = 0;

      nCount = Cnn1.getErrors().getCount();

      // If there are any errors in the collection, print them.
      if( nCount &gt; 0);
      {
         // Collection ranges from 0 to nCount - 1
         for (i = 0; i&lt; nCount; i++)
         {
            ErrItem = Cnn1.getErrors().getItem(i);
            System.out.println("\t Error number: " + ErrItem.getNumber()
               + "\t" + ErrItem.getDescription() );
         }
      }

   }

   // PrintIOError Function

   static void PrintIOError( java.io.IOException je)
   {
      System.out.println("Error \n");
      System.out.println("\tSource = " + je.getClass() + "\n");
      System.out.println("\tDescription = " + je.getMessage() + "\n");
   }
}
// EndMarshalOptionsJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="390c8abf-133e-40da-8b99-8f748a983e4f">MarshalOptions Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="390c8abf-133e-40da-8b99-8f748a983e4f">MarshalOptions</legacyLink> property to specify what rows are sent back to the server—All Rows or only Modified Rows.</caps:sentence>
        </para>
        <code>// BeginMarshalOptionsJ
import java.io.*;
import com.ms.wfc.data.*;

public class MarshalOptionsX
{
   // The main entry point for the application.
   public static void main (String[] args)
   {
      MarshalOptionsX();
      System.exit(0);
   }
   // MarshalX Function

   static void MarshalOptionsX()
   {
      // Define ADO Objects
      Recordset rstEmployees = null;

      // Declarations
      BufferedReader in = 
         new BufferedReader(new InputStreamReader(System.in));
      String line = null;

      try
      {

         // Open Recordset with names from Employees Table.
         String strCnn = " Provider='sqloledb';Data Source='MySqlServer';" +
                "Initial Catalog='Pubs';Integrated Security='SSPI';";

         rstEmployees = new Recordset();
         rstEmployees.setCursorType(AdoEnums.CursorType.KEYSET);
         rstEmployees.setLockType(AdoEnums.LockType.OPTIMISTIC);
         rstEmployees.setCursorLocation(AdoEnums.CursorLocation.CLIENT);

         rstEmployees.open(
            "SELECT fname,lname from Employee ORDER BY lname", 
            strCnn,AdoEnums.CursorType.KEYSET, 
            AdoEnums.LockType.OPTIMISTIC, AdoEnums.CommandType.TEXT);

         // Store original data
         String strOldFirst = rstEmployees.getField("fname").getString();
         String strOldLast = rstEmployees.getField("lname").getString();

         // Change data in edit buffer
         rstEmployees.getField("fname").setString("Linda");
         rstEmployees.getField("lname").setString("Kobara");

         // Show contents of buffer and get user input
         String strMessage = "Edit in progress: "+ "\n"+
                   "Original Data  = \t"+ strOldFirst +" "+
                   strOldLast + "\n" + "Data in Buffer = \t"+
                   rstEmployees.getField("fname").getString()+ " " +
                   rstEmployees.getField("lname").getString()+"\n"+"\n"+
                   "Use Update to replace the original data with " +
                   "the buffered data in the recordset";
         String strMarshalAll = "Would you like to send all the rows" +
                     " in the recordset back to the server";
         String strMarshalModified = "Would you like to send only "+
                         " modified rows back to the server";

         System.out.println(strMessage + "\nEnter (Y/N)...");

         if (in.readLine().equalsIgnoreCase("Y"))
         {
            System.out.println(strMarshalAll);
            System.out.println("\nEnter (Y/N)...");

            if(in.readLine().equalsIgnoreCase("Y"))
            {
               rstEmployees.setMarshalOptions(AdoEnums.MarshalOptions.ALL);
               rstEmployees.update();
            }
            else
            {
               System.out.println(strMarshalModified);
               System.out.println("\nEnter (Y/N)...");

               if (in.readLine().equalsIgnoreCase("Y"))
               {
                  rstEmployees.setMarshalOptions(
                     AdoEnums.MarshalOptions.MODIFIEDONLY);
                  rstEmployees.update();
               }
            }

         }

         // Show the resulting data
         System.out.println("\nData in recordset = " + 
            rstEmployees.getField("fname").getString() + 
            " " + rstEmployees.getField("lname").getString());

         // Restore original data because this is a demonstration
         if (!((strOldFirst.equals(rstEmployees.getField("fname")))
            &amp;&amp;(strOldLast.equals(rstEmployees.getField("lname")))))
         {
            rstEmployees.getField("fname").setString(strOldFirst);
            rstEmployees.getField("lname").setString(strOldLast);
            rstEmployees.update();
         }
         
         System.out.println("\n\nPress &lt;Enter&gt; to continue..");
         in.readLine();
      }

      catch(AdoException ae)
      {
         // Notify the user of any errors that result from ADO

         // As passing a connection, check for null pointer first
         if(rstEmployees!= null)
         {
            PrintProviderError(rstEmployees.getActiveConnection());
         }
         else
         {
            System.out.println("Exception: " + ae.getLocalizedMessage());
         }
      }

      // System Read requires this catch
      catch(java.io.IOException je)
      {
         PrintIOError(je);
      }   
      
      finally
      {
         // Cleanup objects before exit.   
         if (rstEmployees != null)
            if (rstEmployees.getState() == 1)
               rstEmployees.close();
      }
   }

   // PrintProviderError Function

   static void PrintProviderError( Connection Cnn1 )
   {
      // Print Provider errors from Connection object.
      // ErrItem is an item object in the Connections Errors collection.
      com.ms.wfc.data.Error  ErrItem = null;
      long nCount = 0;
      int  i      = 0;

      nCount = Cnn1.getErrors().getCount();

      // If there are any errors in the collection, print them.
      if( nCount &gt; 0);
      {
         // Collection ranges from 0 to nCount - 1
         for (i = 0; i&lt; nCount; i++)
         {
            ErrItem = Cnn1.getErrors().getItem(i);
            System.out.println("\t Error number: " + ErrItem.getNumber()
               + "\t" + ErrItem.getDescription() );
         }
      }

   }

   // PrintIOError Function

   static void PrintIOError( java.io.IOException je)
   {
      System.out.println("Error \n");
      System.out.println("\tSource = " + je.getClass() + "\n");
      System.out.println("\tDescription = " + je.getMessage() + "\n");
   }
}
// EndMarshalOptionsJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="390c8abf-133e-40da-8b99-8f748a983e4f">MarshalOptions Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>