---
title: "Command (ADO/WFC Syntax)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 39d0aa06-03ac-4c9a-8400-83947756ef99
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
# Command (ADO/WFC Syntax)
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
              <code>public Command()
public Command(String commandtext)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt3" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public void cancel()
public com.ms.wfc.data.Parameter createParameter(String
    Name, int Type, int Direction, int Size, Object Value)
public Recordset execute()
public Recordset execute(Object[] parameters)
public Recordset execute(Object[] parameters, int options)
public int executeUpdate(Object[] parameters)
public int executeUpdate(Object[] parameters, int options)
public int executeUpdate()</code>
              <para>
                <caps:sentence sentenceid="0021a37eafaf7a0ed30088e6cb0d2a1b" id="tgt4" class="tgtSentence">The <legacyBold>executeUpdate</legacyBold> method is a special case method that calls the underlying ADO <legacyBold>execute</legacyBold> method with certain parameters.</caps:sentence>
                <caps:sentence sentenceid="21b2d96554814600d76373443a54454b" id="tgt5" class="tgtSentence"> The <legacyBold>executeUpdate</legacyBold> method does not support the return of a <legacyBold>Recordset</legacyBold> object, so the <legacyBold>execute</legacyBold> method's <legacyItalic>options</legacyItalic> parameter is modified with <legacyBold>AdoEnums.ExecuteOptions.NORECORDS</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="b13dba8c8497ab86179540310396b627" id="tgt6" class="tgtSentence"> After the <legacyBold>execute</legacyBold> method completes, its updated <legacyItalic>RecordsAffected </legacyItalic>parameter is passed back to the <legacyBold>executeUpdate</legacyBold> method, which is finally returned as an <legacyBold>int</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt7" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public com.ms.wfc.data.Connection getActiveConnection()
public void setActiveConnection(com.ms.wfc.data.Connection con)
public void setActiveConnection(String conString)
public String getCommandText()
public void setCommandText(String command)
public int getCommandTimeout()
public void setCommandTimeout(int timeout)
public int getCommandType()
public void setCommandType(int type)
public String getName()
public void setName(String name)
public boolean getPrepared()
public void setPrepared(boolean prepared)
public int getState()
public com.ms.wfc.data.Parameter getParameter(int n)
public com.ms.wfc.data.Parameter getParameter(String n)
public com.ms.wfc.data.Parameters getParameters()
public AdoProperties getProperties()</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
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
              <code>public Command()
public Command(String commandtext)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src3" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public void cancel()
public com.ms.wfc.data.Parameter createParameter(String
    Name, int Type, int Direction, int Size, Object Value)
public Recordset execute()
public Recordset execute(Object[] parameters)
public Recordset execute(Object[] parameters, int options)
public int executeUpdate(Object[] parameters)
public int executeUpdate(Object[] parameters, int options)
public int executeUpdate()</code>
              <para>
                <caps:sentence id="src4" class="srcSentence">The <legacyBold>executeUpdate</legacyBold> method is a special case method that calls the underlying ADO <legacyBold>execute</legacyBold> method with certain parameters.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> The <legacyBold>executeUpdate</legacyBold> method does not support the return of a <legacyBold>Recordset</legacyBold> object, so the <legacyBold>execute</legacyBold> method's <legacyItalic>options</legacyItalic> parameter is modified with <legacyBold>AdoEnums.ExecuteOptions.NORECORDS</legacyBold>.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> After the <legacyBold>execute</legacyBold> method completes, its updated <legacyItalic>RecordsAffected </legacyItalic>parameter is passed back to the <legacyBold>executeUpdate</legacyBold> method, which is finally returned as an <legacyBold>int</legacyBold>.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src7" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public com.ms.wfc.data.Connection getActiveConnection()
public void setActiveConnection(com.ms.wfc.data.Connection con)
public void setActiveConnection(String conString)
public String getCommandText()
public void setCommandText(String command)
public int getCommandTimeout()
public void setCommandTimeout(int timeout)
public int getCommandType()
public void setCommandType(int type)
public String getName()
public void setName(String name)
public boolean getPrepared()
public void setPrepared(boolean prepared)
public int getState()
public com.ms.wfc.data.Parameter getParameter(int n)
public com.ms.wfc.data.Parameter getParameter(String n)
public com.ms.wfc.data.Parameters getParameters()
public AdoProperties getProperties()</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>