.. _elemento-article:

<article>
=========

Aparece em
  ``/``
 
Atributos obrigatórios
  1. dtd-version
  2. article-type
  3. xml:lang
  4. xmlns:xlink="http://www.w3.org/1999/xlink"
  5. specific-use="sps-1.3"
 
Ocorre
  Uma vez
 

A tag :ref:`elemento-article` representa o elemento raiz do XML, e deve conter 
obrigatoriamente os atributos ``@dtd-version``, ``@article-type``, ``@xml:lang``, 
``@xmlns:xlink="http://www.w3.org/1999/xlink"`` e ``@specific-use``.

O atributo ``@xmlns:mml="http://www.w3.org/1998/Math/MathML"`` é opcional e 
deve ser utilizado quando equações :term:`MathML` forem identificadas no 
:term:`documento`.

Para ``@dtd-version`` utilizar o valor 1.0 conforme a :term:`DTD`, 
explicitada em :ref:`xml-doctype`. Para ``@article-type`` define-se a tipologia 
de artigos, os valores que podem ser utilizados são:
 
+--------------------+----------------------------------------------------------+
| Valor              | Descrição                                                |
+====================+==========================================================+
|                    | comentários - uma nota crítica ou esclarecedora, escrita |
|                    | para discutir, apoiar ou debater um artigo ou outra      |
| article-commentary | apresentação anteriormente publicada. Pode ser um artigo,|
|                    | carta, editorial, etc. Estas publicações podem aparecer  |
|                    | como comentário, comentário editorial, ponto de vista,   |
|                    | etc.                                                     |
+--------------------+----------------------------------------------------------+
|                    | resenha - análise críticas de livros e outras            |
| book-review        | monografias.                                             |
|                    |                                                          |
+--------------------+----------------------------------------------------------+
| brief-report       | comunicação breve sobre resultados de uma pesquisa.      |
|                    |                                                          |
+--------------------+----------------------------------------------------------+
|                    | relato, descrição ou estudo de caso - pesquisas especiais|
| case-report        | que despertam interesse informativo.                     |
|                    |                                                          |
+--------------------+----------------------------------------------------------+
|                    | errata - corrige erros apresentados em artigos após      |
| correction         | sua publicação online/impressa.                          |
|                    |                                                          |
+--------------------+----------------------------------------------------------+
|                    | editorial - uma declaração de opiniões, crenças e        |
|                    | políticas do editor do periódico, geralmente sobre       |
| editorial          | assuntos de significado científico de interesse da       |
|                    | comunidade científica ou da sociedade.                   |
|                    |                                                          |
+--------------------+----------------------------------------------------------+
|                    | press release - comunicação breve de linguagem           |
| in-brief           | jornalística sobre um artigo ou tema.                    |
|                    |                                                          |
+--------------------+----------------------------------------------------------+
|                    | cartas - comunicação entre pessoas ou instituições       |
| letter             | através de cartas. Geralmente comentando um trabalho     |
|                    | publicado                                                |
+--------------------+----------------------------------------------------------+
|                    | Outro tipo de documento. Pode ser considerado adendo,    |
| other              | anexo, discussão, artigo de preocupação, introdução entre|
|                    | outros.                                                  |
+--------------------+----------------------------------------------------------+
|                    | comunicação breve sobre atualização de investigação ou   |
| rapid-communication| outra notícia.                                           |
|                    |                                                          |
+--------------------+----------------------------------------------------------+
|                    | resposta a carta ou ao comentário, geralmente é usado    |
| reply              | pelo autor original fazendo outros comentários a respeito|
|                    | dos comentários anteriores                               |
|                    |                                                          |
+--------------------+----------------------------------------------------------+
|                    | artigo original - abrange pesquisas, experiências        |
| research-article   | clínicas ou cirúrgicas ou outras contribuições originais.|
|                    |                                                          |
+--------------------+----------------------------------------------------------+
|                    | retratação - a retratação de um artigo científico é um   |
| retraction         | instrumento para corrigir o registro acadêmico publicado |
|                    | equivocadamente, por plágio, por exemplo.                |
+--------------------+----------------------------------------------------------+
|                    | são avaliações críticas sistematizadas da literatura     |
| review-article     | sobre determinado assunto.                               |
|                    |                                                          |
+--------------------+----------------------------------------------------------+
|                    | tradução. Utilizado para artigos que apresentam tradução |
| translation        | de um artigo produzido em idioma diferente.              |
|                    |                                                          |
+--------------------+----------------------------------------------------------+


.. note:: O atributo ``@article-type`` identifica o tipo de documento. 
          Não confundir com a seção em que o documento aparece no sumário.
 

Para ``@xml:lang``, utilizar código de duas letras conforme norma :term:`ISO 639-1`. 
Para uma lista completa dos códigos disponíveis e mais informações sobre a 
norma :term:`ISO 639-1`, acesse http://www.mathguide.de/info/tools/languagecode.html.
 

Exemplo da tag completa versão JATS 1.0:
 
.. code-block:: xml
 
     <article xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:mml="http://www.w3.org/1998/Math/MathML" dtd-version="1.0" specific-use="sps-1.3" article-type="research-article" xml:lang="en">
 


O atributo ``@specific-use`` identifica a versão do schema SciELO PS.
