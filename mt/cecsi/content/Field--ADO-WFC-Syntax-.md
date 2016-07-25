---
title: "Field (ADO/WFC Syntax)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 7e01cb24-2338-4f92-ad46-8d97248e1a4d
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
# Field (ADO/WFC Syntax)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence sentenceid="bf01303ec05e42a8b2352d82e9a911f6" id="tgt1" class="tgtSentence">package com.ms.wfc.data</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt2" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public void appendChunk(byte[] bytes)
public void appendChunk(char[] chars)
public void appendChunk(String chars)
public byte[] getByteChunk(int len)
public char[] getCharChunk(int len)
public String getStringChunk(int len)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt3" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public int getActualSize()
public int getAttributes()
public void setAttributes(int pl)
public com.ms.com.IUnknown getDataFormat()
public void setDataFormat(com.ms.com.IUnknown format)</code>
              <para>
                <caps:sentence sentenceid="277ee22739016854116c8044806aaaf3" id="tgt4" class="tgtSentence">(For more information, see the Microsoft Visual J++ WFC Reference documentation for the com.ms.wfc.data.IDataFormat interface.)</caps:sentence>
              </para>
              <code>public int getDefinedSize()
public void setDefinedSize(int pl)
public String getName()
public int getNumericScale()
public void setNumericScale(byte pbNumericScale)
public Variant getOriginalValue()
public int getPrecision()
public void setPrecision(byte pbPrecision)
public int getType()
public void setType(int pDataType)
public Variant getUnderlyingValue()
public Variant getValue()
public void setValue(Variant value)
public AdoProperties getProperties()</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="1d1004acd43323b144b3e8dc0c3035f0" id="tgt5" class="tgtSentence">Field Accessor Methods</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a8f3512d7d501af95cbb82e910f99179" id="tgt6" class="tgtSentence">The <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object gets or sets the content of that object.</caps:sentence>
                <caps:sentence sentenceid="632f2ea18af4af8297be8267e1ed0564" id="tgt7" class="tgtSentence"> The content is represented as a VARIANT, a type of object that can be assigned a value and any of several data types.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="77d1463f9ab9e9792d3ec56443d5700c" id="tgt8" class="tgtSentence">ADO/WFC implements the <legacyBold>Value</legacyBold> property with the <legacyBold>getValue</legacyBold> method, which returns a VARIANT object; and the <legacyBold>setValue</legacyBold> method, which takes a VARIANT as an argument.</caps:sentence>
                <caps:sentence sentenceid="bed157ee2d677ffd81ffc13df784c032" id="tgt9" class="tgtSentence"> VARIANTs are highly efficient in certain languages, such as Microsoft Visual Basic.</caps:sentence>
                <caps:sentence sentenceid="d4f774198dd1ec444662eb7564967792" id="tgt10" class="tgtSentence"> However, you can attain better performance in Microsoft Visual J++ by using native Java data types.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="b7d329b8cf3a352a764f4c87ffb2f9a7" id="tgt11" class="tgtSentence">In addition to the <legacyBold>Value</legacyBold> property, ADO/WFC provides <legacyItalic>accessor </legacyItalic>methods that use Java data types to get and set the content of <legacyBold>Field</legacyBold> objects.</caps:sentence>
                <caps:sentence sentenceid="d66af0f93f34418347b814eb1da4e65e" id="tgt12" class="tgtSentence"> Most of these methods have names of the form <legacyBold>get</legacyBold><legacyItalic>DataType</legacyItalic> or <legacyBold>set</legacyBold><legacyItalic>DataType</legacyItalic>.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="383cdc424472519d51173bcbf70365ec" id="tgt13" class="tgtSentence">There are two noteworthy exceptions: One of the <legacyBold>getObject</legacyBold> methods returns an object coerced into a specified class.</caps:sentence>
                <caps:sentence sentenceid="f587d2f13e256d70d68cd0977b2ec1f4" id="tgt14" class="tgtSentence"> There is no <legacyBold>getNull</legacyBold> property; instead, there is an <legacyBold>isNull</legacyBold> property that returns a Boolean value indicating whether the field is null.</caps:sentence>
              </para>
              <code>public native boolean <codeFeaturedElement xmlns="">getBoolean</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setBoolean</codeFeaturedElement>(boolean <legacyItalic xmlns="">v</legacyItalic>)
public native byte <codeFeaturedElement xmlns="">getByte</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setByte</codeFeaturedElement>(byte <legacyItalic xmlns="">v</legacyItalic>)
public native byte[] <codeFeaturedElement xmlns="">getBytes</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setBytes</codeFeaturedElement>(byte[] <legacyItalic xmlns="">v</legacyItalic>)
public native double <codeFeaturedElement xmlns="">getDouble</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setDouble</codeFeaturedElement>(double <legacyItalic xmlns="">v</legacyItalic>)
public native float <codeFeaturedElement xmlns="">getFloat</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setFloat</codeFeaturedElement>(float <legacyItalic xmlns="">v</legacyItalic>)
public native int <codeFeaturedElement xmlns="">getInt</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setInt</codeFeaturedElement>(int <legacyItalic xmlns="">v</legacyItalic>)
public native long <codeFeaturedElement xmlns="">getLong</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setLong</codeFeaturedElement>(long <legacyItalic xmlns="">v</legacyItalic>)
public native short <codeFeaturedElement xmlns="">getShort</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setShort</codeFeaturedElement>(short <legacyItalic xmlns="">v</legacyItalic>)
public native String <codeFeaturedElement xmlns="">getString</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setString</codeFeaturedElement>(String <legacyItalic xmlns="">v</legacyItalic>)
public native boolean <codeFeaturedElement xmlns="">isNull</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setNull</codeFeaturedElement>()
public Object <codeFeaturedElement xmlns="">getObject</codeFeaturedElement>()
public Object <codeFeaturedElement xmlns="">getObject</codeFeaturedElement>(Class <legacyItalic xmlns="">c</legacyItalic>)
public void <codeFeaturedElement xmlns="">setObject</codeFeaturedElement>(Object <legacyItalic xmlns="">value</legacyItalic>)</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">package com.ms.wfc.data</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src2" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public void appendChunk(byte[] bytes)
public void appendChunk(char[] chars)
public void appendChunk(String chars)
public byte[] getByteChunk(int len)
public char[] getCharChunk(int len)
public String getStringChunk(int len)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src3" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public int getActualSize()
public int getAttributes()
public void setAttributes(int pl)
public com.ms.com.IUnknown getDataFormat()
public void setDataFormat(com.ms.com.IUnknown format)</code>
              <para>
                <caps:sentence id="src4" class="srcSentence">(For more information, see the Microsoft Visual J++ WFC Reference documentation for the com.ms.wfc.data.IDataFormat interface.)</caps:sentence>
              </para>
              <code>public int getDefinedSize()
public void setDefinedSize(int pl)
public String getName()
public int getNumericScale()
public void setNumericScale(byte pbNumericScale)
public Variant getOriginalValue()
public int getPrecision()
public void setPrecision(byte pbPrecision)
public int getType()
public void setType(int pDataType)
public Variant getUnderlyingValue()
public Variant getValue()
public void setValue(Variant value)
public AdoProperties getProperties()</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src5" class="srcSentence">Field Accessor Methods</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src6" class="srcSentence">The <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property of a <legacyLink xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field</legacyLink> object gets or sets the content of that object.</caps:sentence>
                <caps:sentence id="src7" class="srcSentence"> The content is represented as a VARIANT, a type of object that can be assigned a value and any of several data types.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src8" class="srcSentence">ADO/WFC implements the <legacyBold>Value</legacyBold> property with the <legacyBold>getValue</legacyBold> method, which returns a VARIANT object; and the <legacyBold>setValue</legacyBold> method, which takes a VARIANT as an argument.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> VARIANTs are highly efficient in certain languages, such as Microsoft Visual Basic.</caps:sentence>
                <caps:sentence id="src10" class="srcSentence"> However, you can attain better performance in Microsoft Visual J++ by using native Java data types.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src11" class="srcSentence">In addition to the <legacyBold>Value</legacyBold> property, ADO/WFC provides <legacyItalic>accessor </legacyItalic>methods that use Java data types to get and set the content of <legacyBold>Field</legacyBold> objects.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> Most of these methods have names of the form <legacyBold>get</legacyBold><legacyItalic>DataType</legacyItalic> or <legacyBold>set</legacyBold><legacyItalic>DataType</legacyItalic>.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src13" class="srcSentence">There are two noteworthy exceptions: One of the <legacyBold>getObject</legacyBold> methods returns an object coerced into a specified class.</caps:sentence>
                <caps:sentence id="src14" class="srcSentence"> There is no <legacyBold>getNull</legacyBold> property; instead, there is an <legacyBold>isNull</legacyBold> property that returns a Boolean value indicating whether the field is null.</caps:sentence>
              </para>
              <code>public native boolean <codeFeaturedElement xmlns="">getBoolean</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setBoolean</codeFeaturedElement>(boolean <legacyItalic xmlns="">v</legacyItalic>)
public native byte <codeFeaturedElement xmlns="">getByte</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setByte</codeFeaturedElement>(byte <legacyItalic xmlns="">v</legacyItalic>)
public native byte[] <codeFeaturedElement xmlns="">getBytes</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setBytes</codeFeaturedElement>(byte[] <legacyItalic xmlns="">v</legacyItalic>)
public native double <codeFeaturedElement xmlns="">getDouble</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setDouble</codeFeaturedElement>(double <legacyItalic xmlns="">v</legacyItalic>)
public native float <codeFeaturedElement xmlns="">getFloat</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setFloat</codeFeaturedElement>(float <legacyItalic xmlns="">v</legacyItalic>)
public native int <codeFeaturedElement xmlns="">getInt</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setInt</codeFeaturedElement>(int <legacyItalic xmlns="">v</legacyItalic>)
public native long <codeFeaturedElement xmlns="">getLong</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setLong</codeFeaturedElement>(long <legacyItalic xmlns="">v</legacyItalic>)
public native short <codeFeaturedElement xmlns="">getShort</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setShort</codeFeaturedElement>(short <legacyItalic xmlns="">v</legacyItalic>)
public native String <codeFeaturedElement xmlns="">getString</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setString</codeFeaturedElement>(String <legacyItalic xmlns="">v</legacyItalic>)
public native boolean <codeFeaturedElement xmlns="">isNull</codeFeaturedElement>();
public void <codeFeaturedElement xmlns="">setNull</codeFeaturedElement>()
public Object <codeFeaturedElement xmlns="">getObject</codeFeaturedElement>()
public Object <codeFeaturedElement xmlns="">getObject</codeFeaturedElement>(Class <legacyItalic xmlns="">c</legacyItalic>)
public void <codeFeaturedElement xmlns="">setObject</codeFeaturedElement>(Object <legacyItalic xmlns="">value</legacyItalic>)</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="b10a72fc-3c4b-4186-a70b-993dc9f7a092">Field Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>