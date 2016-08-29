.. _elemento-product:

<product>
=========

Aparece em:

  :ref:`elemento-article-meta`

Atributos obrigatórios:

  1. ``@product-type``

Ocorre:

  Zero ou mais vezes


``<product>`` contém informações do produto resenhado, mas somente deverá ser utilizado quando :ref:`elemento-article` possuir o atributo ``@article-type="book-review"``.
O conteúdo de ``<product>`` deverá ser detalhado apenas quando a referenciar um tipo livro. Caso contrário, fica desnecessário detalhar seu conteúdo.

Exemplos:

    * :ref:`elemento-product-exemplo-1`
    * :ref:`elemento-product-exemplo-2`
    * :ref:`elemento-product-exemplo-3`


Os valores possíveis para ``@product-type`` são:

+-----------+---------------------------------+
| Valor     | Descrição                       |
+===========+=================================+
| book      | referência de livro             |
+-----------+---------------------------------+
| other     | outros tipos                    |
+-----------+---------------------------------+


.. _elemento-product-exemplo-1:

Exemplo de marcação de ``<product>`` do tipo "book"
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

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
            <year>2008</year>
            <publisher-name>Gedisa</publisher-name>
            <publisher-loc>Barcelona</publisher-loc>
            <size units="pages">155</size>
            <isbn>9788497842525</isbn>
            <inline-graphic xlink:href="1234-5678-rctb-45-05-690-gf01.tif"/>
        </product>
        <history>
            ...
        </history>
        ...
    </article-meta>
    ...


.. _elemento-product-exemplo-2:

Exemplo de marcação de ``<product>`` de capítulo de livro
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: xml

    ...
    <article-meta>
        ...
        <product>
            <person-group person-group-type="author">
                <name>
                    <surname>RUMAQUELLA</surname>
                    <given-names>M.</given-names>
                </name>
                <etal/>
            </person-group>
            <chapter-title>Os efeitos da postura sentada na coluna vertebral: uma revisão</chapter-title>
            <source>Anais do 8º Congresso Brasileiro de Pesquisa e Desenvolvimento em Design</source>
            <fpage>4142</fpage>
            <lpage>4146</lpage>
            <year>2008</year>
        </product>
        ...
    </article-meta>
    ...


.. _elemento-product-exemplo-3:

Exemplo de marcação de ``<product>`` com tipo diferente de "book"
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

.. code-block:: xml

    ...
    <product product-type="other">
        GINO. A.S. Um estudo sobre as contribuições de um curso de formação continuada a partir das narrativas de professoras que ensinam matemática (2013), 254 f. Tese (Doutorado em Educação) Faculdade de Educação, Universidade Federal de Minas Gerais - Belo Horizonte. 2013
    </product>
    ...



.. note:: A ordem dos elementos é importante! ``<product>`` deve ser inserido antes de :ref:`elemento-history` ou depois de :ref:`elemento-fpage`.


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
