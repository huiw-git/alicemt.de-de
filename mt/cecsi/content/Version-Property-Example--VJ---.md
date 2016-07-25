---
title: "Version Property Example (VJ++)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 40b2ab58-84b5-4ae6-9226-df9e8f7d97c6
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
# Version Property Example (VJ++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="5b990d7f1587fd3fb32b764b4ca20a25" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="db4cb894-9bd9-422d-a58a-cef6941a5784">Version</legacyLink> property of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object to display the current ADO version.</caps:sentence>
          <caps:sentence sentenceid="b8915aa4e5c14684ae21ef58f033a74a" id="tgt2" class="tgtSentence"> It also uses several dynamic properties to show:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="d6a801bbed0ac3f8a0f9b3999db386db" id="tgt3" class="tgtSentence">Current DBMS name and version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="4389a8dcc21edbbd402929cc385c7049" id="tgt4" class="tgtSentence">OLE DB version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="caa768ca03304f1a57ca8077712bcde1" id="tgt5" class="tgtSentence">Provider name and version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="ea3e9081f441ae96055d1c4976a9adb0" id="tgt6" class="tgtSentence">ODBC version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5f195e9ab22407f8348677bb30de766f" id="tgt7" class="tgtSentence">ODBC driver name and version.</caps:sentence>
            </para>
          </listItem>
        </list>
        <code>// BeginVersionJ
import com.ms.wfc.data.*;
import java.io.*;

public class VersionX
{
   // The main entry point of the application.
   public static void main (String[] args)
   {
      VersionX();
      System.exit(0);
   }
   // VersionX Function
   static void VersionX()
   {
      // Define ADO Objects.
      Connection cnn1 = null;

      // Declarations.
      String strCnn = "Driver={SQL Server};Server='MySqlServer';" +
                  "User ID='MyUserID';Password='MyPassword';database='Pubs';";
      String strVersionInfo;
      BufferedReader in = new 
         BufferedReader(new InputStreamReader(System.in));
      try
      {
         // Open connection.
         cnn1 = new Connection();
         cnn1.open(strCnn);

         strVersionInfo = "\tADO Version:\t\t" + 
            cnn1.getVersion().toString()+"\n"+
            "\tDBMS Name:\t\t" + 
            cnn1.getProperties().getItem("DBMS Name").getString() +"\n"+
            "\tDBMS Version:\t\t"+ 
            cnn1.getProperties().getItem("DBMS Version").getString() + 
            "\n" + "\tOLE DB Version:\t\t" + 
            cnn1.getProperties().getItem("OLE DB Version").getString()+ 
            "\n" + "\tProvider Name:\t\t" + 
            cnn1.getProperties().getItem("Provider Name").getString() + 
            "\n" + "\tProvider Version:\t" + 
            cnn1.getProperties().getItem("Provider Version").
            getString() + "\n" + "\tDriver Name:\t\t" + 
            cnn1.getProperties().getItem("Driver Name").getString() + 
            "\n" + "\tDriver Version:\t\t" + 
            cnn1.getProperties().getItem("Driver Version").getString()+ 
            "\n" + "\tDriver ODBC Version:\t" + 
            cnn1.getProperties().getItem(
            "Driver ODBC Version").getString()+ "\n";
         System.out.println("\n\n" + strVersionInfo);

         System.out.println("Press &lt;Enter&gt; to continue..");
         in.readLine();
      }
      // System read requires this catch.
      catch(java.io.IOException je)
      {
         PrintIOError(je);
      }
      catch(AdoException ae)
      {
         // Notify the user of any errors that result from ADO.

         // As passing a recordset, check for null pointer first.
         if(cnn1!= null)
         {
            PrintProviderError(cnn1);
         }
         else
         {
            System.out.println("Exception: " + ae.getMessage());
         }
      }
      finally
      {
         // Cleanup objects before exit.   
         if (cnn1 != null)
            if (cnn1.getState() == 1)
               cnn1.close();
      }

   }
   // PrintProviderError Function
   static void PrintProviderError(Connection cnn1)
   {
      // Print Provider Errors from Connection Object.
      // ErrItem is an item object in the Connections Errors Collection.
      com.ms.wfc.data.Error               ErrItem = null;
      long                                 nCount = 0;
      int                                       i = 0;

      nCount = cnn1.getErrors().getCount();

      // If there are any errors in the collection, print them.
      if ( nCount &gt; 0)
      {
         // Collection ranges from 0 to nCount-1.
         for ( i=0;i&lt;nCount; i++)
         {
            ErrItem = cnn1.getErrors().getItem(i);
            System.out.println("\t Error Number: " + ErrItem.getNumber() 
               + "\t" + ErrItem.getDescription());
         }
      }
   }
   // PrintIOError Function
   static void PrintIOError(java.io.IOException je)
   {
      System.out.println("Error: \n");
      System.out.println("\t Source: " + je.getClass() + "\n");
      System.out.println("\t Description: "+ je.getMessage() + "\n");
   }
}
// EndVersionJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="db4cb894-9bd9-422d-a58a-cef6941a5784">Version Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="db4cb894-9bd9-422d-a58a-cef6941a5784">Version</legacyLink> property of a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object to display the current ADO version.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> It also uses several dynamic properties to show:</caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">Current DBMS name and version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">OLE DB version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Provider name and version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">ODBC version.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">ODBC driver name and version.</caps:sentence>
            </para>
          </listItem>
        </list>
        <code>// BeginVersionJ
import com.ms.wfc.data.*;
import java.io.*;

public class VersionX
{
   // The main entry point of the application.
   public static void main (String[] args)
   {
      VersionX();
      System.exit(0);
   }
   // VersionX Function
   static void VersionX()
   {
      // Define ADO Objects.
      Connection cnn1 = null;

      // Declarations.
      String strCnn = "Driver={SQL Server};Server='MySqlServer';" +
                  "User ID='MyUserID';Password='MyPassword';database='Pubs';";
      String strVersionInfo;
      BufferedReader in = new 
         BufferedReader(new InputStreamReader(System.in));
      try
      {
         // Open connection.
         cnn1 = new Connection();
         cnn1.open(strCnn);

         strVersionInfo = "\tADO Version:\t\t" + 
            cnn1.getVersion().toString()+"\n"+
            "\tDBMS Name:\t\t" + 
            cnn1.getProperties().getItem("DBMS Name").getString() +"\n"+
            "\tDBMS Version:\t\t"+ 
            cnn1.getProperties().getItem("DBMS Version").getString() + 
            "\n" + "\tOLE DB Version:\t\t" + 
            cnn1.getProperties().getItem("OLE DB Version").getString()+ 
            "\n" + "\tProvider Name:\t\t" + 
            cnn1.getProperties().getItem("Provider Name").getString() + 
            "\n" + "\tProvider Version:\t" + 
            cnn1.getProperties().getItem("Provider Version").
            getString() + "\n" + "\tDriver Name:\t\t" + 
            cnn1.getProperties().getItem("Driver Name").getString() + 
            "\n" + "\tDriver Version:\t\t" + 
            cnn1.getProperties().getItem("Driver Version").getString()+ 
            "\n" + "\tDriver ODBC Version:\t" + 
            cnn1.getProperties().getItem(
            "Driver ODBC Version").getString()+ "\n";
         System.out.println("\n\n" + strVersionInfo);

         System.out.println("Press &lt;Enter&gt; to continue..");
         in.readLine();
      }
      // System read requires this catch.
      catch(java.io.IOException je)
      {
         PrintIOError(je);
      }
      catch(AdoException ae)
      {
         // Notify the user of any errors that result from ADO.

         // As passing a recordset, check for null pointer first.
         if(cnn1!= null)
         {
            PrintProviderError(cnn1);
         }
         else
         {
            System.out.println("Exception: " + ae.getMessage());
         }
      }
      finally
      {
         // Cleanup objects before exit.   
         if (cnn1 != null)
            if (cnn1.getState() == 1)
               cnn1.close();
      }

   }
   // PrintProviderError Function
   static void PrintProviderError(Connection cnn1)
   {
      // Print Provider Errors from Connection Object.
      // ErrItem is an item object in the Connections Errors Collection.
      com.ms.wfc.data.Error               ErrItem = null;
      long                                 nCount = 0;
      int                                       i = 0;

      nCount = cnn1.getErrors().getCount();

      // If there are any errors in the collection, print them.
      if ( nCount &gt; 0)
      {
         // Collection ranges from 0 to nCount-1.
         for ( i=0;i&lt;nCount; i++)
         {
            ErrItem = cnn1.getErrors().getItem(i);
            System.out.println("\t Error Number: " + ErrItem.getNumber() 
               + "\t" + ErrItem.getDescription());
         }
      }
   }
   // PrintIOError Function
   static void PrintIOError(java.io.IOException je)
   {
      System.out.println("Error: \n");
      System.out.println("\t Source: " + je.getClass() + "\n");
      System.out.println("\t Description: "+ je.getMessage() + "\n");
   }
}
// EndVersionJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="db4cb894-9bd9-422d-a58a-cef6941a5784">Version Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>