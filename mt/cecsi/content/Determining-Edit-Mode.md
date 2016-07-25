---
title: "Determining Edit Mode"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 4c7e010d-08cd-4e22-9b32-23c36f02f88c
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
# Determining Edit Mode
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="332080f9b83c3db0e4eeb3e5f307f547" id="tgt1" class="tgtSentence">ADO maintains an editing buffer associated with the current record.</caps:sentence>
          <caps:sentence sentenceid="524186ab838966a162b9791241b70158" id="tgt2" class="tgtSentence"> The <legacyBold>EditMode</legacyBold> property indicates whether changes have been made to this buffer or whether a new record has been created.</caps:sentence>
          <caps:sentence sentenceid="b3d494532950b058e16b09b61ed99203" id="tgt3" class="tgtSentence"> Use <legacyBold>EditMode</legacyBold> to determine the editing status of the current record.</caps:sentence>
          <caps:sentence sentenceid="1f8b1b18bbfb889787e321ae1dd90252" id="tgt4" class="tgtSentence"> You can test for pending changes if an editing process has been interrupted and determine whether you need to use the <legacyBold>Update</legacyBold> or <legacyBold>CancelUpdate</legacyBold> method.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="aeb752104a4835588637edc6b66be8e0" id="tgt5" class="tgtSentence">         <legacyBold>EditMode</legacyBold> returns one of the <legacyBold>EditModeEnum</legacyBold> constants, which are listed in the following table.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt6" class="tgtSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt7" class="tgtSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="4eacd231a7eebf7ed9bd23cb62e6be29" id="tgt8" class="tgtSentence">               <legacyBold>adEditNone</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d1ad8c182967745e5661855c99c97503" id="tgt9" class="tgtSentence">Indicates that no editing operation is in progress.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="70f6703b7dd2df2e49e995833e840d8b" id="tgt10" class="tgtSentence">               <legacyBold>adEditInProgress</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="a50ec37533cee50d9676f0dd3ce70959" id="tgt11" class="tgtSentence">Indicates that data in the current record has been modified but not saved.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="6457b7dbcc3376782bc83ede7af899b3" id="tgt12" class="tgtSentence">               <legacyBold>adEditAdd</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="d87c5a3f41a5b2f1c714ccae9f037046" id="tgt13" class="tgtSentence">Indicates that the <legacyBold>AddNew</legacyBold> method has been called, and the current record in the copy buffer is a new record that has not been saved to the database.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="f19636aadd96efa063420ae4e985cd05" id="tgt14" class="tgtSentence">               <legacyBold>adEditDelete</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="c9ade55f9682c765096c80589b2f1866" id="tgt15" class="tgtSentence">Indicates that the current record has been deleted.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence sentenceid="025cb84e87addbb1657305f8444f95bc" id="tgt16" class="tgtSentence">         <legacyBold>EditMode</legacyBold> can return a valid value only if there is a current record.</caps:sentence>
          <caps:sentence sentenceid="8d3c72e66b982a5b46905f01047000f8" id="tgt17" class="tgtSentence">
            <legacyBold>EditMode</legacyBold> will return an error if <legacyBold>BOF</legacyBold> or <legacyBold>EOF</legacyBold> is <legacyBold>True</legacyBold> or if the current record has been deleted.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">ADO maintains an editing buffer associated with the current record.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> The <legacyBold>EditMode</legacyBold> property indicates whether changes have been made to this buffer or whether a new record has been created.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> Use <legacyBold>EditMode</legacyBold> to determine the editing status of the current record.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> You can test for pending changes if an editing process has been interrupted and determine whether you need to use the <legacyBold>Update</legacyBold> or <legacyBold>CancelUpdate</legacyBold> method.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">         <legacyBold>EditMode</legacyBold> returns one of the <legacyBold>EditModeEnum</legacyBold> constants, which are listed in the following table.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">Constant</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Description</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">               <legacyBold>adEditNone</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">Indicates that no editing operation is in progress.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">               <legacyBold>adEditInProgress</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">Indicates that data in the current record has been modified but not saved.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">               <legacyBold>adEditAdd</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Indicates that the <legacyBold>AddNew</legacyBold> method has been called, and the current record in the copy buffer is a new record that has not been saved to the database.</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">               <legacyBold>adEditDelete</legacyBold>             </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">Indicates that the current record has been deleted.</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence id="src16" class="srcSentence">         <legacyBold>EditMode</legacyBold> can return a valid value only if there is a current record.</caps:sentence>
          <caps:sentence id="src17" class="srcSentence">
            <legacyBold>EditMode</legacyBold> will return an error if <legacyBold>BOF</legacyBold> or <legacyBold>EOF</legacyBold> is <legacyBold>True</legacyBold> or if the current record has been deleted.</caps:sentence>
        </para>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>