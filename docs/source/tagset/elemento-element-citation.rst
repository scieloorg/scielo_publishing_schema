.. _elemento-element-citation:

<element-citation>
==================

Atributos obrigatórios:

  1. ``@publication-type``

+---------------------+---------+
| Aparece em          | Ocorre  |
+=====================+=========+
| :ref:`elemento-ref` | Uma vez |
+---------------------+---------+




``<element-citation>`` apresenta a identificação detalhada de cada referência bibliográfica e deve aparecer apenas como filho do elemento :ref:`elemento-ref`. Além disso, deve apresentar o atributo ``@publication-type``,  que indica o tipo de publicação da referência.

Os valores possíveis para o atributo ``@publication-type`` são:

+-----------+------------------------------------------------------------------+
| Valor     | Descrição                                                        |
+===========+==================================================================+
| book      | Referencia livros. Pode também representar somente uma parte ou  |
|           | capítulo de um livro.                                            |
+-----------+------------------------------------------------------------------+
| confproc  | Identifica documentos relacionados à eventos científicos: atas,  |
|           | anais, resultados, proceedings, convenções, conferências entre   |
|           | outros.                                                          |
+-----------+------------------------------------------------------------------+
| database  | Especifica bases de dados.                                       |
+-----------+------------------------------------------------------------------+
| journal   | Caracteriza publicações seriadas, editadas em unidades           |
|           | sucessivas, com designações numéricas e/ou cronológicas, e       |
|           | destinada a ser continuada indefinidamente.                      |
+-----------+------------------------------------------------------------------+
| patent    | Referencia patentes.                                             |
+-----------+------------------------------------------------------------------+
| report    | Identifica um relatório técnico, normalmente de autoria          |
|           | institucional.                                                   |
+-----------+------------------------------------------------------------------+
| software  | Referencia um software em suportes como CDs, DVDs, suporte       |
|           | online, dispositivos USB etc.                                    |
+-----------+------------------------------------------------------------------+
| thesis    | Caracteriza monografias, dissertações ou teses para obtenção de  |
|           | um grau acadêmico (livre-docência, doutorado, mestrado,          |
|           | bacharelado, licenciatura etc).                                  |
+-----------+------------------------------------------------------------------+
| webpage   | Identifica informações de web sites e blogs.                     |
+-----------+------------------------------------------------------------------+
| legal-doc | Referencia normas jurídicas.                                     |
+-----------+------------------------------------------------------------------+
| newspaper | Identifica artigos de jornal.                                    |
+-----------+------------------------------------------------------------------+
| data      | Referencia dados de pesquisa.                                    |
+-----------+------------------------------------------------------------------+
| other     | Especifica tipos não previstos pela *SciELO PS*.                 |
+-----------+------------------------------------------------------------------+


.. note::

  * Não incluir toda uma informação em um elemento com formatação ``<italic>`` e ``<bold>``;
  * Nunca utilizar pontuação (ponto final, vírgula etc) dentro de :ref:`elemento-element-citation`;
  * Todas as informações de uma referência devem ser marcadas. Caso não exista um elemento específico para determinada informação, esta deve ser inserida em :ref:`elemento-comment`.


Exemplos:

  * :ref:`elemento-element-citation-exemplo-1`
  * :ref:`elemento-element-citation-exemplo-2`
  * :ref:`elemento-element-citation-exemplo-3`
  * :ref:`elemento-element-citation-exemplo-4`
  * :ref:`elemento-element-citation-exemplo-5`
  * :ref:`elemento-element-citation-exemplo-6`
  * :ref:`elemento-element-citation-exemplo-7`
  * :ref:`elemento-element-citation-exemplo-8`
  * :ref:`elemento-element-citation-exemplo-9`
  * :ref:`elemento-element-citation-exemplo-10`
  * :ref:`elemento-element-citation-exemplo-11`
  * :ref:`elemento-element-citation-exemplo-12`
  * :ref:`elemento-element-citation-exemplo-13`
  * :ref:`elemento-element-citation-exemplo-14`
  * :ref:`elemento-element-citation-exemplo-15`
  * :ref:`elemento-element-citation-exemplo-16`


.. _elemento-element-citation-exemplo-1:

1. Periódico
------------

.. code-block:: xml

    <!-- Journal Sample -->

    ...
    <ref-list>
        <ref id="B01">
            <label>1</label>
            <mixed-citation>ARRETCHE, M. Federalism and territorial equality: a contradiction in terms? Dados, Rio de Janeiro, v. 5, n. 02, 2010 . Disponível em: &lt;http://socialsciences.scielo.org.</mixed-citation>
            <element-citation publication-type="journal">
                <person-group person-group-type="author">
                    <name>
                        <surname>ARRETCHE</surname>
                        <given-names>M</given-names>
                    </name>
                </person-group>
                <article-title>Federalism and territorial equality: a contradiction in terms?</article-title>
                <source>Dados</source>
                <publisher-loc>Rio de Janeiro</publisher-loc>
                <volume>5</volume>
                <issue>02</issue>
                <year>2010</year>
                <ext-link ext-link-type="uri" xlink:href="http://socialsciences.scielo.org">http://socialsciences.scielo.org</ext-link>
            </element-citation>
        </ref>
    <ref-list>
    ...


.. _elemento-element-citation-exemplo-2:

2. Capítulo de livro
--------------------

.. code-block:: xml

    <!-- Book Chapter Sample -->

    ...
    <ref-list>
        <ref id="B02">
            <label>2</label>
            <mixed-citation>Calkins BM, Mendeloff AI. The epidemiology of idiopathic inflammatory bowel disease. In: Kirsner JB, Shorter RG, eds. Inflammatory bowel disease, 4th ed. Baltimore: Williams &amp; Wilkins. 1995:31-68.</mixed-citation>
            <element-citation publication-type="book">
              <person-group person-group-type="author">
                <name>
                    <surname>Calkins</surname>
                    <given-names>BM</given-names>
                </name>
                <name>
                    <surname>Mendeloff</surname>
                    <given-names>AI</given-names>
                </name>
              </person-group>
                <chapter-title>The epidemiology of idiopathic inflammatory bowel
                disease.</chapter-title>
                <person-group person-group-type="editor">
                    <name>
                        <surname>Kirsner</surname>
                        <given-names>JB</given-names>
                    </name>
                    <name>
                        <surname>Shorter</surname>
                        <given-names>RG</given-names>
                    </name>
                </person-group>
                <source>Inflammatory bowel disease</source>
                <edition>4th ed</edition>
                <publisher-loc>Baltimore</publisher-loc>
                <publisher-name>Williams &amp; Wilkins</publisher-name>
                <year>1995</year>
                <fpage>31</fpage>
                <lpage>68</lpage>
            </element-citation>
        </ref>
    </ref-list>
    ...


.. _elemento-element-citation-exemplo-3:

3. Livro
--------

.. code-block:: xml

    <!-- Book Sample -->

    ...
    <ref-list>
        <ref id="B03">
            <label>3</label>
            <mixed-citation>LÉVY, Pierre. As tecnologias da inteligência: o futuro do pensamento na era da informática. Edição especial. Rio de Janeiro: Editora 34. 2001. 208 p.</mixed-citation>
        <element-citation publication-type="book">
            <person-group person-group-type="author">
                <name>
                    <surname>LÉVY</surname>
                    <given-names>Pierre</given-names>
                </name>
            </person-group>
            <source>As tecnologias da inteligência: o futuro do pensamento na era da informática</source>
            <edition>edição especial</edition>
            <publisher-loc>Rio de Janeiro</publisher-loc>
            <publisher-name>Editora 34</publisher-name>
            <year>2001</year>
            <size units="pages">208</size>
        </element-citation>
        </ref>
    </ref-list>
    ...


.. _elemento-element-citation-exemplo-4:

4. Página de Internet 1
-----------------------

.. code-block:: xml

    <!-- Webpage Sample -->

    ...
    <ref id="B04">
        <label>4</label>
        <mixed-citation>COB - Comitê Olímpico Brasileiro. Desafio para o corpo. Disponível em: http://www.cob.org.br/esportes/esporte.asp?id=39. (Acesso em 10 abr 2010)</mixed-citation>
        <element-citation publication-type="webpage">
            <person-group person-group-type="author">
                <collab>COB -Comitê Olímpico Brasileiro</collab>
            </person-group>
            <source>Desafio para o corpo</source>
            <comment>Disponível em: <ext-link ext-link-type="uri" xlink:href="http://www.cob.org.br/esportes/esporte.asp?id=39">http://www.cob.org.br/esportes/esporte.asp?id=39</ext-link></comment>
            <date-in-citation content-type="access-date">10 abr 2010</date-in-citation>
        </element-citation>
    </ref>
    ...

.. note:: Quando a referência apresentar URL com texto ("Disponível em:" ou "Available from:"), identificar conforme o exemplo acima.


.. _elemento-element-citation-exemplo-5:

5. Página de Internet 2
-----------------------

.. code-block:: xml

    <!-- Webpage Sample 2 -->

    <ref id="B21">
        <label>21</label>
        <mixed-citation>Fugh-Berman A. PharmedOUT [Internet]. Washington: Georgetown University, Department of Physiology and Biophysics; c2006 [cited 2007 Mar 23]. Available from: http://www.pharmedout.org/.</mixed-citation>
        <element-citation publication-type="webpage">
            <person-group person-group-type="author">
                <name>
                    <surname>Fugh-Berman</surname>
                    <given-names>A</given-names>
                </name>
            </person-group>
            <source>PharmedOUT [Internet]</source>
            <publisher-loc>Washington</publisher-loc>
            <publisher-name>Georgetown University, Department of Physiology and Biophysics</publisher-name>
            <year>c2006</year>
            <date-in-citation>cited 2007 Mar 23</date-in-citation>
            <comment>Available from: <ext-link ext-link-type="uri" xlink:href="http://www.pharmedout.org">http://www.pharmedout.org</ext-link></comment>
        </element-citation>
    </ref>


.. _elemento-element-citation-exemplo-6:

6. Relatório 1
--------------

.. code-block:: xml

    <!-- Report Sample -->

    ...
    <ref-list>
        <ref id="B05">
            <label>5</label>
            <mixed-citation>World Health Organization. Control of the leishmaniases. Geneva: WHO; 2010.(Technical Report Series; 949)</mixed-citation>
            <element-citation publication-type="report">
                <person-group person-group-type="author">
                    <collab>World Health Organization</collab>
                </person-group>
                <source>Control of the leishmaniases</source>
                <publisher-loc>Geneva</publisher-loc>
                <publisher-name>WHO</publisher-name>
                <year>2010</year>
                <comment>(Technical Report Series; 949)</comment>
            </element-citation>
        </ref>
    </ref-list>
    ...


.. _elemento-element-citation-exemplo-7:

7. Relatório 2
--------------

.. code-block:: xml

    <!-- Report Sample -->

    ...
    <ref-list>
        <ref id="B1">
            <mixed-citation>Water HP, Boshuizen HC, Perenboom RJ. Health expectancy of the Dutch population. Bilthoven (Netherlands): National Institute of Public Health and Environmental Protection (NL); 1995. 21 p. Report No.: 431501009</mixed-citation>
            <element-citation publication-type="report">
                <person-group person-group-type="author">
                    <name>
                        <surname>Water</surname>
                        <given-names>HP</given-names>
                    </name>
                    <name>
                        <surname>Boshuizen</surname>
                        <given-names>HC</given-names>
                    </name>
                    <name>
                        <surname>Perenboom</surname>
                        <given-names>RJ</given-names>
                    </name>
                </person-group>
                <source>Health expectancy of the Dutch population</source>
                <publisher-loc>Bilthoven (Netherlands)</publisher-loc>
                <publisher-name>National Institute of Public Health and Environmental Protection (NL)</publisher-name>
                <year>1995</year>
                <size units="pages">21</size>
                <pub-id pub-id-type="other">Report No.: 431501009</pub-id>
            </element-citation>
        </ref>
    </ref-list>
    ...

.. note:: Para referências que apresentam informações de coleção ou série, ex.: "Technical Report Series; 949", identifica-se com o elemento ``<comment>``. Não deve ser confundido com referência bibliográfica do tipo "report", que apresenta número de relatório (Report No.: 431501009). Nesses casos se referencia com o elemento ``<pub-id pub-id-type="other">``.


.. _elemento-element-citation-exemplo-8:

8. Conferência 1
----------------

.. code-block:: xml

    <!-- Confproc (proceedings) Sample -->

    ...
    <ref-list>
        <ref id="B06">
            <label>6</label>
            <mixed-citation>World Health Organization (WHO). Ultrasound in schistosomiasis. A pratical guide to the standardized use of ultrasonography for the assessment of schistosomiasis-related morbidity. Second International Workshop. 22 October, 1996, Niamey, Niger.</mixed-citation>
            <element-citation publication-type="confproc">
                <person-group person-group-type="author">
                    <collab>World Health Organization (WHO)</collab>
                </person-group>
                <source>Ultrasound in schistosomiasis. A pratical guide to the standardized use of ultrasonography for the assessment of schistosomiasis-related morbidity</source>
                <comment>Second International Workshop</comment>
                <day>22</day>
                <month>10</month>
                <publisher-loc>Niamey, Niger</publisher-loc>
                <year>1996</year>
            </element-citation>
        </ref>
    </ref-list>
    ...


.. _elemento-element-citation-exemplo-9:

9. Conferência 2
----------------

.. code-block:: xml

    <!-- Confproc (proceedings) Sample -->

    ...
    <ref id="B42">
        <label>42</label>
        <mixed-citation>Kornilaki, E., &amp; Nunes, T. (1997). What do young children understand about division? In Proceedings of the 21th Annual International Conference of Psychology of Mathematics Education. Lahti, Finland: University of Helsinki.
        </mixed-citation>
        <element-citation publication-type="confproc">
          <person-group person-group-type="author">
            <name>
              <surname>Kornilaki</surname>
              <given-names>E.</given-names>
            </name>
            <name>
              <surname>Nunes</surname>
              <given-names>T.</given-names>
            </name>
          </person-group>
          <year>1997</year>
          <source>What do young children understand about division?</source>
          <conf-name>Proceedings of the 21th Annual International Conference of Psychology of Mathematics Education</conf-name>
          <conf-loc>Lahti, Finland</conf-loc>
          <publisher-name>University of Helsinki</publisher-name>
        </element-citation>
      </ref>
      ...


.. _elemento-element-citation-exemplo-10:

10. Dissertação
---------------

.. code-block:: xml

    <!-- Thesis Sample -->

    ...
    <ref-list>
        <ref id="B07">
            <label>7</label>
            <mixed-citation>Milani RM. Análise dos resultados imediatos da operação para revascularização do miocárdio sem pinçamento total da aorta [Dissertação de mestrado]. Curitiba: Universidade Federal do Paraná; 2000.</mixed-citation>
            <element-citation publication-type="thesis">
                <person-group person-group-type="author">
                    <name>
                        <surname>Milani</surname>
                        <given-names>RM</given-names>
                    </name>
                </person-group>
                <source>Análise dos resultados imediatos da operação para revascularização do miocárdio sem pinçamento total da aorta</source>
                <comment>Dissertação de mestrado</comment>
                <publisher-loc>Curitiba</publisher-loc>
                <publisher-name>Universidade Federal do Paraná</publisher-name>
                <year>2000</year>
            </element-citation>
        </ref>
    </ref-list>
    ...


.. _elemento-element-citation-exemplo-11:

11. Patente
-----------

.. code-block:: xml

    <!-- Patent Sample -->

    ...
    <ref-list>
        <ref id="B08">
            <label>8</label>
            <mixed-citation>EMBRAPA. Medidor digital multissensor de temperatura para solos. BR n. PI 8903105-9, 30 maio 1995.</mixed-citation>
            <element-citation publication-type="patent">
                <person-group person-group-type="author">
                    <collab>EMBRAPA</collab>
                </person-group>
                <source>Medidor digital multissensor de temperatura para solos</source>
                <patent country="BR">PI 8903105-9</patent>
                <day>30</day>
                <month>05</month>
                <year>1995</year>
            </element-citation>
        </ref>
    </ref-list>
    ...


.. _elemento-element-citation-exemplo-12:

12. Software
------------

.. code-block:: xml

    <!-- Software Sample -->

    ...
    <ref-list>
        <ref id="B09">
            <label>9</label>
            <mixed-citation>MICROSOFT. Project for Windows 95: project planning software. Version 4.1. [S.l.]: Microsoft Corporation, 1995. 1 CD-ROM.</mixed-citation>
            <element-citation publication-type="software">
                <person-group person-group-type="editor">
                    <collab>MICROSOFT</collab>
                </person-group>
                <source>Project for Windows 95: project planning software</source>
                <edition>Version 4.1</edition>
                <publisher-name>Microsoft Corporation</publisher-name>
                <year>1995</year>
                <comment>1 CD-ROM</comment>
            </element-citation>
        </ref>
    <ref-list>
    ...


.. _elemento-element-citation-exemplo-13:

13. Base de dados
-----------------

.. code-block:: xml

    <!-- Database Sample -->

    ...
    <ref-list>
        <ref id="B10">
            <label>10</label>
            <mixed-citation>FUNDAÇÃO TROPICAL DE PESQUISAS E TECNOLOGIA "ANDRÉ TOSELLO". Base de Dados Tropical. 1985. Disponível em: &lt;http://www.bdt.fat.org.br/acaro/sp/&gt;. Acesso em: 30 maio 2002.</mixed-citation>
            <element-citation publication-type="database">
                <person-group person-group-type="author">
                    <collab>FUNDAÇÃO TROPICAL DE PESQUISAS E TECNOLOGIA "ANDRÉ TOSELLO"</collab>
                </person-group>
                <source>Base de Dados Tropical</source>
                <year>1985</year>
                <comment>Disponível em: <ext-link ext-link-type="uri" xlink:href="http://www.bdt.fat.org.br/acaro/sp/">http://www.bdt.fat.org.br/acaro/sp/</ext-link></comment>
                <date-in-citation content-type="access-date">30 maio 2002</date-in-citation>
            </element-citation>
        </ref>
    </ref-list>
    ...

.. _elemento-element-citation-exemplo-14:

14. Dados de Pesquisa 1
------------------------

.. code-block:: xml

    <!-- Data Sample -->

    <ref id="B01">
        <label>1</label>
            <element-citation publication-type="data">
                <person-group person-group-type="author">
                    <name>
                        <surname>ANDRADE</surname>
                        <given-names>Márcio</given-names>
                    </name>                        
                </person-group>                      
                <data-title>Estudos de genes em ratos albinos na América Latina</data-title>
                <version>20 jan.</version>
                <year>2018</year>
                <source>Open Science Framework</source>
                <pub-id pub-id-type="art-access-id">NR 109833.1</pub-id>
                <pub-id pub-id-type="doi">10.1590/0123-45620187214</pub-id>
            </element-citation>
    </ref>

.. _elemento-element-citation-exemplo-15:

15. Dados de Pesquisa 2
------------------------

.. code-block:: xml

    <!-- Data Sample -->

    <ref id="B02">
        <label>2</label>
            <element-citation publication-type="data">
                <person-group person-group-type="author">
                    <collab>BEILSTEIN INSTITUIT</collab>                        
                </person-group>                   
                <data-title>Estudos de genes em ratos albinos na América Latina</data-title>
                <version>23 jan.</version>
                <year>2018</year>
                <source>Open Science Framework</source>
                <pub-id pub-id-type="art-access-id">NR 109833.1</pub-id>
                <pub-id pub-id-type="doi">10.1590/0123-45620187214</pub-id>
            </element-citation>
    </ref>


.. _elemento-element-citation-exemplo-16:

16. Dados de Pesquisa 3
------------------------

.. code-block:: xml

    <!-- Data Sample -->

    <ref id="B03">
        <label>3</label>
            <element-citation publication-type="data">
                <person-group person-group-type="author">
                    <name>
                        <surname>ANDRADE</surname>
                        <given-names>Márcio</given-names>
                    </name>                        
                    </person-group>                   
                    <data-title>Estudos de genes em ratos albinos na América Latina</data-title>            
                    <year>2018</year>
                    <source>OSF</source>                    
                    <ext-link ext-link-type="uri" xlink:href="https://osf.io/">https://osf.io/</ext-link>
            </element-citation>
    </ref>


..note:: Para mais informações consulte `Guia de citação de dados de pesquisa SciELO <http://www.scielo.org/local/File/Guia_de_citacao_de_dados.pdf>`_ e `Data citation da JATS4R <http://jats4r.org/data-citations>`_



.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
