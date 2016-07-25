---
title: "Prepared Property Example (VJ++)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: fc52ea7c-1b3b-4874-9db9-4d2e01d794c3
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
# Prepared Property Example (VJ++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="aa30ea28a0e4e3097d4ca3357d7ca46e" id="tgt1" class="tgtSentence">This example demonstrates the <legacyLink xlink:href="11ca8825-765e-4bb4-a6ce-3f6564ad8755">Prepared</legacyLink> property by opening two <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> objects—one prepared and one not prepared.</caps:sentence>
        </para>
        <code>// BeginPreparedJ
import com.ms.wfc.data.*;
import java.io.* ;

public class PreparedX
{
   // The main entry point for the application.

   public static void main (String[] args)
   {
      PreparedX();
      System.exit(0);
   }

   // PreparedX function

   static void PreparedX()
   {
      // Define string variables.
      String strCnn = "Provider='sqloledb';Data Source='MySqlServer';"
            + "Initial Catalog='Pubs';Integrated Security='SSPI';";
      String strCmd = "SELECT title, type FROM Titles ORDER BY type";

      // Define ADO Objects.
      Connection cnConn1 = null;
      Command cmd1 = null;
      Command cmd2 = null;

      // Declarations.
      BufferedReader in = 
         new BufferedReader (new InputStreamReader(System.in));
      long timeStart;
      long timeEnd;
      float timeNotPrepared ;
      float timePrepared;
      int   intLoop;
      String strTemp;

      try
      {
         // Open a connection.
         cnConn1 = new Connection();
         cnConn1.open(strCnn);

         // Create two command objects for the same
         // command - one prepared and one not prepared.
         cmd1 = new Command();
         cmd1.setActiveConnection(cnConn1);
         cmd1.setCommandType(AdoEnums.CommandType.TEXT);
         cmd1.setCommandText(strCmd);

         cmd2 = new Command();
         cmd2.setActiveConnection(cnConn1);
         cmd2.setCommandType(AdoEnums.CommandType.TEXT);
         cmd2.setCommandText(strCmd);
         cmd2.setPrepared(true);

         // Set a timer, then execute the unprepared
         // command 20 times.
         timeStart = System.currentTimeMillis();
         for ( intLoop = 0; intLoop &lt; 20; intLoop++)
            cmd1.execute();
         timeEnd = System.currentTimeMillis();
         timeNotPrepared =(float)(timeEnd - timeStart)/1000f;

         // Reset the timer, then execute the prepared
         // command 20 times.
         timeStart = System.currentTimeMillis();
         for ( intLoop = 0; intLoop &lt; 20; intLoop++)
            cmd2.execute();
         timeEnd = System.currentTimeMillis();
         timePrepared =(float)(timeEnd - timeStart)/1000f;

         // Display performance results.
         System.out.println("\nPerformance Results:");
         System.out.println("\n\tNot Prepared: " + timeNotPrepared + 
            " seconds");
         System.out.println("\n\tPrepared: " + timePrepared + 
            " seconds");
         System.out.println("\n\nPress &lt;Enter&gt; to continue..");
         in.readLine();

      }
      catch( AdoException ae )
      {
         // Notify user of any errors that result from ADO.

         // As passing a Connection, check for null pointer first.
         if (cnConn1!= null)
         {
            PrintProviderError(cnConn1);
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
         if (cnConn1 != null)
            if (cnConn1.getState() == 1)
               cnConn1.close();
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
// EndPreparedJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="11ca8825-765e-4bb4-a6ce-3f6564ad8755">Prepared Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example demonstrates the <legacyLink xlink:href="11ca8825-765e-4bb4-a6ce-3f6564ad8755">Prepared</legacyLink> property by opening two <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> objects—one prepared and one not prepared.</caps:sentence>
        </para>
        <code>// BeginPreparedJ
import com.ms.wfc.data.*;
import java.io.* ;

public class PreparedX
{
   // The main entry point for the application.

   public static void main (String[] args)
   {
      PreparedX();
      System.exit(0);
   }

   // PreparedX function

   static void PreparedX()
   {
      // Define string variables.
      String strCnn = "Provider='sqloledb';Data Source='MySqlServer';"
            + "Initial Catalog='Pubs';Integrated Security='SSPI';";
      String strCmd = "SELECT title, type FROM Titles ORDER BY type";

      // Define ADO Objects.
      Connection cnConn1 = null;
      Command cmd1 = null;
      Command cmd2 = null;

      // Declarations.
      BufferedReader in = 
         new BufferedReader (new InputStreamReader(System.in));
      long timeStart;
      long timeEnd;
      float timeNotPrepared ;
      float timePrepared;
      int   intLoop;
      String strTemp;

      try
      {
         // Open a connection.
         cnConn1 = new Connection();
         cnConn1.open(strCnn);

         // Create two command objects for the same
         // command - one prepared and one not prepared.
         cmd1 = new Command();
         cmd1.setActiveConnection(cnConn1);
         cmd1.setCommandType(AdoEnums.CommandType.TEXT);
         cmd1.setCommandText(strCmd);

         cmd2 = new Command();
         cmd2.setActiveConnection(cnConn1);
         cmd2.setCommandType(AdoEnums.CommandType.TEXT);
         cmd2.setCommandText(strCmd);
         cmd2.setPrepared(true);

         // Set a timer, then execute the unprepared
         // command 20 times.
         timeStart = System.currentTimeMillis();
         for ( intLoop = 0; intLoop &lt; 20; intLoop++)
            cmd1.execute();
         timeEnd = System.currentTimeMillis();
         timeNotPrepared =(float)(timeEnd - timeStart)/1000f;

         // Reset the timer, then execute the prepared
         // command 20 times.
         timeStart = System.currentTimeMillis();
         for ( intLoop = 0; intLoop &lt; 20; intLoop++)
            cmd2.execute();
         timeEnd = System.currentTimeMillis();
         timePrepared =(float)(timeEnd - timeStart)/1000f;

         // Display performance results.
         System.out.println("\nPerformance Results:");
         System.out.println("\n\tNot Prepared: " + timeNotPrepared + 
            " seconds");
         System.out.println("\n\tPrepared: " + timePrepared + 
            " seconds");
         System.out.println("\n\nPress &lt;Enter&gt; to continue..");
         in.readLine();

      }
      catch( AdoException ae )
      {
         // Notify user of any errors that result from ADO.

         // As passing a Connection, check for null pointer first.
         if (cnConn1!= null)
         {
            PrintProviderError(cnConn1);
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
         if (cnConn1 != null)
            if (cnConn1.getState() == 1)
               cnConn1.close();
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
// EndPreparedJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
        <link xlink:href="11ca8825-765e-4bb4-a6ce-3f6564ad8755">Prepared Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>