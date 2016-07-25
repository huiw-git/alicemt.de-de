---
title: "CursorType Property (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: b62c66ca-58d5-430e-9257-eb38c65e48c2
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
# CursorType Property (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="04b768b49c183a87334a163862705694" id="tgt1" class="tgtSentence">Indicates the type of cursor used in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="6f253c84dca33d0cd6f1b864ea701e8a" id="tgt2" class="tgtSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9931f4fbe8f4ec58a4442493d4924818" id="tgt3" class="tgtSentence">Sets or returns a <legacyLink xlink:href="ffc6e245-4471-42ae-84dd-e85bddfce983">CursorTypeEnum</legacyLink> value.</caps:sentence>
            <caps:sentence sentenceid="f7890568d843229a0211c2a51c319424" id="tgt4" class="tgtSentence"> The default value is <legacyBold>adOpenForwardOnly</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="b68944950aeaa62f1d1b332a24fe790a" id="tgt5" class="tgtSentence">Use the <legacyBold>CursorType</legacyBold> property to specify the type of cursor that should be used when opening the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="999285fab751ce931ca3677c873f495c" id="tgt6" class="tgtSentence">Only a setting of <legacyBold>adOpenStatic</legacyBold> is supported if the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            <caps:sentence sentenceid="9698459196ccc1130fc7213826553129" id="tgt7" class="tgtSentence"> If an unsupported value is set, then no error will result; the closest supported <legacyBold>CursorType</legacyBold> will be used instead.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="1e13b2f14f90c6c0d2d2cb10390b3f8a" id="tgt8" class="tgtSentence">If a provider does not support the requested cursor type, it may return another cursor type.</caps:sentence>
            <caps:sentence sentenceid="db2f21dafbd2197ab187848407a98936" id="tgt9" class="tgtSentence"> The <legacyBold>CursorType</legacyBold> property will change to match the actual cursor type in use when the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object is open.</caps:sentence>
            <caps:sentence sentenceid="68f1827a448055c5a98d9ccd545e2d0d" id="tgt10" class="tgtSentence"> To verify specific functionality of the returned cursor, use the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method.</caps:sentence>
            <caps:sentence sentenceid="1976e7d208724cf45f325b90391fff7e" id="tgt11" class="tgtSentence"> After you close the <legacyBold>Recordset</legacyBold>, the <legacyBold>CursorType</legacyBold> property reverts to its original setting.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="400d390a69e742178acb8c924d149601" id="tgt12" class="tgtSentence">The following chart shows the provider functionality (identified by <legacyBold>Supports</legacyBold> method constants) required for each cursor type.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a8efdaccc43f123721c96995271984be" id="tgt13" class="tgtSentence">For a Recordset of this CursorType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="19846dec3005e66432774b52ea42ce64" id="tgt14" class="tgtSentence">The Supports method must return True for all of these constants</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e98ad17a35c13fffa8a30f9a6165b1a4" id="tgt15" class="tgtSentence">
                      <legacyBold>adOpenForwardOnly</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="334c4a4c42fdb79d7ebc3e73b517e6f8" id="tgt16" class="tgtSentence">none</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="50c4fd4e6d24bad36a732dfa1a4b0ccd" id="tgt17" class="tgtSentence">
                      <legacyBold>adOpenKeyset</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bc7021d0f9e0e80001f89ccfb125f739" id="tgt18" class="tgtSentence">
                      <legacyBold>adBookmark</legacyBold>, <legacyBold>adHoldRecords</legacyBold>, <legacyBold>adMovePrevious</legacyBold>, <legacyBold>adResync</legacyBold></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8b69bba0d0a7fb2fdd15028debb317c1" id="tgt19" class="tgtSentence">
                      <legacyBold>adOpenDynamic</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e967549500cf9742438fda026f3fb915" id="tgt20" class="tgtSentence">
                      <legacyBold>adMovePrevious</legacyBold>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5d37d951a08ff7fa49baf4dd739c9f35" id="tgt21" class="tgtSentence">
                      <legacyBold>adOpenStatic</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bc7021d0f9e0e80001f89ccfb125f739" id="tgt22" class="tgtSentence">
                      <legacyBold>adBookmark</legacyBold>, <legacyBold>adHoldRecords</legacyBold>, <legacyBold>adMovePrevious</legacyBold>, <legacyBold>adResync</legacyBold></caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="2ff9374ae227f6f5aaead52a57b11e9f" id="tgt23" class="tgtSentence">Although <legacyBold>Supports</legacyBold>(<legacyBold>adUpdateBatch</legacyBold>) may be true for dynamic and forward-only cursors, for batch updates you should use either a keyset or static cursor.</caps:sentence>
              <caps:sentence sentenceid="d7f36fce00d5590220e2a240bea39d40" id="tgt24" class="tgtSentence"> Set the <legacyLink xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">LockType</legacyLink> property to <legacyBold>adLockBatchOptimistic</legacyBold> and the <legacyBold>CursorLocation</legacyBold> property to <legacyBold>adUseClient</legacyBold> to enable the Cursor Service for OLE DB, which is required for batch updates.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence sentenceid="605312e76c1a5e53a7e19456136f3eff" id="tgt25" class="tgtSentence">The <legacyBold>CursorType</legacyBold> property is read/write when the <legacyBold>Recordset</legacyBold> is closed and read-only when it is open.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="2d113d66182f5ac038ed34aec9d4b7e2" id="tgt26" class="tgtSentence">  <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Recordset</legacyBold> object, the <legacyBold>CursorType</legacyBold> property can be set only to <legacyBold>adOpenStatic</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt27" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2cb4a304-f40a-4897-8b93-82c2d8e93500">Visual Basic Example</link>
        <link xlink:href="b2a80e44-03d8-426e-81b6-dd9dfc30e181">Visual C++ Example</link>
        <link xlink:href="c222016e-415d-485e-86c5-e29feac4297a">Visual J++ Example</link>
        <link xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Indicates the type of cursor used in a <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Settings and Return Values</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src3" class="srcSentence">Sets or returns a <legacyLink xlink:href="ffc6e245-4471-42ae-84dd-e85bddfce983">CursorTypeEnum</legacyLink> value.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> The default value is <legacyBold>adOpenForwardOnly</legacyBold>.</caps:sentence>
          </para>
        </content>
      </section>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src5" class="srcSentence">Use the <legacyBold>CursorType</legacyBold> property to specify the type of cursor that should be used when opening the <legacyBold>Recordset</legacyBold> object.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">Only a setting of <legacyBold>adOpenStatic</legacyBold> is supported if the <legacyLink xlink:href="39c8d86e-7ee9-4182-be5e-aad5ce952f84">CursorLocation</legacyLink> property is set to <legacyBold>adUseClient</legacyBold>.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> If an unsupported value is set, then no error will result; the closest supported <legacyBold>CursorType</legacyBold> will be used instead.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">If a provider does not support the requested cursor type, it may return another cursor type.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> The <legacyBold>CursorType</legacyBold> property will change to match the actual cursor type in use when the <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink> object is open.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> To verify specific functionality of the returned cursor, use the <legacyLink xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports</legacyLink> method.</caps:sentence>
            <caps:sentence id="src11" class="srcSentence"> After you close the <legacyBold>Recordset</legacyBold>, the <legacyBold>CursorType</legacyBold> property reverts to its original setting.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">The following chart shows the provider functionality (identified by <legacyBold>Supports</legacyBold> method constants) required for each cursor type.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">For a Recordset of this CursorType</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">The Supports method must return True for all of these constants</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">
                      <legacyBold>adOpenForwardOnly</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src16" class="srcSentence">none</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src17" class="srcSentence">
                      <legacyBold>adOpenKeyset</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src18" class="srcSentence">
                      <legacyBold>adBookmark</legacyBold>, <legacyBold>adHoldRecords</legacyBold>, <legacyBold>adMovePrevious</legacyBold>, <legacyBold>adResync</legacyBold></caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">
                      <legacyBold>adOpenDynamic</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">
                      <legacyBold>adMovePrevious</legacyBold>             </caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src21" class="srcSentence">
                      <legacyBold>adOpenStatic</legacyBold>             </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">
                      <legacyBold>adBookmark</legacyBold>, <legacyBold>adHoldRecords</legacyBold>, <legacyBold>adMovePrevious</legacyBold>, <legacyBold>adResync</legacyBold></caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
          <alert class="note">
            <para>
              <caps:sentence id="src23" class="srcSentence">Although <legacyBold>Supports</legacyBold>(<legacyBold>adUpdateBatch</legacyBold>) may be true for dynamic and forward-only cursors, for batch updates you should use either a keyset or static cursor.</caps:sentence>
              <caps:sentence id="src24" class="srcSentence"> Set the <legacyLink xlink:href="9920c14e-033a-4de1-8149-0ce9737a3246">LockType</legacyLink> property to <legacyBold>adLockBatchOptimistic</legacyBold> and the <legacyBold>CursorLocation</legacyBold> property to <legacyBold>adUseClient</legacyBold> to enable the Cursor Service for OLE DB, which is required for batch updates.</caps:sentence>
            </para>
          </alert>
          <para>
            <caps:sentence id="src25" class="srcSentence">The <legacyBold>CursorType</legacyBold> property is read/write when the <legacyBold>Recordset</legacyBold> is closed and read-only when it is open.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src26" class="srcSentence">  <legacyBold>Remote Data Service Usage</legacyBold>   When used on a client-side <legacyBold>Recordset</legacyBold> object, the <legacyBold>CursorType</legacyBold> property can be set only to <legacyBold>adOpenStatic</legacyBold>.</caps:sentence>
            </para>
          </alert>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src27" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</link>
          </para>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="2cb4a304-f40a-4897-8b93-82c2d8e93500">Visual Basic Example</link>
        <link xlink:href="b2a80e44-03d8-426e-81b6-dd9dfc30e181">Visual C++ Example</link>
        <link xlink:href="c222016e-415d-485e-86c5-e29feac4297a">Visual J++ Example</link>
        <link xlink:href="298fc41c-0b55-42fc-b373-c5133b4da6a5">Supports Method</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>