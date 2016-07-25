---
title: "CommandTimeout Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: c611f857-d6b0-4dca-8925-f4a02e769eb0
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
# CommandTimeout Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="ae12968017fb31b2939ad0656bf8ea3e" id="tgt1" class="tgtSentence">Indicates how long to wait while executing a command before terminating the attempt and generating an error.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="65b486031c0bf07728afadc2d90b5eeb" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that indicates, in seconds, how long to wait for a command to execute.</caps:sentence>
            <caps:sentence sentenceid="36822011b2c150c0d42f024c32d0d775" id="tgt4" class="tgtSentence"> Default is 30.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="63e894a15966ef39c5347110f9e0a33e" id="tgt5" class="tgtSentence">Use the <legacyBold>CommandTimeout</legacyBold> property on a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object or <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object to allow the cancellation of an <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method call, due to delays from network traffic or heavy server use.</caps:sentence>
            <caps:sentence sentenceid="50a430af7a6b86e9eb2357d065859c2a" id="tgt6" class="tgtSentence"> If the interval set in the <legacyBold>CommandTimeout</legacyBold> property elapses before the command completes execution, an error occurs and ADO cancels the command.</caps:sentence>
            <caps:sentence sentenceid="4c98179429a62c93a56b20a4123b4b70" id="tgt7" class="tgtSentence"> If you set the property to zero, ADO will wait indefinitely until the execution is complete.</caps:sentence>
            <caps:sentence sentenceid="c8291906a2fdffc9539564eef10075ff" id="tgt8" class="tgtSentence"> Make sure the provider and data source to which you are writing code support the <legacyBold>CommandTimeout</legacyBold> functionality.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1949937b457fb6b28d79a91dac4c3fdf" id="tgt9" class="tgtSentence">The <legacyBold>CommandTimeout</legacyBold> setting on a <legacyBold>Connection</legacyBold> object has no effect on the <legacyBold>CommandTimeout</legacyBold> setting on a <legacyBold>Command</legacyBold> object on the same <legacyBold>Connection</legacyBold>; that is, the <legacyBold>Command</legacyBold> object's <legacyBold>CommandTimeout</legacyBold> property does not inherit the value of the <legacyBold>Connection</legacyBold> object's <legacyBold>CommandTimeout</legacyBold> value.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="ab1b330abc0d52cf728fbf97b582f1fb" id="tgt10" class="tgtSentence">On a <legacyBold>Connection</legacyBold> object, the <legacyBold>CommandTimeout</legacyBold> property remains read/write after the <legacyBold>Connection</legacyBold> is opened.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt11" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="dade4531-0bcc-4a52-8f86-b110ba2a3f9d">Visual Basic Example</link>
        <link xlink:href="0d9917c4-9ef0-4d7a-b4ce-4f1fa6ce1817">Visual C++ Example</link>
        <link xlink:href="69a4a219-8d52-401b-9e92-2ef415f68b05">Visual J++ Example</link>
        <link xlink:href="ea74e2a3-c965-43aa-9076-26a084b48ad8">JScriptExample</link>
        <link xlink:href="8904a403-1383-4b4b-b53d-5c01d6f5deac">ConnectionTimeout Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates how long to wait while executing a command before terminating the attempt and generating an error.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Long</languageKeyword> value that indicates, in seconds, how long to wait for a command to execute.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Default is 30.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Use the <legacyBold>CommandTimeout</legacyBold> property on a <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object or <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object to allow the cancellation of an <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method call, due to delays from network traffic or heavy server use.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> If the interval set in the <legacyBold>CommandTimeout</legacyBold> property elapses before the command completes execution, an error occurs and ADO cancels the command.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> If you set the property to zero, ADO will wait indefinitely until the execution is complete.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> Make sure the provider and data source to which you are writing code support the <legacyBold>CommandTimeout</legacyBold> functionality.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src9" class="srcSentence">The <legacyBold>CommandTimeout</legacyBold> setting on a <legacyBold>Connection</legacyBold> object has no effect on the <legacyBold>CommandTimeout</legacyBold> setting on a <legacyBold>Command</legacyBold> object on the same <legacyBold>Connection</legacyBold>; that is, the <legacyBold>Command</legacyBold> object's <legacyBold>CommandTimeout</legacyBold> property does not inherit the value of the <legacyBold>Connection</legacyBold> object's <legacyBold>CommandTimeout</legacyBold> value.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">On a <legacyBold>Connection</legacyBold> object, the <legacyBold>CommandTimeout</legacyBold> property remains read/write after the <legacyBold>Connection</legacyBold> is opened.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="dade4531-0bcc-4a52-8f86-b110ba2a3f9d">Visual Basic Example</link>
        <link xlink:href="0d9917c4-9ef0-4d7a-b4ce-4f1fa6ce1817">Visual C++ Example</link>
        <link xlink:href="69a4a219-8d52-401b-9e92-2ef415f68b05">Visual J++ Example</link>
        <link xlink:href="ea74e2a3-c965-43aa-9076-26a084b48ad8">JScriptExample</link>
        <link xlink:href="8904a403-1383-4b4b-b53d-5c01d6f5deac">ConnectionTimeout Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>