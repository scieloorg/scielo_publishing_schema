.. _elemento-back:

<back>
======

+-----------------------------+-----------------+
| Aparece em                  | Ocorre          |
+=============================+=================+
| :ref:`elemento-article`     | Zero ou uma vez |
+-----------------------------+-----------------+
| :ref:`elemento-response`    | Zero ou uma vez |
+-----------------------------+-----------------+
| :ref:`elemento-sub-article` | Zero ou uma vez |
+-----------------------------+-----------------+


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
                <label>Appendix 1</label>
                <p>Para mais informações <ext-link ext-link-type="uri" xlink:href="https://www.scielo.org">clique aqui</ext-link> para verificar o pdf.</p>
             </app>
        </app-group>
   </back>
   ...



.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
