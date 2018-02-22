.. _elemento-related-article:

<related-article>
=================


Atributos obrigatórios:

  1. ``@related-article-type``
  2. ``@id``

+------------------------------+--------------------+
| Aparece em                   | Ocorre             |
+==============================+====================+
| :ref:`elemento-article-meta` | Zero ou mais vezes |
+------------------------------+--------------------+
| :ref:`elemento-front-stub`   | Zero ou mais vezes |
+------------------------------+--------------------+



Utilizado para indicar um artigo relacionado, publicado ou não, separadamente. Este elemento deve ser inserido para artigos como: :ref:`errata`, resposta de :ref:`artigo-comentado`, retratações e :ref:`elemento-response`.

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
| partial-retraction     | Usado em retratações parciais para indicar o    | 
|                        | artigo que está sendo parcialmente retratado    |
+------------------------+-------------------------------------------------+
| retracted-article      | Usado em retratações para indicar o artigo      |
|                        | que está sendo retratado.                       |
+------------------------+-------------------------------------------------+


.. {"reviewed_on": "20160803", "by": "gandhalf_thewhite@hotmail.com"}
