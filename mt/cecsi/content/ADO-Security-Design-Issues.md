---
title: "ADO Security Design Issues"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 86b83a38-efdf-4831-a6d5-7e470d517d1c
caps.latest.revision: 17
caps.handback.revision: 17
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
# ADO Security Design Issues
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="b2e6ec48221c26a9d532e63d7712aff4" id="tgt1" class="tgtSentence">The following sections describe security design features in ActiveX Data Objects (ADO) 2.8 and later.</caps:sentence>
          <caps:sentence sentenceid="2e18f42ee7f13532548c086dfb72c087" id="tgt2" class="tgtSentence"> These changes were made in ADO 2.8 to improve security.</caps:sentence>
          <caps:sentence sentenceid="1b31671b13fc16c81e51ad07c4258f0e" id="tgt3" class="tgtSentence"> ADO 6.0, which is included in Windows DAC 6.0 in Windows Vista, is functionally equivalent to ADO 2.8, which was included in MDAC 2.8 in Windows XP and Windows Server 2003.</caps:sentence>
          <caps:sentence sentenceid="3ac934bb0b47efa808698cc02d946fc2" id="tgt4" class="tgtSentence"> This topic provides information about how to best secure your applications in ADO 2.8 or later.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence sentenceid="74b9c0c20d198aef145b720e65363491" id="tgt5" class="tgtSentence">If you are updating your application from an earlier version of ADO, it is recommended that you test your updated application on a non-production computer before you deploy it to customers.</caps:sentence>
            <caps:sentence sentenceid="b92d01c19581dce601c16d0ddcd6c9ab" id="tgt6" class="tgtSentence"> This way, you can ensure you are aware of any compatibility issues before you deploy your updated application.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="c5957c8725e3ce294691baa9526a173e" id="tgt7" class="tgtSentence">Internet Explorer File Access Scenarios</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="722ebfad976d1b6ddb75febc71c0d8f1" id="tgt8" class="tgtSentence">The following features effect how ADO 2.8 and later works when it is used in scripted Web pages in Internet Explorer.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="ac67f359398bb85635b2a70024628d13" id="tgt9" class="tgtSentence">Revised and improved security warning message box now used to alert users</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="0590ab0a48cc8e24742929cfb8ccb590" id="tgt10" class="tgtSentence">For ADO 2.7 and earlier, the following warning message appears when a scripted Web page tries to run ADO code from an untrusted provider:</caps:sentence>
              </para>
              <code>This page accesses data on another domain. Do you want to allow this? To 
avoid this message in Internet Explorer, you can add a secure Web site to 
your Trusted Sites zone on the Security tab of the Internet Options dialog 
box.</code>
              <para>
                <caps:sentence sentenceid="ee04e3e6e123aa7686f9b232aa31401c" id="tgt11" class="tgtSentence">For ADO 2.8 and later, the preceding message no longer appears.</caps:sentence>
                <caps:sentence sentenceid="b5511a5d1962c07d1af207f4aaa67d41" id="tgt12" class="tgtSentence"> Instead, the following message appears in this context:</caps:sentence>
              </para>
              <code>This Website uses a data provider that may be unsafe. If you trust the 
Website, click OK, otherwise click Cancel.</code>
              <para>
                <caps:sentence sentenceid="ff73a524caeca3ae42793000c5e6280c" id="tgt13" class="tgtSentence">The preceding message allows the user to make informed decision, while knowing the consequences for either choice:  </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="39b3ccd9c876f0ca1b3f0ce1d8043b75" id="tgt14" class="tgtSentence">If user trusts the site, clicking OK will allow all disk-safe code (all ADO methods and properties with the exceptions of the disk-accessible APIs described later in this topic) to run and execute in the browser window.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="eadb5bf96bf8fdbf5076c809d2ab223c" id="tgt15" class="tgtSentence">If user does not trust the site, clicking Cancel blocks the ADO code for data access from running and executing in its entirety.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="fb9d845598772f509c836727d810deb7" id="tgt16" class="tgtSentence">Disk-accessible code limited now to trusted sites</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="a6397c8f6d4535ce6d2abd7e6992df02" id="tgt17" class="tgtSentence">Additional design changes were made in ADO 2.8 that specifically restrict the ability of a limited set of APIs, which might expose the potential to read from or write to files on the local computer.</caps:sentence>
                <caps:sentence sentenceid="d60e5d21988c56204b5ffd503ff871df" id="tgt18" class="tgtSentence"> Here are the API methods that have been further restricted for safety when running Internet Explorer:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="99a239d9ce1f02bfb7edd9ba1709258c" id="tgt19" class="tgtSentence">For the ADO <legacyBold>Stream</legacyBold> object, if the <legacyLink xlink:href="b18d8d38-7354-4a94-b637-6ac035faa433">LoadFromFile</legacyLink> or <legacyLink xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">SaveToFile</legacyLink> methods are used.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="8ca89938e5187f65dc39bffc38c8d273" id="tgt20" class="tgtSentence">For the ADO <legacyBold>Recordset</legacyBold> object, if either the <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> method or the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method, such as when either the <legacyBold>adCmdFile</legacyBold> option is set or the <legacyLink xlink:href="e75ef0dc-2016-4fcc-8918-23311c0d4e02">Microsoft OLE DB Persistence Provider (MSPersist)</legacyLink> is used.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence sentenceid="7cbff8db9a5c2302dc5287dac363e78e" id="tgt21" class="tgtSentence">For these limited sets of potentially disk-accessible functions, the following behavior occurs for ADO 2.8 and later, if any code that uses these methods is run in Internet Explorer:  </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence sentenceid="be311877459101a6d79cf209178db6cd" id="tgt22" class="tgtSentence">If the site that provided the code was added previously to the Trusted Sites zone list, the code executes in the browser and access is granted to local files.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence sentenceid="b56647671ae20a8e2d5b5cb8a5137b29" id="tgt23" class="tgtSentence">If the site does not appear in the Trusted Sites zone list, the code is blocked and access to local files is denied.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence sentenceid="bc64ca8ab5fb7ed696a1e61d3cbc4a01" id="tgt24" class="tgtSentence">In ADO 2.8 and later, the user is not alerted or advised to add sites to the Trusted Sites zone list.</caps:sentence>
                      <caps:sentence sentenceid="a6ce5f0e76df53c7d2d0eefd8db3d9a0" id="tgt25" class="tgtSentence"> Therefore the management of the Trusted Sites list is the responsibility of those who are deploying or supporting Web site–based applications that require access to the local file system.</caps:sentence>
                    </para>
                  </alert>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="91bbcf40c0e67ffd2a10145a0782fe1d" id="tgt26" class="tgtSentence">Access blocked to the ActiveCommand property on Recordset objects</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="065f0769b064908065526938e8b6c1ef" id="tgt27" class="tgtSentence">When running in Internet Explorer, ADO 2.8 now blocks access to the <legacyLink xlink:href="fb4088d5-5968-42d6-aeaa-3955046bb4da">ActiveCommand</legacyLink> property for an active <legacyBold>Recordset</legacyBold> object and returns an error.</caps:sentence>
                <caps:sentence sentenceid="0d530f364a59f82d434be2acdcbac44b" id="tgt28" class="tgtSentence"> The error occurs regardless of whether the page comes from a Web site registered in the Trusted Sites list.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="8f3419ae4593034783232a98872444c1" id="tgt29" class="tgtSentence">Changes in handling for OLE DB providers and integrated security</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence sentenceid="3ff11656e46d1b2dec841fd41cf8de62" id="tgt30" class="tgtSentence">While reviewing ADO 2.7 and earlier versions for potential security issues and concerns, the following scenario was discovered:</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="b4298f8dc8ff015593ad37acb55b33e9" id="tgt31" class="tgtSentence">In some instances, OLE DB providers who support the Integrated Security <externalLink><linkText>DBPROP_AUTH_INTEGRATED</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms712973.aspx</linkUri></externalLink> property could potentially permit scripted Web pages to reuse the ADO Connection object to connect unintentionally to other servers using the current login credentials of the users.</caps:sentence>
                <caps:sentence sentenceid="ac851361162ae425a3c6a48591b30b13" id="tgt32" class="tgtSentence"> To prevent this, ADO 2.8 and later handle OLE DB providers depending on how they have chosen to provide, or not provide, for integrated security.</caps:sentence>
              </para>
              <para>
                <caps:sentence sentenceid="db4ab9ba193aa04cb8f4005eed221b3e" id="tgt33" class="tgtSentence">For Web pages that are loaded from sites listed in the Trusted Sites zone list, the following table provides a breakdown of how ADO 2.8 and later manages ADO connections in each case.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="73b5f8ce6fcac8bf93105271a292b9cc" id="tgt34" class="tgtSentence">IE settings for user authentication, logon</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="0b207236b5a653006513f5aa2f77e0d1" id="tgt35" class="tgtSentence">Provider supports "Integrated Security" and UID and PWD are specified (SQLOLEDB)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e4c558339df824f5c582def8c3b4fb9b" id="tgt36" class="tgtSentence">Provider does not support "Integrated Security" (JOLT, MSDASQL, MSPersist)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="1631d0ba0852ea150d033dc5677c4ad7" id="tgt37" class="tgtSentence">Provider supports "Integrated Security" and it is set to SSPI (no UID/PWD are specified)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="8c9527da250bdc1b2eda2d2bdf65f7a7" id="tgt38" class="tgtSentence">Automatic logon with current username and password</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="16d555a463718180f53f265242d8d1f5" id="tgt39" class="tgtSentence">Allow connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="16d555a463718180f53f265242d8d1f5" id="tgt40" class="tgtSentence">Allow connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="16d555a463718180f53f265242d8d1f5" id="tgt41" class="tgtSentence">Allow connection</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="26e4734fd3ae26bd4e4bf09137adcdd4" id="tgt42" class="tgtSentence">Prompt for user name and password</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="16d555a463718180f53f265242d8d1f5" id="tgt43" class="tgtSentence">Allow connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="26d89b17dd3350d3aeb7497dd4c35c7b" id="tgt44" class="tgtSentence">Fail connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="26d89b17dd3350d3aeb7497dd4c35c7b" id="tgt45" class="tgtSentence">Fail connection</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="469f975ac17b395e7d55e5f0ecfef6e6" id="tgt46" class="tgtSentence">Automatic logon only in Intranet zone</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="16d555a463718180f53f265242d8d1f5" id="tgt47" class="tgtSentence">Allow connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ac500e1fff474863fdcfc512c14369e8" id="tgt48" class="tgtSentence">Prompt user with security warning</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="ac500e1fff474863fdcfc512c14369e8" id="tgt49" class="tgtSentence">Prompt user with security warning</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="52eb7a857afff614ad579ad4c4821050" id="tgt50" class="tgtSentence">Anonymous logon</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="16d555a463718180f53f265242d8d1f5" id="tgt51" class="tgtSentence">Allow connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="26d89b17dd3350d3aeb7497dd4c35c7b" id="tgt52" class="tgtSentence">Fail connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="26d89b17dd3350d3aeb7497dd4c35c7b" id="tgt53" class="tgtSentence">Fail connection</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence sentenceid="53c48b026fc53be3c11b646ada4b2253" id="tgt54" class="tgtSentence">In the case where a security warning now appears, the message box informs users:</caps:sentence>
              </para>
              <code>This Website is using your identity to access a data source. If you trust this Website, click OK, otherwise click Cancel.</code>
              <para>
                <caps:sentence sentenceid="bbce522387147ca9dd7ee831a625cd89" id="tgt55" class="tgtSentence">The preceding message allows the user to make a more informed decision and proceed accordingly.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence sentenceid="a1c15414de7240b4d1cc9d0c9e730972" id="tgt56" class="tgtSentence">For untrusted sites (that is, sites not listed in the Trusted Sites zone list), if the provider is also untrusted (as discussed earlier in this section), the user might see two security warnings in a row, a warning about the unsafe provider and a second warning about the attempt to use their identity.</caps:sentence>
                  <caps:sentence sentenceid="4506a0cf13a79ba1c26c1f9fb782cb30" id="tgt57" class="tgtSentence"> If the user clicks OK to the first warning, the Internet Explorer settings and response behavior code described in the preceding table are executed.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="91782789b2856e5806d83ccf4ef6f96c" id="tgt58" class="tgtSentence">Controlling whether password text is returned in ADO connection strings</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="9f56046bca1fcc4c9a61865b1faf6137" id="tgt59" class="tgtSentence">When you try get the value of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property on an ADO <legacyBold>Connection</legacyBold> object, the following events occur:  </caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence sentenceid="9a35b82d52e8fd383514c29d067a465d" id="tgt60" class="tgtSentence">If the connection is open, an initialization call is then made to the underlying OLE DB provider to get the connection string.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="5fc16d4c0cfe9750df4b1d89d38190b0" id="tgt61" class="tgtSentence">Depending on the setting in the OLE DB provider of the <externalLink><linkText>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms714905.aspx</linkUri></externalLink> property, passwords are included together with other connection string information that is returned.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="ec530d0d399fd8a70c50e1765ed16e50" id="tgt62" class="tgtSentence">For example, if the ADO Connection dynamic property <unmanagedCodeEntityReference>Persist Security Info</unmanagedCodeEntityReference> is set to <languageKeyword>True</languageKeyword>, password information is included in the connection string returned.</caps:sentence>
            <caps:sentence sentenceid="b1c9b314dbb0bc487b0566a159ff67f7" id="tgt63" class="tgtSentence"> Otherwise, if the underlying provider has set the property to <languageKeyword>False</languageKeyword> (for example with the SQLOLEDB provider), password information is omitted in the returned connection string.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="770b87d4839533a8551aae7d12b4e805" id="tgt64" class="tgtSentence">If you are using third-party (that is, non-Microsoft) OLE DB providers with your ADO application code, you might check how the <legacyBold>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</legacyBold> property is implemented to determine whether inclusion of password information with ADO connection strings is permitted.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="de9e26e567327987f647cdb2196d1c75" id="tgt65" class="tgtSentence">Checking for non-file devices when loading and saving recordsets or streams</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="6f38ecddecb1e515e204fbd595c8673f" id="tgt66" class="tgtSentence">For ADO 2.7 and earlier, file input/output operations such as <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> and <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> that were used to read and write file-based data could in some cases allow a URL or file name to be used that specified a non-disk based file type.</caps:sentence>
            <caps:sentence sentenceid="1d6722cf985eb6a919303b807ffaa5e1" id="tgt67" class="tgtSentence"> For example, LPT1, COM2, PRN.TXT, AUX could be used as an alias for input/output between printers and auxiliary devices on the system using certain</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="9379a8e77f900ac64b9366fdb2ef1927" id="tgt68" class="tgtSentence">For ADO 2.8 and later, this functionality has been updated.</caps:sentence>
            <caps:sentence sentenceid="6ddd745c8a2a7cf4f9b133c713a5f343" id="tgt69" class="tgtSentence"> For opening and saving <legacyBold>Recordset</legacyBold> and <legacyBold>Stream</legacyBold> objects, ADO now performs a file type check to ensure that the input or output device specified in a URL or file name is an actual file.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence sentenceid="3d05f16e9b1cad15b2b27744db7648c6" id="tgt70" class="tgtSentence">File type checking as described in this section only applies for Windows 2000 and later.</caps:sentence>
              <caps:sentence sentenceid="1fed105100d403dde85b0d7f1388981d" id="tgt71" class="tgtSentence"> It does not apply to situations where ADO 2.8 or later is running under earlier Windows releases, such as Windows 98.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerConceptualDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The following sections describe security design features in ActiveX Data Objects (ADO) 2.8 and later.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> These changes were made in ADO 2.8 to improve security.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> ADO 6.0, which is included in Windows DAC 6.0 in Windows Vista, is functionally equivalent to ADO 2.8, which was included in MDAC 2.8 in Windows XP and Windows Server 2003.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> This topic provides information about how to best secure your applications in ADO 2.8 or later.</caps:sentence>
        </para>
        <alert class="important">
          <para>
            <caps:sentence id="src5" class="srcSentence">If you are updating your application from an earlier version of ADO, it is recommended that you test your updated application on a non-production computer before you deploy it to customers.</caps:sentence>
            <caps:sentence id="src6" class="srcSentence"> This way, you can ensure you are aware of any compatibility issues before you deploy your updated application.</caps:sentence>
          </para>
        </alert>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src7" class="srcSentence">Internet Explorer File Access Scenarios</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src8" class="srcSentence">The following features effect how ADO 2.8 and later works when it is used in scripted Web pages in Internet Explorer.</caps:sentence>
          </para>
        </content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src9" class="srcSentence">Revised and improved security warning message box now used to alert users</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src10" class="srcSentence">For ADO 2.7 and earlier, the following warning message appears when a scripted Web page tries to run ADO code from an untrusted provider:</caps:sentence>
              </para>
              <code>This page accesses data on another domain. Do you want to allow this? To 
avoid this message in Internet Explorer, you can add a secure Web site to 
your Trusted Sites zone on the Security tab of the Internet Options dialog 
box.</code>
              <para>
                <caps:sentence id="src11" class="srcSentence">For ADO 2.8 and later, the preceding message no longer appears.</caps:sentence>
                <caps:sentence id="src12" class="srcSentence"> Instead, the following message appears in this context:</caps:sentence>
              </para>
              <code>This Website uses a data provider that may be unsafe. If you trust the 
Website, click OK, otherwise click Cancel.</code>
              <para>
                <caps:sentence id="src13" class="srcSentence">The preceding message allows the user to make informed decision, while knowing the consequences for either choice:  </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src14" class="srcSentence">If user trusts the site, clicking OK will allow all disk-safe code (all ADO methods and properties with the exceptions of the disk-accessible APIs described later in this topic) to run and execute in the browser window.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src15" class="srcSentence">If user does not trust the site, clicking Cancel blocks the ADO code for data access from running and executing in its entirety.</caps:sentence>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src16" class="srcSentence">Disk-accessible code limited now to trusted sites</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src17" class="srcSentence">Additional design changes were made in ADO 2.8 that specifically restrict the ability of a limited set of APIs, which might expose the potential to read from or write to files on the local computer.</caps:sentence>
                <caps:sentence id="src18" class="srcSentence"> Here are the API methods that have been further restricted for safety when running Internet Explorer:</caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">For the ADO <legacyBold>Stream</legacyBold> object, if the <legacyLink xlink:href="b18d8d38-7354-4a94-b637-6ac035faa433">LoadFromFile</legacyLink> or <legacyLink xlink:href="8a8594f2-422b-4d2e-94f8-7fe337445900">SaveToFile</legacyLink> methods are used.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src20" class="srcSentence">For the ADO <legacyBold>Recordset</legacyBold> object, if either the <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> method or the <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> method, such as when either the <legacyBold>adCmdFile</legacyBold> option is set or the <legacyLink xlink:href="e75ef0dc-2016-4fcc-8918-23311c0d4e02">Microsoft OLE DB Persistence Provider (MSPersist)</legacyLink> is used.</caps:sentence>
                  </para>
                </listItem>
              </list>
              <para>
                <caps:sentence id="src21" class="srcSentence">For these limited sets of potentially disk-accessible functions, the following behavior occurs for ADO 2.8 and later, if any code that uses these methods is run in Internet Explorer:  </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <caps:sentence id="src22" class="srcSentence">If the site that provided the code was added previously to the Trusted Sites zone list, the code executes in the browser and access is granted to local files.</caps:sentence>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <caps:sentence id="src23" class="srcSentence">If the site does not appear in the Trusted Sites zone list, the code is blocked and access to local files is denied.</caps:sentence>
                  </para>
                  <alert class="note">
                    <para>
                      <caps:sentence id="src24" class="srcSentence">In ADO 2.8 and later, the user is not alerted or advised to add sites to the Trusted Sites zone list.</caps:sentence>
                      <caps:sentence id="src25" class="srcSentence"> Therefore the management of the Trusted Sites list is the responsibility of those who are deploying or supporting Web site–based applications that require access to the local file system.</caps:sentence>
                    </para>
                  </alert>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src26" class="srcSentence">Access blocked to the ActiveCommand property on Recordset objects</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src27" class="srcSentence">When running in Internet Explorer, ADO 2.8 now blocks access to the <legacyLink xlink:href="fb4088d5-5968-42d6-aeaa-3955046bb4da">ActiveCommand</legacyLink> property for an active <legacyBold>Recordset</legacyBold> object and returns an error.</caps:sentence>
                <caps:sentence id="src28" class="srcSentence"> The error occurs regardless of whether the page comes from a Web site registered in the Trusted Sites list.</caps:sentence>
              </para>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src29" class="srcSentence">Changes in handling for OLE DB providers and integrated security</caps:sentence>
            </title>
            <content>
              <para>
                <caps:sentence id="src30" class="srcSentence">While reviewing ADO 2.7 and earlier versions for potential security issues and concerns, the following scenario was discovered:</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src31" class="srcSentence">In some instances, OLE DB providers who support the Integrated Security <externalLink><linkText>DBPROP_AUTH_INTEGRATED</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms712973.aspx</linkUri></externalLink> property could potentially permit scripted Web pages to reuse the ADO Connection object to connect unintentionally to other servers using the current login credentials of the users.</caps:sentence>
                <caps:sentence id="src32" class="srcSentence"> To prevent this, ADO 2.8 and later handle OLE DB providers depending on how they have chosen to provide, or not provide, for integrated security.</caps:sentence>
              </para>
              <para>
                <caps:sentence id="src33" class="srcSentence">For Web pages that are loaded from sites listed in the Trusted Sites zone list, the following table provides a breakdown of how ADO 2.8 and later manages ADO connections in each case.</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src34" class="srcSentence">IE settings for user authentication, logon</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src35" class="srcSentence">Provider supports "Integrated Security" and UID and PWD are specified (SQLOLEDB)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src36" class="srcSentence">Provider does not support "Integrated Security" (JOLT, MSDASQL, MSPersist)</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src37" class="srcSentence">Provider supports "Integrated Security" and it is set to SSPI (no UID/PWD are specified)</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src38" class="srcSentence">Automatic logon with current username and password</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src39" class="srcSentence">Allow connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src40" class="srcSentence">Allow connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src41" class="srcSentence">Allow connection</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src42" class="srcSentence">Prompt for user name and password</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src43" class="srcSentence">Allow connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src44" class="srcSentence">Fail connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src45" class="srcSentence">Fail connection</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src46" class="srcSentence">Automatic logon only in Intranet zone</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src47" class="srcSentence">Allow connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src48" class="srcSentence">Prompt user with security warning</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src49" class="srcSentence">Prompt user with security warning</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src50" class="srcSentence">Anonymous logon</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src51" class="srcSentence">Allow connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src52" class="srcSentence">Fail connection</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src53" class="srcSentence">Fail connection</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
              <para>
                <caps:sentence id="src54" class="srcSentence">In the case where a security warning now appears, the message box informs users:</caps:sentence>
              </para>
              <code>This Website is using your identity to access a data source. If you trust this Website, click OK, otherwise click Cancel.</code>
              <para>
                <caps:sentence id="src55" class="srcSentence">The preceding message allows the user to make a more informed decision and proceed accordingly.</caps:sentence>
              </para>
              <alert class="note">
                <para>
                  <caps:sentence id="src56" class="srcSentence">For untrusted sites (that is, sites not listed in the Trusted Sites zone list), if the provider is also untrusted (as discussed earlier in this section), the user might see two security warnings in a row, a warning about the unsafe provider and a second warning about the attempt to use their identity.</caps:sentence>
                  <caps:sentence id="src57" class="srcSentence"> If the user clicks OK to the first warning, the Internet Explorer settings and response behavior code described in the preceding table are executed.</caps:sentence>
                </para>
              </alert>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src58" class="srcSentence">Controlling whether password text is returned in ADO connection strings</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src59" class="srcSentence">When you try get the value of the <legacyLink xlink:href="3be75b75-4d36-4479-ab64-9a456869252a">ConnectionString</legacyLink> property on an ADO <legacyBold>Connection</legacyBold> object, the following events occur:  </caps:sentence>
          </para>
          <list class="ordered">
            <listItem>
              <para>
                <caps:sentence id="src60" class="srcSentence">If the connection is open, an initialization call is then made to the underlying OLE DB provider to get the connection string.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src61" class="srcSentence">Depending on the setting in the OLE DB provider of the <externalLink><linkText>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</linkText><linkUri>https://msdn.microsoft.com/library/windows/desktop/ms714905.aspx</linkUri></externalLink> property, passwords are included together with other connection string information that is returned.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src62" class="srcSentence">For example, if the ADO Connection dynamic property <unmanagedCodeEntityReference>Persist Security Info</unmanagedCodeEntityReference> is set to <languageKeyword>True</languageKeyword>, password information is included in the connection string returned.</caps:sentence>
            <caps:sentence id="src63" class="srcSentence"> Otherwise, if the underlying provider has set the property to <languageKeyword>False</languageKeyword> (for example with the SQLOLEDB provider), password information is omitted in the returned connection string.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src64" class="srcSentence">If you are using third-party (that is, non-Microsoft) OLE DB providers with your ADO application code, you might check how the <legacyBold>DBPROP_AUTH_PERSIST_SENSITIVE_AUTHINFO</legacyBold> property is implemented to determine whether inclusion of password information with ADO connection strings is permitted.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src65" class="srcSentence">Checking for non-file devices when loading and saving recordsets or streams</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src66" class="srcSentence">For ADO 2.7 and earlier, file input/output operations such as <legacyLink xlink:href="3236749c-4b71-4235-89e2-ccdfaaa9319d">Open</legacyLink> and <legacyLink xlink:href="ed3d9678-5c28-4e61-8bb3-7dfb66d99cf5">Save</legacyLink> that were used to read and write file-based data could in some cases allow a URL or file name to be used that specified a non-disk based file type.</caps:sentence>
            <caps:sentence id="src67" class="srcSentence"> For example, LPT1, COM2, PRN.TXT, AUX could be used as an alias for input/output between printers and auxiliary devices on the system using certain</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src68" class="srcSentence">For ADO 2.8 and later, this functionality has been updated.</caps:sentence>
            <caps:sentence id="src69" class="srcSentence"> For opening and saving <legacyBold>Recordset</legacyBold> and <legacyBold>Stream</legacyBold> objects, ADO now performs a file type check to ensure that the input or output device specified in a URL or file name is an actual file.</caps:sentence>
          </para>
          <alert class="note">
            <para>
              <caps:sentence id="src70" class="srcSentence">File type checking as described in this section only applies for Windows 2000 and later.</caps:sentence>
              <caps:sentence id="src71" class="srcSentence"> It does not apply to situations where ADO 2.8 or later is running under earlier Windows releases, such as Windows 98.</caps:sentence>
            </para>
          </alert>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerConceptualDocument>
  </caps:SxSSource>
</caps:SxS>