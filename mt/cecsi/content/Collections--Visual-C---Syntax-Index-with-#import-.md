---
title: "Collections (Visual C++ Syntax Index with #import)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 36fbca8e-1884-44b5-806b-d15e30f42fe6
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
# Collections (Visual C++ Syntax Index with #import)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="fffdc5772f7fd5b85f8e1578d763c4b3" id="tgt1" class="tgtSentence">It is useful to know that collections inherit certain common methods and properties.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="70c1a4ccc872830599b9d627d3817042" id="tgt2" class="tgtSentence">All collections inherit the <legacyBold>Count</legacyBold> property and <legacyBold>Refresh</legacyBold> method, and all collections add the <legacyBold>Item</legacyBold> property.</caps:sentence>
          <caps:sentence sentenceid="9540bef3e9c8b5211d67a8bf02dbd651" id="tgt3" class="tgtSentence"> The <legacyBold>Errors</legacyBold> collection adds the <legacyBold>Clear</legacyBold> method.</caps:sentence>
          <caps:sentence sentenceid="3160569abf18e59014879c27da12a24e" id="tgt4" class="tgtSentence"> The <legacyBold>Parameters</legacyBold> collection inherits the <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods, while the <legacyBold>Fields</legacyBold> collection adds the <legacyBold>Append</legacyBold>, <legacyBold>Delete</legacyBold>, and <legacyBold>Update</legacyBold> methods.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="7439ef29259e7f6c884c602c322db7d4" id="tgt5" class="tgtSentence">Properties Collection</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt6" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>HRESULT Refresh( );</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt7" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>long GetCount( ); __declspec(property(get=GetCount)) long Count;
PropertyPtr GetItem( const _variant_t &amp; Index ); __declspec(property(get=GetItem)) PropertyPtr Item[];</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="3c69e3f80ec3f7e1f6d12d9e4a0cea6d" id="tgt8" class="tgtSentence">Errors Collection</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt9" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>HRESULT Clear( );
HRESULT Refresh( );</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt10" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>long GetCount( ); __declspec(property(get=GetCount)) long Count;
PropertyPtr GetItem( const _variant_t &amp; Index ); __declspec(property(get=GetItem)) PropertyPtr Item[];</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="7de80a224c6430583d8aa944e23154fb" id="tgt11" class="tgtSentence">Parameters Collection</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt12" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>HRESULT Append( IDispatch * Object );
HRESULT Delete( const _variant_t &amp; Index );
HRESULT Refresh( );</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt13" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>long GetCount( ); __declspec(property(get=GetCount)) long Count;
PropertyPtr GetItem( const _variant_t &amp; Index ); __declspec(property(get=GetItem)) PropertyPtr Item[];</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="674ea0184650cb95a2fb260332db2e00" id="tgt14" class="tgtSentence">Fields Collection</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt15" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>HRESULT Append( _bstr_t Name, enum DataTypeEnum Type, long DefinedSize, enum FieldAttributeEnum Attrib, const _variant_t &amp; FieldValue = vtMissing );
HRESULT Delete( const _variant_t &amp; Index );
HRESULT Refresh( );
HRESULT Update( );</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt16" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>long GetCount( ); __declspec(property(get=GetCount)) long Count;
PropertyPtr GetItem( const _variant_t &amp; Index ); __declspec(property(get=GetItem)) PropertyPtr Item[];</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors Collection</link>
        <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">It is useful to know that collections inherit certain common methods and properties.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">All collections inherit the <legacyBold>Count</legacyBold> property and <legacyBold>Refresh</legacyBold> method, and all collections add the <legacyBold>Item</legacyBold> property.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> The <legacyBold>Errors</legacyBold> collection adds the <legacyBold>Clear</legacyBold> method.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> The <legacyBold>Parameters</legacyBold> collection inherits the <legacyBold>Append</legacyBold> and <legacyBold>Delete</legacyBold> methods, while the <legacyBold>Fields</legacyBold> collection adds the <legacyBold>Append</legacyBold>, <legacyBold>Delete</legacyBold>, and <legacyBold>Update</legacyBold> methods.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Properties Collection</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src6" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>HRESULT Refresh( );</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src7" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>long GetCount( ); __declspec(property(get=GetCount)) long Count;
PropertyPtr GetItem( const _variant_t &amp; Index ); __declspec(property(get=GetItem)) PropertyPtr Item[];</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Errors Collection</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src9" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>HRESULT Clear( );
HRESULT Refresh( );</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src10" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>long GetCount( ); __declspec(property(get=GetCount)) long Count;
PropertyPtr GetItem( const _variant_t &amp; Index ); __declspec(property(get=GetItem)) PropertyPtr Item[];</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Parameters Collection</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src12" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>HRESULT Append( IDispatch * Object );
HRESULT Delete( const _variant_t &amp; Index );
HRESULT Refresh( );</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src13" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>long GetCount( ); __declspec(property(get=GetCount)) long Count;
PropertyPtr GetItem( const _variant_t &amp; Index ); __declspec(property(get=GetItem)) PropertyPtr Item[];</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src14" class="srcSentence">Fields Collection</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src15" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>HRESULT Append( _bstr_t Name, enum DataTypeEnum Type, long DefinedSize, enum FieldAttributeEnum Attrib, const _variant_t &amp; FieldValue = vtMissing );
HRESULT Delete( const _variant_t &amp; Index );
HRESULT Refresh( );
HRESULT Update( );</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src16" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>long GetCount( ); __declspec(property(get=GetCount)) long Count;
PropertyPtr GetItem( const _variant_t &amp; Index ); __declspec(property(get=GetItem)) PropertyPtr Item[];</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors Collection</link>
        <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
        <link xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>