---
title: "ActiveConnection Property (ADO MD)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 2509b32c-a995-4364-9152-d8c83129bdd8
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
# ActiveConnection Property (ADO MD)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="7d7d52d1deeed596463392cf24235612" id="tgt1" class="tgtSentence">Indicates to which ADO <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object the current cellset or catalog currently belongs.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="74cd823babca996342dee42e03425406" id="tgt3" class="tgtSentence">Sets or returns a <languageKeyword>Variant</languageKeyword> that contains a string defining a connection or <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence sentenceid="dcc75f4156b6d34b5a3d3a241f18e512" id="tgt4" class="tgtSentence"> The default is empty.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="ad70cf349f86683cb8ee45b91711b101" id="tgt5" class="tgtSentence">You can set this property to a valid ADO <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object or to a valid connection string.</caps:sentence>
            <caps:sentence sentenceid="8c4e49badb798aafd9c2ddd003da05e3" id="tgt6" class="tgtSentence"> When this property is set to a connection string, the provider creates a new <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object using this definition and opens the connection.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="61ebbc1ad3915d164d56af378ba8f421" id="tgt7" class="tgtSentence">If you use the <parameterReference>ActiveConnection</parameterReference> argument of the <legacyLink xlink:href="a87d8080-a238-45e5-bc80-9a8625b3810f">Open</legacyLink> method to open a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object, the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property will inherit the value of the argument.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="798ffc3ab69a5d638134ce9dbb30ef77" id="tgt8" class="tgtSentence">Setting the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property of a <legacyLink xlink:href="11f6f896-d69c-44a4-94cd-d54c93140e4a">Catalog</legacyLink> object to <legacyBold>Nothing</legacyBold> releases the associated data, including data in the <legacyLink xlink:href="c79a5e36-71fd-44c4-948d-d6a7a89bb3b5">CubeDefs</legacyLink> collection and any related <legacyLink xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">Dimension</legacyLink>, <legacyLink xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy</legacyLink>, <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink>, and <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> objects.</caps:sentence>
            <caps:sentence sentenceid="5060efb4f473fefe439416b564e7351f" id="tgt9" class="tgtSentence"> Closing a <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object that was used to open a <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> has the same effect as setting the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property to <legacyBold>Nothing</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b7a9f83e98f0b25794dac56db6f7a3af" id="tgt10" class="tgtSentence">Changing the default database of the connection referenced by the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property of a <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> object invalidates the contents of the <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="644d72cdbaa9c807ccf5f06c9039f903" id="tgt11" class="tgtSentence">An error will occur if you attempt to change the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property for an open <unmanagedCodeEntityReference>Cellset</unmanagedCodeEntityReference> object.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="3516e15ba22f0ab32fae5bcd58b700fe" id="tgt12" class="tgtSentence">In Visual Basic, remember to use the <legacyBold>Set</legacyBold> keyword when setting the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property to a <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object.</caps:sentence>
              <caps:sentence sentenceid="23a8696d97163b86e018f49f6de25273" id="tgt13" class="tgtSentence"> If you omit the <legacyBold>Set</legacyBold> keyword, you will actually be setting the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property equal to the <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object's default property, <unmanagedCodeEntityReference>ConnectionString</unmanagedCodeEntityReference>.</caps:sentence>
              <caps:sentence sentenceid="c1db3f4a3dc5ff424ef0c75168365f92" id="tgt14" class="tgtSentence"> The code will work; however, you will create an additional connection to the data source, which may have negative performance implications.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="519fa7b8dd19b2e6f2db1ea1a92bca4c" id="tgt15" class="tgtSentence">When using the MSOLAP data provider, set the data source in a connection string to a server name and set the initial catalog to the name of a catalog from the data source.</caps:sentence>
            <caps:sentence sentenceid="5ec7f1362f9feed264f47132b83a8b9d" id="tgt16" class="tgtSentence"> To connect to a cube file that is disconnected from a server, set the location to the full path to the .CUB file.</caps:sentence>
            <caps:sentence sentenceid="8f29cc827af1e1d014bdc0189f35eea7" id="tgt17" class="tgtSentence"> In either case, set the provider to the provider name.</caps:sentence>
            <caps:sentence sentenceid="59ea894a9d81105916ff75c6d18353a2" id="tgt18" class="tgtSentence"> For example, the following string uses the MSOLAP Provider to connect to a catalog named Bobs Video Store on a server named <userInput>Servername</userInput>:</caps:sentence>
          </para>
          <code>"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"</code>
          <para>
            <caps:sentence sentenceid="e3312696406838aa2d20f55dad516416" id="tgt19" class="tgtSentence">The following string connects to a local cube file at the location C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub:</caps:sentence>
          </para>
          <code>"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"</code>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt20" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="11f6f896-d69c-44a4-94cd-d54c93140e4a">Catalog Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2666ad1c-b48e-4b2c-b269-5a9f4e4a7810">Visual Basic Example</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="a87d8080-a238-45e5-bc80-9a8625b3810f">Open Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates to which ADO <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object the current cellset or catalog currently belongs.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <languageKeyword>Variant</languageKeyword> that contains a string defining a connection or <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default is empty.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">You can set this property to a valid ADO <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object or to a valid connection string.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> When this property is set to a connection string, the provider creates a new <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object using this definition and opens the connection.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src7" class="srcSentence">If you use the <parameterReference>ActiveConnection</parameterReference> argument of the <legacyLink xlink:href="a87d8080-a238-45e5-bc80-9a8625b3810f">Open</legacyLink> method to open a <legacyLink xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset</legacyLink> object, the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property will inherit the value of the argument.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">Setting the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property of a <legacyLink xlink:href="11f6f896-d69c-44a4-94cd-d54c93140e4a">Catalog</legacyLink> object to <legacyBold>Nothing</legacyBold> releases the associated data, including data in the <legacyLink xlink:href="c79a5e36-71fd-44c4-948d-d6a7a89bb3b5">CubeDefs</legacyLink> collection and any related <legacyLink xlink:href="66adbbd2-23a3-4c19-a91b-84c31309aa1b">Dimension</legacyLink>, <legacyLink xlink:href="034af340-ac79-494e-ba5e-2b57da1cb9de">Hierarchy</legacyLink>, <legacyLink xlink:href="37815869-ed30-45fd-9aea-0a986c1b305c">Level</legacyLink>, and <legacyLink xlink:href="3dedf755-0741-4c3f-8b4e-bff8ff8809c8">Member</legacyLink> objects.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> Closing a <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object that was used to open a <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> has the same effect as setting the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property to <legacyBold>Nothing</legacyBold>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src10" class="srcSentence">Changing the default database of the connection referenced by the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property of a <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference> object invalidates the contents of the <unmanagedCodeEntityReference>Catalog</unmanagedCodeEntityReference>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">An error will occur if you attempt to change the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property for an open <unmanagedCodeEntityReference>Cellset</unmanagedCodeEntityReference> object.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src12" class="srcSentence">In Visual Basic, remember to use the <legacyBold>Set</legacyBold> keyword when setting the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property to a <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object.</caps:sentence>
              <caps:sentence id="src13" class="srcSentence"> If you omit the <legacyBold>Set</legacyBold> keyword, you will actually be setting the <unmanagedCodeEntityReference>ActiveConnection</unmanagedCodeEntityReference> property equal to the <unmanagedCodeEntityReference>Connection</unmanagedCodeEntityReference> object's default property, <unmanagedCodeEntityReference>ConnectionString</unmanagedCodeEntityReference>.</caps:sentence>
              <caps:sentence id="src14" class="srcSentence"> The code will work; however, you will create an additional connection to the data source, which may have negative performance implications.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src15" class="srcSentence">When using the MSOLAP data provider, set the data source in a connection string to a server name and set the initial catalog to the name of a catalog from the data source.</caps:sentence>
            <caps:sentence id="src16" class="srcSentence"> To connect to a cube file that is disconnected from a server, set the location to the full path to the .CUB file.</caps:sentence>
            <caps:sentence id="src17" class="srcSentence"> In either case, set the provider to the provider name.</caps:sentence>
            <caps:sentence id="src18" class="srcSentence"> For example, the following string uses the MSOLAP Provider to connect to a catalog named Bobs Video Store on a server named <userInput>Servername</userInput>:</caps:sentence>
          </para>
          <code>"Data Source=Servername;Initial Catalog=Bobs Video Store;Provider=msolap"</code>
          <para>
            <caps:sentence id="src19" class="srcSentence">The following string connects to a local cube file at the location C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub:</caps:sentence>
          </para>
          <code>"Location=C:\MSDASDK\samples\oledb\olap\data\bobsvid.cub;Provider=msolap"</code>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src20" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <table>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <link xlink:href="11f6f896-d69c-44a4-94cd-d54c93140e4a">Catalog Object</link>
                  </para>
                </TD>
                <TD>
                  <para>
                    <link xlink:href="5e2452c0-cac0-49b2-8099-836c35794d50">Cellset Object</link>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2666ad1c-b48e-4b2c-b269-5a9f4e4a7810">Visual Basic Example</link>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
        <link xlink:href="a87d8080-a238-45e5-bc80-9a8625b3810f">Open Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>