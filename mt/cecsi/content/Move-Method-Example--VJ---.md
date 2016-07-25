---
title: "Move Method Example (VJ++)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: b29ddb8c-ceb3-4aad-a240-8030462fceba
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
# Move Method Example (VJ++)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="8bc9354aa5e76c0d243fcf58c3750ab0" id="tgt1" class="tgtSentence">This example uses the <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink> method to position the record pointer based on user input.</caps:sentence>
        </para>
        <code>// BeginMoveJ
import java.io.*;
import com.ms.wfc.data.*;
import com.ms.com.*;

public class MoveX
{
   // The main entry point for the application.

   public static void main (String[] args)
   {
      MoveX();
      System.exit(0);
   }
   // MoveX Function

   static void MoveX()
   {
      // Define ADO Objects
      Recordset rstAuthors = null;

      // Declarations
      String line = null;
      Variant varBookmark;
      String strCommand = null;
      int lngMove;
      BufferedReader in = 
         new BufferedReader(new InputStreamReader(System.in));

      try
      {
         //  Open recordset from Authors table.
         String strCnn = "Provider='sqloledb';Data Source='MySqlServer';"+
            "Initial Catalog='Pubs';Integrated Security='SSPI';";

         rstAuthors = new Recordset();
         rstAuthors.setCursorType(AdoEnums.CursorType.STATIC);

         // Use client cursor to allow use of
         // Absolute Position property.
         rstAuthors.setCursorLocation(AdoEnums.CursorLocation.CLIENT);
         rstAuthors.open("select au_id,au_fname,au_lname,city,state " + 
            "from Authors order by au_lname", 
            strCnn,AdoEnums.CursorType.STATIC, 
            AdoEnums.CursorLocation.CLIENT, AdoEnums.CommandType.TEXT);

         rstAuthors.moveFirst();

         while(true)
         {
            // Display information about current record and
            // ask how many records to move.
            strCommand = "Record:\t\t"+ rstAuthors.getAbsolutePosition() + 
               " of " + rstAuthors.getRecordCount() + "\n" + "\tAuthor:\t\t"
                + rstAuthors.getField("au_fname").getString() + 
                " " + rstAuthors.getField("au_lname").getString() + 
               "\n" +"\tLocation:\t" + 
               rstAuthors.getField("city").getString() +
                ", " +rstAuthors.getField("state").getString()
                +"\n\n"+"\tEnter number of records to move" +
               " (positive or negative).";

            System.out.print("\t"+ strCommand + "\t");
            line =in.readLine();

            // No entry exits program loop.
            if (line.length()== 0)
               break;

            // Converts string entry to int.
            lngMove = Integer.parseInt(line);

            // Store bookmark in case the move goes too far
            // forward or backward.
            varBookmark =(Variant)rstAuthors.getBookmark();

            // Move method requires parameter of data type int.
            rstAuthors.move(lngMove);

            // Trap for BOF and EOF.
            if (rstAuthors.getBOF())
            {
               System.out.println("\tToo far backward!  " +
                  "Returning to the current record.");
               rstAuthors.setBookmark(varBookmark);
            }
            if (rstAuthors.getEOF())
            {
               System.out.println("\tToo far forward!  " +
                  "Returning to the current record.");
               rstAuthors.setBookmark(varBookmark);
            }
         }
         System.out.println("\tPress &lt;Enter&gt; to continue..");
         in.readLine();
      }

      catch(AdoException ae)
      {
         // Notify user of any errors that result from ADO.

         // As passing a recordset, check for null pointer.
         if (rstAuthors!=null)
         {
            PrintProviderError(rstAuthors.getActiveConnection());
         }
         else
         {
            System.out.println(" Exception: "+ ae.getMessage());
         }
      }
      // System Read requires this catch.
      catch(java.io.IOException je)
      {
         PrintIOError(je);
      }
      // Required if the user enter non integer value.
      catch(java.lang.NumberFormatException ne)
      {
         System.out.println("\n\nPlease enter integer values!");
         rstAuthors.close();
      }   
      
      finally
      {
         // Cleanup objects before exit.   
         if (rstAuthors != null)
            if (rstAuthors.getState() == 1)
               rstAuthors.close();
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
// EndMoveJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">This example uses the <legacyLink xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move</legacyLink> method to position the record pointer based on user input.</caps:sentence>
        </para>
        <code>// BeginMoveJ
import java.io.*;
import com.ms.wfc.data.*;
import com.ms.com.*;

public class MoveX
{
   // The main entry point for the application.

   public static void main (String[] args)
   {
      MoveX();
      System.exit(0);
   }
   // MoveX Function

   static void MoveX()
   {
      // Define ADO Objects
      Recordset rstAuthors = null;

      // Declarations
      String line = null;
      Variant varBookmark;
      String strCommand = null;
      int lngMove;
      BufferedReader in = 
         new BufferedReader(new InputStreamReader(System.in));

      try
      {
         //  Open recordset from Authors table.
         String strCnn = "Provider='sqloledb';Data Source='MySqlServer';"+
            "Initial Catalog='Pubs';Integrated Security='SSPI';";

         rstAuthors = new Recordset();
         rstAuthors.setCursorType(AdoEnums.CursorType.STATIC);

         // Use client cursor to allow use of
         // Absolute Position property.
         rstAuthors.setCursorLocation(AdoEnums.CursorLocation.CLIENT);
         rstAuthors.open("select au_id,au_fname,au_lname,city,state " + 
            "from Authors order by au_lname", 
            strCnn,AdoEnums.CursorType.STATIC, 
            AdoEnums.CursorLocation.CLIENT, AdoEnums.CommandType.TEXT);

         rstAuthors.moveFirst();

         while(true)
         {
            // Display information about current record and
            // ask how many records to move.
            strCommand = "Record:\t\t"+ rstAuthors.getAbsolutePosition() + 
               " of " + rstAuthors.getRecordCount() + "\n" + "\tAuthor:\t\t"
                + rstAuthors.getField("au_fname").getString() + 
                " " + rstAuthors.getField("au_lname").getString() + 
               "\n" +"\tLocation:\t" + 
               rstAuthors.getField("city").getString() +
                ", " +rstAuthors.getField("state").getString()
                +"\n\n"+"\tEnter number of records to move" +
               " (positive or negative).";

            System.out.print("\t"+ strCommand + "\t");
            line =in.readLine();

            // No entry exits program loop.
            if (line.length()== 0)
               break;

            // Converts string entry to int.
            lngMove = Integer.parseInt(line);

            // Store bookmark in case the move goes too far
            // forward or backward.
            varBookmark =(Variant)rstAuthors.getBookmark();

            // Move method requires parameter of data type int.
            rstAuthors.move(lngMove);

            // Trap for BOF and EOF.
            if (rstAuthors.getBOF())
            {
               System.out.println("\tToo far backward!  " +
                  "Returning to the current record.");
               rstAuthors.setBookmark(varBookmark);
            }
            if (rstAuthors.getEOF())
            {
               System.out.println("\tToo far forward!  " +
                  "Returning to the current record.");
               rstAuthors.setBookmark(varBookmark);
            }
         }
         System.out.println("\tPress &lt;Enter&gt; to continue..");
         in.readLine();
      }

      catch(AdoException ae)
      {
         // Notify user of any errors that result from ADO.

         // As passing a recordset, check for null pointer.
         if (rstAuthors!=null)
         {
            PrintProviderError(rstAuthors.getActiveConnection());
         }
         else
         {
            System.out.println(" Exception: "+ ae.getMessage());
         }
      }
      // System Read requires this catch.
      catch(java.io.IOException je)
      {
         PrintIOError(je);
      }
      // Required if the user enter non integer value.
      catch(java.lang.NumberFormatException ne)
      {
         System.out.println("\n\nPlease enter integer values!");
         rstAuthors.close();
      }   
      
      finally
      {
         // Cleanup objects before exit.   
         if (rstAuthors != null)
            if (rstAuthors.getState() == 1)
               rstAuthors.close();
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
// EndMoveJ
</code>
      </introduction>
      <relatedTopics>
        <link xlink:href="13fe9381-d00b-4f4a-9162-83c3f21b3837">Move Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>