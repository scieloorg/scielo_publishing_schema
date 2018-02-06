.. _elemento-day:

<day>
=====

+----------------------------------+-------------------------------------------------------------+
| Aparece em                       | Ocorre                                                      |
+==================================+=============================================================+
| :ref:`elemento-pub-date`         | 1. Zero ou uma vez nos elementos de :ref:`elemento-front`   |
+----------------------------------+-------------------------------------------------------------+
| :ref:`elemento-product`          | 2. Zero ou uma vez nos elementos de :ref:`elemento-back`    |
+----------------------------------+-------------------------------------------------------------+
| :ref:`elemento-element-citation` | 1. Zero ou uma vez nos elementos de :ref:`elemento-front`   |
+----------------------------------+-------------------------------------------------------------+
| :ref:`elemento-date-in-citation` | 1. Zero ou uma vez nos elementos de :ref:`elemento-front`   |
+----------------------------------+-------------------------------------------------------------+
| :ref:`elemento-date`             | 1. Zero ou uma vez nos elementos de :ref:`elemento-front`   |
+----------------------------------+-------------------------------------------------------------+



Identifica o dia de acesso ao conteúdo web relativo a uma referência, podendo ser utilizado para compor a data de publicação e/ou a data de histórico.

o elemento contém valor de até 2 dígitos, sendo aceito zero não significativo à esquerda.

Exemplo:

.. code-block:: xml

    ...
    <day>12</day>
    ...


.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
