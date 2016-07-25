---
title: "Handling Errors in JScript"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - JScript
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 3de527e5-2e65-4ab0-9b7f-6d317c4478de
caps.latest.revision: 3
caps.handback.revision: 3
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
# Handling Errors in JScript
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ca49753abfd866de6d89cf8c600d0e71" id="tgt1" class="tgtSentence">Your Microsoft® JScript® code must check the <legacyBold>Count</legacyBold> property of the <legacyBold>Connection</legacyBold> object's <legacyBold>Errors</legacyBold> collection.</caps:sentence>
          <caps:sentence sentenceid="c3c9b722e5cb0b0ab4be37071ec3a1db" id="tgt2" class="tgtSentence"> If the value is greater than 0, iterate through the collection and print the values as you would in any of the other languages.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>&lt;!-- BeginErrorExampleJS --&gt;
&lt;%@ Language=JScript %&gt;
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;title&gt;Error Handling Example (JScript)&lt;/title&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;h1&gt;Error Handling Example (JScript)&lt;/h1&gt;
&lt;%
   var cnn1 = Server.CreateObject("ADODB.Connection");
   var errLoop = Server.CreateObject("ADODB.Error");
   var strError = new String;

   // Intentionally trigger an error.
   cnn1.Open("nothing");

   if (cnn1.Errors.Count &gt; 0) {
      // Enumerate Errors collection and display
      // properties of each Error object.
      for (var i = 1; i &lt; cnn1.Errors.Count; i++) {
         errLoop = cnn1.Errors(i);
         strError = "Error #" &amp; errLoop.Number + "&lt;br&gt;" +
            "   " + errLoop.Description + "&lt;br&gt;" +
            "   (Source: " &amp; errLoop.Source &amp; ")" + "&lt;br&gt;" +
            "   (SQL State: " &amp; errLoop.SQLState + ")" + "&lt;br&gt;" +
            "   (NativeError: " &amp; errLoop.NativeError + ")" + "&lt;br&gt;";
         if (errLoop.HelpFile == "")
            strError = strError +
               "   No Help file available" +
               "&lt;br&gt;&lt;br&gt;";
         else
            strError = strError +
               "   (HelpFile: " &amp; errLoop.HelpFile &amp; ")" &amp; "&lt;br&gt;" +
               "   (HelpContext: " &amp; errLoop.HelpContext &amp; ")" +
               "&lt;br&gt;&lt;br&gt;";
         Response.Write("&lt;p&gt;" &amp; strError &amp; "&lt;/p&gt;");
      }
   }
%&gt;

&lt;/BODY&gt;
&lt;/HTML&gt;
&lt;!-- EndErrorExampleJS --&gt;</code>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Your Microsoft® JScript® code must check the <legacyBold>Count</legacyBold> property of the <legacyBold>Connection</legacyBold> object's <legacyBold>Errors</legacyBold> collection.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> If the value is greater than 0, iterate through the collection and print the values as you would in any of the other languages.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <code>&lt;!-- BeginErrorExampleJS --&gt;
&lt;%@ Language=JScript %&gt;
&lt;HTML&gt;
&lt;HEAD&gt;
&lt;title&gt;Error Handling Example (JScript)&lt;/title&gt;
&lt;/HEAD&gt;
&lt;BODY&gt;
&lt;h1&gt;Error Handling Example (JScript)&lt;/h1&gt;
&lt;%
   var cnn1 = Server.CreateObject("ADODB.Connection");
   var errLoop = Server.CreateObject("ADODB.Error");
   var strError = new String;

   // Intentionally trigger an error.
   cnn1.Open("nothing");

   if (cnn1.Errors.Count &gt; 0) {
      // Enumerate Errors collection and display
      // properties of each Error object.
      for (var i = 1; i &lt; cnn1.Errors.Count; i++) {
         errLoop = cnn1.Errors(i);
         strError = "Error #" &amp; errLoop.Number + "&lt;br&gt;" +
            "   " + errLoop.Description + "&lt;br&gt;" +
            "   (Source: " &amp; errLoop.Source &amp; ")" + "&lt;br&gt;" +
            "   (SQL State: " &amp; errLoop.SQLState + ")" + "&lt;br&gt;" +
            "   (NativeError: " &amp; errLoop.NativeError + ")" + "&lt;br&gt;";
         if (errLoop.HelpFile == "")
            strError = strError +
               "   No Help file available" +
               "&lt;br&gt;&lt;br&gt;";
         else
            strError = strError +
               "   (HelpFile: " &amp; errLoop.HelpFile &amp; ")" &amp; "&lt;br&gt;" +
               "   (HelpContext: " &amp; errLoop.HelpContext &amp; ")" +
               "&lt;br&gt;&lt;br&gt;";
         Response.Write("&lt;p&gt;" &amp; strError &amp; "&lt;/p&gt;");
      }
   }
%&gt;

&lt;/BODY&gt;
&lt;/HTML&gt;
&lt;!-- EndErrorExampleJS --&gt;</code>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>