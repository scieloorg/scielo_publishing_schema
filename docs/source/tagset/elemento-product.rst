.. _elemento-product:

<product>
=========

Este elemento possui :ref:`scielo-brasil`


Atributos obrigatórios:

  1. ``@product-type``

+------------------------------+--------------------+
| Aparece em                   | Ocorre             |
+==============================+====================+
| :ref:`elemento-article-meta` | Zero ou mais vezes |
+------------------------------+--------------------+



O elemento serve para marcação relativa a um produto (por exemplo: um livro, software, site ou componente de hardware) discutido em um artigo. O conteúdo de ``<product>`` deverá ser dissertativo, incluindo separadores conforme o exemplo abaixo:


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
        </person-group>
        <source>La comunidad filosófica: manifiesto por una universidad popular</source>
        <person-group person-group-type="translator">
            <name>
                <surname>Castro</surname>
                <given-names>Antonia García</given-names>
            </name>
        </person-group>
        <publisher-loc>Barcelona</publisher-loc>
        <publisher-name>Gedisa</publisher-name>
        <year>2008</year>
        <size units="pages">155</size>
        <isbn>78-84-9784-252-5</isbn>
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
| book      | livro ou capítulo de livro      |
+-----------+---------------------------------+
| article   | artigo                          |
+-----------+---------------------------------+
| issue     | fascículo                       |
+-----------+---------------------------------+
| website   | site ou blog                    |
+-----------+---------------------------------+
| film      | filme                           |
+-----------+---------------------------------+
| software  | programa de computador          |
+-----------+---------------------------------+
| hardware  | componente físico de computador |
+-----------+---------------------------------+
| other     | outros tipos                    |
+-----------+---------------------------------+



.. note:: A ordem dos elementos é importante! ``<product>`` deve ser inserido antes de :ref:`elemento-history` ou depois de :ref:`elemento-fpage`.



