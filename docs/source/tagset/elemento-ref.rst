.. _elemento-ref:

<ref>
=====

Aparece em:

  :ref:`elemento-ref-list`

Atributos obrigatórios:

  1. ``@id`` (ver :ref:`sugestao-atribuicao-id`)

Ocorre:

  Uma ou mais vezes


O elemento é exclusivo para identificar referências em qualquer norma, e descreve livros, periódicos, conferências etc.


Exemplo:

.. code-block:: xml

    ...
    <ref-list>
        <title>Referências</title>
        <ref id="B1">
            <label>1</label>
            <mixed-citation>. Aires M, Paz AA, Perosa CT. Situação de saúde e grau de dependência de pessoas idosas institucionalizadas. <italic>Rev Gaucha Enferm.</italic> 2009;30(3):192-9.</mixed-citation>
            <element-citation publication-type="journal">
                <person-group person-group-type="author">
                    <name>
                        <surname>Aires</surname>
                        <given-names>M</given-names>
                    </name>
                    <name>
                        <surname>Paz</surname>
                        <given-names>AA</given-names>
                    </name>
                    <name>
                        <surname>Perosa</surname>
                        <given-names>CT</given-names>
                    </name>
                </person-group>
                <article-title>Situação de saúde e grau de dependência de pessoas idosas institucionalizadas</article-title>
                <source>Rev Gaucha Enferm</source>
                <year>2009</year>
                <volume>30</volume>
                <issue>3</issue>
                <fpage>192</fpage>
                <lpage>199</lpage>
            </element-citation>
        </ref>
        ...
    </ref-list>
    ...


.. {"reviewed_on": "20160729", "by": "gandhalf_thewhite@hotmail.com"}
