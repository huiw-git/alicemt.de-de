---
title: "ActiveConnection Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 52d0a96c-14fb-4ad9-b004-4d821bc0a6db
caps.latest.revision: 11
caps.handback.revision: 11
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
# ActiveConnection Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="0446ae6da72be25be94faf2b45091507" id="tgt1" class="tgtSentence">Indicates to which <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object the specified <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink>, <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, or <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object currently belongs.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="8bb3ddac3e79a2cd59d9dde831aed2c4" id="tgt3" class="tgtSentence">Sets or returns a <legacyBold>String</legacyBold> value that contains a definition for a connection if the connection is closed, or a <legacyBold>Variant</legacyBold> containing the current <legacyBold>Connection</legacyBold> object if the connection is open.</caps:sentence>
            <caps:sentence sentenceid="79aa835488fc134e3c0b2bff8da3c128" id="tgt4" class="tgtSentence"> Default is a null object reference.</caps:sentence>
            <caps:sentence sentenceid="6281268c8a579bda4927df3e3f3e65fb" id="tgt5" class="tgtSentence"> See the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="90800ca8dec3135c5342e130dc61a7ad" id="tgt6" class="tgtSentence">Use the <legacyBold>ActiveConnection</legacyBold> property to determine the <legacyBold>Connection</legacyBold> object over which the specified <legacyBold>Command</legacyBold> object will execute or the specified <legacyBold>Recordset</legacyBold> will be opened.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="1dccadfed7bcbb036c56a4afb97e906f" id="tgt7" class="tgtSentence">Command</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a5118b17e0988736b685353325173c67" id="tgt8" class="tgtSentence">For <legacyBold>Command</legacyBold> objects, the <legacyBold>ActiveConnection</legacyBold> property is read/write.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="4fc348615c1c4b622cdb95cf9fcc2d79" id="tgt9" class="tgtSentence">If you attempt to call the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method on a <legacyBold>Command</legacyBold> object before setting this property to an open <legacyBold>Connection</legacyBold> object or valid connection string, an error occurs.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="48fc9819d69b76f8506fdf618453559a" id="tgt10" class="tgtSentence">If a <legacyBold>Connection</legacyBold> object is assigned to the <legacyBold>ActiveConnection</legacyBold> property, the object must be opened.</caps:sentence>
                <caps:sentence sentenceid="fba10e2414bcd8fbd23cf1ba189e9841" id="tgt11" class="tgtSentence"> Assigning a closed Connection object causes an error.</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence sentenceid="aad653ca3ee669635f2938b73098b6d7" id="tgt12" class="tgtSentence">Note</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence sentenceid="232af9f7b06129fde229c73ed17f042d" id="tgt13" class="tgtSentence">
                      <legacyBold>Microsoft Visual Basic</legacyBold>   Setting the <legacyBold>ActiveConnection</legacyBold> property to <legacyItalic>Nothing</legacyItalic> disassociates the <legacyBold>Command</legacyBold> object from the current <legacyBold>Connection</legacyBold> and causes the provider to release any associated resources on the data source.</caps:sentence>
                    <caps:sentence sentenceid="23769bec2d42fcead2ae8a2137ab16f8" id="tgt14" class="tgtSentence"> You can then associate the <legacyBold>Command</legacyBold> object with the same or another <legacyBold>Connection</legacyBold> object.</caps:sentence>
                    <caps:sentence sentenceid="e5852fc5ffacee5f53bd059d041ad6c6" id="tgt15" class="tgtSentence"> Some providers allow you to change the property setting from one <legacyBold>Connection</legacyBold> to another, without having to first set the property to <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="0769a391da04e45f7e91200c9ab7ae09" id="tgt16" class="tgtSentence">If the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection of the <legacyBold>Command</legacyBold> object contains parameters supplied by the provider, the collection is cleared if you set the <legacyBold>ActiveConnection</legacyBold> property to <legacyItalic>Nothing</legacyItalic> or to another <legacyBold>Connection</legacyBold> object.</caps:sentence>
                    <caps:sentence sentenceid="c5848a664bd35ae9cc09b7a8fb067717" id="tgt17" class="tgtSentence"> If you manually create <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> objects and use them to fill the <legacyBold>Parameters</legacyBold> collection of the <legacyBold>Command</legacyBold> object, setting the <legacyBold>ActiveConnection</legacyBold> property to <legacyItalic>Nothing</legacyItalic> or to another <legacyBold>Connection</legacyBold> object leaves the <legacyBold>Parameters</legacyBold> collection intact.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="bd904a8b2d4bf227ad1e48912dc73a91" id="tgt18" class="tgtSentence">Closing the <legacyBold>Connection</legacyBold> object with which a <legacyBold>Command</legacyBold> object is associated sets the <legacyBold>ActiveConnection</legacyBold> property to <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
                    <caps:sentence sentenceid="9a475e2ee7140d3f1f2960940b2323bd" id="tgt19" class="tgtSentence"> Setting this property to a closed <legacyBold>Connection</legacyBold> object generates an error.</caps:sentence>
                  </para>
                </content>
              </section>
            </sections>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="c1e71ce69bff36c1582c5f180ea9a4ff" id="tgt20" class="tgtSentence">Recordset</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a48a9be8daf16fe180e62e35ffbc4ba1" id="tgt21" class="tgtSentence">For open <legacyBold>Recordset</legacyBold> objects or for <legacyBold>Recordset</legacyBold> objects whose <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source</legacyLink> property is set to a valid <legacyBold>Command</legacyBold> object, the <legacyBold>ActiveConnection</legacyBold> property is read-only.</caps:sentence>
                <caps:sentence sentenceid="c55851a7bc0e90c9d011bd5117307c32" id="tgt22" class="tgtSentence"> Otherwise, it is read/write.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="1d22883383dd8950eae8bc5c4e3c372e" id="tgt23" class="tgtSentence">You can set this property to a valid <legacyBold>Connection</legacyBold> object or to a valid connection string.</caps:sentence>
                <caps:sentence sentenceid="0a978907958fefbda3df580d2fb9b1f3" id="tgt24" class="tgtSentence"> In this case, the provider creates a new <legacyBold>Connection</legacyBold> object using this definition and opens the connection.</caps:sentence>
                <caps:sentence sentenceid="f50ac3dd884a0c8fd11a5f755b20b8b5" id="tgt25" class="tgtSentence"> Additionally, the provider may set this property to the new <legacyBold>Connection</legacyBold> object to give you a way to access the <legacyBold>Connection</legacyBold> object for extended error information or to execute other commands.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="afd90076b9e7e1c5225c5864abf599a8" id="tgt26" class="tgtSentence">If you use the <legacyItalic>ActiveConnection</legacyItalic> argument of the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method to open a <legacyBold>Recordset</legacyBold> object, the <legacyBold>ActiveConnection</legacyBold> property will inherit the value of the argument.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="0031f56e03069ccd133fdda3ec788fc5" id="tgt27" class="tgtSentence">If you set the <legacyBold>Source</legacyBold> property of the <legacyBold>Recordset</legacyBold> object to a valid <legacyBold>Command</legacyBold> object variable, the <legacyBold>ActiveConnection</legacyBold> property of the <legacyBold>Recordset</legacyBold> inherits the setting of the <legacyBold>Command</legacyBold> object's <legacyBold>ActiveConnection</legacyBold> property.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="2589c6705bcc0e4e440bdc36355d44ba" id="tgt28" class="tgtSentence">               <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Recordset</legacyBold> object, this property can be set only to a connection string or (in Microsoft Visual Basic or Visual Basic, Scripting Edition) to <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="de17f0f24b49f8364187891f8550ffbb" id="tgt29" class="tgtSentence">Record</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a1b6f4b9695cfd6b8b6150f516742495" id="tgt30" class="tgtSentence">This property is read/write when the <legacyBold>Record</legacyBold> object is closed, and may contain a connection string or reference to an open <legacyBold>Connection</legacyBold> object.</caps:sentence>
                <caps:sentence sentenceid="888001ffbcf482a778d631240e74a545" id="tgt31" class="tgtSentence"> This property is read-only when the <legacyBold>Record</legacyBold> object is open, and contains a reference to an open <legacyBold>Connection</legacyBold> object.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="46ca5d6ff5795747faa1ea22ad8c4dee" id="tgt32" class="tgtSentence">A <legacyBold>Connection</legacyBold> object is created implicitly when the <legacyBold>Record</legacyBold> object is opened from a URL.</caps:sentence>
                <caps:sentence sentenceid="0af9337df969476ed372c3f073210d81" id="tgt33" class="tgtSentence"> Open the <legacyBold>Record</legacyBold> with an existing, open <legacyBold>Connection</legacyBold> object by assigning the <legacyBold>Connection</legacyBold> object to this property, or using the <legacyBold>Connection</legacyBold> object as a parameter in the <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open</legacyLink> method call.</caps:sentence>
                <caps:sentence sentenceid="d8e6086c8d6e4d14c51d9a2c5f5ed34d" id="tgt34" class="tgtSentence"> If the <legacyBold>Record</legacyBold> is opened from an existing <legacyBold>Record</legacyBold> or <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, then it is automatically associated with that <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> object's <legacyBold>Connection</legacyBold> object.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="1cdf0678c0a6d5e5a2fb6cddde2d9630" id="tgt35" class="tgtSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
                  <caps:sentence sentenceid="7fb1f04accf352ebcc15a2b5ca2f177f" id="tgt36" class="tgtSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt37" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
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
        <link xlink:href="69a4a219-8d52-401b-9e92-2ef415f68b05">Visual J++Example</link>
        <link xlink:href="ea74e2a3-c965-43aa-9076-26a084b48ad8">JScriptExample</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates to which <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object the specified <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink>, <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, or <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object currently belongs.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <legacyBold>String</legacyBold> value that contains a definition for a connection if the connection is closed, or a <legacyBold>Variant</legacyBold> containing the current <legacyBold>Connection</legacyBold> object if the connection is open.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Default is a null object reference.</caps:sentence>
            <caps:sentence id="src5" class="srcSentence"> See the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">Use the <legacyBold>ActiveConnection</legacyBold> property to determine the <legacyBold>Connection</legacyBold> object over which the specified <legacyBold>Command</legacyBold> object will execute or the specified <legacyBold>Recordset</legacyBold> will be opened.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src7" class="srcSentence">Command</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src8" class="srcSentence">For <legacyBold>Command</legacyBold> objects, the <legacyBold>ActiveConnection</legacyBold> property is read/write.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src9" class="srcSentence">If you attempt to call the <legacyLink xlink:href="f84a5ff3-0528-4ad7-9bea-9a15103378dd">Execute</legacyLink> method on a <legacyBold>Command</legacyBold> object before setting this property to an open <legacyBold>Connection</legacyBold> object or valid connection string, an error occurs.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src10" class="srcSentence">If a <legacyBold>Connection</legacyBold> object is assigned to the <legacyBold>ActiveConnection</legacyBold> property, the object must be opened.</caps:sentence>
                <caps:sentence id="src11" class="srcSentence"> Assigning a closed Connection object causes an error.</caps:sentence>
              </para>
            </content>
            <sections>
              <section>
                <title>
                  <caps:sentence id="src12" class="srcSentence">Note</caps:sentence>
                </title>
                <content>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">
                      <legacyBold>Microsoft Visual Basic</legacyBold>   Setting the <legacyBold>ActiveConnection</legacyBold> property to <legacyItalic>Nothing</legacyItalic> disassociates the <legacyBold>Command</legacyBold> object from the current <legacyBold>Connection</legacyBold> and causes the provider to release any associated resources on the data source.</caps:sentence>
                    <caps:sentence id="src14" class="srcSentence"> You can then associate the <legacyBold>Command</legacyBold> object with the same or another <legacyBold>Connection</legacyBold> object.</caps:sentence>
                    <caps:sentence id="src15" class="srcSentence"> Some providers allow you to change the property setting from one <legacyBold>Connection</legacyBold> to another, without having to first set the property to <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">If the <legacyLink xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters</legacyLink> collection of the <legacyBold>Command</legacyBold> object contains parameters supplied by the provider, the collection is cleared if you set the <legacyBold>ActiveConnection</legacyBold> property to <legacyItalic>Nothing</legacyItalic> or to another <legacyBold>Connection</legacyBold> object.</caps:sentence>
                    <caps:sentence id="src17" class="srcSentence"> If you manually create <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> objects and use them to fill the <legacyBold>Parameters</legacyBold> collection of the <legacyBold>Command</legacyBold> object, setting the <legacyBold>ActiveConnection</legacyBold> property to <legacyItalic>Nothing</legacyItalic> or to another <legacyBold>Connection</legacyBold> object leaves the <legacyBold>Parameters</legacyBold> collection intact.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">Closing the <legacyBold>Connection</legacyBold> object with which a <legacyBold>Command</legacyBold> object is associated sets the <legacyBold>ActiveConnection</legacyBold> property to <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
                    <caps:sentence id="src19" class="srcSentence"> Setting this property to a closed <legacyBold>Connection</legacyBold> object generates an error.</caps:sentence>
                  </para>
                </content>
              </section>
            </sections>
          </section>
          <section>
            <title>
              <caps:sentence id="src20" class="srcSentence">Recordset</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src21" class="srcSentence">For open <legacyBold>Recordset</legacyBold> objects or for <legacyBold>Recordset</legacyBold> objects whose <legacyLink xlink:href="a05ba2c9-2821-4343-8607-4de9b764ec91">Source</legacyLink> property is set to a valid <legacyBold>Command</legacyBold> object, the <legacyBold>ActiveConnection</legacyBold> property is read-only.</caps:sentence>
                <caps:sentence id="src22" class="srcSentence"> Otherwise, it is read/write.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src23" class="srcSentence">You can set this property to a valid <legacyBold>Connection</legacyBold> object or to a valid connection string.</caps:sentence>
                <caps:sentence id="src24" class="srcSentence"> In this case, the provider creates a new <legacyBold>Connection</legacyBold> object using this definition and opens the connection.</caps:sentence>
                <caps:sentence id="src25" class="srcSentence"> Additionally, the provider may set this property to the new <legacyBold>Connection</legacyBold> object to give you a way to access the <legacyBold>Connection</legacyBold> object for extended error information or to execute other commands.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src26" class="srcSentence">If you use the <legacyItalic>ActiveConnection</legacyItalic> argument of the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method to open a <legacyBold>Recordset</legacyBold> object, the <legacyBold>ActiveConnection</legacyBold> property will inherit the value of the argument.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src27" class="srcSentence">If you set the <legacyBold>Source</legacyBold> property of the <legacyBold>Recordset</legacyBold> object to a valid <legacyBold>Command</legacyBold> object variable, the <legacyBold>ActiveConnection</legacyBold> property of the <legacyBold>Recordset</legacyBold> inherits the setting of the <legacyBold>Command</legacyBold> object's <legacyBold>ActiveConnection</legacyBold> property.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src28" class="srcSentence">               <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Recordset</legacyBold> object, this property can be set only to a connection string or (in Microsoft Visual Basic or Visual Basic, Scripting Edition) to <legacyItalic>Nothing</legacyItalic>.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src29" class="srcSentence">Record</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src30" class="srcSentence">This property is read/write when the <legacyBold>Record</legacyBold> object is closed, and may contain a connection string or reference to an open <legacyBold>Connection</legacyBold> object.</caps:sentence>
                <caps:sentence id="src31" class="srcSentence"> This property is read-only when the <legacyBold>Record</legacyBold> object is open, and contains a reference to an open <legacyBold>Connection</legacyBold> object.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src32" class="srcSentence">A <legacyBold>Connection</legacyBold> object is created implicitly when the <legacyBold>Record</legacyBold> object is opened from a URL.</caps:sentence>
                <caps:sentence id="src33" class="srcSentence"> Open the <legacyBold>Record</legacyBold> with an existing, open <legacyBold>Connection</legacyBold> object by assigning the <legacyBold>Connection</legacyBold> object to this property, or using the <legacyBold>Connection</legacyBold> object as a parameter in the <legacyLink xlink:href="ab79a623-88a9-40b6-a017-a658bf19b778">Open</legacyLink> method call.</caps:sentence>
                <caps:sentence id="src34" class="srcSentence"> If the <legacyBold>Record</legacyBold> is opened from an existing <legacyBold>Record</legacyBold> or <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, then it is automatically associated with that <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> object's <legacyBold>Connection</legacyBold> object.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src35" class="srcSentence">URLs using the http scheme will automatically invoke the <legacyLink xlink:href="66a208d9-b580-4655-a41e-1d36e5b5bfca">Microsoft OLE DB Provider for Internet Publishing</legacyLink>.</caps:sentence>
                  <caps:sentence id="src36" class="srcSentence"> For more information, see <legacyLink xlink:href="6a34a7ef-50cc-4c3d-82f7-106b9a8f3caf">Absolute and Relative URLs</legacyLink>.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
        </sections>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src37" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
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
        <link xlink:href="69a4a219-8d52-401b-9e92-2ef415f68b05">Visual J++Example</link>
        <link xlink:href="ea74e2a3-c965-43aa-9076-26a084b48ad8">JScriptExample</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString Property</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>