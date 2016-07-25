---
title: "ADO Error Reference"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: f653393e-d4b0-4c34-ad5f-2bdf56bc1305
caps.latest.revision: 3
caps.handback.revision: 3
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
# ADO Error Reference
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="623108cc146f55a73f23ccf9419b20aa" id="tgt1" class="tgtSentence">The <legacyBold>ErrorValueEnum</legacyBold> constant describes the ADO error values.</caps:sentence>
          <caps:sentence sentenceid="db282cb3ffcdcbf7b92b5a77ab7060b5" id="tgt2" class="tgtSentence"> For a complete listing of these enumerated constants, including values, see <legacyLink xlink:href="0ce201c3-6657-4c87-ae81-0d7dc5b5a431">Appendix B: ADO Errors</legacyLink>.</caps:sentence>
          <caps:sentence sentenceid="578835d1d8cc9e0c06a4cbc25de3b66b" id="tgt3" class="tgtSentence"> This section will examine some of the more interesting errors and explain some specific situations that can raise them, or solutions to fix the problem.</caps:sentence>
          <caps:sentence sentenceid="21d62d965491f06234df0125dd1b4945" id="tgt4" class="tgtSentence"> Both the <legacyBold>ErrorValueEnum</legacyBold> constant and the short positive decimal number are listed.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b1bc248a7ff2b2e95569f56de68615df" id="tgt5" class="tgtSentence">Number</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="74f11781d1d8ff360de37cc91bddcc05" id="tgt6" class="tgtSentence">ErrorValueEnum constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c10bb66dfb0b3661d2e566e4a33c8758" id="tgt7" class="tgtSentence">Description/Possible causes</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="e93028bdc1aacdfb3687181f2031765d" id="tgt8" class="tgtSentence">3000</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="d75ad83df371afe1934c93d354025f03" id="tgt9" class="tgtSentence">adErrProviderFailed</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4939a0de4e9a42f3dbaaa1fa3072d7ea" id="tgt10" class="tgtSentence">Provider failed to perform the requested operation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="908c9a564a86426585b29f5335b619bc" id="tgt11" class="tgtSentence">3001</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="67aacfd2108aa7624a20f5496c65382a" id="tgt12" class="tgtSentence">adErrInvalidArgument</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fd0b9f7e4126329b27e78050fdf0d765" id="tgt13" class="tgtSentence">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</caps:sentence>
                    <caps:sentence sentenceid="b13f6907c3662c6df94c0664aa978618" id="tgt14" class="tgtSentence"> This error is often caused by a typographical error in an SQL SELECT statement.</caps:sentence>
                    <caps:sentence sentenceid="487d9b3a9fe079813aa5c8ed7346bce8" id="tgt15" class="tgtSentence"> For example, a misspelled field name or table name can generate this error.</caps:sentence>
                    <caps:sentence sentenceid="4346b27ad2aef80b35afd7c6e9c0c381" id="tgt16" class="tgtSentence"> This error can also occur when a field or table named in a SELECT statement does not exist in the data store.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="d806ca13ca3449af72a1ea5aedbed26a" id="tgt17" class="tgtSentence">3002</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="8591b15cbcfc773b83549e99f51b4a9a" id="tgt18" class="tgtSentence">adErrOpeningFile</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8003d8c7181ec5313cd93a4202a5a661" id="tgt19" class="tgtSentence">File could not be opened.</caps:sentence>
                    <caps:sentence sentenceid="0b6c57d649ecd943eee1bb237d8ac88e" id="tgt20" class="tgtSentence"> A misspelled file name was specified, or a file has been moved, renamed, or deleted.</caps:sentence>
                    <caps:sentence sentenceid="c904b7f82ee95a1d61fe1cf591162155" id="tgt21" class="tgtSentence"> Over a network, the drive might be temporarily unavailable or network traffic might be preventing a connection.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="a4380923dd651c195b1631af7c829187" id="tgt22" class="tgtSentence">3003</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="b77e023dc7b95bc5d65bd93ac55cbccb" id="tgt23" class="tgtSentence">adErrReadFile</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c452f28098c0f42979b0b0f49fe8810f" id="tgt24" class="tgtSentence">File could not be read.</caps:sentence>
                    <caps:sentence sentenceid="abfd133bc8d930167ca65852d0e957b7" id="tgt25" class="tgtSentence"> The name of the file is specified incorrectly, the file might have been moved or deleted, or the file might have become corrupted.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="20479c788fb27378c2c99eadcf207e7f" id="tgt26" class="tgtSentence">3004</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="075fd4376d167bcd55be28918240914c" id="tgt27" class="tgtSentence">adErrWriteFile</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="390bfc036ec1567e9291f9f08e80655a" id="tgt28" class="tgtSentence">Write to file failed.</caps:sentence>
                    <caps:sentence sentenceid="d2de937c016df65065c7f9a81d48329b" id="tgt29" class="tgtSentence"> You might have closed a file and then tried to write to it, or the file might be corrupted.</caps:sentence>
                    <caps:sentence sentenceid="bf9b5f603be9aa302feed189b12f423f" id="tgt30" class="tgtSentence"> If the file is located on a network drive, transient network conditions might prevent writing to a network drive.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9cb9ed4f35cf7c2f295cc2bc6f732a84" id="tgt31" class="tgtSentence">3021</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="761778e23c21996175184b4df488d782" id="tgt32" class="tgtSentence">adErrNoCurrentRecord</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7bebc2a5006c65b59816f853a819429" id="tgt33" class="tgtSentence">Either <legacyBold>BOF</legacyBold> or <legacyBold>EOF</legacyBold> is True, or the current record has been deleted.</caps:sentence>
                    <caps:sentence sentenceid="b5e885ea78e1d1e390b106db866684fa" id="tgt34" class="tgtSentence"> Requested operation requires a current record.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="273bb0ce733e6562ac4456c9b9075534" id="tgt35" class="tgtSentence">An attempt was made to update records by using <legacyBold>Find</legacyBold> or <legacyBold>Seek</legacyBold> to move the record pointer to the desired record.</caps:sentence>
                    <caps:sentence sentenceid="c0c7830363c913c83e525b3d659586d5" id="tgt36" class="tgtSentence"> If the record is not found, <legacyBold>EOF</legacyBold> will be True.</caps:sentence>
                    <caps:sentence sentenceid="5f5e86c857f6bf05977d0e980651b321" id="tgt37" class="tgtSentence"> This error can also occur after a failed <legacyBold>AddNew</legacyBold> or <legacyBold>Delete</legacyBold> because there is no current record when these methods fail.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="94b5bde6de888ddf9cde6748ad2523d1" id="tgt38" class="tgtSentence">3219</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3a6cacdb831a10aeddae346e0191e826" id="tgt39" class="tgtSentence">adErrIllegalOperation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3320f18e2a04f511f9173928e43de3db" id="tgt40" class="tgtSentence">Operation is not allowed in this context.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="5812f92450ccaf17275500841c70924a" id="tgt41" class="tgtSentence">3220</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="59fb23f96ec4e2ce1bbcd65e13f4e89d" id="tgt42" class="tgtSentence">adErrCantChangeProvider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="9b8e317b07fe1ce915cd4dfe21677838" id="tgt43" class="tgtSentence">Supplied provider is different from the one already in use.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="d309cd6396e744600c943fada20f686a" id="tgt44" class="tgtSentence">3246</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="e780a0713239569e15d01f090d08d64a" id="tgt45" class="tgtSentence">adErrInTransaction</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="970fb6b0213b972c630d819b3e78aa3a" id="tgt46" class="tgtSentence">
                      <legacyBold>Connection</legacyBold> object cannot be explicitly closed while in a transaction.</caps:sentence>
                    <caps:sentence sentenceid="612973126f51ca8ca40aa1979ce59fba" id="tgt47" class="tgtSentence"> A <legacyBold>Recordset</legacyBold> or <legacyBold>Connection</legacyBold> object that is currently participating in a transaction cannot be closed.</caps:sentence>
                    <caps:sentence sentenceid="7fe70ec7e9a72d16efc6fc6ed9f5b295" id="tgt48" class="tgtSentence"> Call either <legacyBold>RollbackTrans</legacyBold> or <legacyBold>CommitTrans</legacyBold> before closing the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="504c296f8eb5fd521e744da4e8371f28" id="tgt49" class="tgtSentence">3251</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="e064a9ef087b9e4efa3b9258322f2117" id="tgt50" class="tgtSentence">adErrFeatureNotAvailable</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="87711e521f7b7ce9de6314778200e040" id="tgt51" class="tgtSentence">The object or provider is not capable of performing the requested operation.</caps:sentence>
                    <caps:sentence sentenceid="1d66c3e6c7e18843b59c7faae5d7fb32" id="tgt52" class="tgtSentence"> Some operations depend on a particular provider version.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="f4334c131c781e2a6f0a5e34814c8147" id="tgt53" class="tgtSentence">3265</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="0eed1a17f5361e2dd9b60874a7111bc0" id="tgt54" class="tgtSentence">adErrItemNotFound</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="84551089549c8301c7fc5d0ecf859c33" id="tgt55" class="tgtSentence">Item cannot be found in the collection corresponding to the requested name or ordinal.</caps:sentence>
                    <caps:sentence sentenceid="9ae2b666a5b9d00e8833d8aa0c516636" id="tgt56" class="tgtSentence"> An incorrect field or table name has been specified.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="0e7e05fa1026b0c5459267608ae320b8" id="tgt57" class="tgtSentence">3367</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3535be0f4e22ac975606243a3af38149" id="tgt58" class="tgtSentence">adErrObjectInCollection</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e989275e701d984bc1b20e172866c551" id="tgt59" class="tgtSentence">Object is already in collection.</caps:sentence>
                    <caps:sentence sentenceid="66cbd54be53c06dd795e12c3257d3699" id="tgt60" class="tgtSentence"> Cannot append.</caps:sentence>
                    <caps:sentence sentenceid="e58a8c84f519b5bd78c82f8df9dd042c" id="tgt61" class="tgtSentence"> An object cannot be added to the same collection twice.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="643de7cf7ba769c7466ccbc4adfd7fac" id="tgt62" class="tgtSentence">3420</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="a414c3fbee1dc96edf5f882d19ffe7b6" id="tgt63" class="tgtSentence">adErrObjectNotSet</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="944f79da74bfc952823bfc6d2036a0b1" id="tgt64" class="tgtSentence">Object is no longer valid.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="e846fb8a4f365ca8e84393d4f34e1b07" id="tgt65" class="tgtSentence">3421</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="27cd03dcf580e86590aab5e95ff8f01c" id="tgt66" class="tgtSentence">adErrDataConversion</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="d4d979068847a806f2f078ee3c1472a6" id="tgt67" class="tgtSentence">Application uses a value of the wrong type for the current operation.</caps:sentence>
                    <caps:sentence sentenceid="0afd8964491b9540a66e82ab5199e192" id="tgt68" class="tgtSentence"> You might have supplied a string to an operation that expects a stream, for example.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9308b0d6e5898366a4a986bc33f3d3e7" id="tgt69" class="tgtSentence">3704</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="8b77f5ab31cb2c989e17113b46f75576" id="tgt70" class="tgtSentence">adErrObjectClosed</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="71c488de73428d38b5e711c77eb8d903" id="tgt71" class="tgtSentence">Operation is not allowed when the object is closed.</caps:sentence>
                    <caps:sentence sentenceid="ad5b2445ca15525a2a69757c54e286ba" id="tgt72" class="tgtSentence"> The <legacyBold>Connection</legacyBold> or <legacyBold>Recordset</legacyBold> has been closed.</caps:sentence>
                    <caps:sentence sentenceid="3d5abd650c610d17f3a2539fb285a76c" id="tgt73" class="tgtSentence"> For example, some other routine might have closed a global object.</caps:sentence>
                    <caps:sentence sentenceid="c7cc2139e9a35e65698ff6eb43219705" id="tgt74" class="tgtSentence"> You can prevent this error by checking the <legacyBold>State</legacyBold> property before you attempt an operation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="2cfa3753d6a524711acb5fce38eeca1a" id="tgt75" class="tgtSentence">3705</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="0ba10029905b6fb005b14319ecdce080" id="tgt76" class="tgtSentence">adErrObjectOpen</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a97ff13987f72756164a7cb71c045255" id="tgt77" class="tgtSentence">Operation is not allowed when the object is open.</caps:sentence>
                    <caps:sentence sentenceid="8ffb1f7d51ebe493a5af1f739ba94ee8" id="tgt78" class="tgtSentence"> An object that is open cannot be opened.</caps:sentence>
                    <caps:sentence sentenceid="6ce8c1282fdcd9cf5687df4c9b402b63" id="tgt79" class="tgtSentence"> Fields cannot be appended to an open <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="4764f37856fc727f70b666b8d0c4ab7a" id="tgt80" class="tgtSentence">3706</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3cd3e9e639bdb1e5d0ed4955636278ad" id="tgt81" class="tgtSentence">adErrProviderNotFound</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="494a7842b31f54c0d62e4053891b680c" id="tgt82" class="tgtSentence">Provider cannot be found.</caps:sentence>
                    <caps:sentence sentenceid="a4743f4705a8057b1b1434b2a763584b" id="tgt83" class="tgtSentence"> It may not be properly installed.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="4576d7493ae6e0b250c3ccf3b134e220" id="tgt84" class="tgtSentence">The name of the provider might be incorrectly specified, the specified provider might not be installed on the computer where your code is being executed, or the installation might have become corrupted.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="2ad9e5e943e43cad612a7996c12a8796" id="tgt85" class="tgtSentence">3707</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="d83e20925a0904022e3ea4dbc6c8ba81" id="tgt86" class="tgtSentence">adErrBoundToCommand</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3a34eb67174023454bcc33abc8a9dc6c" id="tgt87" class="tgtSentence">The <legacyBold>ActiveConnection</legacyBold> property of a <legacyBold>Recordset</legacyBold> object, which has a <legacyBold>Command</legacyBold> object as its source, cannot be changed.</caps:sentence>
                    <caps:sentence sentenceid="50a6a47b5dfd67577f6c66e1e1905fd8" id="tgt88" class="tgtSentence"> The application attempted to assign a new <legacyBold>Connection</legacyBold> object to a <legacyBold>Recordset</legacyBold> that has a <legacyBold>Command</legacyBold> object as its source.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="34ffeb359a192eb8174b6854643cc046" id="tgt89" class="tgtSentence">3708</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="b7a21b33027a5e8a12c5b27f5da69d12" id="tgt90" class="tgtSentence">adErrInvalidParamInfo</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="915bbc960c8f07d5fa0a846c644b74d8" id="tgt91" class="tgtSentence">
                      <legacyBold>Parameter</legacyBold> object is improperly defined.</caps:sentence>
                    <caps:sentence sentenceid="7b34ee764aee7f35d550093b3a2f5010" id="tgt92" class="tgtSentence"> Inconsistent or incomplete information was provided.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="56db57b4db0a6fcb7f9e0c0b504f6472" id="tgt93" class="tgtSentence">3709</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="1d76903b04f7989946131cfa03a7f8a0" id="tgt94" class="tgtSentence">adErrInvalidConnection</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="cbc3bcd76523c0477947e910aa071935" id="tgt95" class="tgtSentence">The connection cannot be used to perform this operation.</caps:sentence>
                    <caps:sentence sentenceid="caac1fb72e23081fe96abab2d88bd3b1" id="tgt96" class="tgtSentence"> It is either closed or invalid in this context.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="5505712229fb1eb500efadddc0353264" id="tgt97" class="tgtSentence">3710</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="60f2be375c7722d18b08dccc831995b4" id="tgt98" class="tgtSentence">adErrNotReentrant</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3854a51bae151a7d4825212cfa1dd1cf" id="tgt99" class="tgtSentence">Operation cannot be performed while processing event.</caps:sentence>
                    <caps:sentence sentenceid="dabb7b54bd90cbb3a52b5f6a04760598" id="tgt100" class="tgtSentence"> An operation cannot be performed within an event handler that causes the event to fire again.</caps:sentence>
                    <caps:sentence sentenceid="d3d62c0cbc20edca06ed5b0847f94b92" id="tgt101" class="tgtSentence"> For example, navigation methods should not be called from within a <legacyBold>WillMove</legacyBold> event handler.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="aba18772fc70c8cbf79a79f413ef102b" id="tgt102" class="tgtSentence">3711</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3a259aa4c2b72bee47f9770f5874381e" id="tgt103" class="tgtSentence">adErrStillExecuting</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f6293da9724c9638e87e1802438ae7b8" id="tgt104" class="tgtSentence">Operation cannot be performed while executing asynchronously.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="87ae6fb631f7c8a627e8e28785d9992d" id="tgt105" class="tgtSentence">3712</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="8d1ed7087c4426e9c4ffbf6f0513b24d" id="tgt106" class="tgtSentence">adErrOperationCancelled</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7e5191c87692a08cb12040fec2643746" id="tgt107" class="tgtSentence">Operation has been canceled by the user.</caps:sentence>
                    <caps:sentence sentenceid="47c2adaa8f46adf11f4585f72b1cba9c" id="tgt108" class="tgtSentence"> The application has called the <legacyBold>CancelUpdate</legacyBold> or <legacyBold>CancelBatch</legacyBold> method and the current operation has been canceled.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="7553e94d39fd4649ff75386a83ed3789" id="tgt109" class="tgtSentence">3713</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="f423bd7deeaee58d6bf0682890adc917" id="tgt110" class="tgtSentence">adErrStillConnecting</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="0a0a934682cdcc54f368c052dabba12d" id="tgt111" class="tgtSentence">Operation cannot be performed while connecting asynchronously.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="e36286b94d3c219f414e0427e5f73aa5" id="tgt112" class="tgtSentence">3714</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3909d7df3f096d55bd741ae9e2f6f0bc" id="tgt113" class="tgtSentence">adErrInvalidTransaction</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3ea05580b30159a801601c9178daec33" id="tgt114" class="tgtSentence">Coordinating transaction is invalid or has not started.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="d2d2c6e2445eef2bcff6bf0fdf69846c" id="tgt115" class="tgtSentence">3715</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="c9b1bf11dedb1a22470f4be2a85d3e19" id="tgt116" class="tgtSentence">adErrNotExecuting</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bced4afda1d5c7733e1587608cab638c" id="tgt117" class="tgtSentence">Operation cannot be performed while not executing.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="1b32a022c52c0c6255c2a32e580be34f" id="tgt118" class="tgtSentence">3716</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="f6ef47cd13e2d06b0268b8af04f409bf" id="tgt119" class="tgtSentence">adErrUnsafeOperation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49569dfbb84d0ea56abffd85f7e530e3" id="tgt120" class="tgtSentence">Safety settings on this computer prohibit accessing a data source on another domain.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="240c945bb72980130446fc2b40fbb8e0" id="tgt121" class="tgtSentence">3717</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="def2ed5be5ec2fd3554e3bb111b24748" id="tgt122" class="tgtSentence">adWrnSecurityDialog</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b88803d94826b8c1fa07949132d711e5" id="tgt123" class="tgtSentence">For internal use only.</caps:sentence>
                    <caps:sentence sentenceid="77ec12974f40f8487db7ae6ce87ef0b7" id="tgt124" class="tgtSentence"> Don't use.</caps:sentence>
                    <caps:sentence sentenceid="e69f45d9a3d07c2f8e7e5b8f0cbc6a6d" id="tgt125" class="tgtSentence"> (Entry was included for the sake of completeness.</caps:sentence>
                    <caps:sentence sentenceid="f8d72d92057f2330f77ccadb9b9150b3" id="tgt126" class="tgtSentence"> This error should not appear in your code.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9d068c869fd3e03fc606ec297fcd00be" id="tgt127" class="tgtSentence">3718</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="23ca00192239b4721d643d5b92a80f6d" id="tgt128" class="tgtSentence">adWrnSecurityDialogHeader</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b88803d94826b8c1fa07949132d711e5" id="tgt129" class="tgtSentence">For internal use only.</caps:sentence>
                    <caps:sentence sentenceid="77ec12974f40f8487db7ae6ce87ef0b7" id="tgt130" class="tgtSentence"> Don't use.</caps:sentence>
                    <caps:sentence sentenceid="93dc5ab364c39e03d13ff501fc8476b2" id="tgt131" class="tgtSentence"> (Entry included for the sake of completeness.</caps:sentence>
                    <caps:sentence sentenceid="f8d72d92057f2330f77ccadb9b9150b3" id="tgt132" class="tgtSentence"> This error should not appear in your code.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9e740b84bb48a64dde25061566299467" id="tgt133" class="tgtSentence">3719</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="54ff6582457be04968adf14e15e37160" id="tgt134" class="tgtSentence">adErrIntegrityViolation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="4f7bb02613c70cecb68d47cdd4dba315" id="tgt135" class="tgtSentence">Data value conflicts with the integrity constraints of the field.</caps:sentence>
                    <caps:sentence sentenceid="ff050bb86e0b2a35a2e63fddf9e640a7" id="tgt136" class="tgtSentence"> A new value for a <legacyBold>Field</legacyBold> would cause a duplicate key.</caps:sentence>
                    <caps:sentence sentenceid="9f9edebf67f9e2ad2e1a1a7759ab5450" id="tgt137" class="tgtSentence"> A value that forms one side of a relationship between two records might not be updatable.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="532b81fa223a1b1ec74139a5b8151d12" id="tgt138" class="tgtSentence">3720</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="1f70cde482ee9a1ded9036ccf3e9e757" id="tgt139" class="tgtSentence">adErrPermissionDenied</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8046c352cc2db8155331b20f69e9ba6d" id="tgt140" class="tgtSentence">Insufficient permission prevents writing to the field.</caps:sentence>
                    <caps:sentence sentenceid="74b1a3bde0e25f3a1c2959e555bace0b" id="tgt141" class="tgtSentence"> The user named in the connection string does not have the proper permissions to write to a <legacyBold>Field</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9e406957d45fcb6c6f38c2ada7bace91" id="tgt142" class="tgtSentence">3721</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="e2ffad914bb05ba5356837bfa23b40cb" id="tgt143" class="tgtSentence">adErrDataOverflow</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5ceee11ee6f18abd6020a0ddbb8ca861" id="tgt144" class="tgtSentence">Data value is too large to be represented by the field data type.</caps:sentence>
                    <caps:sentence sentenceid="6728eb99fe68a1406476d93520fce907" id="tgt145" class="tgtSentence"> A numeric value that is too large for the intended field was assigned.</caps:sentence>
                    <caps:sentence sentenceid="9d910643560e716b599e64c5a7721e1c" id="tgt146" class="tgtSentence"> For example, a long integer value was assigned to a short integer field.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="56e6a93212e4482d99c84a639d254b67" id="tgt147" class="tgtSentence">3722</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="c1cd27c6c0b89e1d9a79b6556b739add" id="tgt148" class="tgtSentence">adErrSchemaViolation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="24f2de2d2ffb5b936cf81654ea490530" id="tgt149" class="tgtSentence">Data value conflicts with the data type or constraints of the field.</caps:sentence>
                    <caps:sentence sentenceid="f14531bec3232335bbf60daab2bd6b67" id="tgt150" class="tgtSentence"> The data store has validation constraints that differ from the <legacyBold>Field</legacyBold> value.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="afa299a4d1d8c52e75dd8a24c3ce534f" id="tgt151" class="tgtSentence">3723</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="908aacdf057c6672b0c600bbe5852f5e" id="tgt152" class="tgtSentence">adErrSignMismatch</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bcd3581be7efca5337e4fa5e2d9de71f" id="tgt153" class="tgtSentence">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="4172f3101212a2009c74b547b6ddf935" id="tgt154" class="tgtSentence">3724</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="e785bb2fa6ff45378a737a276783487c" id="tgt155" class="tgtSentence">adErrCantConvertvalue</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f450dc03cb31f394b26c728d390e08e8" id="tgt156" class="tgtSentence">Data value cannot be converted for reasons other than sign mismatch or data overflow.</caps:sentence>
                    <caps:sentence sentenceid="00920bdd9dc794284dffa4cde31dd310" id="tgt157" class="tgtSentence"> For example, conversion would have truncated data.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="94ef7214c4a90790186e255304f8fd1f" id="tgt158" class="tgtSentence">3725</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="2273a44c1021e632121436dbb3089eb6" id="tgt159" class="tgtSentence">adErrCantCreate</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e743fa8deecea1165d1a1a5c4aeca2d6" id="tgt160" class="tgtSentence">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9fe77ac7060e716f2d42631d156825c0" id="tgt161" class="tgtSentence">3726</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="6eae27104830fd5aacb15b9af863ded5" id="tgt162" class="tgtSentence">adErrColumnNotOnThisRow</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fcb08b89ebac561cbdfe42ecf91be811" id="tgt163" class="tgtSentence">Record does not contain this field.</caps:sentence>
                    <caps:sentence sentenceid="5565d046f588cbe431f8d0c2de020113" id="tgt164" class="tgtSentence"> An incorrect field name was specified or a field not in the <legacyBold>Fields</legacyBold> collection of the current record was referenced.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="d3802b1dc0d80d8a3c8ccc6ccc068e7c" id="tgt165" class="tgtSentence">3727</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="fb2730e5ec1cb47c3a8a0f503ba6ab68" id="tgt166" class="tgtSentence">adErrURLDoesNotExist</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b4bdaa76c73e049d0ebd5bf933a7d255" id="tgt167" class="tgtSentence">Either the source URL or the parent of the destination URL does not exist.</caps:sentence>
                    <caps:sentence sentenceid="664354e1f5d1a867950890345dc2ed6c" id="tgt168" class="tgtSentence"> There is a typographical error in either the source or destination URL.</caps:sentence>
                    <caps:sentence sentenceid="5b11c00442a8f3e09c3182d225b23038" id="tgt169" class="tgtSentence"> You might have <codeInline>http://mysite/photo/myphoto.jpg</codeInline> when you should actually have <codeInline>http://mysite/photos/myphoto.jpg</codeInline> instead.</caps:sentence>
                    <caps:sentence sentenceid="ab3e4a471b544a9596faad39d51dbf55" id="tgt170" class="tgtSentence"> The typographical error in the parent URL (in this case, <legacyItalic>photo</legacyItalic> instead of <legacyItalic>photos</legacyItalic>) has caused the error.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="460b491b917d4185ed1f5be97229721a" id="tgt171" class="tgtSentence">3728</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="e832d77749ab99284a649432cbc86d27" id="tgt172" class="tgtSentence">adErrTreePermissionDenied</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="41b87c5dee1e655921d9908f672380e7" id="tgt173" class="tgtSentence">Permissions are insufficient to access tree or subtree.</caps:sentence>
                    <caps:sentence sentenceid="591c1ac3b20f180fd5bf39d3997e99f6" id="tgt174" class="tgtSentence"> The user named in the connection string does not have the appropriate permissions.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="cb16b8498f74ba6b6a6873518624168c" id="tgt175" class="tgtSentence">3729</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="f413461715943ab2c12697513fd413c7" id="tgt176" class="tgtSentence">adErrInvalidURL</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5cf210c84c9e237930bf489fd85cf7c2" id="tgt177" class="tgtSentence">URL contains invalid characters.</caps:sentence>
                    <caps:sentence sentenceid="5d9bb7c619f141251a03ccd86b7565b4" id="tgt178" class="tgtSentence"> Make sure the URL is typed correctly.</caps:sentence>
                    <caps:sentence sentenceid="4a092181f43e8a884d16cc3a6c174629" id="tgt179" class="tgtSentence"> The URL follows the scheme registered to the current provider (for example, Internet Publishing Provider is registered for http).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="d8c24ca8f23c562a5600876ca2a550ce" id="tgt180" class="tgtSentence">3730</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="323b38eb44cdee770bc206ce41cd02d1" id="tgt181" class="tgtSentence">adErrResourceLocked</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b0d9568cd4d358547ae2fc184a2a5620" id="tgt182" class="tgtSentence">Object represented by the specified URL is locked by one or more other processes.</caps:sentence>
                    <caps:sentence sentenceid="c64a0aecf35fc5df7abcd1bc46393673" id="tgt183" class="tgtSentence"> Wait until the process has finished and attempt the operation again.</caps:sentence>
                    <caps:sentence sentenceid="de08fe45f87b8a8fc98b0c6724041afc" id="tgt184" class="tgtSentence"> The object you are trying to access has been locked by another user or by another process in your application.</caps:sentence>
                    <caps:sentence sentenceid="58c3de85735cfcfbc1ccb5402fde8601" id="tgt185" class="tgtSentence"> This is most likely to arise in a multi-user environment.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="7ec3b3cf674f4f1d23e9d30c89426cce" id="tgt186" class="tgtSentence">3731</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="74b55526ce103018ec8c14a40d78a18a" id="tgt187" class="tgtSentence">adErrResourceExists</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="044bc9d3d6b3a998156449705513b8fd" id="tgt188" class="tgtSentence">Copy operation cannot be performed.</caps:sentence>
                    <caps:sentence sentenceid="c223ff5a8dd5a041e026cec1a4507c70" id="tgt189" class="tgtSentence"> Object named by destination URL already exists.</caps:sentence>
                    <caps:sentence sentenceid="e8088e2075d6d4b8ddb332493ae57e2e" id="tgt190" class="tgtSentence"> Specify <legacyBold>adCopyOverwrite</legacyBold> to replace the object.</caps:sentence>
                    <caps:sentence sentenceid="cb9af070914ec2937fab34e69cf86ed0" id="tgt191" class="tgtSentence"> If you do not specify <legacyBold>adCopyOverwrite</legacyBold> when copying the files in a directory, the copy fails when you try to copy an item that already exists in the destination location.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="ee23e7ad9b473ad072d57aaa9b2a5222" id="tgt192" class="tgtSentence">3732</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="eabe9c9f32b3468f142ed67388a7a8ca" id="tgt193" class="tgtSentence">adErrCannotComplete</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1a33a9fc4898cb9473271703acb5dbeb" id="tgt194" class="tgtSentence">The server cannot complete the operation.</caps:sentence>
                    <caps:sentence sentenceid="f9e47f8cfa8a8f323c08112abb803fbe" id="tgt195" class="tgtSentence"> This might be because the server is busy with other operations or it might be low on resources.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="64d52e08cc03e6090bc1ef30b73ccb85" id="tgt196" class="tgtSentence">3733</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="82f1f61c6d3dcab1a2cca858515f226f" id="tgt197" class="tgtSentence">adErrVolumeNotFound</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="12f9b1a7d575a973f5b5378c0cdae762" id="tgt198" class="tgtSentence">Provider cannot locate the storage device indicated by the URL.</caps:sentence>
                    <caps:sentence sentenceid="5d9bb7c619f141251a03ccd86b7565b4" id="tgt199" class="tgtSentence"> Make sure the URL is typed correctly.</caps:sentence>
                    <caps:sentence sentenceid="9bf7bbd38e87408404643520d5c476f9" id="tgt200" class="tgtSentence"> The URL of the storage device might be incorrect, but this error can occur for other reasons.</caps:sentence>
                    <caps:sentence sentenceid="57b6557141d9ce1a7f4ecbedcbe95855" id="tgt201" class="tgtSentence"> The device might be offline or a large volume of network traffic might prevent the connection from being made.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="9d752cb08ef466fc480fba981cfa44a1" id="tgt202" class="tgtSentence">3734</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="1e9628b77d34f2e1a545f9dc72aeb385" id="tgt203" class="tgtSentence">adErrOutOfSpace</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="90ea01da8010bd5d6b8f93b1a97cea52" id="tgt204" class="tgtSentence">Operation cannot be performed.</caps:sentence>
                    <caps:sentence sentenceid="4a9e098bb4c35472495cacb30dcc96b9" id="tgt205" class="tgtSentence"> Provider cannot obtain enough storage space.</caps:sentence>
                    <caps:sentence sentenceid="5f4c8b13e2d99aa350ff57f92d8d3937" id="tgt206" class="tgtSentence"> There might not be enough RAM or hard-drive space for temporary files on the server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="dc0c398086fee58f9d64e1e47aa4e586" id="tgt207" class="tgtSentence">3735</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="70f3101b0878148f8f2effa19cd05255" id="tgt208" class="tgtSentence">adErrResourceOutOfScope</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="79db6534060533bad96e00b28466eb88" id="tgt209" class="tgtSentence">Source or destination URL is outside the scope of the current record.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3e195b0793297114c668f772c6e2d9ba" id="tgt210" class="tgtSentence">3736</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="fe2cc8b8aa6b3a83fee7a94e2af5e657" id="tgt211" class="tgtSentence">adErrUnavailable</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a23d35186ac10e3a6db99247320b80d4" id="tgt212" class="tgtSentence">Operation failed to complete and the status is unavailable.</caps:sentence>
                    <caps:sentence sentenceid="3835735f5d7033f0221ef20d578c14bb" id="tgt213" class="tgtSentence"> The field may be unavailable or the operation was not attempted.</caps:sentence>
                    <caps:sentence sentenceid="d8a423beb131855c2d842fa8f172a964" id="tgt214" class="tgtSentence"> Another user might have changed or deleted the field you are trying to access.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="3db11d259a9db7fb8965bdf25ec850b9" id="tgt215" class="tgtSentence">3737</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="b5aea24e0e9016d884dae081c7188a52" id="tgt216" class="tgtSentence">adErrURLNamedRowDoesNotExist</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2ff7b013f2b727c293209db2f735c683" id="tgt217" class="tgtSentence">Record named by this URL does not exist.</caps:sentence>
                    <caps:sentence sentenceid="b2d2209237a70931ae18c6d58329c1db" id="tgt218" class="tgtSentence"> While attempting to open a file using a <legacyBold>Record</legacyBold> object, either the file name or the path to the file was misspelled.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="16738419b15b05e74e1ecb164430bfa8" id="tgt219" class="tgtSentence">3738</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="0ba06e633c62f187cdd93f4ced95810e" id="tgt220" class="tgtSentence">adErrDelResOutOfScope</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3a951d8e00c3aeab9f3de670e75d0aff" id="tgt221" class="tgtSentence">The URL of the object to be deleted is outside the scope of the current record.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="d8847be3f7cc1b14e9173908bebb2106" id="tgt222" class="tgtSentence">3747</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="999c389f1ff6329c8ad9c2185acaf17d" id="tgt223" class="tgtSentence">adErrCatalogNotSet</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="3418c0591c545897ff0bf6340e67ca32" id="tgt224" class="tgtSentence">Operation requires a valid <legacyBold>ParentCatalog</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="aaaccd2766ec67aecbe26459bb828d81" id="tgt225" class="tgtSentence">3748</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="49ad26c9488e2a8fe65df1983602c7fd" id="tgt226" class="tgtSentence">adErrCantChangeConnection</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b95be705e17420e2f1e6eeba8c23d6ad" id="tgt227" class="tgtSentence">Connection was denied.</caps:sentence>
                    <caps:sentence sentenceid="e15d163823a4517ca93ddd000276b9bf" id="tgt228" class="tgtSentence"> The new connection you requested has different characteristics than the one already in use.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="f9beb1e831faf6aaec2a5cecaf1af293" id="tgt229" class="tgtSentence">3749</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="85209059c923d3d59abb5663db2481d0" id="tgt230" class="tgtSentence">adErrFieldsUpdateFailed</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="712b01818b356ce05a6d49a66296c49a" id="tgt231" class="tgtSentence">Fields update failed.</caps:sentence>
                    <caps:sentence sentenceid="1f7e9d1353e41e6bc3c5002314c18f7d" id="tgt232" class="tgtSentence"> For further information, examine the <legacyBold>Status </legacyBold>property of individual field objects.</caps:sentence>
                    <caps:sentence sentenceid="427771f4ef9f1515c109310a2cdf420c" id="tgt233" class="tgtSentence"> This error can occur in two situations: when changing a <legacyBold>Field</legacyBold> object's value in the process of changing or adding a record to the database; and when changing the properties of the <legacyBold>Field</legacyBold> object itself.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence sentenceid="6cb42500ce27127e9e410023c78b203b" id="tgt234" class="tgtSentence">The <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> update failed due to a problem with one of the fields in the current record.</caps:sentence>
                    <caps:sentence sentenceid="4730406dc117099e1d8ff9b517b9ffb5" id="tgt235" class="tgtSentence"> Enumerate the <legacyBold>Fields</legacyBold> collection and check the <legacyBold>Status</legacyBold> property of each field to determine the cause of the problem.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="685ac8cadc1be5ac98da9556bc1c8d9e" id="tgt236" class="tgtSentence">3750</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="20bc93d939b4090eeb4212754699857c" id="tgt237" class="tgtSentence">adErrDenyNotSupported</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1f45ebab218f80b876c92859832841ef" id="tgt238" class="tgtSentence">Provider does not support sharing restrictions.</caps:sentence>
                    <caps:sentence sentenceid="a00ae68aa68202f67935e21545af9ba4" id="tgt239" class="tgtSentence"> An attempt was made to restrict file sharing and your provider does not support the concept.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="21ce689121e39821d07d04faab328370" id="tgt240" class="tgtSentence">3751</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence sentenceid="40dc224be9451444df6595ec761b46a0" id="tgt241" class="tgtSentence">adErrDenyTypeNotSupported</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ec2981c2639797308376573b3d4c9db0" id="tgt242" class="tgtSentence">Provider does not support the requested kind of sharing restriction.</caps:sentence>
                    <caps:sentence sentenceid="2abda1e6e62e9d83efe6f2017774a711" id="tgt243" class="tgtSentence"> An attempt was made to establish a particular type of file-sharing restriction that is not supported by your provider.</caps:sentence>
                    <caps:sentence sentenceid="2d5a3cfb49776cc83dc34c4c8422eaf6" id="tgt244" class="tgtSentence"> See the provider's documentation to determine what file-sharing restrictions are supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">The <legacyBold>ErrorValueEnum</legacyBold> constant describes the ADO error values.</caps:sentence>
          <caps:sentence id="src2" class="srcSentence"> For a complete listing of these enumerated constants, including values, see <legacyLink xlink:href="0ce201c3-6657-4c87-ae81-0d7dc5b5a431">Appendix B: ADO Errors</legacyLink>.</caps:sentence>
          <caps:sentence id="src3" class="srcSentence"> This section will examine some of the more interesting errors and explain some specific situations that can raise them, or solutions to fix the problem.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> Both the <legacyBold>ErrorValueEnum</legacyBold> constant and the short positive decimal number are listed.</caps:sentence>
        </para>
      </introduction>
      <section>
        <content>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src5" class="srcSentence">Number</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src6" class="srcSentence">ErrorValueEnum constant</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src7" class="srcSentence">Description/Possible causes</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src8" class="srcSentence">3000</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src9" class="srcSentence">adErrProviderFailed</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src10" class="srcSentence">Provider failed to perform the requested operation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src11" class="srcSentence">3001</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src12" class="srcSentence">adErrInvalidArgument</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src13" class="srcSentence">Arguments are of the wrong type, are out of acceptable range, or are in conflict with one another.</caps:sentence>
                    <caps:sentence id="src14" class="srcSentence"> This error is often caused by a typographical error in an SQL SELECT statement.</caps:sentence>
                    <caps:sentence id="src15" class="srcSentence"> For example, a misspelled field name or table name can generate this error.</caps:sentence>
                    <caps:sentence id="src16" class="srcSentence"> This error can also occur when a field or table named in a SELECT statement does not exist in the data store.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src17" class="srcSentence">3002</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src18" class="srcSentence">adErrOpeningFile</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src19" class="srcSentence">File could not be opened.</caps:sentence>
                    <caps:sentence id="src20" class="srcSentence"> A misspelled file name was specified, or a file has been moved, renamed, or deleted.</caps:sentence>
                    <caps:sentence id="src21" class="srcSentence"> Over a network, the drive might be temporarily unavailable or network traffic might be preventing a connection.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src22" class="srcSentence">3003</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src23" class="srcSentence">adErrReadFile</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src24" class="srcSentence">File could not be read.</caps:sentence>
                    <caps:sentence id="src25" class="srcSentence"> The name of the file is specified incorrectly, the file might have been moved or deleted, or the file might have become corrupted.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src26" class="srcSentence">3004</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src27" class="srcSentence">adErrWriteFile</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src28" class="srcSentence">Write to file failed.</caps:sentence>
                    <caps:sentence id="src29" class="srcSentence"> You might have closed a file and then tried to write to it, or the file might be corrupted.</caps:sentence>
                    <caps:sentence id="src30" class="srcSentence"> If the file is located on a network drive, transient network conditions might prevent writing to a network drive.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src31" class="srcSentence">3021</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src32" class="srcSentence">adErrNoCurrentRecord</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Either <legacyBold>BOF</legacyBold> or <legacyBold>EOF</legacyBold> is True, or the current record has been deleted.</caps:sentence>
                    <caps:sentence id="src34" class="srcSentence"> Requested operation requires a current record.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">An attempt was made to update records by using <legacyBold>Find</legacyBold> or <legacyBold>Seek</legacyBold> to move the record pointer to the desired record.</caps:sentence>
                    <caps:sentence id="src36" class="srcSentence"> If the record is not found, <legacyBold>EOF</legacyBold> will be True.</caps:sentence>
                    <caps:sentence id="src37" class="srcSentence"> This error can also occur after a failed <legacyBold>AddNew</legacyBold> or <legacyBold>Delete</legacyBold> because there is no current record when these methods fail.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src38" class="srcSentence">3219</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src39" class="srcSentence">adErrIllegalOperation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">Operation is not allowed in this context.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src41" class="srcSentence">3220</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src42" class="srcSentence">adErrCantChangeProvider</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src43" class="srcSentence">Supplied provider is different from the one already in use.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src44" class="srcSentence">3246</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src45" class="srcSentence">adErrInTransaction</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">
                      <legacyBold>Connection</legacyBold> object cannot be explicitly closed while in a transaction.</caps:sentence>
                    <caps:sentence id="src47" class="srcSentence"> A <legacyBold>Recordset</legacyBold> or <legacyBold>Connection</legacyBold> object that is currently participating in a transaction cannot be closed.</caps:sentence>
                    <caps:sentence id="src48" class="srcSentence"> Call either <legacyBold>RollbackTrans</legacyBold> or <legacyBold>CommitTrans</legacyBold> before closing the object.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src49" class="srcSentence">3251</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src50" class="srcSentence">adErrFeatureNotAvailable</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src51" class="srcSentence">The object or provider is not capable of performing the requested operation.</caps:sentence>
                    <caps:sentence id="src52" class="srcSentence"> Some operations depend on a particular provider version.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src53" class="srcSentence">3265</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src54" class="srcSentence">adErrItemNotFound</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src55" class="srcSentence">Item cannot be found in the collection corresponding to the requested name or ordinal.</caps:sentence>
                    <caps:sentence id="src56" class="srcSentence"> An incorrect field or table name has been specified.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src57" class="srcSentence">3367</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src58" class="srcSentence">adErrObjectInCollection</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">Object is already in collection.</caps:sentence>
                    <caps:sentence id="src60" class="srcSentence"> Cannot append.</caps:sentence>
                    <caps:sentence id="src61" class="srcSentence"> An object cannot be added to the same collection twice.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src62" class="srcSentence">3420</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src63" class="srcSentence">adErrObjectNotSet</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">Object is no longer valid.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src65" class="srcSentence">3421</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src66" class="srcSentence">adErrDataConversion</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">Application uses a value of the wrong type for the current operation.</caps:sentence>
                    <caps:sentence id="src68" class="srcSentence"> You might have supplied a string to an operation that expects a stream, for example.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src69" class="srcSentence">3704</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src70" class="srcSentence">adErrObjectClosed</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src71" class="srcSentence">Operation is not allowed when the object is closed.</caps:sentence>
                    <caps:sentence id="src72" class="srcSentence"> The <legacyBold>Connection</legacyBold> or <legacyBold>Recordset</legacyBold> has been closed.</caps:sentence>
                    <caps:sentence id="src73" class="srcSentence"> For example, some other routine might have closed a global object.</caps:sentence>
                    <caps:sentence id="src74" class="srcSentence"> You can prevent this error by checking the <legacyBold>State</legacyBold> property before you attempt an operation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src75" class="srcSentence">3705</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src76" class="srcSentence">adErrObjectOpen</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src77" class="srcSentence">Operation is not allowed when the object is open.</caps:sentence>
                    <caps:sentence id="src78" class="srcSentence"> An object that is open cannot be opened.</caps:sentence>
                    <caps:sentence id="src79" class="srcSentence"> Fields cannot be appended to an open <legacyBold>Recordset</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src80" class="srcSentence">3706</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src81" class="srcSentence">adErrProviderNotFound</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src82" class="srcSentence">Provider cannot be found.</caps:sentence>
                    <caps:sentence id="src83" class="srcSentence"> It may not be properly installed.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">The name of the provider might be incorrectly specified, the specified provider might not be installed on the computer where your code is being executed, or the installation might have become corrupted.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src85" class="srcSentence">3707</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src86" class="srcSentence">adErrBoundToCommand</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src87" class="srcSentence">The <legacyBold>ActiveConnection</legacyBold> property of a <legacyBold>Recordset</legacyBold> object, which has a <legacyBold>Command</legacyBold> object as its source, cannot be changed.</caps:sentence>
                    <caps:sentence id="src88" class="srcSentence"> The application attempted to assign a new <legacyBold>Connection</legacyBold> object to a <legacyBold>Recordset</legacyBold> that has a <legacyBold>Command</legacyBold> object as its source.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src89" class="srcSentence">3708</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src90" class="srcSentence">adErrInvalidParamInfo</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src91" class="srcSentence">
                      <legacyBold>Parameter</legacyBold> object is improperly defined.</caps:sentence>
                    <caps:sentence id="src92" class="srcSentence"> Inconsistent or incomplete information was provided.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src93" class="srcSentence">3709</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src94" class="srcSentence">adErrInvalidConnection</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src95" class="srcSentence">The connection cannot be used to perform this operation.</caps:sentence>
                    <caps:sentence id="src96" class="srcSentence"> It is either closed or invalid in this context.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src97" class="srcSentence">3710</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src98" class="srcSentence">adErrNotReentrant</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">Operation cannot be performed while processing event.</caps:sentence>
                    <caps:sentence id="src100" class="srcSentence"> An operation cannot be performed within an event handler that causes the event to fire again.</caps:sentence>
                    <caps:sentence id="src101" class="srcSentence"> For example, navigation methods should not be called from within a <legacyBold>WillMove</legacyBold> event handler.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src102" class="srcSentence">3711</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src103" class="srcSentence">adErrStillExecuting</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src104" class="srcSentence">Operation cannot be performed while executing asynchronously.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src105" class="srcSentence">3712</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src106" class="srcSentence">adErrOperationCancelled</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src107" class="srcSentence">Operation has been canceled by the user.</caps:sentence>
                    <caps:sentence id="src108" class="srcSentence"> The application has called the <legacyBold>CancelUpdate</legacyBold> or <legacyBold>CancelBatch</legacyBold> method and the current operation has been canceled.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src109" class="srcSentence">3713</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src110" class="srcSentence">adErrStillConnecting</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">Operation cannot be performed while connecting asynchronously.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src112" class="srcSentence">3714</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src113" class="srcSentence">adErrInvalidTransaction</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">Coordinating transaction is invalid or has not started.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src115" class="srcSentence">3715</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src116" class="srcSentence">adErrNotExecuting</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src117" class="srcSentence">Operation cannot be performed while not executing.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src118" class="srcSentence">3716</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src119" class="srcSentence">adErrUnsafeOperation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src120" class="srcSentence">Safety settings on this computer prohibit accessing a data source on another domain.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src121" class="srcSentence">3717</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src122" class="srcSentence">adWrnSecurityDialog</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src123" class="srcSentence">For internal use only.</caps:sentence>
                    <caps:sentence id="src124" class="srcSentence"> Don't use.</caps:sentence>
                    <caps:sentence id="src125" class="srcSentence"> (Entry was included for the sake of completeness.</caps:sentence>
                    <caps:sentence id="src126" class="srcSentence"> This error should not appear in your code.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src127" class="srcSentence">3718</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src128" class="srcSentence">adWrnSecurityDialogHeader</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src129" class="srcSentence">For internal use only.</caps:sentence>
                    <caps:sentence id="src130" class="srcSentence"> Don't use.</caps:sentence>
                    <caps:sentence id="src131" class="srcSentence"> (Entry included for the sake of completeness.</caps:sentence>
                    <caps:sentence id="src132" class="srcSentence"> This error should not appear in your code.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src133" class="srcSentence">3719</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src134" class="srcSentence">adErrIntegrityViolation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src135" class="srcSentence">Data value conflicts with the integrity constraints of the field.</caps:sentence>
                    <caps:sentence id="src136" class="srcSentence"> A new value for a <legacyBold>Field</legacyBold> would cause a duplicate key.</caps:sentence>
                    <caps:sentence id="src137" class="srcSentence"> A value that forms one side of a relationship between two records might not be updatable.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src138" class="srcSentence">3720</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src139" class="srcSentence">adErrPermissionDenied</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src140" class="srcSentence">Insufficient permission prevents writing to the field.</caps:sentence>
                    <caps:sentence id="src141" class="srcSentence"> The user named in the connection string does not have the proper permissions to write to a <legacyBold>Field</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src142" class="srcSentence">3721</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src143" class="srcSentence">adErrDataOverflow</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src144" class="srcSentence">Data value is too large to be represented by the field data type.</caps:sentence>
                    <caps:sentence id="src145" class="srcSentence"> A numeric value that is too large for the intended field was assigned.</caps:sentence>
                    <caps:sentence id="src146" class="srcSentence"> For example, a long integer value was assigned to a short integer field.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src147" class="srcSentence">3722</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src148" class="srcSentence">adErrSchemaViolation</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src149" class="srcSentence">Data value conflicts with the data type or constraints of the field.</caps:sentence>
                    <caps:sentence id="src150" class="srcSentence"> The data store has validation constraints that differ from the <legacyBold>Field</legacyBold> value.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src151" class="srcSentence">3723</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src152" class="srcSentence">adErrSignMismatch</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src153" class="srcSentence">Conversion failed because the data value was signed and the field data type used by the provider was unsigned.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src154" class="srcSentence">3724</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src155" class="srcSentence">adErrCantConvertvalue</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src156" class="srcSentence">Data value cannot be converted for reasons other than sign mismatch or data overflow.</caps:sentence>
                    <caps:sentence id="src157" class="srcSentence"> For example, conversion would have truncated data.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src158" class="srcSentence">3725</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src159" class="srcSentence">adErrCantCreate</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src160" class="srcSentence">Data value cannot be set or retrieved because the field data type was unknown, or the provider had insufficient resources to perform the operation.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src161" class="srcSentence">3726</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src162" class="srcSentence">adErrColumnNotOnThisRow</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src163" class="srcSentence">Record does not contain this field.</caps:sentence>
                    <caps:sentence id="src164" class="srcSentence"> An incorrect field name was specified or a field not in the <legacyBold>Fields</legacyBold> collection of the current record was referenced.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src165" class="srcSentence">3727</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src166" class="srcSentence">adErrURLDoesNotExist</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src167" class="srcSentence">Either the source URL or the parent of the destination URL does not exist.</caps:sentence>
                    <caps:sentence id="src168" class="srcSentence"> There is a typographical error in either the source or destination URL.</caps:sentence>
                    <caps:sentence id="src169" class="srcSentence"> You might have <codeInline>http://mysite/photo/myphoto.jpg</codeInline> when you should actually have <codeInline>http://mysite/photos/myphoto.jpg</codeInline> instead.</caps:sentence>
                    <caps:sentence id="src170" class="srcSentence"> The typographical error in the parent URL (in this case, <legacyItalic>photo</legacyItalic> instead of <legacyItalic>photos</legacyItalic>) has caused the error.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src171" class="srcSentence">3728</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src172" class="srcSentence">adErrTreePermissionDenied</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src173" class="srcSentence">Permissions are insufficient to access tree or subtree.</caps:sentence>
                    <caps:sentence id="src174" class="srcSentence"> The user named in the connection string does not have the appropriate permissions.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src175" class="srcSentence">3729</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src176" class="srcSentence">adErrInvalidURL</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src177" class="srcSentence">URL contains invalid characters.</caps:sentence>
                    <caps:sentence id="src178" class="srcSentence"> Make sure the URL is typed correctly.</caps:sentence>
                    <caps:sentence id="src179" class="srcSentence"> The URL follows the scheme registered to the current provider (for example, Internet Publishing Provider is registered for http).</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src180" class="srcSentence">3730</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src181" class="srcSentence">adErrResourceLocked</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src182" class="srcSentence">Object represented by the specified URL is locked by one or more other processes.</caps:sentence>
                    <caps:sentence id="src183" class="srcSentence"> Wait until the process has finished and attempt the operation again.</caps:sentence>
                    <caps:sentence id="src184" class="srcSentence"> The object you are trying to access has been locked by another user or by another process in your application.</caps:sentence>
                    <caps:sentence id="src185" class="srcSentence"> This is most likely to arise in a multi-user environment.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src186" class="srcSentence">3731</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src187" class="srcSentence">adErrResourceExists</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src188" class="srcSentence">Copy operation cannot be performed.</caps:sentence>
                    <caps:sentence id="src189" class="srcSentence"> Object named by destination URL already exists.</caps:sentence>
                    <caps:sentence id="src190" class="srcSentence"> Specify <legacyBold>adCopyOverwrite</legacyBold> to replace the object.</caps:sentence>
                    <caps:sentence id="src191" class="srcSentence"> If you do not specify <legacyBold>adCopyOverwrite</legacyBold> when copying the files in a directory, the copy fails when you try to copy an item that already exists in the destination location.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src192" class="srcSentence">3732</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src193" class="srcSentence">adErrCannotComplete</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src194" class="srcSentence">The server cannot complete the operation.</caps:sentence>
                    <caps:sentence id="src195" class="srcSentence"> This might be because the server is busy with other operations or it might be low on resources.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src196" class="srcSentence">3733</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src197" class="srcSentence">adErrVolumeNotFound</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src198" class="srcSentence">Provider cannot locate the storage device indicated by the URL.</caps:sentence>
                    <caps:sentence id="src199" class="srcSentence"> Make sure the URL is typed correctly.</caps:sentence>
                    <caps:sentence id="src200" class="srcSentence"> The URL of the storage device might be incorrect, but this error can occur for other reasons.</caps:sentence>
                    <caps:sentence id="src201" class="srcSentence"> The device might be offline or a large volume of network traffic might prevent the connection from being made.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src202" class="srcSentence">3734</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src203" class="srcSentence">adErrOutOfSpace</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src204" class="srcSentence">Operation cannot be performed.</caps:sentence>
                    <caps:sentence id="src205" class="srcSentence"> Provider cannot obtain enough storage space.</caps:sentence>
                    <caps:sentence id="src206" class="srcSentence"> There might not be enough RAM or hard-drive space for temporary files on the server.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src207" class="srcSentence">3735</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src208" class="srcSentence">adErrResourceOutOfScope</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src209" class="srcSentence">Source or destination URL is outside the scope of the current record.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src210" class="srcSentence">3736</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src211" class="srcSentence">adErrUnavailable</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src212" class="srcSentence">Operation failed to complete and the status is unavailable.</caps:sentence>
                    <caps:sentence id="src213" class="srcSentence"> The field may be unavailable or the operation was not attempted.</caps:sentence>
                    <caps:sentence id="src214" class="srcSentence"> Another user might have changed or deleted the field you are trying to access.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src215" class="srcSentence">3737</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src216" class="srcSentence">adErrURLNamedRowDoesNotExist</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src217" class="srcSentence">Record named by this URL does not exist.</caps:sentence>
                    <caps:sentence id="src218" class="srcSentence"> While attempting to open a file using a <legacyBold>Record</legacyBold> object, either the file name or the path to the file was misspelled.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src219" class="srcSentence">3738</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src220" class="srcSentence">adErrDelResOutOfScope</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src221" class="srcSentence">The URL of the object to be deleted is outside the scope of the current record.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src222" class="srcSentence">3747</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src223" class="srcSentence">adErrCatalogNotSet</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src224" class="srcSentence">Operation requires a valid <legacyBold>ParentCatalog</legacyBold>.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src225" class="srcSentence">3748</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src226" class="srcSentence">adErrCantChangeConnection</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src227" class="srcSentence">Connection was denied.</caps:sentence>
                    <caps:sentence id="src228" class="srcSentence"> The new connection you requested has different characteristics than the one already in use.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src229" class="srcSentence">3749</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src230" class="srcSentence">adErrFieldsUpdateFailed</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src231" class="srcSentence">Fields update failed.</caps:sentence>
                    <caps:sentence id="src232" class="srcSentence"> For further information, examine the <legacyBold>Status </legacyBold>property of individual field objects.</caps:sentence>
                    <caps:sentence id="src233" class="srcSentence"> This error can occur in two situations: when changing a <legacyBold>Field</legacyBold> object's value in the process of changing or adding a record to the database; and when changing the properties of the <legacyBold>Field</legacyBold> object itself.</caps:sentence>
                  </para>
                  <para>
                    <caps:sentence id="src234" class="srcSentence">The <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> update failed due to a problem with one of the fields in the current record.</caps:sentence>
                    <caps:sentence id="src235" class="srcSentence"> Enumerate the <legacyBold>Fields</legacyBold> collection and check the <legacyBold>Status</legacyBold> property of each field to determine the cause of the problem.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src236" class="srcSentence">3750</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src237" class="srcSentence">adErrDenyNotSupported</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src238" class="srcSentence">Provider does not support sharing restrictions.</caps:sentence>
                    <caps:sentence id="src239" class="srcSentence"> An attempt was made to restrict file sharing and your provider does not support the concept.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src240" class="srcSentence">3751</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <legacyBold>
                      <caps:sentence id="src241" class="srcSentence">adErrDenyTypeNotSupported</caps:sentence>
                    </legacyBold>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src242" class="srcSentence">Provider does not support the requested kind of sharing restriction.</caps:sentence>
                    <caps:sentence id="src243" class="srcSentence"> An attempt was made to establish a particular type of file-sharing restriction that is not supported by your provider.</caps:sentence>
                    <caps:sentence id="src244" class="srcSentence"> See the provider's documentation to determine what file-sharing restrictions are supported.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>