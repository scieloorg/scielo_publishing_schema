.. _elemento-data-title:

<data-title>
============


+----------------------------------+--------------------+
| Aparece em                       | Ocorre             |
+==================================+====================+
| :ref:`elemento-product`          | Zero ou mais vezes |
+----------------------------------+--------------------+
| :ref:`elemento-element-citation` | Zero ou mais vezes |
+----------------------------------+--------------------+


Identifica referência do tipo base de dados.

Exemplo:

.. code-block:: xml

   ...
   <element-citation publication-type="database">
     <person-group person-group-type="author">
        <collab>NCBI</collab>
     </person-group>
   <data-title>Genome Information by organism</data-title>
     <source>Genome Database</source>
   <publisher-loc>Bethesda (MD)</publisher-loc>
   <publisher-name>National Library of Medicine (US)</publisher-name>
     <year>1950</year>
     <comment>Available from: <ext-link ext-link-type="uri" xlink:href="https://www.ncbi.nlm.nih.gov/genome/browse/">https://www.ncbi.nlm.nih.gov/genome/browse/</ext-link></comment>
     <date-in-citation content-type="access-date">2017 Sep 4</date-in-citation>
   </element-citation>
   ...
   
.. note:: Elemento válido apenas na versão 1.1 da JATS. Consulte exemplo de declaração para a versão JATS v1.1 em `!DOCTYPE <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/1.7-branch/tagset/xml-doctype.html>`_.

.. {"reviewed_on": "20170904", "by": "carolina.tanigushi@scielo.org"}