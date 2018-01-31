.. _elemento-title-group:

<title-group>
=============

+------------------------------+---------+
| Aparece em                   | Ocorre  |
+==============================+=========+
| :ref:`elemento-article-meta` | Uma vez |
+------------------------------+---------+
| :ref:`elemento-front-stub`   | Uma vez |
+------------------------------+---------+



Especifica o título ou o conjunto de títulos do artigo. Nele são identificados :ref:`elemento-article-title` e
:ref:`elemento-trans-title-group`.

.. note:: ``<title-group>`` deve ser inserido abaixo de :ref:`elemento-article-categories` ou antes de :ref:`elemento-contrib-group`.

Exemplos:

* :ref:`elemento-titlegroup-exemplo-1`
* :ref:`elemento-titlegroup-exemplo-2`


.. _elemento-titlegroup-exemplo-1:

Exemplo de título em um único idioma:
-------------------------------------

.. code-block:: xml

	...
	<title-group>
    	<article-title>El impacto de la guerra en la salud de la infancia siria</article-title>
	</title-group>
	...



.. _elemento-titlegroup-exemplo-2:

Exemplo de título no idioma principal e tradução:
-------------------------------------------------

.. code-block:: xml

	...
	<title-group>
    	<article-title>Conocimientos de los pediatras sobre la laringomalacia: ¿siempre es un proceso banal?</article-title>
    	<trans-title-group xml:lang="en">
        	<trans-title>Pediatrician knowledge about laryngomalacia: is it always a banal process?</trans-title>
    	</trans-title-group>
	</title-group>
	...
	


.. {"reviewed_on": "20160803", "by": "gandhalf_thewhite@hotmail.com"}
