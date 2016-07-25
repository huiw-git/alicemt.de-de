---
title: "Provider and DefaultDatabase Properties Example (VJ++)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fdc26576-37d0-4fa1-9afa-75d0e7133675
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
# Provider and DefaultDatabase Properties Example (VJ++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="41244bf79c94e8bb6077e927069a15b1" id="tgt1" class="tgtSentence">This example demonstrates the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property by opening three <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> objects using different providers.</caps:sentence>
          <caps:sentence sentenceid="28fd276f98380c9a4fbb7f181d91426c" id="tgt2" class="tgtSentence"> It also uses the <legacyLink xlink:href="41e8a8dd-e69c-4a09-8736-93502e01961c">DefaultDatabase</legacyLink> property to set the default database for the Microsoft ODBC Provider.</caps:sentence>
        </para>
        <code>// BeginProviderJ
import java.io.*;
import com.ms.wfc.data.*;

public class ProviderX
{
   //    The main entry point of the application.
   public static void main (String[] args)
   {
      ProviderX();
      System.exit(0);
   }
   // ProviderX Function
   static void ProviderX()
   {
      // Define ADO Objects.
      Connection cnn1 = null;
      Connection cnn2 = null;
      Connection cnn3 = null;

      // Declarations.
      BufferedReader in = 
         new BufferedReader(new InputStreamReader(System.in));
      try
      {
         // Open a connection using the Microsoft ODBC Provider.
         cnn1 = new Connection();
         cnn1.setConnectionString("driver={SQL Server};"+
             "server='MySqlServer';User ID='MyUserID';Password='MyPassword';");
         cnn1.open();
         cnn1.setDefaultDatabase("Pubs");

         // Display the provider.
         System.out.println("\n\n\tCnn1 provider: "+ cnn1.getProvider());

         // Open connection using the OLE DB Provider for Microsoft Jet.
         cnn2 = new Connection();
         cnn2.setProvider("Microsoft.Jet.OLEDB.4.0");
         cnn2.open("Northwind.mdb","admin","");

         // Display the provider.
         System.out.println("\n\n\tCnn2 provider: " + 
            cnn2.getProvider());

         // Open a connection using the Microsoft SQL Server Provider.
         cnn3 = new Connection();
         cnn3.setProvider("sqloledb");
         cnn3.open("Data Source='MySqlServer';Initial Catalog='Pubs';Integrated Security='SSPI';","","");

         // Display the provider.
         System.out.println("\n\n\tCnn3 provider: " + 
            cnn3.getProvider());

         System.out.println("\n\n\tPress &lt;Enter&gt; to continue..");
         in.readLine();
      }
      catch(AdoException ae)
      {
         // Notify the user of any errors that result from ADO.

         // As passing a Connection, check for null pointer first.
         if(cnn1 != null)
         {
            PrintProviderError(cnn1);
         }
         else
         {
            System.out.println("Exception: " + ae.getLocalizedMessage());
         }
      }
      // System read requires needs this catch.
      catch(java.io.IOException je)
      {
         PrintIOError(je);
      }   
      
      finally
      {
         // Cleanup objects before exit.   
         if (cnn1 != null)
            if (cnn1.getState() == 1)
               cnn1.close();   
         if (cnn2 != null)
            if (cnn2.getState() == 1)
               cnn2.close();   
         if (cnn3 != null)
            if (cnn3.getState() == 1)
               cnn3.close();
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
// EndProviderJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="41e8a8dd-e69c-4a09-8736-93502e01961c">DefaultDatabase Property</link>
        <link xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example demonstrates the <legacyLink xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider</legacyLink> property by opening three <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> objects using different providers.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> It also uses the <legacyLink xlink:href="41e8a8dd-e69c-4a09-8736-93502e01961c">DefaultDatabase</legacyLink> property to set the default database for the Microsoft ODBC Provider.</caps:sentence>
        </para>
        <code>// BeginProviderJ
import java.io.*;
import com.ms.wfc.data.*;

public class ProviderX
{
   //    The main entry point of the application.
   public static void main (String[] args)
   {
      ProviderX();
      System.exit(0);
   }
   // ProviderX Function
   static void ProviderX()
   {
      // Define ADO Objects.
      Connection cnn1 = null;
      Connection cnn2 = null;
      Connection cnn3 = null;

      // Declarations.
      BufferedReader in = 
         new BufferedReader(new InputStreamReader(System.in));
      try
      {
         // Open a connection using the Microsoft ODBC Provider.
         cnn1 = new Connection();
         cnn1.setConnectionString("driver={SQL Server};"+
             "server='MySqlServer';User ID='MyUserID';Password='MyPassword';");
         cnn1.open();
         cnn1.setDefaultDatabase("Pubs");

         // Display the provider.
         System.out.println("\n\n\tCnn1 provider: "+ cnn1.getProvider());

         // Open connection using the OLE DB Provider for Microsoft Jet.
         cnn2 = new Connection();
         cnn2.setProvider("Microsoft.Jet.OLEDB.4.0");
         cnn2.open("Northwind.mdb","admin","");

         // Display the provider.
         System.out.println("\n\n\tCnn2 provider: " + 
            cnn2.getProvider());

         // Open a connection using the Microsoft SQL Server Provider.
         cnn3 = new Connection();
         cnn3.setProvider("sqloledb");
         cnn3.open("Data Source='MySqlServer';Initial Catalog='Pubs';Integrated Security='SSPI';","","");

         // Display the provider.
         System.out.println("\n\n\tCnn3 provider: " + 
            cnn3.getProvider());

         System.out.println("\n\n\tPress &lt;Enter&gt; to continue..");
         in.readLine();
      }
      catch(AdoException ae)
      {
         // Notify the user of any errors that result from ADO.

         // As passing a Connection, check for null pointer first.
         if(cnn1 != null)
         {
            PrintProviderError(cnn1);
         }
         else
         {
            System.out.println("Exception: " + ae.getLocalizedMessage());
         }
      }
      // System read requires needs this catch.
      catch(java.io.IOException je)
      {
         PrintIOError(je);
      }   
      
      finally
      {
         // Cleanup objects before exit.   
         if (cnn1 != null)
            if (cnn1.getState() == 1)
               cnn1.close();   
         if (cnn2 != null)
            if (cnn2.getState() == 1)
               cnn2.close();   
         if (cnn3 != null)
            if (cnn3.getState() == 1)
               cnn3.close();
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
// EndProviderJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="41e8a8dd-e69c-4a09-8736-93502e01961c">DefaultDatabase Property</link>
        <link xlink:href="0ff70e72-0061-4ffc-90fb-e3ea23129bb2">Provider Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>