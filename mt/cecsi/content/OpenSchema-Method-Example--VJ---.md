---
title: "OpenSchema Method Example (VJ++)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4c1240f1-7464-47db-9761-2d547419aedd
caps.latest.revision: 10
caps.handback.revision: 10
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
# OpenSchema Method Example (VJ++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="1bfe9c80a25f4ed480e73b46a7f39130" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema</legacyLink> method to display the name and type of each table in the <legacyBold><legacyItalic>Pubs</legacyItalic></legacyBold> database.</caps:sentence>
        </para>
        <code>// BeginOpenSchemaJ
import com.ms.wfc.data.*;
import java.io.*;
import com.ms.com.*;

public class OpenSchemaX
{
 // The main entry point of the application.

public static void main (String[] args)
{
   System.out.println("\nResults for OpenSchemaX:\n\n");
   OpenSchemaX();
   System.out.println("\nResults for OpenSchemaX2:\n\n");
   OpenSchemaX2();
   System.exit(0);
}

// OpenSchemaX Function
   static void OpenSchemaX()
   {
      // Define ADO Objects
      Connection cnn1 = null;
      Recordset rstSchema = null;

      //  Declarations
      String strCnn;
      BufferedReader in = new BufferedReader(new InputStreamReader(System.in));
      int intDisplayRecords = 5;
      int intRecordCount = 0;

      try
      {

         cnn1 = new Connection();
         strCnn = "Provider = Microsoft.Jet.OLEDB.4.0;" +
            "Data Source=Northwind.mdb;";
         cnn1.open(strCnn);
         rstSchema = cnn1.openSchema(AdoEnums.Schema.TABLES);

         while (!rstSchema.getEOF())
         {

            System.out.println("Table Name: " + 
               rstSchema.getField("TABLE_NAME").getString()+"\n"+
               "Table Type: " + 
               rstSchema.getField("TABLE_TYPE").getString()+"\n");
            intRecordCount++;
            if ( intRecordCount == intDisplayRecords)
            {
               System.out.println("Press &lt;Enter&gt; to continue..");
               in.readLine();
               intRecordCount = 0;
            }
            rstSchema.moveNext();

         }
         System.out.println("Press &lt;Enter&gt; to continue..");
         in.readLine();

      }
      catch(AdoException ae)
      {
         // Notify user of any errors that result from ADO.

         // As passing a Recordset, check for null pointer first.
         if(rstSchema != null)
         {
            PrintProviderError(rstSchema.getActiveConnection());
         }
         else
         {
            System.out.println("Exception: " + ae.getMessage());
         }
      }
      // System read requires this catch.
      catch(java.io.IOException je)
      {
         PrintIOError(je);
      }   
      
      finally
      {
         // Cleanup objects before exit.   
         if (rstSchema != null)
            if (rstSchema.getState() == 1)
               rstSchema.close();  
         if (cnn1 != null)
            if (cnn1.getState() == 1)
               cnn1.close();
      }
   }

   // OpenSchemaX2 Function

   static void OpenSchemaX2()
   {
      // Define ADO Objects
      Connection cnn2 = null;
      Recordset rstSchema = null;

      // Declarations
      String strCnn;
      BufferedReader in = 
         new BufferedReader(new InputStreamReader(System.in));
      int intDisplayRecords = 5;
      int intRecordCount = 0;

      try
      {
         cnn2 = new Connection();
         strCnn = "Provider = Microsoft.Jet.OLEDB.4.0;" +
            "Data Source=Northwind.mdb;";
         cnn2.open(strCnn);

         Variant[] va = new Variant[4];
         va[0] = new Variant();
         va[1] = new Variant();
         va[2] = new Variant();
         va[3] = new Variant("VIEW");
         rstSchema = cnn2.openSchema(AdoEnums.Schema.TABLES,(Object[])va);

         while (!rstSchema.getEOF())
         {
            System.out.println("Table Name: " + 
               rstSchema.getField("TABLE_NAME").getString()+"\n"+
               "Table Type: " + 
               rstSchema.getField("TABLE_TYPE").getString()+"\n");
            intRecordCount++;
            if ( intRecordCount == intDisplayRecords)
            {
               System.out.println("Press &lt;Enter&gt; to continue..");
               in.readLine();
               intRecordCount = 0;
            }
            rstSchema.moveNext();

         }
         System.out.println("Press &lt;Enter&gt; to continue..");
         in.readLine();

      }
      catch(AdoException ae)
      {
         // Notify user of any errors that result from ADO.

         // As passing a Recordset, check for null pointer first.
         if(rstSchema != null)
         {
            PrintProviderError(rstSchema.getActiveConnection());
         }
         else
         {
            System.out.println("Exception: " + ae.getMessage());
         }
      }
      // System read requires this catch.
      catch(java.io.IOException je)
      {
         PrintIOError(je);
      }  
      
      finally
      {
         // Cleanup Objects before exit.
         rstSchema.close();
         cnn2.close();
         // Cleanup objects before exit.   
         if (rstSchema != null)
            if (rstSchema.getState() == 1)
               rstSchema.close();  
         if (cnn2 != null)
            if (cnn2.getState() == 1)
               cnn2.close();
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
// EndOpenSchemaJ</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema</legacyLink> method to display the name and type of each table in the <legacyBold><legacyItalic>Pubs</legacyItalic></legacyBold> database.</caps:sentence>
        </para>
        <code>// BeginOpenSchemaJ
import com.ms.wfc.data.*;
import java.io.*;
import com.ms.com.*;

public class OpenSchemaX
{
 // The main entry point of the application.

public static void main (String[] args)
{
   System.out.println("\nResults for OpenSchemaX:\n\n");
   OpenSchemaX();
   System.out.println("\nResults for OpenSchemaX2:\n\n");
   OpenSchemaX2();
   System.exit(0);
}

// OpenSchemaX Function
   static void OpenSchemaX()
   {
      // Define ADO Objects
      Connection cnn1 = null;
      Recordset rstSchema = null;

      //  Declarations
      String strCnn;
      BufferedReader in = new BufferedReader(new InputStreamReader(System.in));
      int intDisplayRecords = 5;
      int intRecordCount = 0;

      try
      {

         cnn1 = new Connection();
         strCnn = "Provider = Microsoft.Jet.OLEDB.4.0;" +
            "Data Source=Northwind.mdb;";
         cnn1.open(strCnn);
         rstSchema = cnn1.openSchema(AdoEnums.Schema.TABLES);

         while (!rstSchema.getEOF())
         {

            System.out.println("Table Name: " + 
               rstSchema.getField("TABLE_NAME").getString()+"\n"+
               "Table Type: " + 
               rstSchema.getField("TABLE_TYPE").getString()+"\n");
            intRecordCount++;
            if ( intRecordCount == intDisplayRecords)
            {
               System.out.println("Press &lt;Enter&gt; to continue..");
               in.readLine();
               intRecordCount = 0;
            }
            rstSchema.moveNext();

         }
         System.out.println("Press &lt;Enter&gt; to continue..");
         in.readLine();

      }
      catch(AdoException ae)
      {
         // Notify user of any errors that result from ADO.

         // As passing a Recordset, check for null pointer first.
         if(rstSchema != null)
         {
            PrintProviderError(rstSchema.getActiveConnection());
         }
         else
         {
            System.out.println("Exception: " + ae.getMessage());
         }
      }
      // System read requires this catch.
      catch(java.io.IOException je)
      {
         PrintIOError(je);
      }   
      
      finally
      {
         // Cleanup objects before exit.   
         if (rstSchema != null)
            if (rstSchema.getState() == 1)
               rstSchema.close();  
         if (cnn1 != null)
            if (cnn1.getState() == 1)
               cnn1.close();
      }
   }

   // OpenSchemaX2 Function

   static void OpenSchemaX2()
   {
      // Define ADO Objects
      Connection cnn2 = null;
      Recordset rstSchema = null;

      // Declarations
      String strCnn;
      BufferedReader in = 
         new BufferedReader(new InputStreamReader(System.in));
      int intDisplayRecords = 5;
      int intRecordCount = 0;

      try
      {
         cnn2 = new Connection();
         strCnn = "Provider = Microsoft.Jet.OLEDB.4.0;" +
            "Data Source=Northwind.mdb;";
         cnn2.open(strCnn);

         Variant[] va = new Variant[4];
         va[0] = new Variant();
         va[1] = new Variant();
         va[2] = new Variant();
         va[3] = new Variant("VIEW");
         rstSchema = cnn2.openSchema(AdoEnums.Schema.TABLES,(Object[])va);

         while (!rstSchema.getEOF())
         {
            System.out.println("Table Name: " + 
               rstSchema.getField("TABLE_NAME").getString()+"\n"+
               "Table Type: " + 
               rstSchema.getField("TABLE_TYPE").getString()+"\n");
            intRecordCount++;
            if ( intRecordCount == intDisplayRecords)
            {
               System.out.println("Press &lt;Enter&gt; to continue..");
               in.readLine();
               intRecordCount = 0;
            }
            rstSchema.moveNext();

         }
         System.out.println("Press &lt;Enter&gt; to continue..");
         in.readLine();

      }
      catch(AdoException ae)
      {
         // Notify user of any errors that result from ADO.

         // As passing a Recordset, check for null pointer first.
         if(rstSchema != null)
         {
            PrintProviderError(rstSchema.getActiveConnection());
         }
         else
         {
            System.out.println("Exception: " + ae.getMessage());
         }
      }
      // System read requires this catch.
      catch(java.io.IOException je)
      {
         PrintIOError(je);
      }  
      
      finally
      {
         // Cleanup Objects before exit.
         rstSchema.close();
         cnn2.close();
         // Cleanup objects before exit.   
         if (rstSchema != null)
            if (rstSchema.getState() == 1)
               rstSchema.close();  
         if (cnn2 != null)
            if (cnn2.getState() == 1)
               cnn2.close();
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
// EndOpenSchemaJ</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="850cf3ce-f18f-4e7c-8597-96c1dc504866">OpenSchema Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>