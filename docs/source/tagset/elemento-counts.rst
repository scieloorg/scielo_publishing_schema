.. _elemento-counts:

<counts>
--------

Aparece em
  :ref:`elemento-article-meta`
 
Ocorre
  Zero ou uma vez


Na elaboração do XML alguns dados são importantes para determinar a 
quantidade de elementos presentes no artigo, por isso utiliza-se a tag 
``<counts>`` para contabilizar o número exato de tabelas, figuras, 
referências, equações e páginas presentes no arquivo. Esta tag deve ser 
inserida como último item de :ref:`elemento-article-meta`.

 
Os elementos que identificam os totais são:

* ``<fig-count>``: Total de figuras no :term:`documento`
* ``<table-count>``: Total de tabelas no documento
* ``<equation-count>``: Total de equações do documento
* ``<ref-count>``: Total de referências no documento
* ``<page-count>``: Total de páginas do artigo
 
Exemplo:

.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <counts>
            <fig-count count="5"/>
            <table-count count="3"/>
            <equation-count count="10"/>
            <ref-count count="26"/>
            <page-count count="6"/>
        </counts>
    </article-meta>
    ...
 
.. note:: A ordem dos elementos é importante.
          No caso de o :term:`documento` não apresentar alguns dos elementos contabilizados,
          o valor dos respectivos atributos ``@count`` deve ser ``0``. e.g.
          ``<equation-count count="0"/>``.

.. note:: No caso de haver :ref:`elemento-article` e :ref:`elemento-sub-article`, 
          deve-se contabilizar o total de elementos em ambos.
