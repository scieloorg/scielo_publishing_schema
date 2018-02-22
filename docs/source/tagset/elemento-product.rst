.. _elemento-product:

<product>
=========

Atributos obrigatórios:

  1. ``@product-type``

+------------------------------+--------------------+
| Aparece em                   | Ocorre             |
+==============================+====================+
| :ref:`elemento-article-meta` | Zero ou mais vezes |
+------------------------------+--------------------+



``<product>`` contém informações do produto resenhado, mas somente deverá ser utilizado quando :ref:`elemento-article` possuir o atributo ``@article-type="book-review"``. O conteúdo de ``<product>`` deverá conter conteúdo dissertativo, incluindo separadores conforme o exemplo abaixo:


.. _elemento-product-exemplo-1:

Exemplo de marcação de ``<product>`` de livro
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: xml

    ...
    <article-meta>
        ...
        <product product-type="book">
            <person-group person-group-type="author">
                <name>
                    <surname>ONFRAY</surname> 
                    <given-names>Michel</given-names>
                </name>
            </person-group>. 
            <source>La comunidad filosófica: manifiesto por una universidad popular</source> Trad. e notas de 
            <person-group person-group-type="translator">
                <name>
                    <surname>Castro</surname> 
                    <given-names>Antonia García</given-names>
                </name>
            </person-group>. 
            <publisher-loc>Barcelona</publisher-loc>: 
            <publisher-name>Gedisa</publisher-name>, 
            <year>2008</year> 
            <size units="pages">155</size>p.
        </product>
        <history>
            ...
        </history>
        ...
    </article-meta>
    ...


Os valores possíveis para ``@product-type`` são:

+-----------+---------------------------------+
| Valor     | Descrição                       |
+===========+=================================+
| book      | para livro ou capítulo de livro |
+-----------+---------------------------------+
| other     | outros tipos                    |
+-----------+---------------------------------+


.. note:: A ordem dos elementos é importante! ``<product>`` deve ser inserido antes de :ref:`elemento-history` ou depois de :ref:`elemento-fpage`.


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
