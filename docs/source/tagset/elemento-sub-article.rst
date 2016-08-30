.. _elemento-sub-article:

<sub-article>
=============

Aparece em:

  :ref:`elemento-article`
  ``<sub-article>``


Atributos obrigatórios:

  1. ``@article-type``
  2. ``@id`` (Ver :ref:`sugestao-atribuicao-id`)
  3. ``@xml:lang``

Ocorre:

  Zero ou mais vezes


Identifica um artigo dentro de outro. Geralmente, os sub-artigos herdam os metadados do artigo pai, sendo portanto necessário inserir um elemento :ref:`elemento-front-stub`.

Os valores possíveis de ``@article-type`` em ``<sub-article>`` são:

+--------------------+----------------------------------------------------------+
| Valor              | Descrição                                                |
+====================+==========================================================+
|                    | resumo - uma apresentação precisa e resumida de uma      |
| abstract           | obra sem agregar interpretação ou crítica, acompanhada   |
|                    | de uma referência bibliográfica da obra original.        |
+--------------------+----------------------------------------------------------+
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

``@xml:lang`` deve conter um código alfabético de duas letras conforme norma :term:`ISO 639-1`. Uma lista completa dos códigos disponíveis e demais informações encontram-se disponíveis na página `Language codes according to ISO 639-1 <http://www.mathguide.de/info/tools/languagecode.html>`_.


Exemplo:

.. code-block:: xml

    ...
    <sub-article article-type="translation" xml:lang="en" id="S1">
        ...
    </sub-article>
    ...


.. note:: Geralmente o elemento ``<sub-article>`` é utilizado para identificar artigos traduzidos ou conjunto de cartas, resumos, teses etc.


.. {"reviewed_on": "20160629", "by": "gandhalf_thewhite@hotmail.com"}
