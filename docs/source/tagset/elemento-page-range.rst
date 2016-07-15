.. _elemento-page-range:

<page-range>
============

Aparece em:

  :ref:`elemento-product`
  :ref:`elemento-element-citation`

Ocorre:

  Zero ou uma vez

Identifica um ou mais sub-intervalos de paginação contidos entre os valores de :ref:`elemento-fpage` e :ref:`elemento-lpage` em uma referência bibliográfica. Cada sub-intervalo pode ser composto de um valor numérico (denotando uma página simples) ou dois valores numéricos separados por hífen (indicando um intervalo de páginas). Sub-intervalos são separados por vírgula.

Exemplo:

.. code-block:: xml

    ...
    <ref>
        <element-citation publication-type="book">
            ...
            <fpage>300</fpage>
            <lpage>420</lpage>
            <page-range>300-301, 305, 407-420</page-range>
            ...
        </element-citation>
        ...
    </ref>
    ...

.. note:: A inserção do intervalo de paginação deve ocorrer após a informação de última página (:ref:`elemento-lpage`).


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
