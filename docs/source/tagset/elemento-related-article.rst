.. _elemento-related-article:

<related-article>
=================

Aparece em:

  :ref:`elemento-article-meta`
  :ref:`elemento-front-stub`


Atributos obrigatórios:

  1. ``@related-article-type``
  2. ``@id``

Ocorre:

  Zero ou mais vezes


Utilizado para indicar um artigo relacionado, publicado ou não, separadamente. Este elemento deve ser inserido para artigos como: :ref:`errata` ou resposta de :ref:`artigo-comentado`.

Os valores possíveis para o atributo ``@related-article-type`` são:

+------------------------+-------------------------------------------+
| Valor                  | Descrição                                 |
+========================+===========================================+
| corrected-article      | Utilizado em errata para indicar o artigo |
|                        | objeto da correção.                       |
+------------------------+-------------------------------------------+
| commentary-article     | Utilizado em comentário ou editorial para |
|                        | citar o artigo que está sendo comentado.  |
+------------------------+-------------------------------------------+


Para *Errata* o elemento :ref:`elemento-related-article` deve, obrigatoriamente, apresentar os seguintes atributos: ``@related-article-type``; ``@id``; ``@xlink:href`` e ``@ext-link-type``.

Os valores possíveis para ``@ext-link-type`` são:

* doi
* scielo-pid
* scielo-aid

Exemplo:



.. {"reviewed_on": "20160628", "by": "gandhalf_thewhite@hotmail.com"}
