.. _elemento-page-range:

<page-range>
^^^^^^^^^^^^

Aparece em
  :ref:`elemento-product`,
  :ref:`elemento-element-citation`
  
Ocorre 
  Zero ou uma vez


Identifica um intervalo de paginação mencionados numa referência.

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

.. note:: A inserção do intervalo de paginação deve ser inserido após à
          informação de última página :ref:`elemento-lpage`.

