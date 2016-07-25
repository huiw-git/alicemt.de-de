---
title: "IsolationLevel and Mode Properties Example (VJ++)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 7662d89a-c5f9-44db-8c93-606db48cdd96
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
# IsolationLevel and Mode Properties Example (VJ++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7f4d28714c781ad53c10f5a3a0259fbd" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property to open an exclusive connection, and the <legacyLink xlink:href="ea84e4b2-fbf2-4eef-b9ce-796b22e21800">IsolationLevel</legacyLink> property to open a transaction that is conducted in isolation of other transactions.</caps:sentence>
        </para>
        <code>// BeginIsolationLevelJ
import com.ms.wfc.data.*;
import java.io.*;

public class IsolationLevelX
{
   // The main entry point for the application.
   public static void main (String[] args)
   {
      IsolationLevelX();
      System.exit(0);
   }

   // IsolationLevelX Function

   static void IsolationLevelX()
   {
      // Define ADO Objects
      Connection cnn1 = null;
      Recordset rstTitles = null;

      // Assign connection string to variable
      String strCnn = "Provider='sqloledb';Data Source='MySqlServer';"+
                  "Initial Catalog='Pubs';Integrated Security='SSPI';";

      // Declarations
      BufferedReader in = 
         new BufferedReader ( new InputStreamReader(System.in));
      String line = null;

      try
      {
         // Open connection and Titles table
         cnn1 = new Connection();

         cnn1.setMode(AdoEnums.ConnectMode.SHAREEXCLUSIVE);
         cnn1.setIsolationLevel(AdoEnums.IsolationLevel.ISOLATED);
         cnn1.open(strCnn);

         rstTitles = new Recordset();
         rstTitles.setCursorType(AdoEnums.CursorType.DYNAMIC);
         rstTitles.setLockType(AdoEnums.LockType.PESSIMISTIC);
         rstTitles.open("Titles", cnn1, AdoEnums.CursorType.DYNAMIC, 
            AdoEnums.LockType.PESSIMISTIC);

         cnn1.beginTrans();

         // Display the connection mode
         if (cnn1.getMode() == AdoEnums.ConnectMode.SHAREEXCLUSIVE)
            System.out.println("\n\tConnection mode is exclusive");
         else
            System.out.println("\n\tConnection mode is not exclusive");
         System.out.println("\nPress &lt;Enter&gt; to continue..");
         in.readLine();

         // Display the Isolation level
         if ( cnn1.getIsolationLevel() == AdoEnums.IsolationLevel.ISOLATED)
            System.out.println("\tTransaction is Isolated\n");
         else
            System.out.println("\tTransaction is not Isolated\n");
         System.out.println("\nPress &lt;Enter&gt; to continue..");
         in.readLine();

         // Change the type of psychology titles
         while(!rstTitles.getEOF())
         {

            if(rstTitles.getField("Type").getString().trim().
               equals(new String("psychology")))
            {
               rstTitles.getField("Type").setString("self_help");
               rstTitles.update();
            }
            rstTitles.moveNext();

         }

         // Print current data in recordset
         rstTitles.requery();
         while(!rstTitles.getEOF())
         {
            System.out.println(rstTitles.getField("Title").getString() + 
               " - " + rstTitles.getField("Type").getString() );
            rstTitles.moveNext();
         }
         System.out.println("\nPress &lt;Enter&gt; to continue..");
         in.readLine();

         // Restore original data
         cnn1.rollbackTrans();
      }
      catch(AdoException ae)
      {
         // Notify the user of any errors that result from ADO

         // As passing a connection, check for null pointer first
         if(cnn1 !=null)
         {
            PrintProviderError(cnn1);
         }
         else
         {
            System.out.println("Exception:" + ae.getLocalizedMessage());
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
         if (rstTitles != null)
            if (rstTitles.getState() == 1)
               rstTitles.close();   
         if (cnn1 != null)
            if (cnn1.getState() == 1)
               cnn1.close();
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
// EndIsolationLevelJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="ea84e4b2-fbf2-4eef-b9ce-796b22e21800">IsolationLevel Property</link>
        <link xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode</legacyLink> property to open an exclusive connection, and the <legacyLink xlink:href="ea84e4b2-fbf2-4eef-b9ce-796b22e21800">IsolationLevel</legacyLink> property to open a transaction that is conducted in isolation of other transactions.</caps:sentence>
        </para>
        <code>// BeginIsolationLevelJ
import com.ms.wfc.data.*;
import java.io.*;

public class IsolationLevelX
{
   // The main entry point for the application.
   public static void main (String[] args)
   {
      IsolationLevelX();
      System.exit(0);
   }

   // IsolationLevelX Function

   static void IsolationLevelX()
   {
      // Define ADO Objects
      Connection cnn1 = null;
      Recordset rstTitles = null;

      // Assign connection string to variable
      String strCnn = "Provider='sqloledb';Data Source='MySqlServer';"+
                  "Initial Catalog='Pubs';Integrated Security='SSPI';";

      // Declarations
      BufferedReader in = 
         new BufferedReader ( new InputStreamReader(System.in));
      String line = null;

      try
      {
         // Open connection and Titles table
         cnn1 = new Connection();

         cnn1.setMode(AdoEnums.ConnectMode.SHAREEXCLUSIVE);
         cnn1.setIsolationLevel(AdoEnums.IsolationLevel.ISOLATED);
         cnn1.open(strCnn);

         rstTitles = new Recordset();
         rstTitles.setCursorType(AdoEnums.CursorType.DYNAMIC);
         rstTitles.setLockType(AdoEnums.LockType.PESSIMISTIC);
         rstTitles.open("Titles", cnn1, AdoEnums.CursorType.DYNAMIC, 
            AdoEnums.LockType.PESSIMISTIC);

         cnn1.beginTrans();

         // Display the connection mode
         if (cnn1.getMode() == AdoEnums.ConnectMode.SHAREEXCLUSIVE)
            System.out.println("\n\tConnection mode is exclusive");
         else
            System.out.println("\n\tConnection mode is not exclusive");
         System.out.println("\nPress &lt;Enter&gt; to continue..");
         in.readLine();

         // Display the Isolation level
         if ( cnn1.getIsolationLevel() == AdoEnums.IsolationLevel.ISOLATED)
            System.out.println("\tTransaction is Isolated\n");
         else
            System.out.println("\tTransaction is not Isolated\n");
         System.out.println("\nPress &lt;Enter&gt; to continue..");
         in.readLine();

         // Change the type of psychology titles
         while(!rstTitles.getEOF())
         {

            if(rstTitles.getField("Type").getString().trim().
               equals(new String("psychology")))
            {
               rstTitles.getField("Type").setString("self_help");
               rstTitles.update();
            }
            rstTitles.moveNext();

         }

         // Print current data in recordset
         rstTitles.requery();
         while(!rstTitles.getEOF())
         {
            System.out.println(rstTitles.getField("Title").getString() + 
               " - " + rstTitles.getField("Type").getString() );
            rstTitles.moveNext();
         }
         System.out.println("\nPress &lt;Enter&gt; to continue..");
         in.readLine();

         // Restore original data
         cnn1.rollbackTrans();
      }
      catch(AdoException ae)
      {
         // Notify the user of any errors that result from ADO

         // As passing a connection, check for null pointer first
         if(cnn1 !=null)
         {
            PrintProviderError(cnn1);
         }
         else
         {
            System.out.println("Exception:" + ae.getLocalizedMessage());
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
         if (rstTitles != null)
            if (rstTitles.getState() == 1)
               rstTitles.close();   
         if (cnn1 != null)
            if (cnn1.getState() == 1)
               cnn1.close();
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
// EndIsolationLevelJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="ea84e4b2-fbf2-4eef-b9ce-796b22e21800">IsolationLevel Property</link>
        <link xlink:href="808661eb-0d7c-4e6d-8e40-9dc3bef3d77a">Mode Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>