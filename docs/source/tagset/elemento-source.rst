.. _elemento-source:

<source>
========

+----------------------------------+-----------------+
| Aparece em                       | Ocorre          |
+==================================+=================+
| :ref:`elemento-element-citation` | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-product`          | Zero ou uma vez |
+----------------------------------+-----------------+


Identifica o título da fonte principal de uma referência ou de um produto. O atributo ``@xml:lang`` não deve ser utilizado.

Exemplo:

.. code-block:: xml

    ...
    <element-citation publication-type="journal">
              ...
         <article-title>The consequences of childhood overweight and obesity</article-title>
         <source>Future Child</source>
         <year>2006</year>
              ...
    </element-citation>
    ...


.. {"reviewed_on": "20160629", "by": "gandhalf_thewhite@hotmail.com"}
