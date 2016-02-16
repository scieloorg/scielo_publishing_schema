.. _elemento-pub-date:

<pub-date>
----------

Aparece em
  :ref:`elemento-article-meta`
 
Atributos obrigatórios
  1. pub-type='epub' ou pub-type='epub-ppub'
 
Ocorre
  Uma vez


Para a marcação da data de publicação do artigo/número utiliza-se a 
tag ``<pub-date>`` a qual pode conter os elementos :ref:`elemento-day`, 
:ref:`elemento-month`, :ref:`elemento-season` e obrigatoriamente 
:ref:`elemento-year`. Esta tag deve estar acompanhada do atributo ``@pub-type``.
 
A data de publicação pode ser do tipo ``epub-ppub`` se houver uma versão 
impressa do número, apenas ``epub`` para publicação digital ou em 
``ahead-of-print``.
 
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

 
Os valores de dia, mês e ano devem ser representados segundo a data de 
publicação do número, que geralmente consta no sumário.
 
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
 
