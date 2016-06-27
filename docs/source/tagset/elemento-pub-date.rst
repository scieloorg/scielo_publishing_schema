.. _elemento-pub-date:

<pub-date>
----------

Aparece em:

  :ref:`elemento-article-meta`

Atributos obrigatórios:

  1. ``@pub-type='epub'`` ou ``@pub-type='epub-ppub'``

Ocorre:

  Uma vez


A data de publicação do artigo/número utiliza o elemento ``<pub-date>``, o qual pode conter os elementos :ref:`elemento-day`, :ref:`elemento-month`, :ref:`elemento-season` e, obrigatoriamente, :ref:`elemento-year` que deve estar acompanhada do atributo ``@pub-type``.

``@pub-type`` pode ser ``epub-ppub`` se houver uma versão impressa do número ou apenas ``epub`` para publicação digital ou em ``ahead-of-print``.

Exemplo de marcação de data de publicação nas versões impressa e digital:

.. code-block:: xml

    ...
    <article-meta>
        ...
        <pub-date pub-type="epub-ppub">
            <season>Jan-Feb</season>
            <year>2014</year>
        </pub-date>
        ...
    </article-meta>
    ...


Os valores de dia, mês e ano devem ser representados de acordo com a data de publicação do número, geralmente constante no sumário.

Exemplo de marcação de data de publicação na versão digital:

.. code-block:: xml

    ...
    <article-meta>
        ...
        <pub-date pub-type="epub">
            <day>17</day>
            <month>03</month>
            <year>2014</year>
        </pub-date>
        ...
    </article-meta>
    ...


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
