.. _elemento-edition:

<edition>
^^^^^^^^^

Aparece em:

  :ref:`elemento-product`
  :ref:`elemento-element-citation`

Ocorre:

  Zero ou mais vezes

Identifica o número da edição de um documento em uma referência (``<element-citation>``). Pode também conter a versão de um software ou base de dados (``<product>``).

Exemplo 1:

.. code-block:: xml

   ...
   <element-citation>
      ...
      <source>Ce qui nos relie</source>
      <edition>Editon de l'Aube</edition>
      <publisher-loc>La Tour d'Aigues</publisher-loc>
      <fpage>189</fpage>
      <lpage>208</lpage>
   </element-citation>
   ...


Exemplo 2:

.. code-block:: xml

   ...
   <element-citation>
      ...
      <publisher-name>Springer</publisher-name>
      <edition>2nd</edition>
      <publisher-loc>Dordrecht, The Netherlands</publisher-loc>
      <fpage>436</fpage>
   </element-citation>
   ...


.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
