.. _elemento-day:

<day>
=====

+----------------------------------+-----------------+
| Aparece em                       | Ocorre          |
+==================================+=================+
| :ref:`elemento-pub-date`         | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-product`          | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-element-citation` | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-date-in-citation` | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-date`             | Zero ou uma vez |
+----------------------------------+-----------------+



Identifica o dia de acesso ao conteúdo web relativo a uma referência, podendo ser utilizado para compor a data de publicação e/ou a data de histórico.

o elemento contém valor de até 2 dígitos, sendo aceito zero não significativo à esquerda.

Exemplo:

.. code-block:: xml

    ...
    <day>12</day>
    ...

.. note:: Este elemento é obrigatório em :ref:`elemento-pub-date` com atributo ``@date-type`` com valor "pub" e em em :ref:`elemento-date` com atributo ``@date-type`` com valor "received" e "accepted".


.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
