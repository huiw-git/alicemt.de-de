---
title: "JScript Code Example to Return a Recordset"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - JScript
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 74aad8a6-06cc-4a2c-811a-d78f9b741d84
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
# JScript Code Example to Return a Recordset
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence sentenceid="78e3ec70199d44db6ed3ef0b7accedd0" id="tgt1" class="tgtSentence">JScript Code (rs.js)</caps:sentence>
        </title>
        <content>
          <code>main();

function main()
{
  DP = "SQLOLEDB";
  DS = "MySQLServer";
  DB = "NORTHWIND";

  adOpenForwardOnly = 0;
  adLockReadOnly = 1;
  adCmdText = 1;
  try 
  {
    var objRs = new ActiveXObject("ADODB.Recordset");
  }
  catch (e)
  {
    alert("ADODB namespace not found.");
    exit(0);
  }

  strConn =  "Provider="         +DP+
            ";Initial Catalog="  +DB+
            ";Data Source="      +DS+
            ";Integrated Security=SSPI;"
  strComm = "SELECT ProductID,ProductName,UnitPrice "+
            "FROM Products " + 
            "WHERE CategoryID = 7"  // select Produce

  objRs.open(strComm, 
             strConn, 
             adOpenForwardOnly,
             adLockReadOnly,
             adCmdText);

  objRs.MoveFirst();
  while (objRs.EOF != true) 
  {
    alert(objRs("ProductID")+"\t"
         +objRs("ProductName")+"\t"
         +objRs("UnitPrice"));
    objRs.MoveNext();
  }

  objRs.Close
  objRs = null;
}


function alert(str)
{
  WScript.Echo(str);
}</code>
          <procedure>
            <title>
              <caps:sentence sentenceid="eab739b3bf4161ac88e7077cd075b8e8" id="tgt2" class="tgtSentence">Try It!</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="88bfd083969781de373f9a111f9063e6" id="tgt3" class="tgtSentence">Save the code above into a text file.</caps:sentence>
                    <caps:sentence sentenceid="55d2abd1a75096614fd4fc6e77211b28" id="tgt4" class="tgtSentence"> Save the file as rs.js.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="260567535e1c5021f9ce6a469af101ed" id="tgt5" class="tgtSentence">Open a command prompt and cd to the directory where you have saved the JScript file (rs.js).</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence sentenceid="fdcd1aaa45e0588113843f02265fd172" id="tgt6" class="tgtSentence">Type <codeInline>CScript rs.js</codeInline> from the command prompt.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">JScript Code (rs.js)</caps:sentence>
        </title>
        <content>
          <code>main();

function main()
{
  DP = "SQLOLEDB";
  DS = "MySQLServer";
  DB = "NORTHWIND";

  adOpenForwardOnly = 0;
  adLockReadOnly = 1;
  adCmdText = 1;
  try 
  {
    var objRs = new ActiveXObject("ADODB.Recordset");
  }
  catch (e)
  {
    alert("ADODB namespace not found.");
    exit(0);
  }

  strConn =  "Provider="         +DP+
            ";Initial Catalog="  +DB+
            ";Data Source="      +DS+
            ";Integrated Security=SSPI;"
  strComm = "SELECT ProductID,ProductName,UnitPrice "+
            "FROM Products " + 
            "WHERE CategoryID = 7"  // select Produce

  objRs.open(strComm, 
             strConn, 
             adOpenForwardOnly,
             adLockReadOnly,
             adCmdText);

  objRs.MoveFirst();
  while (objRs.EOF != true) 
  {
    alert(objRs("ProductID")+"\t"
         +objRs("ProductName")+"\t"
         +objRs("UnitPrice"));
    objRs.MoveNext();
  }

  objRs.Close
  objRs = null;
}


function alert(str)
{
  WScript.Echo(str);
}</code>
          <procedure>
            <title>
              <caps:sentence id="src2" class="srcSentence">Try It!</caps:sentence>
            </title>
            <steps class="ordered">
              <step>
                <content>
                  <para>
                    <caps:sentence id="src3" class="srcSentence">Save the code above into a text file.</caps:sentence>
                    <caps:sentence id="src4" class="srcSentence"> Save the file as rs.js.</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src5" class="srcSentence">Open a command prompt and cd to the directory where you have saved the JScript file (rs.js).</caps:sentence>
                  </para>
                </content>
              </step>
              <step>
                <content>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">Type <codeInline>CScript rs.js</codeInline> from the command prompt.</caps:sentence>
                  </para>
                </content>
              </step>
            </steps>
          </procedure>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>