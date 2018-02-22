.. _elemento-trans-title-group:

<trans-title-group>
===================

Atributos obrigatórios:

  1. ``@xml:lang``

+-----------------------------+--------------------+
| Aparece em                  | Ocorre             |
+=============================+====================+
| :ref:`elemento-title-group` | Zero ou mais vezes |
+-----------------------------+--------------------+



Usado para apresentar o título traduzido ou um conjunto de títulos traduzidos do artigo. O atributo ``@xml:lang`` é mandatório e identifica o idioma traduzido do título.

.. note:: Caso o artigo tenha versão(ões) traduzida(s), ``<trans-title-group>`` não deve ser inserido, exceto nos casos em que haja títulos traduzidos diferentes da(s) tradução(ões) disponíveis em :ref:`elemento-sub-article`.

Exemplo:

.. code-block:: xml

	...
	<title-group>
    	<article-title>Between spiritual wellbeing and spiritual distress: possible related factors in elderly patients with cancer</article-title>
    	<trans-title-group xml:lang="pt">
    		<trans-title>Entre o bem-estar espiritual e a angústia espiritual: possíveis fatores relacionados a idosos com cancro</trans-title>
    	</trans-title-group>
	</title-group>
	...

.. {"reviewed_on": "20160629", "by": "gandhalf_thewhite@hotmail.com"}
