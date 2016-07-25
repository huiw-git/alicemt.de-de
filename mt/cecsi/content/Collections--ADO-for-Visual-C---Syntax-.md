---
title: "Collections (ADO for Visual C++ Syntax)"
ms.custom: na
ms.date: 05/16/2016
ms.devlang: 
  - C++
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 6a0109a0-f2d9-4f7c-8e1e-42763f9acaea
caps.latest.revision: 10
caps.handback.revision: 10
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
# Collections (ADO for Visual C++ Syntax)
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence sentenceid="166e64f6c3677d0c513901242a3e702d" id="tgt1" class="tgtSentence">Parameters</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt2" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>Append(IDispatch *Object);
Delete(VARIANT Index);
Refresh(void);</code>
              <para>
                <caps:sentence sentenceid="d1aee644e17abda9397214172b7615de" id="tgt3" class="tgtSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append Method (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete Method (ADO Parameters Collection)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt4" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>get_Count(long *c);
get_Item(VARIANT Index, _ADOParameter **ppvObject);</code>
              <para>
                <caps:sentence sentenceid="d1aee644e17abda9397214172b7615de" id="tgt5" class="tgtSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count Property (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item Property (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="d05b6ed7d2345020440df396d6da7f73" id="tgt6" class="tgtSentence">Fields</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt7" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>Append(BSTR bstrName, DataTypeEnum Type, long DefinedSize, FieldAttributeEnum Attrib);
Delete(VARIANT Index);
Refresh(void);</code>
              <para>
                <caps:sentence sentenceid="d1aee644e17abda9397214172b7615de" id="tgt8" class="tgtSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append Method (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete Method (ADO Parameters Collection)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt9" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>get_Count(long *c);
get_Item(VARIANT Index, ADOField **ppvObject);</code>
              <para>
                <caps:sentence sentenceid="d1aee644e17abda9397214172b7615de" id="tgt10" class="tgtSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count Property (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item Property (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="07213a0161f52846ab198be103b5ab43" id="tgt11" class="tgtSentence">Errors</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt12" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>Clear(void);
Refresh(void);</code>
              <para>
                <caps:sentence sentenceid="d1aee644e17abda9397214172b7615de" id="tgt13" class="tgtSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear Method (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt14" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>get_Count(long *c);
get_Item(VARIANT Index, ADOError **ppvObject);</code>
              <para>
                <caps:sentence sentenceid="d1aee644e17abda9397214172b7615de" id="tgt15" class="tgtSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count Property (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item Property (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt16" class="tgtSentence">Properties</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence sentenceid="a9ac5a6cc3cbe84f9c18323af2b9007f" id="tgt17" class="tgtSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>Refresh(void);</code>
              <para>
                <caps:sentence sentenceid="d1aee644e17abda9397214172b7615de" id="tgt18" class="tgtSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence sentenceid="74693d2fc58b46bd06410f278e39aa71" id="tgt19" class="tgtSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>get_Count(long *c);
get_Item(VARIANT Index, ADOProperty **ppvObject);</code>
              <para>
                <caps:sentence sentenceid="d1aee644e17abda9397214172b7615de" id="tgt20" class="tgtSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count Property (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item Property (ADO)</link>
                  </para>
                </listItem>
              </list>
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
      <introduction></introduction>
      <section>
        <title>
          <caps:sentence id="src1" class="srcSentence">Parameters</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src2" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>Append(IDispatch *Object);
Delete(VARIANT Index);
Refresh(void);</code>
              <para>
                <caps:sentence id="src3" class="srcSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append Method (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete Method (ADO Parameters Collection)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src4" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>get_Count(long *c);
get_Item(VARIANT Index, _ADOParameter **ppvObject);</code>
              <para>
                <caps:sentence id="src5" class="srcSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count Property (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item Property (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src6" class="srcSentence">Fields</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src7" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>Append(BSTR bstrName, DataTypeEnum Type, long DefinedSize, FieldAttributeEnum Attrib);
Delete(VARIANT Index);
Refresh(void);</code>
              <para>
                <caps:sentence id="src8" class="srcSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="f8a9bbed-ba9c-4698-945d-317ad22d2e92">Append Method (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="160c575e-df63-4ade-a2d3-5fd8f72e70cc">Delete Method (ADO Parameters Collection)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src9" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>get_Count(long *c);
get_Item(VARIANT Index, ADOField **ppvObject);</code>
              <para>
                <caps:sentence id="src10" class="srcSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count Property (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item Property (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src11" class="srcSentence">Errors</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src12" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>Clear(void);
Refresh(void);</code>
              <para>
                <caps:sentence id="src13" class="srcSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="0a61ba7a-20b8-426a-91a0-9040e7c5a98a">Clear Method (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src14" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>get_Count(long *c);
get_Item(VARIANT Index, ADOError **ppvObject);</code>
              <para>
                <caps:sentence id="src15" class="srcSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count Property (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item Property (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
        </sections>
      </section>
      <section>
        <title>
          <caps:sentence id="src16" class="srcSentence">Properties</caps:sentence>
        </title>
        <content></content>
        <sections>
          <section>
            <title>
              <caps:sentence id="src17" class="srcSentence">Methods</caps:sentence>
            </title>
            <content>
              <code>Refresh(void);</code>
              <para>
                <caps:sentence id="src18" class="srcSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="089b7ca7-684f-4259-8032-5bd1ecc54426">Refresh Method (ADO)</link>
                  </para>
                </listItem>
              </list>
            </content>
          </section>
          <section>
            <title>
              <caps:sentence id="src19" class="srcSentence">Properties</caps:sentence>
            </title>
            <content>
              <code>get_Count(long *c);
get_Item(VARIANT Index, ADOProperty **ppvObject);</code>
              <para>
                <caps:sentence id="src20" class="srcSentence">For more information, see </caps:sentence>
              </para>
              <list class="bullet">
                <listItem>
                  <para>
                    <link xlink:href="da9ccd1f-d402-41a2-940c-45556fc5340d">Count Property (ADO)</link>
                  </para>
                </listItem>
                <listItem>
                  <para>
                    <link xlink:href="e11484bb-c5c7-42d8-9bb8-21572125d727">Item Property (ADO)</link>
                  </para>
                </listItem>
              </list>
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