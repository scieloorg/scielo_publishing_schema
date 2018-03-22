.. _elemento-year:

<year>
======

+----------------------------------+---------------------+
| Aparece em                       | Ocorre              |
+==================================+=====================+
| :ref:`elemento-date`             | Uma vez             |
+----------------------------------+---------------------+
| :ref:`elemento-element-citation` | Zero ou mais vezes  |
+----------------------------------+---------------------+
| :ref:`elemento-product`          | Zero ou mais vezes  |
+----------------------------------+---------------------+
| :ref:`elemento-pub-date`         | Uma vez             |
+----------------------------------+---------------------+



Identifica o ano em referências, podendo representar o ano de publicação de um documento, de fabricação de um software, de criação de uma base de dados etc. Também é utilizado em :ref:`elemento-front` para identificar o ano da publicação de um artigo (ver :ref:`elemento-pub-date`) ou de um produto (ver :ref:`elemento-product`).

Exemplos:

  * :ref:`elemento-year-exemplo-1`
  * :ref:`elemento-year-exemplo-2`
  * :ref:`elemento-year-exemplo-3`


.. _elemento-year-exemplo-1:

Exemplo de ``<year>`` em ``<article-meta>``:
--------------------------------------------

.. code-block:: xml

	...
	<article-meta>
   	...
   		<pub-date pub-type="epub-ppub">
    		<season>Apr-Jun</season>
      		<year>2016</year>
   		</pub-date>
	</article-meta>
	...


.. _elemento-year-exemplo-2:

Exemplo de ``<year>`` em ``<element-citation>``:
------------------------------------------------

.. code-block:: xml

	...
	<element-citation publication-type="journal">
   		...
   		<source>Pediatric aerodigestive disorders</source>
   		<year>2009</year>
   		...
	</element-citation>
	...


.. _elemento-year-exemplo-3:

Exemplo de ``<year>`` em ``<product>``:
---------------------------------------

.. code-block:: xml

	...
   	<product product-type="book">
   		...
      	<year>2014</year>
      	<source>A revision of Axinaea (Melastomataceae)</source>
    	...
   </product>
   ...



