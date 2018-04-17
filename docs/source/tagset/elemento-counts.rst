.. _elemento-counts:

<counts>
========

+------------------------------+-----------------+
| Aparece em                   | Ocorre          |
+==============================+=================+
| :ref:`elemento-article-meta` | Zero ou uma vez |
+------------------------------+-----------------+


Elemento utilizado para contabilizar o número exato de tabelas, figuras, referências, equações e páginas presentes no documento. Deve ser inserido como último item de :ref:`elemento-article-meta`.

Os elementos que identificam os totais no :term:`documento` são:

* ``<fig-count>``: Total de figuras
* ``<table-count>``: Total de tabelas
* ``<equation-count>``: Total de equações
* ``<ref-count>``: Total de referências
* ``<page-count>``: Total de páginas

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

.. note:: 
 * A ordem dos elementos é importante. 
 * Caso o :term:`documento` não apresente algum dos elementos contabilizados, deve-se retirar o elemento de ``<counts>``. 
 * No caso de haver :ref:`elemento-sub-article` e/ou :ref:`elemento-response`, deve-se contabilizar o total de elementos em ambos.


.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
