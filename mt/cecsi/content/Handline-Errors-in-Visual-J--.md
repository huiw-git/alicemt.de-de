---
title: "Handline Errors in Visual J++"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 70be5873-b95c-47a6-a793-d97c5b41e7e4
caps.latest.revision: 4
caps.handback.revision: 4
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
# Handline Errors in Visual J++
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="296a8f1a26d76db0353b6c3a77f944f9" id="tgt1" class="tgtSentence">Handle ADO errors in your Microsoft® Visual J++® applications using a <legacyBold>try catch</legacyBold> block.</caps:sentence>
          <caps:sentence sentenceid="8a7739cc10aa01a649308e72553dd1ba" id="tgt2" class="tgtSentence"> Once an error has been thrown, you can iterate through the collection, successively handling each error.</caps:sentence>
          <caps:sentence sentenceid="b0711a741d47aa0ed0f8e4e2b3aaa78d" id="tgt3" class="tgtSentence"> The following Visual J++ example shows a console application that deliberately causes an error.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="fe8402fb502bc74bd5f5549bebcdbc75" id="tgt4" class="tgtSentence">When the <legacyBold>catch</legacyBold> block is activated, it calls the PrintProviderError function to display the errors.</caps:sentence>
          <caps:sentence sentenceid="8a6861d4cde680312be72de495bcc8f6" id="tgt5" class="tgtSentence"> The PrintProviderError function iterates through the <legacyBold>Errors</legacyBold> collection and sends a line to the standard output device that describes each error in the collection.</caps:sentence>
        </para>
        <code>// BeginErrorExampleVJ
// The WFC class includes the ADO objects.

import com.ms.wfc.data.*;
import java.io.* ;

public class ErrorExample
{
   /**
    * The main entry point for the application. 
    *
    * @param args Array of parameters passed to the application
    * via the command line.
    */
   public static void main (String[] args)
   {
      ForceError();
      System.exit(0);
   }

   static void DescriptionX()
   {
      BufferedReader in = new 
         BufferedReader(new InputStreamReader(System.in));

     // Define ADO Objects.
      Connection cnConn1 = null;

      try
      {
         // Create an error by trying to
       // Open a database that doesn't exist.
         cnConn1 = new Connection();
         cnConn1.open("nothing");
      }
      catch( AdoException ae )
      {
         // Notify user of any errors that result from ADO.
         PrintProviderError(cnConn1);
      }

     try
     {
       System.out.println("\nPress &lt;Enter&gt; key to continue.");
       in.readLine();
     }
      // System read requires this catch.
      catch( java.io.IOException je)
      {
         PrintIOError(je);
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

   // PrintIOError Function

   static void PrintIOError( java.io.IOException je)
   {
      System.out.println("Error \n");
      System.out.println("\tSource = " + je.getClass() + "\n");
      System.out.println("\tDescription = " + je.getMessage() + "\n");
   }
}
// EndErrorExampleVJ</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Handle ADO errors in your Microsoft® Visual J++® applications using a <legacyBold>try catch</legacyBold> block.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> Once an error has been thrown, you can iterate through the collection, successively handling each error.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The following Visual J++ example shows a console application that deliberately causes an error.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src4" class="srcSentence">When the <legacyBold>catch</legacyBold> block is activated, it calls the PrintProviderError function to display the errors.</caps:sentence>
          <caps:sentence id="src5" class="srcSentence"> The PrintProviderError function iterates through the <legacyBold>Errors</legacyBold> collection and sends a line to the standard output device that describes each error in the collection.</caps:sentence>
        </para>
        <code>// BeginErrorExampleVJ
// The WFC class includes the ADO objects.

import com.ms.wfc.data.*;
import java.io.* ;

public class ErrorExample
{
   /**
    * The main entry point for the application. 
    *
    * @param args Array of parameters passed to the application
    * via the command line.
    */
   public static void main (String[] args)
   {
      ForceError();
      System.exit(0);
   }

   static void DescriptionX()
   {
      BufferedReader in = new 
         BufferedReader(new InputStreamReader(System.in));

     // Define ADO Objects.
      Connection cnConn1 = null;

      try
      {
         // Create an error by trying to
       // Open a database that doesn't exist.
         cnConn1 = new Connection();
         cnConn1.open("nothing");
      }
      catch( AdoException ae )
      {
         // Notify user of any errors that result from ADO.
         PrintProviderError(cnConn1);
      }

     try
     {
       System.out.println("\nPress &lt;Enter&gt; key to continue.");
       in.readLine();
     }
      // System read requires this catch.
      catch( java.io.IOException je)
      {
         PrintIOError(je);
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

   // PrintIOError Function

   static void PrintIOError( java.io.IOException je)
   {
      System.out.println("Error \n");
      System.out.println("\tSource = " + je.getClass() + "\n");
      System.out.println("\tDescription = " + je.getMessage() + "\n");
   }
}
// EndErrorExampleVJ</code>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>