---
title: "CursorLocation Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 39c8d86e-7ee9-4182-be5e-aad5ce952f84
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
# CursorLocation Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="677007e48496a9ed18d6dc143899295f" id="tgt1" class="tgtSentence">Indicates the location of the cursor service.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings And Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="7611b6cfb09bf77d3935bfcae8ec6fe6" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that can be set to one of the <legacyLink xlink:href="acb255ff-1734-4b70-89bb-aef862b4c63b">CursorLocationEnum</legacyLink> values.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="7146c2f44958c1f2f619d48ed57411c5" id="tgt4" class="tgtSentence">This property allows you to choose between various cursor libraries accessible to the provider.</caps:sentence>
            <caps:sentence sentenceid="bfb86fbe98eb7ee020cefcd50af7ac18" id="tgt5" class="tgtSentence"> Usually, you can choose between using a client-side cursor library or one that is located on the server.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="f7fca736d821227e39c79ebbc2d0bf54" id="tgt6" class="tgtSentence">This property setting affects connections established only after the property has been set.</caps:sentence>
            <caps:sentence sentenceid="7e292b63b119443540166db25001ef14" id="tgt7" class="tgtSentence"> Changing the <legacyBold>CursorLocation</legacyBold> property has no effect on existing connections.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b37e25a656cf1ba305aa16b189c6f76b" id="tgt8" class="tgtSentence">Cursors returned by the <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> method inherit this setting.</caps:sentence>
            <caps:sentence sentenceid="2cdb3994b7328ad7b35da85495a4f909" id="tgt9" class="tgtSentence">
              <legacyBold>Recordset</legacyBold> objects will automatically inherit this setting from their associated connections.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="3a053d76a6e70bb3cc0c6afae08f251c" id="tgt10" class="tgtSentence">This property is read/write on a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> or a closed <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, and read-only on an open <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="05033f687a4943fbad9febbdece3054b" id="tgt11" class="tgtSentence"> <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Recordset</legacyBold> or <legacyBold>Connection</legacyBold> object, the <legacyBold>CursorLocation</legacyBold> property can only be set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt12" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the location of the cursor service.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings And Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that can be set to one of the <legacyLink xlink:href="acb255ff-1734-4b70-89bb-aef862b4c63b">CursorLocationEnum</legacyLink> values.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src4" class="srcSentence">This property allows you to choose between various cursor libraries accessible to the provider.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> Usually, you can choose between using a client-side cursor library or one that is located on the server.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">This property setting affects connections established only after the property has been set.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Changing the <legacyBold>CursorLocation</legacyBold> property has no effect on existing connections.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">Cursors returned by the <legacyLink xlink:href="03c69320-96b2-4d85-8d49-a13b13e31578">Execute</legacyLink> method inherit this setting.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence">
              <legacyBold>Recordset</legacyBold> objects will automatically inherit this setting from their associated connections.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">This property is read/write on a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> or a closed <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, and read-only on an open <legacyBold>Recordset</legacyBold>.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src11" class="srcSentence"> <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Recordset</legacyBold> or <legacyBold>Connection</legacyBold> object, the <legacyBold>CursorLocation</legacyBold> property can only be set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src12" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>