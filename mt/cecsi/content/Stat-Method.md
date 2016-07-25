---
title: "Stat Method"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
apitype: COM
ms.assetid: 99a2b2d4-e6b1-4205-b011-72d024ea7240
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
# Stat Method
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="57bd5d39fb6e5a45eda903923dcfeb9f" id="tgt1" class="tgtSentence">Retrieves information about a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
Long <parameterReference>stream</parameterReference>.Stat(StatStg, StatFlag)</legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence sentenceid="b944950a5da0625c32ca484aed2a8764" id="tgt2" class="tgtSentence">A <languageKeyword>Long</languageKeyword> value indicating the status of the operation.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="f2da1159c7b73a7ce56657e273250a9b" id="tgt3" class="tgtSentence"> <legacyItalic>StatStg</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="54f4808754725f9143e2230299642200" id="tgt4" class="tgtSentence">A STATSTG structure that will be filled in with information about the stream.</caps:sentence>
                <caps:sentence sentenceid="70b717aecae711c9610abc916804894c" id="tgt5" class="tgtSentence"> The implementation of the <unmanagedCodeEntityReference>Stat</unmanagedCodeEntityReference> method used by the ADO Stream object does not fill in all of the fields of the structure.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="6fe1be7ba78cb703d4762b0516dac1e4" id="tgt6" class="tgtSentence"> <legacyItalic>StatFlag</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="11c2c04fc2eb76c5eed4fba6308200c3" id="tgt7" class="tgtSentence">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation.</caps:sentence>
                <caps:sentence sentenceid="19396d16a94d5b677b37d25bb19cbe1c" id="tgt8" class="tgtSentence"> Values are taken from the STATFLAG enumeration.</caps:sentence>
                <caps:sentence sentenceid="0ad125ca693091c97164fe69f3bf0f3b" id="tgt9" class="tgtSentence"> The STATFLAG enumeration has two values</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="617ac08757d38a5a7ed91c224f0e90a0" id="tgt10" class="tgtSentence">Constant</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="2063c1608d6e0baf80249c42e2be5804" id="tgt11" class="tgtSentence">Value</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="e95f70b539bdf18fa32f39c9fc2526f8" id="tgt12" class="tgtSentence">STATFLAG_DEFAULT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="cfcd208495d565ef66e7dff9f98764da" id="tgt13" class="tgtSentence">0</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="9157aefb6763d272e427714554b13a95" id="tgt14" class="tgtSentence">STATFLAG_NONAME</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence sentenceid="c4ca4238a0b923820dcc509a6f75849b" id="tgt15" class="tgtSentence">1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence sentenceid="eaee3956c11ed7b0140f717c749370f2" id="tgt16" class="tgtSentence">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:  </caps:sentence>
          </para>
          <definitionTable>
            <definedTerm>
              <caps:sentence sentenceid="f01ed94606277d2ce1f73e1fc15f2221" id="tgt17" class="tgtSentence"> <legacyItalic>pwcsName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="593d2df8423505d16c77cb5a2b2cd115" id="tgt18" class="tgtSentence">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG_NONAME was not specified.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="b16d5cf8f5d000032a249dae1d54036a" id="tgt19" class="tgtSentence"> <legacyItalic>cbSize</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="ed1953387c7fae482809f0877fe6dffc" id="tgt20" class="tgtSentence">Specifies the size in bytes of the stream or byte array.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="f2f16d8fe933d2909f8f5f2d54120d1a" id="tgt21" class="tgtSentence"> <legacyItalic>mtime</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="5332c4240c79fd99c083c8b3cbd009a3" id="tgt22" class="tgtSentence">Indicates the last modification time for this storage, stream, or byte array.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="620ca78fda46021121622eb06adfc2db" id="tgt23" class="tgtSentence"> <legacyItalic>ctime</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="58254d0883328bc83a39d808e75ac9a3" id="tgt24" class="tgtSentence">Indicates the creation time for this storage, stream, or byte array.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence sentenceid="a7549593281a9380ca25d220be694597" id="tgt25" class="tgtSentence"> <legacyItalic>atime</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence sentenceid="e10ce1b7be1a88e6c51481110bf2a548" id="tgt26" class="tgtSentence">Indicates the last access time for this storage, stream or byte array.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <para>
            <caps:sentence sentenceid="0ae4f5dea889d7d930efa824294da7ac" id="tgt27" class="tgtSentence">If STATFLAG_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="4a1d4e6eccc1b837246dcf1175bbfcbd" id="tgt28" class="tgtSentence">If STATFLAG_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E_NOTIMPL.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence sentenceid="2f342d3be839cc5b67ae0de7d404b8e6" id="tgt29" class="tgtSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">Retrieves information about a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object.</caps:sentence>
        </para>
      </introduction>
      <syntaxSection>
        <legacySyntax>
Long <parameterReference>stream</parameterReference>.Stat(StatStg, StatFlag)</legacySyntax>
      </syntaxSection>
      <returnValue>
        <content>
          <para>
            <caps:sentence id="src2" class="srcSentence">A <languageKeyword>Long</languageKeyword> value indicating the status of the operation.</caps:sentence>
          </para>
        </content>
      </returnValue>
      <parameters>
        <content>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src3" class="srcSentence"> <legacyItalic>StatStg</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src4" class="srcSentence">A STATSTG structure that will be filled in with information about the stream.</caps:sentence>
                <caps:sentence id="src5" class="srcSentence"> The implementation of the <unmanagedCodeEntityReference>Stat</unmanagedCodeEntityReference> method used by the ADO Stream object does not fill in all of the fields of the structure.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src6" class="srcSentence"> <legacyItalic>StatFlag</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src7" class="srcSentence">Specifies that this method does not return some of the members in the STATSTG structure, thus saving a memory allocation operation.</caps:sentence>
                <caps:sentence id="src8" class="srcSentence"> Values are taken from the STATFLAG enumeration.</caps:sentence>
                <caps:sentence id="src9" class="srcSentence"> The STATFLAG enumeration has two values</caps:sentence>
              </para>
              <table>
                <thead>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src10" class="srcSentence">Constant</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src11" class="srcSentence">Value</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </thead>
                <tbody>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src12" class="srcSentence">STATFLAG_DEFAULT</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src13" class="srcSentence">0</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                  <tr>
                    <TD>
                      <para>
                        <caps:sentence id="src14" class="srcSentence">STATFLAG_NONAME</caps:sentence>
                      </para>
                    </TD>
                    <TD>
                      <para>
                        <caps:sentence id="src15" class="srcSentence">1</caps:sentence>
                      </para>
                    </TD>
                  </tr>
                </tbody>
              </table>
            </definition>
          </definitionTable>
        </content>
      </parameters>
      <languageReferenceRemarks>
        <content>
          <para>
            <caps:sentence id="src16" class="srcSentence">The version of the Stat method implemented for the ADO Stream object fills in the following fields of the STATSTG structure:  </caps:sentence>
          </para>
          <definitionTable>
            <definedTerm>
              <caps:sentence id="src17" class="srcSentence"> <legacyItalic>pwcsName</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src18" class="srcSentence">A string containing the name of the stream, if one is available and the StatFlag value STATFLAG_NONAME was not specified.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src19" class="srcSentence"> <legacyItalic>cbSize</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src20" class="srcSentence">Specifies the size in bytes of the stream or byte array.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src21" class="srcSentence"> <legacyItalic>mtime</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src22" class="srcSentence">Indicates the last modification time for this storage, stream, or byte array.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src23" class="srcSentence"> <legacyItalic>ctime</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src24" class="srcSentence">Indicates the creation time for this storage, stream, or byte array.</caps:sentence>
              </para>
            </definition>
            <definedTerm>
              <caps:sentence id="src25" class="srcSentence"> <legacyItalic>atime</legacyItalic> </caps:sentence>
            </definedTerm>
            <definition>
              <para>
                <caps:sentence id="src26" class="srcSentence">Indicates the last access time for this storage, stream or byte array.</caps:sentence>
              </para>
            </definition>
          </definitionTable>
          <para>
            <caps:sentence id="src27" class="srcSentence">If STATFLAG_NONAME is specified in the StatFlag parameter, the name of the stream is not returned.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src28" class="srcSentence">If STATFLAG_NONAME was not specified in the StatFlag parameter, and there is no name available for the current stream, this value will be E_NOTIMPL.</caps:sentence>
          </para>
        </content>
      </languageReferenceRemarks>
      <section>
        <title>
          <caps:sentence id="src29" class="srcSentence">Applies To</caps:sentence>
        </title>
        <content>
          <para>
            <link xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream Object</link>
          </para>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>