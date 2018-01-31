.. _elemento-volume:

<volume>
========

+----------------------------------+-----------------+
| Aparece em                       | Ocorre          |
+==================================+=================+
| :ref:`elemento-article-meta`     | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-element-citation` | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-product`          | Zero ou uma vez |
+----------------------------------+-----------------+



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
