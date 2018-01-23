.. _elemento-edition:

<edition>
=========

+----------------------------------+--------------------+
| Aparece em                       | Ocorre             |
+==================================+====================+
| :ref:`elemento-product`          | Zero ou mais vezes |
+----------------------------------+--------------------+
| :ref:`elemento-element-citation` | Zero ou mais vezes |
+----------------------------------+--------------------+


Identifica a edição de um documento em uma referência.

Exemplos:

  * :ref:`elemento-edition-exemplo-1`
  * :ref:`elemento-edition-exemplo-2`


.. _elemento-edition-exemplo-1:

Exemplo de ``<edition>`` envolvendo texto:
------------------------------------------

.. code-block:: xml

   ...
   <element-citation publication-type="book">
      ...
      <source>Ce qui nos relie</source>
      <edition>Editon de l'Aube</edition>
      <publisher-loc>La Tour d'Aigues</publisher-loc>
      <fpage>189</fpage>
      <lpage>208</lpage>
   </element-citation>
   ...


.. _elemento-edition-exemplo-2:

Exemplo de ``<edition>`` envolvendo número:
-------------------------------------------

.. code-block:: xml

   ...
   <element-citation publication-type="book">
      ...
      <publisher-name>Springer</publisher-name>
      <edition>2nd</edition>
      <publisher-loc>Dordrecht, The Netherlands</publisher-loc>
      <fpage>436</fpage>
   </element-citation>
   ...


.. {"reviewed_on": "20170904", "by": "carolina.tanigushi@scielo.org"}