---
title: "State Property Example (VJ++)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 74b59bbe-0244-4516-9b1d-dc513bd03a3d
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
# State Property Example (VJ++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="a8ac5f69b409ce3269d1703ca696ac5f" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property to display a message while asynchronous connections are opening and asynchronous commands are executing.</caps:sentence>
        </para>
        <code>// BeginStateJ
import com.ms.wfc.data.*;
import java.io.*;

public class StateX
{
   // The main entry point of the application.
   public static void main (String[] args)
   {
      StateX();
      System.exit(0);
   }
   // StateX Function
   static void StateX()
   {
      // Define ADO Objects.
      Connection cnn1 = null;
      Connection cnn2 = null;
      Command cmdChange = null;
      Command cmdRestore = null;

      // Declarations.
      String strCnn = "Provider='sqloledb';Data Source='MySqlServer';"+
                  "Initial Catalog='Pubs';Integrated Security='SSPI';";
      BufferedReader in = 
         new BufferedReader(new InputStreamReader(System.in));

      try
      {
         // Open two Asynchronous connections, displaying
         // a message while connecting.
         cnn1 = new Connection();
         cnn2 = new Connection();

         cnn1.open(strCnn,"","",AdoEnums.ConnectOption.ASYNCCONNECT);
         while(cnn1.getState()==AdoEnums.ObjectState.CONNECTING)
            System.out.println("Opening the first connection....");

         cnn2.open(strCnn,"","",AdoEnums.ConnectOption.ASYNCCONNECT);
         while(cnn2.getState()==AdoEnums.ObjectState.CONNECTING)
            System.out.println("Opening the second connection....");

         // Create two command Objects.
         cmdChange = new Command();
         cmdChange.setActiveConnection(cnn1);
         cmdChange.setCommandText("UPDATE Titles SET type = 'self_help'"+
                            "WHERE type = 'psychology'");

         cmdRestore = new Command();
         cmdRestore.setActiveConnection(cnn2);
         cmdRestore.setCommandText(
            "UPDATE Titles SET type = 'psychology'"+
            "WHERE type = 'self_help'");

         // Executing the commands, displaying a message
         // while they are executing.
         cmdChange.execute(null,AdoEnums.ExecuteOption.ASYNCEXECUTE);

         while(cmdChange.getState() == AdoEnums.ObjectState.EXECUTING)
            System.out.println("Change command executing....");

         cmdRestore.execute(null,AdoEnums.ExecuteOption.ASYNCEXECUTE);

         while(cmdRestore.getState() == AdoEnums.ObjectState.EXECUTING)
            System.out.println("Restore command executing....");

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
         // Notify user of any errors resulting from ADO.

         // As passing a connection, check for null pointer first.
         if(cnn1 != null)
         {
            System.out.println("The error has occured in cnn1:");
            PrintProviderError(cnn1);
         }
         else if(cnn2 != null)
         {
            System.out.println("The error has occured in cnn2:");
            PrintProviderError(cnn2);
         }
         else
         {
            System.out.println("Exception: "+ ae.getMessage());
         }
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
// EndStateJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State</legacyLink> property to display a message while asynchronous connections are opening and asynchronous commands are executing.</caps:sentence>
        </para>
        <code>// BeginStateJ
import com.ms.wfc.data.*;
import java.io.*;

public class StateX
{
   // The main entry point of the application.
   public static void main (String[] args)
   {
      StateX();
      System.exit(0);
   }
   // StateX Function
   static void StateX()
   {
      // Define ADO Objects.
      Connection cnn1 = null;
      Connection cnn2 = null;
      Command cmdChange = null;
      Command cmdRestore = null;

      // Declarations.
      String strCnn = "Provider='sqloledb';Data Source='MySqlServer';"+
                  "Initial Catalog='Pubs';Integrated Security='SSPI';";
      BufferedReader in = 
         new BufferedReader(new InputStreamReader(System.in));

      try
      {
         // Open two Asynchronous connections, displaying
         // a message while connecting.
         cnn1 = new Connection();
         cnn2 = new Connection();

         cnn1.open(strCnn,"","",AdoEnums.ConnectOption.ASYNCCONNECT);
         while(cnn1.getState()==AdoEnums.ObjectState.CONNECTING)
            System.out.println("Opening the first connection....");

         cnn2.open(strCnn,"","",AdoEnums.ConnectOption.ASYNCCONNECT);
         while(cnn2.getState()==AdoEnums.ObjectState.CONNECTING)
            System.out.println("Opening the second connection....");

         // Create two command Objects.
         cmdChange = new Command();
         cmdChange.setActiveConnection(cnn1);
         cmdChange.setCommandText("UPDATE Titles SET type = 'self_help'"+
                            "WHERE type = 'psychology'");

         cmdRestore = new Command();
         cmdRestore.setActiveConnection(cnn2);
         cmdRestore.setCommandText(
            "UPDATE Titles SET type = 'psychology'"+
            "WHERE type = 'self_help'");

         // Executing the commands, displaying a message
         // while they are executing.
         cmdChange.execute(null,AdoEnums.ExecuteOption.ASYNCEXECUTE);

         while(cmdChange.getState() == AdoEnums.ObjectState.EXECUTING)
            System.out.println("Change command executing....");

         cmdRestore.execute(null,AdoEnums.ExecuteOption.ASYNCEXECUTE);

         while(cmdRestore.getState() == AdoEnums.ObjectState.EXECUTING)
            System.out.println("Restore command executing....");

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
         // Notify user of any errors resulting from ADO.

         // As passing a connection, check for null pointer first.
         if(cnn1 != null)
         {
            System.out.println("The error has occured in cnn1:");
            PrintProviderError(cnn1);
         }
         else if(cnn2 != null)
         {
            System.out.println("The error has occured in cnn2:");
            PrintProviderError(cnn2);
         }
         else
         {
            System.out.println("Exception: "+ ae.getMessage());
         }
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
// EndStateJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="0b993bac-2653-40b1-bcbb-5b57b6aae2bf">State Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>