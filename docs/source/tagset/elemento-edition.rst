.. _elemento-edition:

<edition>
^^^^^^^^^

Aparece em:

  :ref:`elemento-product`
  :ref:`elemento-element-citation`

Ocorre:

  Zero ou mais vezes

Identifica o número da edição de um documento em uma referência, mas também pode indicar a versão de um software ou base de dados.

Exemplo 1:

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


Exemplo 3:

.. code-block:: xml

   ...
   <element-citation publication-type="database">
        <source>DialogWeb [Internet]</source>
        <edition>Version 2.5</edition>
        <publisher-loc>Cary (NC)</publisher-loc>
        <publisher-name>The Dialog Corporation</publisher-name>
        <year>c1997 -  </year>
        <date-in-citation>cited 2007 Feb 1</date-in-citation>
        <comment>Available from:
        <ext-link ext-link-type="uri" xlink:href="http://www.dialogweb.com/">http://www.dialogweb.com/</ext-link>.
     </comment>
   </element-citation>


.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
