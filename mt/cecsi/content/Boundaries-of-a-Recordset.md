---
title: "Boundaries of a Recordset"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: c0dd4a0f-478d-4c5e-b5d5-7535f211d064
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
# Boundaries of a Recordset
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9e33f495c46570ca7b6a0fe1cc1eeeb3" id="tgt1" class="tgtSentence">       <legacyBold>Recordset</legacyBold> supports the <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> properties to delineate the beginning and end, respectively, of the dataset.</caps:sentence>
          <caps:sentence sentenceid="c3ffa46e5f3dbbac868c9699e0f87a36" id="tgt2" class="tgtSentence"> You can think of <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> as "phantom" records that are positioned at the beginning and end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="3614d0b67a949961f5898bfd6a353ec3" id="tgt3" class="tgtSentence"> Counting <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold>, our sample <legacyBold>Recordset</legacyBold> would now look like this:</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="cb67418f474bb3b2b21b66cad9903671" id="tgt4" class="tgtSentence">ProductID</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="af48c28310ee21958dc2e18cd8931006" id="tgt5" class="tgtSentence">ProductName</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="6ec30798c6c454112f9e7602cad8a562" id="tgt6" class="tgtSentence">UnitPrice</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="c9a3639b57c741dcd0334c28032e4280" id="tgt7" class="tgtSentence">BOF</caps:sentence>
                </para>
              </TD>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para> </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="8f14e45fceea167a5a36dedd4bea2543" id="tgt8" class="tgtSentence">7</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fc937ee4bc0e02154ac237d6016a70f9" id="tgt9" class="tgtSentence">Uncle Bob's Organic Dried Pears</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="dd986c04126f00a30158facd05409ffc" id="tgt10" class="tgtSentence">30.0000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="dfc3194543ebadf9c259174914c374ab" id="tgt11" class="tgtSentence">14   </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5df7f1701b778d03d57456afea567922" id="tgt12" class="tgtSentence">Tofu</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4b45f0162741df63b3e3275b3f97625a" id="tgt13" class="tgtSentence">23.2500</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="802dec10fe006738441fea9766d7c518" id="tgt14" class="tgtSentence">28   </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="83abeb51e88540f92b94b0e093d99a1a" id="tgt15" class="tgtSentence">Rssle Sauerkraut</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="719464c9a55af0f7b4eeb3d71b433113" id="tgt16" class="tgtSentence">45.6000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="b690b6baaf1e98713e6fbd05766c8a70" id="tgt17" class="tgtSentence">51   </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="57dff3a96fb1434cc3ba684ab1d661fa" id="tgt18" class="tgtSentence">Manjimup Dried Apples</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9d40d810dddcaade7299cdba2a78211c" id="tgt19" class="tgtSentence">53.0000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="ad61ab143223efbc24c7d2583be69251" id="tgt20" class="tgtSentence">74</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="037c61573ada8ba1a351164b56241b39" id="tgt21" class="tgtSentence">Longlife Tofu</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="863d6e51a2cc27a080f62327e719b41e" id="tgt22" class="tgtSentence">10.0000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="2e51b1ab42e8a4a67f3445174be5191b" id="tgt23" class="tgtSentence">EOF</caps:sentence>
                </para>
              </TD>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para> </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence sentenceid="b6d236d05732fb265f5e7938482f103f" id="tgt24" class="tgtSentence">When a cursor moves past the last record, <legacyBold>EOF </legacyBold>is set to <legacyBold>True</legacyBold>; otherwise, its value is <legacyBold>False</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="9d2e273800b557aa6443db1a1115636c" id="tgt25" class="tgtSentence"> Similarly, when the cursor moves before the first record, <legacyBold>BOF</legacyBold> is set to <legacyBold>True</legacyBold>; otherwise, its value is <legacyBold>False</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="eff33ba85ffda56789b7f7c5f99ef598" id="tgt26" class="tgtSentence"> These properties are commonly used to enumerate records in the dataset, as illustrated in the following JScript code fragment.</caps:sentence>
        </para>
        <code>while (objRecordset.EOF != true) 
{
   // Work on the current record.
   ...
   // Advance the cursor forward to the next record.
   objRecordset.MoveNext();
}
or
while (objRecordset.BOF != true) 
{
   // Work on the current record.
   ...
   // Move the cursor to the previous record.
   objRecordset.MovePrevious();
}</code>
        <para>
          <caps:sentence sentenceid="0ff79ed237dacb96b69f33f4576b4563" id="tgt27" class="tgtSentence">If both <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> are <legacyBold>True</legacyBold>, the <legacyBold>Recordset</legacyBold> object is empty.</caps:sentence>
          <caps:sentence sentenceid="2a4f8f50953a0033e52900dedb8860a4" id="tgt28" class="tgtSentence"> Both properties will be <legacyBold>False</legacyBold> for a newly opened, non-empty <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          <caps:sentence sentenceid="6ca98a2dfdbfcd8e64d8bd9b567f12a9" id="tgt29" class="tgtSentence"> You can use the <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> properties together to determine if a <legacyBold>Recordset</legacyBold> object is empty or not, as shown in the following JScript code fragment.</caps:sentence>
        </para>
        <code>if (objRecordset.EOF == true &amp;&amp; objRecordset.BOF == true)
{
   WScript.Echo("we got an empty dataset.");
}
else
{
   WScript.Echo("we got a full dataset.");
}</code>
        <para>
          <caps:sentence sentenceid="dba4f6dc6f3e6a0733bae1295f4baf77" id="tgt30" class="tgtSentence">This scheme works for all types of cursor and is independent of the underlying providers.</caps:sentence>
          <caps:sentence sentenceid="f2e7ccfc85db0ddd17058038941b82c6" id="tgt31" class="tgtSentence"> If you attempt to determine the emptiness of a <legacyBold>Recordset</legacyBold> object by checking if its <legacyBold>RecordCount</legacyBold> property value is zero (0) or not, you must take precautions to use an appropriate cursor and provider that support returning of the number of records in the result.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="fe012bcf5cdf64fd6f2969b6b007b3b5" id="tgt32" class="tgtSentence">If you delete the last remaining record in the <legacyBold>Recordset</legacyBold> object, the cursor is left in an indeterminate state.</caps:sentence>
          <caps:sentence sentenceid="7bd078095129d330fb7872d65008732c" id="tgt33" class="tgtSentence"> The <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> properties may remain <legacyBold>False</legacyBold> until you attempt to reposition the current record, depending upon the provider.</caps:sentence>
          <caps:sentence sentenceid="1231d2cfe6fad28bd97f64245921b4bb" id="tgt34" class="tgtSentence"> For more information, see <legacyLink xlink:href="bfed5cfa-7f57-463b-9da2-0c612a079d30">Deleting Records Using the Delete Method</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">       <legacyBold>Recordset</legacyBold> supports the <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> properties to delineate the beginning and end, respectively, of the dataset.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> You can think of <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> as "phantom" records that are positioned at the beginning and end of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Counting <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold>, our sample <legacyBold>Recordset</legacyBold> would now look like this:</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence">ProductID</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence">ProductName</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">UnitPrice</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">BOF</caps:sentence>
                </para>
              </TD>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para> </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">7</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">Uncle Bob's Organic Dried Pears</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">30.0000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">14   </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">Tofu</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">23.2500</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">28   </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">Rssle Sauerkraut</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">45.6000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">51   </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">Manjimup Dried Apples</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">53.0000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">74</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src21" class="srcSentence">Longlife Tofu</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src22" class="srcSentence">10.0000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src23" class="srcSentence">EOF</caps:sentence>
                </para>
              </TD>
              <TD>
                <para> </para>
              </TD>
              <TD>
                <para> </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence id="src24" class="srcSentence">When a cursor moves past the last record, <legacyBold>EOF </legacyBold>is set to <legacyBold>True</legacyBold>; otherwise, its value is <legacyBold>False</legacyBold>.</caps:sentence>
          <caps:sentence id="src25" class="srcSentence"> Similarly, when the cursor moves before the first record, <legacyBold>BOF</legacyBold> is set to <legacyBold>True</legacyBold>; otherwise, its value is <legacyBold>False</legacyBold>.</caps:sentence>
          <caps:sentence id="src26" class="srcSentence"> These properties are commonly used to enumerate records in the dataset, as illustrated in the following JScript code fragment.</caps:sentence>
        </para>
        <code>while (objRecordset.EOF != true) 
{
   // Work on the current record.
   ...
   // Advance the cursor forward to the next record.
   objRecordset.MoveNext();
}
or
while (objRecordset.BOF != true) 
{
   // Work on the current record.
   ...
   // Move the cursor to the previous record.
   objRecordset.MovePrevious();
}</code>
        <para>
          <caps:sentence id="src27" class="srcSentence">If both <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> are <legacyBold>True</legacyBold>, the <legacyBold>Recordset</legacyBold> object is empty.</caps:sentence>
          <caps:sentence id="src28" class="srcSentence"> Both properties will be <legacyBold>False</legacyBold> for a newly opened, non-empty <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          <caps:sentence id="src29" class="srcSentence"> You can use the <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> properties together to determine if a <legacyBold>Recordset</legacyBold> object is empty or not, as shown in the following JScript code fragment.</caps:sentence>
        </para>
        <code>if (objRecordset.EOF == true &amp;&amp; objRecordset.BOF == true)
{
   WScript.Echo("we got an empty dataset.");
}
else
{
   WScript.Echo("we got a full dataset.");
}</code>
        <para>
          <caps:sentence id="src30" class="srcSentence">This scheme works for all types of cursor and is independent of the underlying providers.</caps:sentence>
          <caps:sentence id="src31" class="srcSentence"> If you attempt to determine the emptiness of a <legacyBold>Recordset</legacyBold> object by checking if its <legacyBold>RecordCount</legacyBold> property value is zero (0) or not, you must take precautions to use an appropriate cursor and provider that support returning of the number of records in the result.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src32" class="srcSentence">If you delete the last remaining record in the <legacyBold>Recordset</legacyBold> object, the cursor is left in an indeterminate state.</caps:sentence>
          <caps:sentence id="src33" class="srcSentence"> The <legacyBold>BOF</legacyBold> and <legacyBold>EOF</legacyBold> properties may remain <legacyBold>False</legacyBold> until you attempt to reposition the current record, depending upon the provider.</caps:sentence>
          <caps:sentence id="src34" class="srcSentence"> For more information, see <legacyLink xlink:href="bfed5cfa-7f57-463b-9da2-0c612a079d30">Deleting Records Using the Delete Method</legacyLink>.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>