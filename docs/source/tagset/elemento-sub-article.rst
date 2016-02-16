.. _elemento-sub-article:
 
<sub-article>
-------------

Aparece em
  :ref:`elemento-article`,
  ``<sub-article>``


Atributos obrigatórios
  1. article-type
  2. id (Ver :ref:`sugestao-atribuicao-id`)
  3. xml:lang

Ocorre
  Zero ou mais vezes


Tag utilizada para identificar artigos que estão dentro de outro artigo. 
Geralmente os sub-artigos herdam os metadados do artigo pai e, para isso, é 
necessário inserir uma tag :ref:`elemento-front-stub`

Para verificar os possíveis valores de ``@article-type`` em ``<sub-article>`` veja o quadro abaixo:

+--------------------+----------------------------------------------------------+
| Valor              | Descrição                                                |
+====================+==========================================================+
|                    | resumo - uma apresentação precisa e resumida de uma      |
| abstract           | obra sem agregar interpretação ou crítica, acompanhado   |
|                    | de uma referência bibliográfica da obra original.        |
+--------------------+----------------------------------------------------------+
|                    | cartas - comunicação entre pessoas ou instituições       |
| letter             | através de cartas. Geralmente comentando um trabalho     |
|                    | publicado                                                |
+--------------------+----------------------------------------------------------+
|                    | resposta- resposta a uma carta ou a um comentário, que   |
| reply              | não está diretamente relacionado ao artigo principal.    |
|                    |                                                          |
+--------------------+----------------------------------------------------------+
|                    | tradução. Utilizado para artigos que apresentam tradução |
| translation        | de um artigo produzido em idioma diferente.              |
|                    |                                                          |
+--------------------+----------------------------------------------------------+

Para ``@xml:lang``, utilizar código de duas letras conforme norma :term:`ISO 639-1`. 
Para uma lista completa dos códigos disponíveis e mais informações sobre a 
norma :term:`ISO 639-1`, acesse http://www.mathguide.de/info/tools/languagecode.html.
 

Exemplo da tag completa:
 
.. code-block:: xml
 
    ...
    <sub-article article-type="translation" xml:lang="en" id="S1">
        ...
    </sub-article>
    ...


.. note:: Geralmente a tag ``<sub-article>`` é utilizada para identificar 
          arquivos traduzidos ou conjunto de cartas, resumos, teses etc.
 
