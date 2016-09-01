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

+------------------------+-------------------------------------------------+
| Valor                  | Descrição                                       |
+========================+=================================================+
| corrected-article      | Utilizado em errata para indicar o artigo       |
|                        | objeto da correção.                             |
+------------------------+-------------------------------------------------+
| commentary-article     | Utilizado em comentário ou editorial para       |
|                        | citar o artigo que está sendo comentado.        |
+------------------------+-------------------------------------------------+
| letter                 | Nomeia uma carta para publicação ou uma         |
|                        | resposta para carta.                            |
+------------------------+-------------------------------------------------+
| partial-retraction     | Retratação ou recusa de parte de materiais      | 
|                        | o artigo que está sendo parcialmente retratado. |
+------------------------+-------------------------------------------------+
| retracted-article      | Usado em retratações parciais para indicar      |
|                        | artigo que está sendo retratado.                |
+------------------------+-------------------------------------------------+
| translated-article     | Utilizado em documentos traduzidos para         |
|                        | indicar o artigo no idioma.                     |
+------------------------+-------------------------------------------------+


.. {"reviewed_on": "20160803", "by": "gandhalf_thewhite@hotmail.com"}
