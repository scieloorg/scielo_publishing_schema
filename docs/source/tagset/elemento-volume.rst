.. _elemento-volume:

<volume>
--------

Aparece em:

  :ref:`elemento-article-meta`
  :ref:`elemento-element-citation`

Ocorre:

  1. Zero ou uma vez em :ref:`elemento-front`
  2. Zero ou mais vezes em :ref:`elemento-back`


Representa o volume de uma publicação.

Caso haja suplemento de volume, este deve ser identificado em :ref:`elemento-issue` em :ref:`elemento-front`.

.. note:: ``<volume>`` deve ocorrer depois de :ref:`elemento-pub-date` ou antes de :ref:`elemento-issue`.


Exemplo ``v10s1``:

.. code-block:: xml

    ...
    <front>
        ...
        <article-meta>
            ...
            <volume>10</volume>
            <issue>suppl 1</issue>
            ...
        </article-meta>
        ...
    </front>
    ...


.. {"reviewed_on": "20160803", "by": "gandhalf_thewhite@hotmail.com"}
