---
title: "Records and Provider-Supplied Fields"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: 77f95e0a-0cf2-411a-a792-593f77330fbd
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
# Records and Provider-Supplied Fields
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="6c67ca18966376f0770ba0c48c0c1a06" id="tgt1" class="tgtSentence">When a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object is opened, its source can be the current row of an open <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, an absolute URL, or a relative URL in conjunction with an open <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="ed450737362fc52b035fe3252bbda16c" id="tgt2" class="tgtSentence">If the <legacyBold>Record</legacyBold> is opened from a <legacyBold>Recordset</legacyBold>, the <legacyBold>Record</legacyBold> object <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection will contain all the fields from the <legacyBold>Recordset</legacyBold>, plus any fields added by the underlying provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="3bffec1980354dbddc6c48257628768f" id="tgt3" class="tgtSentence">The provider may insert additional fields that serve as supplementary characteristics of the <legacyBold>Record</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="fe2a20f6a192d744ab32291f02e7402c" id="tgt4" class="tgtSentence"> As a result, a <legacyBold>Record</legacyBold> may have unique fields not in the <legacyBold>Recordset</legacyBold> as a whole or any <legacyBold>Record</legacyBold> derived from another row of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="8657723bd7de7a7403f09f33aa5d76b6" id="tgt5" class="tgtSentence">For example, all rows of a <legacyBold>Recordset</legacyBold> derived from an e-mail data source might have columns such as From, To, and Subject.</caps:sentence>
          <caps:sentence sentenceid="dc1333c5273e254fc7355ec5cc19b3bf" id="tgt6" class="tgtSentence"> A <legacyBold>Record</legacyBold> derived from that <legacyBold>Recordset</legacyBold> will have the same fields.</caps:sentence>
          <caps:sentence sentenceid="10e4c3323ed52f61b948812800a2c887" id="tgt7" class="tgtSentence"> However, the <legacyBold>Record</legacyBold> may also have other fields unique to the particular message represented by that <legacyBold>Record</legacyBold>, such as Attachment and Cc (carbon copy).</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="68121285565acb6cd92e41942bfca2ab" id="tgt8" class="tgtSentence">Although the <legacyBold>Record</legacyBold> object and current row of the <legacyBold>Recordset</legacyBold> have the same fields, they are different because <legacyBold>Record</legacyBold> and <legacyBold>Recordset</legacyBold> objects have different methods and properties.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="efc82f4b3fd4407374f622c9379b90fc" id="tgt9" class="tgtSentence">A field held in common by the <legacyBold>Record</legacyBold> and <legacyBold>Recordset</legacyBold> can be modified on either object.</caps:sentence>
          <caps:sentence sentenceid="43ebc82c8dc3acc31fb81367d2b98976" id="tgt10" class="tgtSentence"> However, the field cannot be deleted on the <legacyBold>Record</legacyBold> object, although the underlying provider may support setting the field to null.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="1cd27dcb80c5641d92be73a8ae4777a2" id="tgt11" class="tgtSentence">After the <legacyBold>Record</legacyBold> is opened, you can programmatically add fields.</caps:sentence>
          <caps:sentence sentenceid="c6ec563b5245922295e34658844fefa3" id="tgt12" class="tgtSentence"> You can also delete fields that you have added, but you cannot delete fields from the original <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence sentenceid="a652b29b66bc451fc81f9fcd80ecffce" id="tgt13" class="tgtSentence">You can also open the <legacyBold>Record</legacyBold> object directly from a URL.</caps:sentence>
          <caps:sentence sentenceid="dc4074c66d73ff3cf6b872a604fbd080" id="tgt14" class="tgtSentence"> In this case, the fields added to the <legacyBold>Record</legacyBold> depend on the underlying provider.</caps:sentence>
          <caps:sentence sentenceid="2f19e3efc3c92ea4a4a625cf5107f5d4" id="tgt15" class="tgtSentence"> Currently, most providers add a set of fields that describe the entity represented by the <legacyBold>Record</legacyBold>.</caps:sentence>
          <caps:sentence sentenceid="d1d54ea413fff36cc62c43b1fed4d3a1" id="tgt16" class="tgtSentence"> If the entity consists of a stream of bytes, such as a simple file, a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object can usually be opened from the <legacyBold>Record</legacyBold>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence sentenceid="94d7af4e42435585b76c138925e7f599" id="tgt17" class="tgtSentence">Special Fields for Document Source Providers</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="bc9d6a43da12a025f75c7d73cb3cfd35" id="tgt18" class="tgtSentence">A special class of providers, called <legacyItalic>document source providers</legacyItalic>, manages folders and documents.</caps:sentence>
            <caps:sentence sentenceid="111162165c5a30c9a1f74b4df1252fac" id="tgt19" class="tgtSentence"> When a <legacyBold>Record</legacyBold> object represents a document or a <legacyBold>Recordset</legacyBold> object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document instead of the actual document itself.</caps:sentence>
            <caps:sentence sentenceid="2f7b36b2f002d2c27e6c098d24b305b3" id="tgt20" class="tgtSentence"> Typically, one field contains a reference to the <legacyBold>Stream</legacyBold> that represents the document.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b5413edf5f0804572b66923e690d0ef8" id="tgt21" class="tgtSentence">These fields constitute a resource <legacyBold>record</legacyBold> or <legacyBold>recordset</legacyBold> and are listed for the specific providers that support them in <legacyLink xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="e4a892d433cec9574c008263f2f100ad" id="tgt22" class="tgtSentence">Two constants index the <legacyBold>Fields</legacyBold> collection of a resource <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> to retrieve a pair of commonly used fields.</caps:sentence>
            <caps:sentence sentenceid="a6c7a1524c07b8d07b0194350863073a" id="tgt23" class="tgtSentence"> The <legacyBold>Field</legacyBold> object <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property returns the desired content.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence sentenceid="f0d4a8323c0fe06c7f83451d405010e3" id="tgt24" class="tgtSentence">The field accessed with the <legacyBold>adDefaultStream</legacyBold> constant contains a default stream associated with the <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                <caps:sentence sentenceid="d360b424a0659f32cccfb410c1a1567d" id="tgt25" class="tgtSentence"> The provider assigns a default stream to an object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence sentenceid="05e05f3d09c504ffcc7d36235f3ac2c5" id="tgt26" class="tgtSentence">The field accessed with the <legacyBold>adRecordURL</legacyBold> constant contains the absolute URL that identifies the document.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence sentenceid="83ac1947d608bd115564f284de83bda1" id="tgt27" class="tgtSentence">A document source provider does not support the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of <legacyBold>Record</legacyBold> and <legacyBold>Field</legacyBold> objects.</caps:sentence>
            <caps:sentence sentenceid="1a51d9639e1334a66114d49af0450f30" id="tgt28" class="tgtSentence"> The content of the <legacyBold>Properties</legacyBold> collection is null for such objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence sentenceid="b41a3f94e6973665c9e4085281362d95" id="tgt29" class="tgtSentence">A document source provider may add a provider-specific property such as <legacyBold>Datasource Type</legacyBold> to identify whether it is a document source provider.</caps:sentence>
            <caps:sentence sentenceid="3f0d57148c6fd9789e7f32f8cb3b4ac8" id="tgt30" class="tgtSentence"> For more information about how to determine your type of provider, see your provider documentation.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence sentenceid="ee0500ab3f459bc65bbe8bf3e4227569" id="tgt31" class="tgtSentence">Resource Recordset Columns</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence sentenceid="5d204946639f861ba14a6c58f5c7b846" id="tgt32" class="tgtSentence">A <legacyItalic>resource recordset </legacyItalic>consists of the following columns.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8b4341e678f3cb95b8f3105187413970" id="tgt33" class="tgtSentence">Column name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="db38663d69a856001aa3894023481212" id="tgt34" class="tgtSentence">Type </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="67daf92c833c41c95db874e18fcb2786" id="tgt35" class="tgtSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="88c347803fe56d9af1fe8e33046e19ec" id="tgt36" class="tgtSentence">RESOURCE_PARSENAME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8ea86e7481b22f4fb0b50f225bb4304" id="tgt37" class="tgtSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1417f3802fa8be3a64299bc2c303326f" id="tgt38" class="tgtSentence">Read-only.</caps:sentence>
                    <caps:sentence sentenceid="57b03b4f4dccec61c8c34ae86d51923e" id="tgt39" class="tgtSentence"> Indicates the URL of the resource.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="22d01fae5e41fb4a73828b59528dae12" id="tgt40" class="tgtSentence">RESOURCE_PARENTNAME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8ea86e7481b22f4fb0b50f225bb4304" id="tgt41" class="tgtSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1417f3802fa8be3a64299bc2c303326f" id="tgt42" class="tgtSentence">Read-only.</caps:sentence>
                    <caps:sentence sentenceid="56f2b932e1df0c4835c59ba3a84944e0" id="tgt43" class="tgtSentence"> Indicates the absolute URL of the parent record.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="66ffb4ea044837ce46d8ed208e0b842a" id="tgt44" class="tgtSentence">RESOURCE_ABSOLUTEPARSENAME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8ea86e7481b22f4fb0b50f225bb4304" id="tgt45" class="tgtSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1417f3802fa8be3a64299bc2c303326f" id="tgt46" class="tgtSentence">Read-only.</caps:sentence>
                    <caps:sentence sentenceid="d3edbbe075f369c3b4e1bb03ab3fe30e" id="tgt47" class="tgtSentence"> Indicates the absolute URL of the resource, which is the concatenation of PARENTNAME and PARSENAME.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="17aa761cde17c4b8a8dd39532883c541" id="tgt48" class="tgtSentence">RESOURCE_ISHIDDEN</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37d52c4baad3447a789a5339c3378dbc" id="tgt49" class="tgtSentence">AdBoolean</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="5a3cd6e842358173bc4b4f6e17c7df8a" id="tgt50" class="tgtSentence">True if the resource is hidden.</caps:sentence>
                    <caps:sentence sentenceid="57fe594edb6d7f06e3a42fd3ccec28d6" id="tgt51" class="tgtSentence"> No rows will be returned unless the command that creates the rowset explicitly selects rows where RESOURCE_ISHIDDEN is True.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="49767589aa173ea0dd5b2ae05d0feefa" id="tgt52" class="tgtSentence">RESOURCE_ISREADONLY</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37d52c4baad3447a789a5339c3378dbc" id="tgt53" class="tgtSentence">AdBoolean</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="bf4215f235bd69e8d5c64d1c5c7c10dc" id="tgt54" class="tgtSentence">True if the resource is read-only.</caps:sentence>
                    <caps:sentence sentenceid="60e7b654d5bbc57bc09e1c3b4742f011" id="tgt55" class="tgtSentence"> Tries to open this resource with DBBINDFLAG_WRITE and will fail with DB_E_READONLY.</caps:sentence>
                    <caps:sentence sentenceid="563f2d05d79fd0673637c138845bd9f8" id="tgt56" class="tgtSentence"> This property can be edited even when the resource has only been opened for reading.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1369592b7bd3330670e5c136808ae1fe" id="tgt57" class="tgtSentence">RESOURCE_CONTENTTYPE</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8ea86e7481b22f4fb0b50f225bb4304" id="tgt58" class="tgtSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="c9769e8668b804c142509953198e947b" id="tgt59" class="tgtSentence">Indicates the likely use of the document—for example, a lawyer's brief.</caps:sentence>
                    <caps:sentence sentenceid="605d0851d29f01f2b4abdce11b1efd01" id="tgt60" class="tgtSentence"> This may correspond to the Office template that was used to create the document.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1ad561f0a0c58027667b49aba9fc370d" id="tgt61" class="tgtSentence">RESOURCE_CONTENTCLASS</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8ea86e7481b22f4fb0b50f225bb4304" id="tgt62" class="tgtSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="2399cf9b785901d61ec9875cedaa2897" id="tgt63" class="tgtSentence">Indicates the MIME type of the document, indicating the format such as "<codeInline>text/html</codeInline>".</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="64393a5c7c6c82c3ab8d91b1d86bf98f" id="tgt64" class="tgtSentence">RESOURCE_CONTENTLANGUAGE</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8ea86e7481b22f4fb0b50f225bb4304" id="tgt65" class="tgtSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="21945863769e53b3beef84b371ff79aa" id="tgt66" class="tgtSentence">Indicates the language in which the content is stored.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="fedf09f0193253eebfed804e6c19978f" id="tgt67" class="tgtSentence">RESOURCE_CREATIONTIME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="8e404f4e4211ed81b6446ad93ddf492b" id="tgt68" class="tgtSentence">adFileTime </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1417f3802fa8be3a64299bc2c303326f" id="tgt69" class="tgtSentence">Read-only.</caps:sentence>
                    <caps:sentence sentenceid="eaaadd8951e4d4b45d26c57f4d77fd64" id="tgt70" class="tgtSentence"> Indicates a FILETIME structure that contains the time the resource was created.</caps:sentence>
                    <caps:sentence sentenceid="9500d8f2cac61335ce6cb75f028a1af4" id="tgt71" class="tgtSentence"> The time is reported in Coordinated Universal Time (UTC) format.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1caebaca8f29019b5c6e4d957070feed" id="tgt72" class="tgtSentence">RESOURCE_LASTACCESSTIME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="58298a73bdbf93666a0022f248f336fa" id="tgt73" class="tgtSentence">AdFileTime</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1417f3802fa8be3a64299bc2c303326f" id="tgt74" class="tgtSentence">Read-only.</caps:sentence>
                    <caps:sentence sentenceid="f8889f8a72ebdef5579e0e8408415dd2" id="tgt75" class="tgtSentence"> Indicates a FILETIME structure that contains the time that the resource was last accessed.</caps:sentence>
                    <caps:sentence sentenceid="301c089c451671523d4b3d9aa45d3ddd" id="tgt76" class="tgtSentence"> The time is in UTC format.</caps:sentence>
                    <caps:sentence sentenceid="2bf268f706bab20bba23b16e235679cd" id="tgt77" class="tgtSentence"> The FILETIME members are zero if the provider does not support this time member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="ada58934f09508f1db915c36447bc861" id="tgt78" class="tgtSentence">RESOURCE_LASTWRITETIME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="58298a73bdbf93666a0022f248f336fa" id="tgt79" class="tgtSentence">AdFileTime</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1417f3802fa8be3a64299bc2c303326f" id="tgt80" class="tgtSentence">Read-only.</caps:sentence>
                    <caps:sentence sentenceid="8a11401b33bc5e0991a2292bbe321ca6" id="tgt81" class="tgtSentence"> Indicates a FILETIME structure that contains the time that the resource was last written.</caps:sentence>
                    <caps:sentence sentenceid="301c089c451671523d4b3d9aa45d3ddd" id="tgt82" class="tgtSentence"> The time is in UTC format.</caps:sentence>
                    <caps:sentence sentenceid="2bf268f706bab20bba23b16e235679cd" id="tgt83" class="tgtSentence"> The FILETIME members are zero if the provider does not support this time member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f34faff65e01f30d2c1e2ee7ab9ec900" id="tgt84" class="tgtSentence">RESOURCE_STREAMSIZE</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="354aa52927e3b3013cb62754b82a1527" id="tgt85" class="tgtSentence">asUnsignedBigInt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1417f3802fa8be3a64299bc2c303326f" id="tgt86" class="tgtSentence">Read-only.</caps:sentence>
                    <caps:sentence sentenceid="c1036e0e23fc4fefa096ee17e519e4be" id="tgt87" class="tgtSentence"> Indicates the size of the resource's default stream, in bytes.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="6e63d8c680c01ff446ddc5fcdd7744df" id="tgt88" class="tgtSentence">RESOURCE_ISCOLLECTION</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37d52c4baad3447a789a5339c3378dbc" id="tgt89" class="tgtSentence">AdBoolean</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1417f3802fa8be3a64299bc2c303326f" id="tgt90" class="tgtSentence">Read-only.</caps:sentence>
                    <caps:sentence sentenceid="dea1e2ba74ba45920daa74e123a4c5e1" id="tgt91" class="tgtSentence"> True if the resource is a collection, such as a directory.</caps:sentence>
                    <caps:sentence sentenceid="953874d5a119985c2234670df010db81" id="tgt92" class="tgtSentence"> False if the resource is a simple file.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="976daf748afc217193c667a3f1b872e5" id="tgt93" class="tgtSentence">RESOURCE_ISSTRUCTUREDDOCUMENT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37d52c4baad3447a789a5339c3378dbc" id="tgt94" class="tgtSentence">AdBoolean</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e6e1b8bc4765c9f26a078a2508e7a9c3" id="tgt95" class="tgtSentence">True if the resource is a structured document.</caps:sentence>
                    <caps:sentence sentenceid="94ae53caaa7720290f87ab7e74dd5931" id="tgt96" class="tgtSentence"> False if the resource is not a structured document.</caps:sentence>
                    <caps:sentence sentenceid="cdc1e1925cf5fd1570988040c9b86cc0" id="tgt97" class="tgtSentence"> It could be a collection or a simple file.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="b4d3ed671715085fe02a16c1f77afa9c" id="tgt98" class="tgtSentence">DEFAULT_DOCUMENT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8ea86e7481b22f4fb0b50f225bb4304" id="tgt99" class="tgtSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1417f3802fa8be3a64299bc2c303326f" id="tgt100" class="tgtSentence">Read-only.</caps:sentence>
                    <caps:sentence sentenceid="64a151df6511e196c73278fff23bf4e0" id="tgt101" class="tgtSentence"> Indicates that this resource contains a URL to the default simple document of a folder or a structured document.</caps:sentence>
                    <caps:sentence sentenceid="9ed796204b4ce3db22353191d41bdfd6" id="tgt102" class="tgtSentence"> Used when the default stream is requested from a resource.</caps:sentence>
                    <caps:sentence sentenceid="9b4986122bff7889eada3c6031552b47" id="tgt103" class="tgtSentence"> This property is blank for a simple file.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="7c0aed8af52305e13a6b9045f231ee1b" id="tgt104" class="tgtSentence">CHAPTERED_CHILDREN</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="a7603bbeec3b3d9b1d22369b8ca409f5" id="tgt105" class="tgtSentence">AdChapter</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1417f3802fa8be3a64299bc2c303326f" id="tgt106" class="tgtSentence">Read-only.</caps:sentence>
                    <caps:sentence sentenceid="ba708b45d07f9118a1ba649a9c2f11ec" id="tgt107" class="tgtSentence"> Optional.</caps:sentence>
                    <caps:sentence sentenceid="b5d90722fd75da31a6b32ac383bc3c6a" id="tgt108" class="tgtSentence"> Indicates the chapter of the rowset that contains the children of the resource.</caps:sentence>
                    <caps:sentence sentenceid="ec0ccb843d8709c3cf9ed6d40e98bd1d" id="tgt109" class="tgtSentence"> (The <legacyItalic>OLE DB Provider for Internet Publishing</legacyItalic> does not use this column.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f0a444ffdeba85a5b5930d0e5e44fed2" id="tgt110" class="tgtSentence">RESOURCE_DISPLAYNAME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="f8ea86e7481b22f4fb0b50f225bb4304" id="tgt111" class="tgtSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1417f3802fa8be3a64299bc2c303326f" id="tgt112" class="tgtSentence">Read-only.</caps:sentence>
                    <caps:sentence sentenceid="d3a87eada7becb8cec588c4bbe912a16" id="tgt113" class="tgtSentence"> Indicates the display name of the resource.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence sentenceid="e361906926b263011a874c4c281d798d" id="tgt114" class="tgtSentence">RESOURCE_ISROOT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="37d52c4baad3447a789a5339c3378dbc" id="tgt115" class="tgtSentence">AdBoolean</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence sentenceid="1417f3802fa8be3a64299bc2c303326f" id="tgt116" class="tgtSentence">Read-only.</caps:sentence>
                    <caps:sentence sentenceid="5f38058cef44910f87dce22dd3a44dea" id="tgt117" class="tgtSentence"> True if the resource is the root of a collection or structured document.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSTarget>
  <caps:SxSSource locale="en-US">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence id="src1" class="srcSentence">When a <legacyLink xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record</legacyLink> object is opened, its source can be the current row of an open <legacyLink xlink:href="ede1415f-c3df-4cc5-a05b-2576b2b84b60">Recordset</legacyLink>, an absolute URL, or a relative URL in conjunction with an open <legacyLink xlink:href="ef6b1824-5b12-43db-89d7-8f3d13896d4d">Connection</legacyLink> object.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src2" class="srcSentence">If the <legacyBold>Record</legacyBold> is opened from a <legacyBold>Recordset</legacyBold>, the <legacyBold>Record</legacyBold> object <legacyLink xlink:href="7c371474-b88f-4730-afa5-44163a0488d5">Fields</legacyLink> collection will contain all the fields from the <legacyBold>Recordset</legacyBold>, plus any fields added by the underlying provider.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src3" class="srcSentence">The provider may insert additional fields that serve as supplementary characteristics of the <legacyBold>Record</legacyBold>.</caps:sentence>
          <caps:sentence id="src4" class="srcSentence"> As a result, a <legacyBold>Record</legacyBold> may have unique fields not in the <legacyBold>Recordset</legacyBold> as a whole or any <legacyBold>Record</legacyBold> derived from another row of the <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src5" class="srcSentence">For example, all rows of a <legacyBold>Recordset</legacyBold> derived from an e-mail data source might have columns such as From, To, and Subject.</caps:sentence>
          <caps:sentence id="src6" class="srcSentence"> A <legacyBold>Record</legacyBold> derived from that <legacyBold>Recordset</legacyBold> will have the same fields.</caps:sentence>
          <caps:sentence id="src7" class="srcSentence"> However, the <legacyBold>Record</legacyBold> may also have other fields unique to the particular message represented by that <legacyBold>Record</legacyBold>, such as Attachment and Cc (carbon copy).</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src8" class="srcSentence">Although the <legacyBold>Record</legacyBold> object and current row of the <legacyBold>Recordset</legacyBold> have the same fields, they are different because <legacyBold>Record</legacyBold> and <legacyBold>Recordset</legacyBold> objects have different methods and properties.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src9" class="srcSentence">A field held in common by the <legacyBold>Record</legacyBold> and <legacyBold>Recordset</legacyBold> can be modified on either object.</caps:sentence>
          <caps:sentence id="src10" class="srcSentence"> However, the field cannot be deleted on the <legacyBold>Record</legacyBold> object, although the underlying provider may support setting the field to null.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src11" class="srcSentence">After the <legacyBold>Record</legacyBold> is opened, you can programmatically add fields.</caps:sentence>
          <caps:sentence id="src12" class="srcSentence"> You can also delete fields that you have added, but you cannot delete fields from the original <legacyBold>Recordset</legacyBold>.</caps:sentence>
        </para>
        <para>
          <caps:sentence id="src13" class="srcSentence">You can also open the <legacyBold>Record</legacyBold> object directly from a URL.</caps:sentence>
          <caps:sentence id="src14" class="srcSentence"> In this case, the fields added to the <legacyBold>Record</legacyBold> depend on the underlying provider.</caps:sentence>
          <caps:sentence id="src15" class="srcSentence"> Currently, most providers add a set of fields that describe the entity represented by the <legacyBold>Record</legacyBold>.</caps:sentence>
          <caps:sentence id="src16" class="srcSentence"> If the entity consists of a stream of bytes, such as a simple file, a <legacyLink xlink:href="0514531f-009d-4519-abc3-d727014a39f1">Stream</legacyLink> object can usually be opened from the <legacyBold>Record</legacyBold>.</caps:sentence>
        </para>
      </introduction>
      <section>
        <title>
          <caps:sentence id="src17" class="srcSentence">Special Fields for Document Source Providers</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src18" class="srcSentence">A special class of providers, called <legacyItalic>document source providers</legacyItalic>, manages folders and documents.</caps:sentence>
            <caps:sentence id="src19" class="srcSentence"> When a <legacyBold>Record</legacyBold> object represents a document or a <legacyBold>Recordset</legacyBold> object represents a folder of documents, the document source provider populates those objects with a unique set of fields that describe characteristics of the document instead of the actual document itself.</caps:sentence>
            <caps:sentence id="src20" class="srcSentence"> Typically, one field contains a reference to the <legacyBold>Stream</legacyBold> that represents the document.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src21" class="srcSentence">These fields constitute a resource <legacyBold>record</legacyBold> or <legacyBold>recordset</legacyBold> and are listed for the specific providers that support them in <legacyLink xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</legacyLink>.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src22" class="srcSentence">Two constants index the <legacyBold>Fields</legacyBold> collection of a resource <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> to retrieve a pair of commonly used fields.</caps:sentence>
            <caps:sentence id="src23" class="srcSentence"> The <legacyBold>Field</legacyBold> object <legacyLink xlink:href="48919c74-86d4-462e-99b9-8854ceb8d683">Value</legacyLink> property returns the desired content.</caps:sentence>
          </para>
          <list class="bullet">
            <listItem>
              <para>
                <caps:sentence id="src24" class="srcSentence">The field accessed with the <legacyBold>adDefaultStream</legacyBold> constant contains a default stream associated with the <legacyBold>Record</legacyBold> or <legacyBold>Recordset</legacyBold> object.</caps:sentence>
                <caps:sentence id="src25" class="srcSentence"> The provider assigns a default stream to an object.</caps:sentence>
              </para>
            </listItem>
            <listItem>
              <para>
                <caps:sentence id="src26" class="srcSentence">The field accessed with the <legacyBold>adRecordURL</legacyBold> constant contains the absolute URL that identifies the document.</caps:sentence>
              </para>
            </listItem>
          </list>
          <para>
            <caps:sentence id="src27" class="srcSentence">A document source provider does not support the <legacyLink xlink:href="1d539aa8-ce0d-4418-ab03-8d0a3c1e9d82">Properties</legacyLink> collection of <legacyBold>Record</legacyBold> and <legacyBold>Field</legacyBold> objects.</caps:sentence>
            <caps:sentence id="src28" class="srcSentence"> The content of the <legacyBold>Properties</legacyBold> collection is null for such objects.</caps:sentence>
          </para>
          <para>
            <caps:sentence id="src29" class="srcSentence">A document source provider may add a provider-specific property such as <legacyBold>Datasource Type</legacyBold> to identify whether it is a document source provider.</caps:sentence>
            <caps:sentence id="src30" class="srcSentence"> For more information about how to determine your type of provider, see your provider documentation.</caps:sentence>
          </para>
        </content>
      </section>
      <section>
        <title>
          <caps:sentence id="src31" class="srcSentence">Resource Recordset Columns</caps:sentence>
        </title>
        <content>
          <para>
            <caps:sentence id="src32" class="srcSentence">A <legacyItalic>resource recordset </legacyItalic>consists of the following columns.</caps:sentence>
          </para>
          <table>
            <thead>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src33" class="srcSentence">Column name</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src34" class="srcSentence">Type </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src35" class="srcSentence">Description</caps:sentence>
                  </para>
                </TD>
              </tr>
            </thead>
            <tbody>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src36" class="srcSentence">RESOURCE_PARSENAME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src37" class="srcSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src38" class="srcSentence">Read-only.</caps:sentence>
                    <caps:sentence id="src39" class="srcSentence"> Indicates the URL of the resource.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src40" class="srcSentence">RESOURCE_PARENTNAME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src41" class="srcSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src42" class="srcSentence">Read-only.</caps:sentence>
                    <caps:sentence id="src43" class="srcSentence"> Indicates the absolute URL of the parent record.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src44" class="srcSentence">RESOURCE_ABSOLUTEPARSENAME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src45" class="srcSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src46" class="srcSentence">Read-only.</caps:sentence>
                    <caps:sentence id="src47" class="srcSentence"> Indicates the absolute URL of the resource, which is the concatenation of PARENTNAME and PARSENAME.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src48" class="srcSentence">RESOURCE_ISHIDDEN</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src49" class="srcSentence">AdBoolean</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src50" class="srcSentence">True if the resource is hidden.</caps:sentence>
                    <caps:sentence id="src51" class="srcSentence"> No rows will be returned unless the command that creates the rowset explicitly selects rows where RESOURCE_ISHIDDEN is True.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src52" class="srcSentence">RESOURCE_ISREADONLY</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src53" class="srcSentence">AdBoolean</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src54" class="srcSentence">True if the resource is read-only.</caps:sentence>
                    <caps:sentence id="src55" class="srcSentence"> Tries to open this resource with DBBINDFLAG_WRITE and will fail with DB_E_READONLY.</caps:sentence>
                    <caps:sentence id="src56" class="srcSentence"> This property can be edited even when the resource has only been opened for reading.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src57" class="srcSentence">RESOURCE_CONTENTTYPE</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src58" class="srcSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src59" class="srcSentence">Indicates the likely use of the document—for example, a lawyer's brief.</caps:sentence>
                    <caps:sentence id="src60" class="srcSentence"> This may correspond to the Office template that was used to create the document.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src61" class="srcSentence">RESOURCE_CONTENTCLASS</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src62" class="srcSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src63" class="srcSentence">Indicates the MIME type of the document, indicating the format such as "<codeInline>text/html</codeInline>".</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src64" class="srcSentence">RESOURCE_CONTENTLANGUAGE</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src65" class="srcSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src66" class="srcSentence">Indicates the language in which the content is stored.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src67" class="srcSentence">RESOURCE_CREATIONTIME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src68" class="srcSentence">adFileTime </caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src69" class="srcSentence">Read-only.</caps:sentence>
                    <caps:sentence id="src70" class="srcSentence"> Indicates a FILETIME structure that contains the time the resource was created.</caps:sentence>
                    <caps:sentence id="src71" class="srcSentence"> The time is reported in Coordinated Universal Time (UTC) format.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src72" class="srcSentence">RESOURCE_LASTACCESSTIME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src73" class="srcSentence">AdFileTime</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src74" class="srcSentence">Read-only.</caps:sentence>
                    <caps:sentence id="src75" class="srcSentence"> Indicates a FILETIME structure that contains the time that the resource was last accessed.</caps:sentence>
                    <caps:sentence id="src76" class="srcSentence"> The time is in UTC format.</caps:sentence>
                    <caps:sentence id="src77" class="srcSentence"> The FILETIME members are zero if the provider does not support this time member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src78" class="srcSentence">RESOURCE_LASTWRITETIME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src79" class="srcSentence">AdFileTime</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src80" class="srcSentence">Read-only.</caps:sentence>
                    <caps:sentence id="src81" class="srcSentence"> Indicates a FILETIME structure that contains the time that the resource was last written.</caps:sentence>
                    <caps:sentence id="src82" class="srcSentence"> The time is in UTC format.</caps:sentence>
                    <caps:sentence id="src83" class="srcSentence"> The FILETIME members are zero if the provider does not support this time member.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src84" class="srcSentence">RESOURCE_STREAMSIZE</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src85" class="srcSentence">asUnsignedBigInt</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src86" class="srcSentence">Read-only.</caps:sentence>
                    <caps:sentence id="src87" class="srcSentence"> Indicates the size of the resource's default stream, in bytes.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src88" class="srcSentence">RESOURCE_ISCOLLECTION</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src89" class="srcSentence">AdBoolean</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src90" class="srcSentence">Read-only.</caps:sentence>
                    <caps:sentence id="src91" class="srcSentence"> True if the resource is a collection, such as a directory.</caps:sentence>
                    <caps:sentence id="src92" class="srcSentence"> False if the resource is a simple file.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src93" class="srcSentence">RESOURCE_ISSTRUCTUREDDOCUMENT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src94" class="srcSentence">AdBoolean</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src95" class="srcSentence">True if the resource is a structured document.</caps:sentence>
                    <caps:sentence id="src96" class="srcSentence"> False if the resource is not a structured document.</caps:sentence>
                    <caps:sentence id="src97" class="srcSentence"> It could be a collection or a simple file.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src98" class="srcSentence">DEFAULT_DOCUMENT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src99" class="srcSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src100" class="srcSentence">Read-only.</caps:sentence>
                    <caps:sentence id="src101" class="srcSentence"> Indicates that this resource contains a URL to the default simple document of a folder or a structured document.</caps:sentence>
                    <caps:sentence id="src102" class="srcSentence"> Used when the default stream is requested from a resource.</caps:sentence>
                    <caps:sentence id="src103" class="srcSentence"> This property is blank for a simple file.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src104" class="srcSentence">CHAPTERED_CHILDREN</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src105" class="srcSentence">AdChapter</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src106" class="srcSentence">Read-only.</caps:sentence>
                    <caps:sentence id="src107" class="srcSentence"> Optional.</caps:sentence>
                    <caps:sentence id="src108" class="srcSentence"> Indicates the chapter of the rowset that contains the children of the resource.</caps:sentence>
                    <caps:sentence id="src109" class="srcSentence"> (The <legacyItalic>OLE DB Provider for Internet Publishing</legacyItalic> does not use this column.)</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src110" class="srcSentence">RESOURCE_DISPLAYNAME</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src111" class="srcSentence">AdVarWChar</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src112" class="srcSentence">Read-only.</caps:sentence>
                    <caps:sentence id="src113" class="srcSentence"> Indicates the display name of the resource.</caps:sentence>
                  </para>
                </TD>
              </tr>
              <tr>
                <TD>
                  <para>
                    <caps:sentence id="src114" class="srcSentence">RESOURCE_ISROOT</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src115" class="srcSentence">AdBoolean</caps:sentence>
                  </para>
                </TD>
                <TD>
                  <para>
                    <caps:sentence id="src116" class="srcSentence">Read-only.</caps:sentence>
                    <caps:sentence id="src117" class="srcSentence"> True if the resource is the root of a collection or structured document.</caps:sentence>
                  </para>
                </TD>
              </tr>
            </tbody>
          </table>
        </content>
      </section>
      <relatedTopics>
        <link xlink:href="db83ed2c-a8e3-460c-8682-64667e4d5d01">Record Object</link>
        <link xlink:href="e2581b47-b11e-4e1e-b96c-d39c77c5b48a">Appendix A: Providers</link>
      </relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>