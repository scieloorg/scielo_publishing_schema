.. _elemento-back:

<back>
======

Aparece em:

  :ref:`elemento-article`
  :ref:`elemento-response`
  :ref:`elemento-sub-article`

Ocorre:

  Zero ou uma vez

Parte final do :term:`documento` que compreende:


+----------------------+--------------------------+
| Itens                | Elementos                |
+======================+==========================+
| lista de referências | :ref:`elemento-ref-list` |
+----------------------+--------------------------+
| notas gerais         | :ref:`elemento-fn-group` |
+----------------------+--------------------------+
| agradecimento        | :ref:`elemento-ack`      |
+----------------------+--------------------------+
| apêndice             | ``app-group``            |
+----------------------+--------------------------+
| material suplementar | ``app-group``            |
+----------------------+--------------------------+
| anexo                | ``app-group``            |
+----------------------+--------------------------+
| glossário            | :ref:`elemento-glossary` |
+----------------------+--------------------------+


Exemplo:

.. code-block:: xml

   ...
   <back>
        <ref-list>
             <title>References</title>
             <ref id="B1">
             <mixed-citation>Associação Brasileira das Indústrias Exportadoras de Carnes. (2012, fevereiro 29). [Entrevista com o Antônio Camardelli]. Presidente da ABIEC. Retrieved from http://www.abiec.com.br/noticia.asp?id=779#.Uj8VnWt5mSM  </mixed-citation>
             <element-citation publication-type="book">
                  <person-group person-group-type="author">
                       <collab>Associação Brasileira das Indústrias Exportadoras de Carnes</collab>
                  </person-group>
                  <year>2012,</year>
                  <source>[Entrevista com o Antônio Camardelli]. Presidente da ABIEC</source>
                  <ext-link ext-link-type="uri" xlink:href="http://www.abiec.com.br/noticia.asp?id=779#.Uj8VnWt5mSM">http://www.abiec.com.br/noticia.asp?id=779#.Uj8VnWt5mSM</ext-link>
             </element-citation>
             </ref>
             <ref id="B2">
                  <mixed-citation>Blumentritt, T. P. (2003). Foreign subsidiaries' government affairs activities. Business &amp; Society, 42(2), 202-233. doi: 10.1177/0007650303042002003</mixed-citation>
                  <element-citation publication-type="journal">
                       <person-group person-group-type="author">
                            <name>
                                <surname>Blumentritt</surname>
                                <given-names>T. P.</given-names>
                            </name>
                       </person-group>
                       <year>2003</year>
                       <article-title>Foreign subsidiaries' government affairs activities</article-title>
                       <source>Business &amp; Society</source>
                       <volume>42</volume>
                       <issue>2</issue>
                       <fpage>202</fpage>
                       <lpage>233</lpage>
                       <pub-id pub-id-type="doi">10.1177/0007650303042002003</pub-id>
                  </element-citation>
             </ref>
           ...
        </ref-list>
        <app-group>
             <app id="app1">
                  <label>ANNEX A</label>
                  <table-wrap id="t6">
                       <label>Table 6</label>
                       <caption>
                            <title>Multivariate analysis of risk factors associated with readmission - Model 2</title>
                       </caption>
                       <graphic xlink:href="1234-5678-rctb-45-05-0110-gt031.tif"/>
                  </table-wrap>
             </app>
        </app-group>
   </back>
   ...



.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
