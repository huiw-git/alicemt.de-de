---
title: "Command Object Overview"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e84a14b1-3c2a-4f7d-a966-9e08a93948df
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
# Command Object Overview
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="954f8f251e5bcff0305b6c2066388cfb" id="tgt1" class="tgtSentence">With a <legacyBold>Command</legacyBold> object, you can do the following:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence sentenceid="9cff675ac7fbb741d88cce7377f034a0" id="tgt2" class="tgtSentence">Define the executable text of the command (for example, a SQL statement or a stored procedure) by using the <legacyBold>CommandText</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="0368f4cef71cc88888b3dc7b863cc954" id="tgt3" class="tgtSentence">Define parameterized queries or stored procedure arguments by using <legacyBold>Parameter</legacyBold> objects and the <legacyBold>Parameters</legacyBold> collection.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="9428a1b1e3880c5e9e1842d7ebb4f762" id="tgt4" class="tgtSentence">Execute a command and return a <legacyBold>Recordset</legacyBold> object, if appropriate, by using the <legacyBold>Execute</legacyBold> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="6c56da0887aa74d1b272b7ee47b5eb05" id="tgt5" class="tgtSentence">Specify the type of command by using the <legacyBold>CommandType</legacyBold> property prior to execution to optimize performance.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="650f1cb29c3e8bb44bea420ffe10ca26" id="tgt6" class="tgtSentence">Specify specific information about the command text by using the <legacyBold>Dialect</legacyBold> property of the <legacyBold>Command</legacyBold> object.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="d6795bc4fbbac358d7cbbfb6f44ac80f" id="tgt7" class="tgtSentence">Control whether the provider saves a prepared (or compiled) version of the command prior to execution by using the <legacyBold>Prepared</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="5ae912b656ba7c0c6ec54b93651839a2" id="tgt8" class="tgtSentence">Set the number of seconds that a provider will wait for a command to execute by using the <legacyBold>CommandTimeout</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="2f36715341ea126a3b3e00ce40529abb" id="tgt9" class="tgtSentence">Associate an open connection with a <legacyBold>Command</legacyBold> object by setting its <legacyBold>ActiveConnection</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="a5f11ca3a96b59b9614a01b28402fc81" id="tgt10" class="tgtSentence">Set the <legacyBold>Name</legacyBold> property to identify the <legacyBold>Command</legacyBold> object as a method on the associated <legacyBold>Connection</legacyBold> object.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="6f5a0e84c3df8e4226a83d8c55f1d908" id="tgt11" class="tgtSentence">Pass a <legacyBold>Command</legacyBold> object to the <legacyBold>Source</legacyBold> property of a <legacyBold>Recordset</legacyBold> in order to obtain data.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence sentenceid="144b9e6561e0d53077c156418277fa73" id="tgt12" class="tgtSentence">Pass a <legacyBold>Stream</legacyBold> object containing a command (for example, an XML command) to a provider that supports it.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">With a <legacyBold>Command</legacyBold> object, you can do the following:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <caps:sentence id="src2" class="srcSentence">Define the executable text of the command (for example, a SQL statement or a stored procedure) by using the <legacyBold>CommandText</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src3" class="srcSentence">Define parameterized queries or stored procedure arguments by using <legacyBold>Parameter</legacyBold> objects and the <legacyBold>Parameters</legacyBold> collection.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src4" class="srcSentence">Execute a command and return a <legacyBold>Recordset</legacyBold> object, if appropriate, by using the <legacyBold>Execute</legacyBold> method.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src5" class="srcSentence">Specify the type of command by using the <legacyBold>CommandType</legacyBold> property prior to execution to optimize performance.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src6" class="srcSentence">Specify specific information about the command text by using the <legacyBold>Dialect</legacyBold> property of the <legacyBold>Command</legacyBold> object.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src7" class="srcSentence">Control whether the provider saves a prepared (or compiled) version of the command prior to execution by using the <legacyBold>Prepared</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src8" class="srcSentence">Set the number of seconds that a provider will wait for a command to execute by using the <legacyBold>CommandTimeout</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src9" class="srcSentence">Associate an open connection with a <legacyBold>Command</legacyBold> object by setting its <legacyBold>ActiveConnection</legacyBold> property.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src10" class="srcSentence">Set the <legacyBold>Name</legacyBold> property to identify the <legacyBold>Command</legacyBold> object as a method on the associated <legacyBold>Connection</legacyBold> object.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src11" class="srcSentence">Pass a <legacyBold>Command</legacyBold> object to the <legacyBold>Source</legacyBold> property of a <legacyBold>Recordset</legacyBold> in order to obtain data.</caps:sentence>
            </para>
          </listItem>
          <listItem>
            <para>
              <caps:sentence id="src12" class="srcSentence">Pass a <legacyBold>Stream</legacyBold> object containing a command (for example, an XML command) to a provider that supports it.</caps:sentence>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>