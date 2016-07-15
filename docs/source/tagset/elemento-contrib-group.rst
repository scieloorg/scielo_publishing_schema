.. _elemento-contrib-group:

<contrib-group>
===============

Aparece em:

  :ref:`elemento-article-meta`

Ocorre:

  Uma vez

Contém o grupo de elementos relativos à contribuição na elaboração do artigo. Os contribuintes mais frequentes são os autores pessoais, instituições e grupos de pesquisa.

Os principais elementos de ``<contrib-group>`` são:

* :ref:`elemento-contrib`;
* :ref:`elemento-xref`;
* :ref:`elemento-collab`;
* :ref:`elemento-aff`; e
* :ref:`elemento-role`.

Exemplo:

.. code-block:: xml

    ...
    <contrib-group>
        <contrib contrib-type="author">
            <contrib-id contrib-id-type="orcid">0000-0001-8528-2091</contrib-id>
            <contrib-id contrib-id-type="scopus">24771926600</contrib-id>
            <name>
                <surname>Einstein</surname>
                <given-names>Albert</given-names>
            </name>
            ...
        </contrib>
        <contrib contrib-type="author">
            <contrib-id contrib-id-type="lattes">4760273612238540</contrib-id>
            <name>
                <surname>Meneghini</surname>
                <given-names>Rogerio</given-names>
            </name>
            ...
        </contrib>
        ...
    </contrib-group>
    ...


.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
