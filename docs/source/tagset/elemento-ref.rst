.. _elemento-ref:

<ref>
-----

Aparece em:

  :ref:`elemento-ref-list`

Atributos obrigatórios:

  1. ``@id`` (ver :ref:`sugestao-atribuicao-id`)

Ocorre:

  Uma ou mais vezes


Há diversos tipos de referências e normas para apresentá-las num documento textual (:term:`ABNT`, :term:`Vancouver`, :term:`APA`, :term:`ISO` e ``OTHER``). Independente da norma utilizada, a representação dos elementos essenciais de uma referência em XML devem ser identificados corretamente.


Exemplo:

.. code-block:: xml

    ...
    <ref-list>
        <title></title>
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

.. {"reviewed_on": "20160628", "by": "gandhalf_thewhite@hotmail.com"}
