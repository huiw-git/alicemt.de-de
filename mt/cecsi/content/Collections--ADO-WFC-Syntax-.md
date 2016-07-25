---
title: "Collections (ADO/WFC Syntax)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 073f9a0e-c755-42dd-9f71-4647d68e331a
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
# Collections (ADO/WFC Syntax)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="57374143a31faae406b13948b475689e" id="tgt1" class="tgtSentence">       <legacyBold>package com.ms.wfc.data</legacyBold>     </caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="166e64f6c3677d0c513901242a3e702d" id="tgt2" class="tgtSentence">Parameters</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt3" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public void append(com.ms.wfc.data.Parameter param)
public void delete(int n)
public void delete(String s)
public void refresh()
public Parameter getItem(int n)
public Parameter getItem(String s)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt4" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public int getCount()</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="d05b6ed7d2345020440df396d6da7f73" id="tgt5" class="tgtSentence">Fields</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt6" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public void append(String name, int type)
public void append(String name, int type, int definedSize)
public void append(String name, int type, int definedSize, int attrib)
public void delete(int n)
public void delete(String s)
public void refresh()
public com.ms.wfc.data.Field getItem(int n)
public com.ms.wfc.data.Field getItem(String s)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt7" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public int getCount()</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="07213a0161f52846ab198be103b5ab43" id="tgt8" class="tgtSentence">Errors</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt9" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public void clear()
public void refresh()
public com.ms.wfc.data.Error getItem(int n)
public com.ms.wfc.data.Error getItem(String s)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt10" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public int getCount()</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors Collection</link>
        <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">       <legacyBold>package com.ms.wfc.data</legacyBold>     </caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src2" class="srcSentence">Parameters</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src3" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public void append(com.ms.wfc.data.Parameter param)
public void delete(int n)
public void delete(String s)
public void refresh()
public Parameter getItem(int n)
public Parameter getItem(String s)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src4" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public int getCount()</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Fields</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src6" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public void append(String name, int type)
public void append(String name, int type, int definedSize)
public void append(String name, int type, int definedSize, int attrib)
public void delete(int n)
public void delete(String s)
public void refresh()
public com.ms.wfc.data.Field getItem(int n)
public com.ms.wfc.data.Field getItem(String s)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src7" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public int getCount()</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src8" class="srcSentence">Errors</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src9" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public void clear()
public void refresh()
public com.ms.wfc.data.Error getItem(int n)
public com.ms.wfc.data.Error getItem(String s)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src10" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public int getCount()</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="290819e1-7b39-4e1e-a93b-801257138b00">Errors Collection</link>
        <link xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields Collection</link>
        <link xlink:href="497cae10-3913-422a-9753-dcbb0a639b1b">Parameters Collection</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>