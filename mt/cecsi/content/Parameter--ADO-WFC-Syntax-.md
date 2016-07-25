---
title: "Parameter (ADO/WFC Syntax)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: d00d1e1e-14b1-41a2-a00f-2a3cb7396f15
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
# Parameter (ADO/WFC Syntax)
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
              <caps:sentence sentenceid="6ca268371eeb5d93eefeb68f96157666" id="tgt2" class="tgtSentence">Constructor</caps:sentence>
            </title>
            <content>
              <code>public Parameter()
public Parameter(String name)
public Parameter(String name, int type)
public Parameter(String name, int type, int dir)
public Parameter(String name, int type, int dir, int size)
public Parameter(String name, int type, int dir, int size, Object value)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt3" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public void appendChunk(byte[] bytes)
public void appendChunk(char[] chars)
public void appendChunk(String chars)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt4" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public int getAttributes()
public void setAttributes(int attr)
public int getDirection()
public void setDirection(int dir)
public String getName()
public void setName(String name)
public int getNumericScale()
public void setNumericScale(int scale)
public int getPrecision()
public void setPrecision(int prec)
public int getSize()
public void setSize(int size)
public int getType()
public void setType(int type)
public com.ms.com.Variant getValue()
public void setValue(Object v)
public AdoProperties getProperties()</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="ea1996e1e8f018dd0c220ef412a45ff6" id="tgt5" class="tgtSentence">Parameter Accessor Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="87e7b3d07400856dc7a16e2aa8abbb3d" id="tgt6" class="tgtSentence">The <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property of a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object gets or sets the content of that object.</caps:sentence>
            <caps:sentence sentenceid="632f2ea18af4af8297be8267e1ed0564" id="tgt7" class="tgtSentence"> The content is represented as a VARIANT, a type of object that can be assigned a value and any of several data types.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="77d1463f9ab9e9792d3ec56443d5700c" id="tgt8" class="tgtSentence">ADO/WFC implements the <legacyBold>Value</legacyBold> property with the <legacyBold>getValue</legacyBold> method, which returns a VARIANT object; and the <legacyBold>setValue</legacyBold> method, which takes a VARIANT as an argument.</caps:sentence>
            <caps:sentence sentenceid="bed157ee2d677ffd81ffc13df784c032" id="tgt9" class="tgtSentence"> VARIANTs are highly efficient in certain languages, such as Microsoft Visual Basic.</caps:sentence>
            <caps:sentence sentenceid="d4f774198dd1ec444662eb7564967792" id="tgt10" class="tgtSentence"> However, you can attain better performance in Microsoft Visual J++ by using native Java data types.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="35e6290cc6bac39a8896f9bd760e4d75" id="tgt11" class="tgtSentence">In addition to the <legacyBold>Value</legacyBold> property, ADO/WFC provides <legacyItalic>accessor </legacyItalic>methods that use Java data types to get and set the content of <legacyBold>Parameter</legacyBold> objects.</caps:sentence>
            <caps:sentence sentenceid="d66af0f93f34418347b814eb1da4e65e" id="tgt12" class="tgtSentence"> Most of these methods have names of the form <legacyBold>get</legacyBold><legacyItalic>DataType</legacyItalic> or <legacyBold>set</legacyBold><legacyItalic>DataType</legacyItalic>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="98da47ca6c8404bbdf1c5365519ced32" id="tgt13" class="tgtSentence">There is one noteworthy exception: There is no <legacyBold>getNull</legacyBold> property; instead, there is an <legacyBold>isNull</legacyBold> property that returns a Boolean value indicating whether the field is null.</caps:sentence>
          </para>
          <code>public boolean <codeFeaturedElement xmlns="">getBoolean</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setBoolean</codeFeaturedElement>(boolean <legacyItalic xmlns="">v</legacyItalic>)
public byte <codeFeaturedElement xmlns="">getByte</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setByte</codeFeaturedElement>(byte <legacyItalic xmlns="">v</legacyItalic>)
public double <codeFeaturedElement xmlns="">getDouble</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setDouble</codeFeaturedElement>(double <legacyItalic xmlns="">v</legacyItalic>)
public float <codeFeaturedElement xmlns="">getFloat</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setFloat</codeFeaturedElement>(float <legacyItalic xmlns="">v</legacyItalic>)
public int <codeFeaturedElement xmlns="">getInt</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setInt</codeFeaturedElement>(int <legacyItalic xmlns="">v</legacyItalic>)
public long <codeFeaturedElement xmlns="">getLong</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setLong</codeFeaturedElement>(long <legacyItalic xmlns="">v</legacyItalic>)
public short <codeFeaturedElement xmlns="">getShort</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setShort</codeFeaturedElement>(short <legacyItalic xmlns="">v</legacyItalic>)
public String <codeFeaturedElement xmlns="">getString</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setString</codeFeaturedElement>(String <legacyItalic xmlns="">v</legacyItalic>)
public boolean <codeFeaturedElement xmlns="">isNull</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setNull</codeFeaturedElement>()</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter Object</link>
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
              <caps:sentence id="src2" class="srcSentence">Constructor</caps:sentence>
            </title>
            <content>
              <code>public Parameter()
public Parameter(String name)
public Parameter(String name, int type)
public Parameter(String name, int type, int dir)
public Parameter(String name, int type, int dir, int size)
public Parameter(String name, int type, int dir, int size, Object value)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src3" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public void appendChunk(byte[] bytes)
public void appendChunk(char[] chars)
public void appendChunk(String chars)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src4" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public int getAttributes()
public void setAttributes(int attr)
public int getDirection()
public void setDirection(int dir)
public String getName()
public void setName(String name)
public int getNumericScale()
public void setNumericScale(int scale)
public int getPrecision()
public void setPrecision(int prec)
public int getSize()
public void setSize(int size)
public int getType()
public void setType(int type)
public com.ms.com.Variant getValue()
public void setValue(Object v)
public AdoProperties getProperties()</code>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src5" class="srcSentence">Parameter Accessor Methods</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src6" class="srcSentence">The <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property of a <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> object gets or sets the content of that object.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> The content is represented as a VARIANT, a type of object that can be assigned a value and any of several data types.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src8" class="srcSentence">ADO/WFC implements the <legacyBold>Value</legacyBold> property with the <legacyBold>getValue</legacyBold> method, which returns a VARIANT object; and the <legacyBold>setValue</legacyBold> method, which takes a VARIANT as an argument.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> VARIANTs are highly efficient in certain languages, such as Microsoft Visual Basic.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> However, you can attain better performance in Microsoft Visual J++ by using native Java data types.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">In addition to the <legacyBold>Value</legacyBold> property, ADO/WFC provides <legacyItalic>accessor </legacyItalic>methods that use Java data types to get and set the content of <legacyBold>Parameter</legacyBold> objects.</caps:sentence>
            <caps:sentence id="src12" class="srcSentence"> Most of these methods have names of the form <legacyBold>get</legacyBold><legacyItalic>DataType</legacyItalic> or <legacyBold>set</legacyBold><legacyItalic>DataType</legacyItalic>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src13" class="srcSentence">There is one noteworthy exception: There is no <legacyBold>getNull</legacyBold> property; instead, there is an <legacyBold>isNull</legacyBold> property that returns a Boolean value indicating whether the field is null.</caps:sentence>
          </para>
          <code>public boolean <codeFeaturedElement xmlns="">getBoolean</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setBoolean</codeFeaturedElement>(boolean <legacyItalic xmlns="">v</legacyItalic>)
public byte <codeFeaturedElement xmlns="">getByte</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setByte</codeFeaturedElement>(byte <legacyItalic xmlns="">v</legacyItalic>)
public double <codeFeaturedElement xmlns="">getDouble</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setDouble</codeFeaturedElement>(double <legacyItalic xmlns="">v</legacyItalic>)
public float <codeFeaturedElement xmlns="">getFloat</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setFloat</codeFeaturedElement>(float <legacyItalic xmlns="">v</legacyItalic>)
public int <codeFeaturedElement xmlns="">getInt</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setInt</codeFeaturedElement>(int <legacyItalic xmlns="">v</legacyItalic>)
public long <codeFeaturedElement xmlns="">getLong</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setLong</codeFeaturedElement>(long <legacyItalic xmlns="">v</legacyItalic>)
public short <codeFeaturedElement xmlns="">getShort</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setShort</codeFeaturedElement>(short <legacyItalic xmlns="">v</legacyItalic>)
public String <codeFeaturedElement xmlns="">getString</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setString</codeFeaturedElement>(String <legacyItalic xmlns="">v</legacyItalic>)
public boolean <codeFeaturedElement xmlns="">isNull</codeFeaturedElement>()
public void <codeFeaturedElement xmlns="">setNull</codeFeaturedElement>()</code>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>