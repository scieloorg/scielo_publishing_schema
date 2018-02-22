.. _elemento-patent:

<patent>
========

Atributos obrigatórios:

  1. ``@country``

+----------------------------------+-----------------+
| Aparece em                       | Ocorre          |
+==================================+=================+
| :ref:`elemento-element-citation` | Zero ou uma vez |
+----------------------------------+-----------------+


Identifica um número de patente. Deve ter o atributo ``@country`` contendo o código de país de acordo com a norma :term:`ISO 3166`, com dois caracteres alfabéticos.

Os códigos de país podem ser consultados na página da `norma ISO 3166 <https://www.iso.org/obp/ui/#iso:pub:PUB500001:en>`_.

Exemplo de patente americana:

.. code-block:: xml

    ...
    <element-citation>
        <patent country="US">US 6,980,855</patent>
    </element-citation>
    ...


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
