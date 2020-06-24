.. _elemento-front:

<front>
=======

+-------------------------+---------+
| Aparece em              | Ocorre  |
+=========================+=========+
| :ref:`elemento-article` | Uma vez |
+-------------------------+---------+


Parte inicial do documento que compreende:

+--------------------------+------------------------------+
| Itens                    | Elementos                    |
+==========================+==============================+
| informações do periódico | :ref:`elemento-journal-meta` |
+--------------------------+------------------------------+
| informações do artigo    | :ref:`elemento-article-meta` |
+--------------------------+------------------------------+

  

Exemplo:

.. code-block:: xml

   ...
   <front>
        <journal-meta>
             <journal-id journal-id-type="publisher-id">scie</journal-id>
             <journal-title-group>
                  <journal-title>SciELO Journal</journal-title>
                  <abbrev-journal-title abbrev-type="publisher">Scie. Jour.</abbrev-journal-title>
             </journal-title-group>
             <issn pub-type="ppub">1234-5678</issn>
             <issn pub-type="epub">8765-4321</issn>
             <publisher>
                  <publisher-name>Packer and Cia</publisher-name>
             </publisher>
        </journal-meta>
        <article-meta>
             <article-id pub-id-type="doi">10.1590/1234-5678v01n01a01</article-id>
             <article-categories>
                  <subj-group subj-group-type="heading">
                       <subject>Original Articles</subject>
                  </subj-group>
             </article-categories>
             <title-group>
                  <article-title>Pellentesque eleifend ex nec arcu accumsan finibus</article-title>
             </title-group>
             <contrib-group>
                  <contrib contrib-type="author">
                       <name>
                             <surname>Lestrange</surname>
                             <given-names>Bellatrix</given-names>
                       </name>
                       <xref ref-type="aff" rid="aff1">1</xref>
                       <xref ref-type="corresp" rid="c1">*</xref>
                  </contrib>
                  <contrib contrib-type="author">
                       <name>
                             <surname>McGonagall</surname>
                             <given-names>Minerva</given-names>
                       </name>
                       <xref ref-type="aff" rid="aff1">1</xref>
                  </contrib>
                  <contrib contrib-type="author">
                       <name>
                             <surname>Dumbledore</surname>
                             <given-names>Albus Percival Wulfric Brian</given-names>
                       </name>
                       <xref ref-type="aff" rid="aff1">1</xref>
                  </contrib>
                  <aff id="aff1">
                       <label>1</label>
                       <institution content-type="original">Universidade de Hogwarts - UH, Faculdade de Ciência, Parnaíba, PI, Brazil</institution>
                       <institution content-type="orgname">Universidade de Hogwarts</institution>
                       <institution content-type="orgdiv1">Faculdade de Ciência</institution>
                       <addr-line>
                            <city>Parnaíba</city>
                            <state>PI</state>
                       </addr-line>
                       <country country="BR">Brazil</country>
                  </aff>
             </contrib-group>
             <author-notes>
                  <corresp id="c1">
                  <label>*</label>Correspondence to:  Minerva McGonagall Rua Beco Diagonal 2076 - Ininga CEP: 12345-000 Teresina, PI, E-mail: <email>mcgonagall@nimbus2000.com</email>
                  </corresp>
             </author-notes>
             <pub-date publication-format="electronic" date-type="pub">
                 <day>01</day>
                 <month>01</month>
                 <year>2019</year>
             </pub-date>
             <pub-date publication-format="electronic" date-type="collection">
                 <season>Jan-Feb</season>
                 <year>2019</year>
             </pub-date>
             <volume>14</volume>
             <issue>04</issue>
             <fpage>256</fpage>
             <lpage>261</lpage>
             <history>
                  <date date-type="received">
                       <day>21</day>
                       <month>10</month>
                       <year>2014</year>
                  </date>
                  <date date-type="accepted">
                       <day>09</day>
                       <month>12</month>
                       <year>2014</year>
                  </date>
             </history>
             <permissions>
                  <license license-type="open-access" xlink:href="https://creativecommons.org/licenses/by/4.0/" xml:lang="en">
                       <license-p>This is an article published in open access under a Creative Commons license</license-p>
                  </license>
             </permissions>
             <abstract>
                  <title>Abstract</title>
                  <sec>
                       <title>Objectives:</title>
                       <p>Ut ut augue placerat, mollis mauris eget, tempus odio. Pellentesque eleifend ex nec arcu accumsan finibus. Praesent ac eleifend nibh, molestie pellentesque purus.</p>
                  </sec>
                  <sec>
                       <title>Methods:</title>
                       <p>Pellentesque in rhoncus nulla. Aliquam elementum euismod pulvinar. Vestibulum consequat, nisi sit amet auctor sodales, risus erat condimentum libero, eget avada kedava ultrices sem ante id est. Duis hendrerit est augue, sit amet varius erat semper id. Mauris non tortor et mauris dignissim ultricies.</p>
                  </sec>
                  <sec>
                       <title>Results:</title>
                       <p> Maecenas auctor bibendum aliquam. Vestibulum accumsan consectetur tellus, sed placerat purus. Nullam ullamcorper tincidunt diam quis bazinga tincidunt. Pellentesque convallis arcu quis nunc sodales, eu pretium diam pulvinar. Integer posuere nulla non aliquet varius. Sed a velit non nunc dignissim tempus.</p>
                  </sec>
                  <sec>
                       <title>Conclusions:</title>
                       <p> Cruciatus Cras accumsan consequat urna, vitae placerat sem. Aenean elementum ex sed est feugiat, eget posuere nisl eleifend. Praesent posuere erat vel mauris malesuada accumsan. Suspendisse potenti. Nam nec justo elit.</p>
                  </sec>
             </abstract>
             <kwd-group xml:lang="en">
                  <title>Keywords:</title>
                  <kwd>ipsum</kwd>
                  <kwd>lorem</kwd>
                  <kwd>imperdiet</kwd>
             </kwd-group>
        </article-meta>
   </front>
   ...


