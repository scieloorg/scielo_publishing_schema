.. _elemento-sub-article:

<sub-article>
=============


Atributos obrigatórios:

  1. ``@article-type``
  2. ``@id`` (Ver :ref:`sugestao-atribuicao-id`)
  3. ``@xml:lang``

+-------------------------+--------------------+
| Aparece em              | Ocorre             |
+=========================+====================+
| :ref:`elemento-article` | Zero ou mais vezes |
+-------------------------+--------------------+
| ``<sub-article>``       | Zero ou mais vezes |
+-------------------------+--------------------+



Identifica um artigo dentro de outro. Geralmente, os sub-artigos herdam os metadados do artigo pai, sendo portanto necessário inserir um elemento :ref:`elemento-front-stub`.

Os valores possíveis de ``@article-type`` em ``<sub-article>`` são:

+--------------------+----------------------------------------------------------+
| Valor              | Descrição                                                |
+====================+==========================================================+
|                    | cartas - comunicação entre pessoas ou instituições       |
| letter             | através de cartas. Geralmente, comentando um trabalho    |
|                    | publicado.                                               |
+--------------------+----------------------------------------------------------+
|                    | resposta - resposta a uma carta ou a um comentário que   |
| reply              | não está diretamente relacionado ao artigo principal.    |
|                    |                                                          |
+--------------------+----------------------------------------------------------+
|                    | tradução - utilizado para o texto traduzido de um artigo |
| translation        | produzido em idioma diferente.                           |
|                    |                                                          |
+--------------------+----------------------------------------------------------+
| referee-report     | Parecer / Revisão por pares aberta (Open Peer Review     |
|                    | ou OPR)                                                  |
+--------------------+----------------------------------------------------------+


O idioma do texto em ``@xml:lang`` é descrito pela norma :term:`ISO 639-1` como um código de dois caracteres alfabéticos em caixa baixa, cujo conteúdo encontra-se disponível no `site <http://www.mathguide.de/info/tools/languagecode.html>`_.


Exemplo:

.. code-block:: xml

    ...
    <sub-article article-type="translation" xml:lang="en" id="S1">
        ...
    </sub-article>
    ...


