.. _elemento-isbn:

<isbn>
======

+----------------------------------+--------------------+
| Aparece em                       | Ocorre             |
+==================================+====================+
| :ref:`elemento-product`          | Zero ou mais vezes |
+----------------------------------+--------------------+
| :ref:`elemento-element-citation` | Zero ou mais vezes |
+----------------------------------+--------------------+



Identifica o :term:`ISBN` em uma referência bibliográfica ou produto.

Exemplo:

.. code-block:: xml

   <element-citation publication-type="book">
     <person-group person-group-type="author">
     <name>
       <surname>Stern</surname>
       <given-names>SD</given-names>
     </name>
     <etal/>
   </person-group>
     <source>Symptom to diagnosis:an evidence-based guide</source>
     <publisher-loc>New York</publisher-loc>
     <publisher-name>Lange Medical Books</publisher-name>
     <year>c2006</year>
     <size units="page">434 p</size>
     <isbn>9780071463898</isbn>
   </element-citation>


.. {"reviewed_on": "20160729", "by": "gandhalf_thewhite@hotmail.com"}
