.. _elemento-pub-date:

<pub-date>
==========

Aparece em:

  :ref:`elemento-article-meta`

Atributos obrigatórios:

  1. ``@pub-type``

Ocorre:

  Uma vez


A data de publicação do artigo/número utiliza o elemento ``<pub-date>``, o qual pode conter os elementos :ref:`elemento-day`, :ref:`elemento-month`, :ref:`elemento-season` e, obrigatoriamente, :ref:`elemento-year`.

``<pub-date>`` deve estar acompanhada do atributo ``@pub-type``, que pode ser ``epub-ppub`` se houver uma versão impressa do número ou apenas ``epub`` quando: a. for apenas publicação online; b. quando se tratar de um documento *Rolling Pass* ou c. em caso de ser modalidade :term:`ahead of print`.


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

.. code-block:: xml

    ...
    <article-meta>
        ...
        <pub-date pub-type="epub-ppub">
            <day>21</day>
            <month>07</month>
            <year>2016</year>
        </pub-date>
        ...
    </article-meta>
    ...


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


.. {"reviewed_on": "20160803", "by": "gandhalf_thewhite@hotmail.com"}
