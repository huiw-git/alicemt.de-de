---
title: "Connection (ADO/WFC Syntax)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 8cfc35bb-91e2-47da-ad4c-982e9162cd51
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
# Connection (ADO/WFC Syntax)
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
              <code>public Connection()
public Connection(String connectionstring)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt3" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public int beginTrans()
public void commitTrans()
public void rollbackTrans()
public void cancel()
public void close()
public com.ms.wfc.data.Recordset execute(String commandText)
public com.ms.wfc.data.Recordset execute(String commandText, int options)
public int executeUpdate(String commandText)
public int executeUpdate(String commandText, int options)</code>
              <para>
                <caps:sentence sentenceid="0021a37eafaf7a0ed30088e6cb0d2a1b" id="tgt4" class="tgtSentence">The <legacyBold>executeUpdate</legacyBold> method is a special case method that calls the underlying ADO <legacyBold>execute</legacyBold> method with certain parameters.</caps:sentence>
                <caps:sentence sentenceid="21b2d96554814600d76373443a54454b" id="tgt5" class="tgtSentence"> The <legacyBold>executeUpdate</legacyBold> method does not support the return of a <legacyBold>Recordset</legacyBold> object, so the <legacyBold>execute</legacyBold> method's <legacyItalic>options</legacyItalic> parameter is modified with <legacyBold>AdoEnums.ExecuteOptions.NORECORDS</legacyBold>.</caps:sentence>
                <caps:sentence sentenceid="b13dba8c8497ab86179540310396b627" id="tgt6" class="tgtSentence"> After the <legacyBold>execute</legacyBold> method completes, its updated <legacyItalic>RecordsAffected </legacyItalic>parameter is passed back to the <legacyBold>executeUpdate</legacyBold> method, which is finally returned as an <legacyBold>int</legacyBold>.</caps:sentence>
              </para>
              <code>public void open() 
public void open(String connectionString)
public void open(String connectionString, String userID)
public void open(String connectionString, String userID, String password)
public void open(String connectionString, String userID, String password, int options)
public Recordset openSchema(int schema, Object[]
    restrictions, String schemaID)
public Recordset openSchema(int schema)
public Recordset openSchema(int schema, Object[] restrictions)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt7" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public int getAttributes()
public void setAttributes(int attr)
public int getCommandTimeout()
public void setCommandTimeout(int timeout)
public String getConnectionString()
public void setConnectionString(String con)
public int getConnectionTimeout()
public void setConnectionTimeout(int timeout)
public int getCursorLocation()
public void setCursorLocation(int cursorLoc)
public String getDefaultDatabase()
public void setDefaultDatabase(String db)
public int getIsolationLevel()
public void setIsolationLevel(int level)
public int getMode()
public void setMode(int mode)
public String getProvider()
public void setProvider(String provider)
public int getState()
public String getVersion()
public AdoProperties getProperties()
public com.ms.wfc.data.Errors getErrors()</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="16908b0605f2645dfcb4c3a8d248cef3" id="tgt8" class="tgtSentence">Events</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="276d96f05aabe47f2c409664d64fa5d1" id="tgt9" class="tgtSentence">For more information about ADO/WFC events, see <legacyLink xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</legacyLink>.</caps:sentence>
              </para>
              <code>public void addOnBeginTransComplete(ConnectionEventHandler handler)
public void removeOnBeginTransComplete(ConnectionEventHandler handler)
public void addOnCommitTransComplete(ConnectionEventHandler handler)
public void removeOnCommitTransComplete(ConnectionEventHandler handler)
public void addOnConnectComplete(ConnectionEventHandler handler)
public void removeOnConnectComplete(ConnectionEventHandler handler)
public void addOnDisconnect(ConnectionEventHandler handler)
public void removeOnDisconnect(ConnectionEventHandler handler)
public void addOnExecuteComplete(ConnectionEventHandler handler)
public void removeOnExecuteComplete(ConnectionEventHandler handler)
public void addOnInfoMessage(ConnectionEventHandler handler)
public void removeOnInfoMessage(ConnectionEventHandler handler)
public void addOnRollbackTransComplete(ConnectionEventHandler handler)
public void removeOnRollbackTransComplete(ConnectionEventHandler handler)
public void addOnWillConnect(ConnectionEventHandler handler)
public void removeOnWillConnect(ConnectionEventHandler handler)
public void addOnWillExecute(ConnectionEventHandler handler)
public void removeOnWillExecute(ConnectionEventHandler handler)</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
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
              <code>public Connection()
public Connection(String connectionstring)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src3" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>public int beginTrans()
public void commitTrans()
public void rollbackTrans()
public void cancel()
public void close()
public com.ms.wfc.data.Recordset execute(String commandText)
public com.ms.wfc.data.Recordset execute(String commandText, int options)
public int executeUpdate(String commandText)
public int executeUpdate(String commandText, int options)</code>
              <para>
                <caps:sentence id="src4" class="srcSentence">The <legacyBold>executeUpdate</legacyBold> method is a special case method that calls the underlying ADO <legacyBold>execute</legacyBold> method with certain parameters.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> The <legacyBold>executeUpdate</legacyBold> method does not support the return of a <legacyBold>Recordset</legacyBold> object, so the <legacyBold>execute</legacyBold> method's <legacyItalic>options</legacyItalic> parameter is modified with <legacyBold>AdoEnums.ExecuteOptions.NORECORDS</legacyBold>.</caps:sentence>
                <caps:sentence id="src6" class="srcSentence"> After the <legacyBold>execute</legacyBold> method completes, its updated <legacyItalic>RecordsAffected </legacyItalic>parameter is passed back to the <legacyBold>executeUpdate</legacyBold> method, which is finally returned as an <legacyBold>int</legacyBold>.</caps:sentence>
              </para>
              <code>public void open() 
public void open(String connectionString)
public void open(String connectionString, String userID)
public void open(String connectionString, String userID, String password)
public void open(String connectionString, String userID, String password, int options)
public Recordset openSchema(int schema, Object[]
    restrictions, String schemaID)
public Recordset openSchema(int schema)
public Recordset openSchema(int schema, Object[] restrictions)</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src7" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>public int getAttributes()
public void setAttributes(int attr)
public int getCommandTimeout()
public void setCommandTimeout(int timeout)
public String getConnectionString()
public void setConnectionString(String con)
public int getConnectionTimeout()
public void setConnectionTimeout(int timeout)
public int getCursorLocation()
public void setCursorLocation(int cursorLoc)
public String getDefaultDatabase()
public void setDefaultDatabase(String db)
public int getIsolationLevel()
public void setIsolationLevel(int level)
public int getMode()
public void setMode(int mode)
public String getProvider()
public void setProvider(String provider)
public int getState()
public String getVersion()
public AdoProperties getProperties()
public com.ms.wfc.data.Errors getErrors()</code>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src8" class="srcSentence">Events</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src9" class="srcSentence">For more information about ADO/WFC events, see <legacyLink xlink:href="eded7e8c-a25f-46a6-bc2b-32d89a54d1bc">ADO Event Instantiation by Language</legacyLink>.</caps:sentence>
              </para>
              <code>public void addOnBeginTransComplete(ConnectionEventHandler handler)
public void removeOnBeginTransComplete(ConnectionEventHandler handler)
public void addOnCommitTransComplete(ConnectionEventHandler handler)
public void removeOnCommitTransComplete(ConnectionEventHandler handler)
public void addOnConnectComplete(ConnectionEventHandler handler)
public void removeOnConnectComplete(ConnectionEventHandler handler)
public void addOnDisconnect(ConnectionEventHandler handler)
public void removeOnDisconnect(ConnectionEventHandler handler)
public void addOnExecuteComplete(ConnectionEventHandler handler)
public void removeOnExecuteComplete(ConnectionEventHandler handler)
public void addOnInfoMessage(ConnectionEventHandler handler)
public void removeOnInfoMessage(ConnectionEventHandler handler)
public void addOnRollbackTransComplete(ConnectionEventHandler handler)
public void removeOnRollbackTransComplete(ConnectionEventHandler handler)
public void addOnWillConnect(ConnectionEventHandler handler)
public void removeOnWillConnect(ConnectionEventHandler handler)
public void addOnWillExecute(ConnectionEventHandler handler)
public void removeOnWillExecute(ConnectionEventHandler handler)</code>
            </content>
          </section>
        </sections>
      </section>
      <relatedTopics>
        <link xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>