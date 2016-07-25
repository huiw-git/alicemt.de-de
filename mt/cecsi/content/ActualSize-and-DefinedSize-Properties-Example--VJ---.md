---
title: "ActualSize and DefinedSize Properties Example (VJ++)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 2a0936e6-6452-4fef-9295-50407a13d691
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
# ActualSize and DefinedSize Properties Example (VJ++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c7dd961455ffb400a9c5d53b5e462806" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="722803d0-cef5-4d4c-b79d-3f2f58052229">ActualSize</legacyLink> and <legacyLink xlink:href="3ee27314-a305-4fbc-8433-9ee9a909afd6">DefinedSize</legacyLink> properties to display the defined size and actual size of a field.</caps:sentence>
        </para>
        <code>// BeginActualSizeJ
import com.ms.wfc.data.*;
import java.io.*;

public class ActualSizeX
{
   // The main entry point for the application.

   public static void main (String[] args)
   {
      ActualSizeX();
      System.exit(0);
   }

   // ActualSizeX function

   static void ActualSizeX()
   {

      // Define ADO Objects.
      Recordset rstStores = null;

      // Declarations.
      BufferedReader in = new 
         BufferedReader(new InputStreamReader(System.in));
      String line = null;
      String strCnn = "Provider='sqloledb';Data Source='MySqlServer';"
         + "Initial Catalog='Pubs';Integrated Security='SSPI';";

      String strStoreName;
      String strMessage;
      String strDSize,strASize;
      int intDefinedSize;
      int intActualSize;
      int intChoice = 0;

      try
      {
         // Open recordset with Stores table.
         rstStores = new Recordset();
         rstStores.open("stores", strCnn,
            AdoEnums.CursorType.FORWARDONLY ,
            AdoEnums.LockType.READONLY ,
            AdoEnums.CommandType.TABLE);

         // Loop through the Recordset displaying the contents
         // of the stor_name field, the field's defined size
         // and it's actual size.

         while ( !(rstStores.getEOF( ))) // continuous loop
         {
            // Read data field in the variables.
            strStoreName = rstStores.getField("stor_name").getString();
            intDefinedSize = 
               rstStores.getField("stor_name").getDefinedSize();
            strDSize = Integer.toString(intDefinedSize);
            intActualSize = rstStores.getField 
               ("stor_name").getActualSize ();
            strASize = Integer.toString(intActualSize);

            // Display current record information.
            strMessage = "\nStore name: " + strStoreName + "\n"
                + "Defined Size : " + strDSize + "\n"
                + "Actual Size : " + strASize;

            System.out.println(strMessage);
            System.out.println("\nPress &lt;Enter&gt; key to continue.");
            in.readLine();
            rstStores.moveNext();
         }
      }
      catch( AdoException ae )
      {
         // Notify user of any errors that result from ADO.

         // Check for null pointer for connection object.
         if (rstStores.getActiveConnection()==null)
            System.out.println("Exception: " + ae.getMessage());
         // As passing a Recordset, check for null pointer first.
         if (rstStores != null)
         {
            PrintProviderError(rstStores.getActiveConnection());
         }
         else
         {
            System.out.println("Exception: " + ae.getMessage());
         }
      }

      // System read requires this catch.
      catch( java.io.IOException je)
      {
         PrintIOError(je);
      }
            
      finally
      {
         // Cleanup objects before exit.   
         if (rstStores != null)
            if (rstStores.getState() == 1)
               rstStores.close();
      }
   }

   // PrintProviderError Function

   static void PrintProviderError( Connection Cnn1 )
   {
      // Print Provider errors from Connection object.
      // ErrItem is an item object in the Connection's Errors collection.
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

   //.PrintIOError Function
   
   static void PrintIOError( java.io.IOException je)
   {
      System.out.println("Error \n");
      System.out.println("\tSource = " + je.getClass() + "\n");
      System.out.println("\tDescription = " + je.getMessage() + "\n");
   }
}
// EndActualSizeJ</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="722803d0-cef5-4d4c-b79d-3f2f58052229">ActualSize Property</link>
        <link xlink:href="3ee27314-a305-4fbc-8433-9ee9a909afd6">DefinedSize Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="722803d0-cef5-4d4c-b79d-3f2f58052229">ActualSize</legacyLink> and <legacyLink xlink:href="3ee27314-a305-4fbc-8433-9ee9a909afd6">DefinedSize</legacyLink> properties to display the defined size and actual size of a field.</caps:sentence>
        </para>
        <code>// BeginActualSizeJ
import com.ms.wfc.data.*;
import java.io.*;

public class ActualSizeX
{
   // The main entry point for the application.

   public static void main (String[] args)
   {
      ActualSizeX();
      System.exit(0);
   }

   // ActualSizeX function

   static void ActualSizeX()
   {

      // Define ADO Objects.
      Recordset rstStores = null;

      // Declarations.
      BufferedReader in = new 
         BufferedReader(new InputStreamReader(System.in));
      String line = null;
      String strCnn = "Provider='sqloledb';Data Source='MySqlServer';"
         + "Initial Catalog='Pubs';Integrated Security='SSPI';";

      String strStoreName;
      String strMessage;
      String strDSize,strASize;
      int intDefinedSize;
      int intActualSize;
      int intChoice = 0;

      try
      {
         // Open recordset with Stores table.
         rstStores = new Recordset();
         rstStores.open("stores", strCnn,
            AdoEnums.CursorType.FORWARDONLY ,
            AdoEnums.LockType.READONLY ,
            AdoEnums.CommandType.TABLE);

         // Loop through the Recordset displaying the contents
         // of the stor_name field, the field's defined size
         // and it's actual size.

         while ( !(rstStores.getEOF( ))) // continuous loop
         {
            // Read data field in the variables.
            strStoreName = rstStores.getField("stor_name").getString();
            intDefinedSize = 
               rstStores.getField("stor_name").getDefinedSize();
            strDSize = Integer.toString(intDefinedSize);
            intActualSize = rstStores.getField 
               ("stor_name").getActualSize ();
            strASize = Integer.toString(intActualSize);

            // Display current record information.
            strMessage = "\nStore name: " + strStoreName + "\n"
                + "Defined Size : " + strDSize + "\n"
                + "Actual Size : " + strASize;

            System.out.println(strMessage);
            System.out.println("\nPress &lt;Enter&gt; key to continue.");
            in.readLine();
            rstStores.moveNext();
         }
      }
      catch( AdoException ae )
      {
         // Notify user of any errors that result from ADO.

         // Check for null pointer for connection object.
         if (rstStores.getActiveConnection()==null)
            System.out.println("Exception: " + ae.getMessage());
         // As passing a Recordset, check for null pointer first.
         if (rstStores != null)
         {
            PrintProviderError(rstStores.getActiveConnection());
         }
         else
         {
            System.out.println("Exception: " + ae.getMessage());
         }
      }

      // System read requires this catch.
      catch( java.io.IOException je)
      {
         PrintIOError(je);
      }
            
      finally
      {
         // Cleanup objects before exit.   
         if (rstStores != null)
            if (rstStores.getState() == 1)
               rstStores.close();
      }
   }

   // PrintProviderError Function

   static void PrintProviderError( Connection Cnn1 )
   {
      // Print Provider errors from Connection object.
      // ErrItem is an item object in the Connection's Errors collection.
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

   //.PrintIOError Function
   
   static void PrintIOError( java.io.IOException je)
   {
      System.out.println("Error \n");
      System.out.println("\tSource = " + je.getClass() + "\n");
      System.out.println("\tDescription = " + je.getMessage() + "\n");
   }
}
// EndActualSizeJ</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="722803d0-cef5-4d4c-b79d-3f2f58052229">ActualSize Property</link>
        <link xlink:href="3ee27314-a305-4fbc-8433-9ee9a909afd6">DefinedSize Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>