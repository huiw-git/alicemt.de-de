---
title: "Sample Recordset for Examining Data"
ms.custom: na
ms.date: 05/16/2016
ms.reviewer: na
ms.suite: na
ms.tgt_pltfrm: na
ms.topic: article
ms.assetid: e770e626-68b1-4ddf-a217-d7b30311e2ee
caps.latest.revision: 12
caps.handback.revision: 12
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
# Sample Recordset for Examining Data
<?xml version="1.0" encoding="utf-8"?>
<caps:SxS xmlns:caps="http://schemas.microsoft.com/build/caps/2013/11">
  <caps:SxSTarget locale="de-DE">
    <developerReferenceWithoutSyntaxDocument xsi:schemaLocation="http://ddue.schemas.microsoft.com/authoring/2003/5 http://dduestorage.blob.core.windows.net/ddueschema/developer.xsd" xmlns="http://ddue.schemas.microsoft.com/authoring/2003/5" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance">
      <introduction>
        <para>
          <caps:sentence sentenceid="c9b5bfb8432c7de75bd80e98edcdad78" id="tgt1" class="tgtSentence">First, let's look at the <legacyBold>Recordset</legacyBold> object as returned using the following SQL query, executed against the Northwind sample data base in Microsoft SQL Server.</caps:sentence>
        </para>
        <code>SELECT ProductID,ProductName,UnitPrice 
FROM Products 
WHERE CategoryID = 7  </code>
        <para>
          <caps:sentence sentenceid="58be74a664be9b7192cf9cc12aad3ef7" id="tgt2" class="tgtSentence">The resultant <legacyBold>Recordset</legacyBold> object contains all the produces in the database shown in the following table.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="cb67418f474bb3b2b21b66cad9903671" id="tgt3" class="tgtSentence">ProductID</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="b091db7582897e22a216c47809ef2cd6" id="tgt4" class="tgtSentence"> ProductName </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="8545a0b3f5794e3d5a62c760b843d713" id="tgt5" class="tgtSentence"> UnitPrice</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="8f14e45fceea167a5a36dedd4bea2543" id="tgt6" class="tgtSentence">7</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="fc937ee4bc0e02154ac237d6016a70f9" id="tgt7" class="tgtSentence">Uncle Bob's Organic Dried Pears</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="dd986c04126f00a30158facd05409ffc" id="tgt8" class="tgtSentence">30.0000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="aab3238922bcc25a6f606eb525ffdc56" id="tgt9" class="tgtSentence">14</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="5df7f1701b778d03d57456afea567922" id="tgt10" class="tgtSentence">Tofu</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="4b45f0162741df63b3e3275b3f97625a" id="tgt11" class="tgtSentence">23.2500</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="33e75ff09dd601bbe69f351039152189" id="tgt12" class="tgtSentence">28</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="83abeb51e88540f92b94b0e093d99a1a" id="tgt13" class="tgtSentence">Rssle Sauerkraut</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="719464c9a55af0f7b4eeb3d71b433113" id="tgt14" class="tgtSentence">45.6000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="2838023a778dfaecdc212708f721b788" id="tgt15" class="tgtSentence">51</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="57dff3a96fb1434cc3ba684ab1d661fa" id="tgt16" class="tgtSentence">Manjimup Dried Apples</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="9d40d810dddcaade7299cdba2a78211c" id="tgt17" class="tgtSentence">53.0000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence sentenceid="ad61ab143223efbc24c7d2583be69251" id="tgt18" class="tgtSentence">74</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="037c61573ada8ba1a351164b56241b39" id="tgt19" class="tgtSentence">Longlife Tofu</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence sentenceid="863d6e51a2cc27a080f62327e719b41e" id="tgt20" class="tgtSentence">10.0000</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence sentenceid="a21e93698041c90d91cc18a92c54670b" id="tgt21" class="tgtSentence">If you are interested in getting these results yourself, try the following JScript example:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="74aad8a6-06cc-4a2c-811a-d78f9b741d84">
                <caps:sentence sentenceid="aadbffe4458f5af16e3bab05a82223b5" id="tgt22" class="tgtSentence">JScript Example to Return a Recordset</caps:sentence>
              </legacyLink>
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
          <caps:sentence id="src1" class="srcSentence">First, let's look at the <legacyBold>Recordset</legacyBold> object as returned using the following SQL query, executed against the Northwind sample data base in Microsoft SQL Server.</caps:sentence>
        </para>
        <code>SELECT ProductID,ProductName,UnitPrice 
FROM Products 
WHERE CategoryID = 7  </code>
        <para>
          <caps:sentence id="src2" class="srcSentence">The resultant <legacyBold>Recordset</legacyBold> object contains all the produces in the database shown in the following table.</caps:sentence>
        </para>
        <table>
          <thead>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src3" class="srcSentence">ProductID</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src4" class="srcSentence"> ProductName </caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src5" class="srcSentence"> UnitPrice</caps:sentence>
                </para>
              </TD>
            </tr>
          </thead>
          <tbody>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src6" class="srcSentence">7</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src7" class="srcSentence">Uncle Bob's Organic Dried Pears</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src8" class="srcSentence">30.0000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src9" class="srcSentence">14</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src10" class="srcSentence">Tofu</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src11" class="srcSentence">23.2500</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src12" class="srcSentence">28</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src13" class="srcSentence">Rssle Sauerkraut</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src14" class="srcSentence">45.6000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src15" class="srcSentence">51</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src16" class="srcSentence">Manjimup Dried Apples</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src17" class="srcSentence">53.0000</caps:sentence>
                </para>
              </TD>
            </tr>
            <tr>
              <TD>
                <para>
                  <caps:sentence id="src18" class="srcSentence">74</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src19" class="srcSentence">Longlife Tofu</caps:sentence>
                </para>
              </TD>
              <TD>
                <para>
                  <caps:sentence id="src20" class="srcSentence">10.0000</caps:sentence>
                </para>
              </TD>
            </tr>
          </tbody>
        </table>
        <para>
          <caps:sentence id="src21" class="srcSentence">If you are interested in getting these results yourself, try the following JScript example:  </caps:sentence>
        </para>
        <list class="bullet">
          <listItem>
            <para>
              <legacyLink xlink:href="74aad8a6-06cc-4a2c-811a-d78f9b741d84">
                <caps:sentence id="src22" class="srcSentence">JScript Example to Return a Recordset</caps:sentence>
              </legacyLink>
            </para>
          </listItem>
        </list>
      </introduction>
      <relatedTopics></relatedTopics>
    </developerReferenceWithoutSyntaxDocument>
  </caps:SxSSource>
</caps:SxS>