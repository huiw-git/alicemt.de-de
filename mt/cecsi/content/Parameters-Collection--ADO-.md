---
title: "Parameters Collection (ADO)"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 497cae10-3913-422a-9753-dcbb0a639b1b
caps.latest.revision: 19
caps.handback.revision: 19
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
# Parameters Collection (ADO)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="9d98746d0e84d9123d1337efd0d6a8b9" id="tgt1" class="tgtSentence">Contains all the <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> objects of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="ff028842e74c31689cf6f461dfc2b047" id="tgt2" class="tgtSentence">A <legacyBold>Command</legacyBold> object has a <legacyBold>Parameters</legacyBold> collection made up of <legacyBold>Parameter</legacyBold> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="475e850fb7b64e813623635f770a59ce" id="tgt3" class="tgtSentence">Using the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method on a <legacyBold>Command</legacyBold> object's <legacyBold>Parameters</legacyBold> collection retrieves provider parameter information for the stored procedure or parameterized query specified in the <legacyBold>Command</legacyBold> object.</caps:sentence>
            <caps:sentence sentenceid="5a66a74c210263390430715c84af9fb9" id="tgt4" class="tgtSentence"> Some providers do not support stored procedure calls or parameterized queries; calling the <legacyBold>Refresh</legacyBold> method on the <legacyBold>Parameters</legacyBold> collection when using such a provider will return an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="615d24d6066e45f4f0c6831c6d56275e" id="tgt5" class="tgtSentence">If you have not defined your own <legacyBold>Parameter</legacyBold> objects and you access the <legacyBold>Parameters</legacyBold> collection before calling the <legacyBold>Refresh</legacyBold> method, ADO will automatically call the method and populate the collection for you.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="58cc182a9d0449bed22024a51f02ea7f" id="tgt6" class="tgtSentence">You can minimize calls to the provider to improve performance if you know the properties of the parameters associated with the stored procedure or parameterized query you wish to call.</caps:sentence>
            <caps:sentence sentenceid="e7992c1ee692d2e7476f9fb15233fc92" id="tgt7" class="tgtSentence"> Use the <legacyLink xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter</legacyLink> method to create <legacyBold>Parameter</legacyBold> objects with the appropriate property settings and use the <legacyLink xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append</legacyLink> method to add them to the <legacyBold>Parameters</legacyBold> collection.</caps:sentence>
            <caps:sentence sentenceid="9bb341e4987a64222a1328d5860eead3" id="tgt8" class="tgtSentence"> This lets you set and return parameter values without having to call the provider for the parameter information.</caps:sentence>
            <caps:sentence sentenceid="410909bd9c905b7b17c4e614e7d43fe8" id="tgt9" class="tgtSentence"> If you are writing to a provider that does not supply parameter information, you must manually populate the <legacyBold>Parameters</legacyBold> collection using this method to be able to use parameters at all.</caps:sentence>
            <caps:sentence sentenceid="1c647f8e4fc283eb7c9a2b87427d8692" id="tgt10" class="tgtSentence"> Use the <legacyLink xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete</legacyLink> method to remove <legacyBold>Parameter</legacyBold> objects from the <legacyBold>Parameters</legacyBold> collection if necessary.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="fbaaa8b32e5a207f23478a7f31007cc9" id="tgt11" class="tgtSentence">The objects in the <legacyBold>Parameters</legacyBold> collection of a <legacyBold>Recordset</legacyBold> go out of scope (therefore becoming unavailable) when the <legacyBold>Recordset</legacyBold> is closed.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="2e1eef1471464c56e95cd740247e4d8e" id="tgt12" class="tgtSentence">When calling a stored procedure with <legacyBold>Command</legacyBold>, the return value/output parameter of a stored procedure is retrieved as follows:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="b8fc0b2315b97e2c23a5ebc4b219aff3" id="tgt13" class="tgtSentence">When calling a stored procedure that has no parameters, the <legacyBold>Refresh</legacyBold> method on the <legacyBold>Parameters</legacyBold> collection should be called before calling the <legacyBold>Execute</legacyBold> method on the <legacyBold>Command</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="83fb9cf55dde485ece5f1288c0e9ff88" id="tgt14" class="tgtSentence">When calling a stored procedure with parameters and explicitly appending a parameter to the <legacyBold>Parameters</legacyBold> collection with <legacyBold>Append</legacyBold>, the return value/output parameter should be appended to the <legacyBold>Parameters</legacyBold> collection.</caps:sentence>
                <caps:sentence sentenceid="8eb8e9e8636ba3c8d8c41b2ab483c9ce" id="tgt15" class="tgtSentence"> The return value must first be appended to the <legacyBold>Parameters</legacyBold> collection.</caps:sentence>
                <caps:sentence sentenceid="0a10114ba667089adf9a1d2ab364d0be" id="tgt16" class="tgtSentence"> Use <legacyBold>Append</legacyBold> to add the other parameters into the <legacyBold>Parameters</legacyBold> collection in the order of definition.</caps:sentence>
                <caps:sentence sentenceid="a9973c150b2ab28cdd298909b4d7d4e4" id="tgt17" class="tgtSentence"> For example, the stored procedure SPWithParam has two parameters.</caps:sentence>
                <caps:sentence sentenceid="292650d3eef12a2477ab3c09d6ceb5f5" id="tgt18" class="tgtSentence"> The first parameter, <parameterReference>InParam</parameterReference>, is an input parameter defined as adVarChar (20), and the second parameter, <parameterReference>OutParam</parameterReference>, is an output parameter defined as adVarChar (20).</caps:sentence>
                <caps:sentence sentenceid="8b0c7330f6152f4c48a419cba9b1f60d" id="tgt19" class="tgtSentence"> You can retrieve the return value/output parameter with the following code.</caps:sentence>
              </para>
              <code>' Open Connection Conn
set ccmd = CreateObject("ADODB.Command")
ccmd.Activeconnection= Conn

ccmd.CommandText="SPWithParam"
ccmd.commandType = 4 'adCmdStoredProc

ccmd.parameters.Append ccmd.CreateParameter(, adInteger, adParamReturnValue, , NULL)   ' return value
ccmd.parameters.Append ccmd.CreateParameter("InParam", adVarChar, adParamInput, 20, "hello world")   ' input parameter
ccmd.parameters.Append ccmd.CreateParameter("OutParam", adVarChar, adParamOuput, 20, NULL)   ' output parameter

ccmd.execute()

' Access ccmd.parameters(0) as return value of this stored procedure
' Access ccmd.parameters("OutParam") as the output parameter of this stored procedure.
</code>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="bb493b47b6868750ec4ed928ec81aafa" id="tgt20" class="tgtSentence">When calling a stored procedure with parameters and configuring the parameters by calling the <legacyBold>Item</legacyBold> method on the <legacyBold>Parameters</legacyBold> collection, the return value/output parameter of the stored procedure can be retrieved from the <legacyBold>Parameters</legacyBold> collection.</caps:sentence>
                <caps:sentence sentenceid="a9973c150b2ab28cdd298909b4d7d4e4" id="tgt21" class="tgtSentence"> For example, the stored procedure SPWithParam has two parameters.</caps:sentence>
                <caps:sentence sentenceid="292650d3eef12a2477ab3c09d6ceb5f5" id="tgt22" class="tgtSentence"> The first parameter, <parameterReference>InParam</parameterReference>, is an input parameter defined as adVarChar (20), and the second parameter, <parameterReference>OutParam</parameterReference>, is an output parameter defined as adVarChar (20).</caps:sentence>
                <caps:sentence sentenceid="8b0c7330f6152f4c48a419cba9b1f60d" id="tgt23" class="tgtSentence"> You can retrieve the return value/output parameter with the following code.</caps:sentence>
              </para>
              <code>' Open Connection Conn
set ccmd = CreateObject("ADODB.Command")
ccmd.Activeconnection= Conn

ccmd.CommandText="SPWithParam"
ccmd.commandType = 4 'adCmdStoredProc

ccmd.parameters.Item("InParam").value = "hello world" ' input parameter
ccmd.execute()

' Access ccmd.parameters(0) as return value of stored procedure
' Access ccmd.parameters(2) or ccmd.parameters("OutParam") as the output parameter.</code>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="509ab2ed06270bae5c4ea9aea0b3a564" id="tgt24" class="tgtSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="63b3f9a3-1c36-4d06-a6b0-49b5eb5adf06">
                  <caps:sentence sentenceid="48fd4c47dfed84a12d63c2f4767968f8" id="tgt25" class="tgtSentence">Parameters Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append Method</link>
        <link xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter Method</link>
        <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Contains all the <legacyLink xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter</legacyLink> objects of a <legacyLink xlink:href="a02c22fb-542d-465e-a629-30fd59dcbebf">Command</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">A <legacyBold>Command</legacyBold> object has a <legacyBold>Parameters</legacyBold> collection made up of <legacyBold>Parameter</legacyBold> objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src3" class="srcSentence">Using the <legacyLink xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh</legacyLink> method on a <legacyBold>Command</legacyBold> object's <legacyBold>Parameters</legacyBold> collection retrieves provider parameter information for the stored procedure or parameterized query specified in the <legacyBold>Command</legacyBold> object.</caps:sentence>
            <caps:sentence id="src4" class="srcSentence"> Some providers do not support stored procedure calls or parameterized queries; calling the <legacyBold>Refresh</legacyBold> method on the <legacyBold>Parameters</legacyBold> collection when using such a provider will return an error.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src5" class="srcSentence">If you have not defined your own <legacyBold>Parameter</legacyBold> objects and you access the <legacyBold>Parameters</legacyBold> collection before calling the <legacyBold>Refresh</legacyBold> method, ADO will automatically call the method and populate the collection for you.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src6" class="srcSentence">You can minimize calls to the provider to improve performance if you know the properties of the parameters associated with the stored procedure or parameterized query you wish to call.</caps:sentence>
            <caps:sentence id="src7" class="srcSentence"> Use the <legacyLink xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter</legacyLink> method to create <legacyBold>Parameter</legacyBold> objects with the appropriate property settings and use the <legacyLink xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append</legacyLink> method to add them to the <legacyBold>Parameters</legacyBold> collection.</caps:sentence>
            <caps:sentence id="src8" class="srcSentence"> This lets you set and return parameter values without having to call the provider for the parameter information.</caps:sentence>
            <caps:sentence id="src9" class="srcSentence"> If you are writing to a provider that does not supply parameter information, you must manually populate the <legacyBold>Parameters</legacyBold> collection using this method to be able to use parameters at all.</caps:sentence>
            <caps:sentence id="src10" class="srcSentence"> Use the <legacyLink xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete</legacyLink> method to remove <legacyBold>Parameter</legacyBold> objects from the <legacyBold>Parameters</legacyBold> collection if necessary.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src11" class="srcSentence">The objects in the <legacyBold>Parameters</legacyBold> collection of a <legacyBold>Recordset</legacyBold> go out of scope (therefore becoming unavailable) when the <legacyBold>Recordset</legacyBold> is closed.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src12" class="srcSentence">When calling a stored procedure with <legacyBold>Command</legacyBold>, the return value/output parameter of a stored procedure is retrieved as follows:</caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src13" class="srcSentence">When calling a stored procedure that has no parameters, the <legacyBold>Refresh</legacyBold> method on the <legacyBold>Parameters</legacyBold> collection should be called before calling the <legacyBold>Execute</legacyBold> method on the <legacyBold>Command</legacyBold> object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src14" class="srcSentence">When calling a stored procedure with parameters and explicitly appending a parameter to the <legacyBold>Parameters</legacyBold> collection with <legacyBold>Append</legacyBold>, the return value/output parameter should be appended to the <legacyBold>Parameters</legacyBold> collection.</caps:sentence>
                <caps:sentence id="src15" class="srcSentence"> The return value must first be appended to the <legacyBold>Parameters</legacyBold> collection.</caps:sentence>
                <caps:sentence id="src16" class="srcSentence"> Use <legacyBold>Append</legacyBold> to add the other parameters into the <legacyBold>Parameters</legacyBold> collection in the order of definition.</caps:sentence>
                <caps:sentence id="src17" class="srcSentence"> For example, the stored procedure SPWithParam has two parameters.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> The first parameter, <parameterReference>InParam</parameterReference>, is an input parameter defined as adVarChar (20), and the second parameter, <parameterReference>OutParam</parameterReference>, is an output parameter defined as adVarChar (20).</caps:sentence>
                <caps:sentence id="src19" class="srcSentence"> You can retrieve the return value/output parameter with the following code.</caps:sentence>
              </para>
              <code>' Open Connection Conn
set ccmd = CreateObject("ADODB.Command")
ccmd.Activeconnection= Conn

ccmd.CommandText="SPWithParam"
ccmd.commandType = 4 'adCmdStoredProc

ccmd.parameters.Append ccmd.CreateParameter(, adInteger, adParamReturnValue, , NULL)   ' return value
ccmd.parameters.Append ccmd.CreateParameter("InParam", adVarChar, adParamInput, 20, "hello world")   ' input parameter
ccmd.parameters.Append ccmd.CreateParameter("OutParam", adVarChar, adParamOuput, 20, NULL)   ' output parameter

ccmd.execute()

' Access ccmd.parameters(0) as return value of this stored procedure
' Access ccmd.parameters("OutParam") as the output parameter of this stored procedure.
</code>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src20" class="srcSentence">When calling a stored procedure with parameters and configuring the parameters by calling the <legacyBold>Item</legacyBold> method on the <legacyBold>Parameters</legacyBold> collection, the return value/output parameter of the stored procedure can be retrieved from the <legacyBold>Parameters</legacyBold> collection.</caps:sentence>
                <caps:sentence id="src21" class="srcSentence"> For example, the stored procedure SPWithParam has two parameters.</caps:sentence>
                <caps:sentence id="src22" class="srcSentence"> The first parameter, <parameterReference>InParam</parameterReference>, is an input parameter defined as adVarChar (20), and the second parameter, <parameterReference>OutParam</parameterReference>, is an output parameter defined as adVarChar (20).</caps:sentence>
                <caps:sentence id="src23" class="srcSentence"> You can retrieve the return value/output parameter with the following code.</caps:sentence>
              </para>
              <code>' Open Connection Conn
set ccmd = CreateObject("ADODB.Command")
ccmd.Activeconnection= Conn

ccmd.CommandText="SPWithParam"
ccmd.commandType = 4 'adCmdStoredProc

ccmd.parameters.Item("InParam").value = "hello world" ' input parameter
ccmd.execute()

' Access ccmd.parameters(0) as return value of stored procedure
' Access ccmd.parameters(2) or ccmd.parameters("OutParam") as the output parameter.</code>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src24" class="srcSentence">This section contains the following topic.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <legacyLink xlink:href="63b3f9a3-1c36-4d06-a6b0-49b5eb5adf06">
                  <caps:sentence id="src25" class="srcSentence">Parameters Collection Properties, Methods, and Events</caps:sentence>
                </legacyLink>
              </para>
            </listItem>
          </list>
        </content>
      </languageReferenceRemarks>
      <relatedTopics>
        <link xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append Method</link>
        <link xlink:href="9666fdcc-0544-4ed7-a97b-c415f2a56d7e">CreateParameter Method</link>
        <link xlink:href="e010e794-7f0f-4026-8b5b-37328e437d63">Parameter Object</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>