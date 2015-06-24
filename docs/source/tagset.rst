.. _xml-encoding:

encoding
========
Atributo que especifica a codificação de caracteres usada na elaboração do documento. 
Para o SciELO, todos os XMLs devem ser codificados em :term:`UTF-8`.
 
Para maiores detalhes leia a especificação do padrão :term:`XML` 
(`2.8 Prolog and Document Type Declaration <http://www.w3.org/TR/2000/REC-xml-20001006#sec-prolog-dtd>`_).
 
.. code-block:: xml
 
    <?xml version="1.0" encoding="utf-8"?>
 

.. _xml-doctype:

<!DOCTYPE>
==========
 
A tag de declaração ``<!DOCTYPE>`` serve para indicar a :term:`DTD` 
à qual o XML é associado, ou seja, as regras estruturais do documento. 
O SciELO Publishing Schema utiliza como base o padrão *JATS 1.0*. 
 
Exemplo versão JATS 1.0:
 
.. code-block:: xml
 
    <!DOCTYPE article PUBLIC "-//NLM//DTD JATS (Z39.96) Journal Publishing DTD v1.0 20120330//EN" "JATS-journalpublishing1.dtd">
 

 
Tags Flutuantes
===============

As chamadas tags flutuantes podem aparecer em todo o documento, :ref:`elemento-front`, 
:ref:`elemento-body` e :ref:`elemento-back`.


.. _elemento-xref:

<xref>
------

Aparece em
  :ref:`elemento-article-title`,
  :ref:`elemento-trans-title`,
  :ref:`elemento-contrib`,
  :ref:`elemento-p`,
  ``th``,
  ``td``.
  ``verse-line``,
  :ref:`elemento-attrib`.
 
Atributos obrigatórios
  1. rid
  2. ref-type
 
Ocorre
  Zero ou mais vezes


Tag de Referência Cruzada usada para relacionar e/ou fazer link com alguma 
informação no texto. 
 
Os atributos obrigatórios para ``xref`` são:
 
* ``@rid``: representa "a referência ao id" e é utilizado para fazer a ligação 
  de elementos que possuem ``@id`` no arquivo. É imprescindível que haja um 
  ``@id`` para cada ``@rid`` e ambos deverão ter o valor idêntico para 
  sua relação.
* ``@ref-type``: especifica o tipo de referência cruzada. Os valores para 
  este atributo podem ser:
 

+------------------------+-----------------------------------------+
| Valor                  | Descrição                               |
+========================+=========================================+
| aff                    | afiliação                               |
+------------------------+-----------------------------------------+
| app                    | apêndice                                |
+------------------------+-----------------------------------------+
| author-notes           | notas de autor (ou relacionado a autor) |
+------------------------+-----------------------------------------+
| bibr                   | referência bibliográfica                |
+------------------------+-----------------------------------------+
| contrib                | contribuinte                            |
+------------------------+-----------------------------------------+
| corresp                | autor correspondente                    |
+------------------------+-----------------------------------------+
| disp-formula           | fórmula                                 |
+------------------------+-----------------------------------------+
| fig                    | figura ou grupos de figuras             |
+------------------------+-----------------------------------------+
| fn                     | nota de rodapé                          |
+------------------------+-----------------------------------------+
| sec                    | seção                                   |
+------------------------+-----------------------------------------+
| supplementary-material | material suplementar                    |
+------------------------+-----------------------------------------+
| table                  | tabela ou grupo de tabelas              |
+------------------------+-----------------------------------------+
| table-fn               | nota de rodapé de tabelas               |
+------------------------+-----------------------------------------+
 
Exemplos:
 

.. code-block:: xml

    ...
    <article-meta>
        ...
        <contrib-group>
            <contrib contrib-type="author">
                <name>
                    <surname>Lacerda</surname>
                    <given-names>Marcus VG</given-names>
                </name>
                <xref ref-type="aff" rid="aff1">1</xref>
            </contrib>
            <aff id="aff1">
                <label>1</label>
                <institution content-type="orgname">Universidade do Estado do Amazonas</institution>
                <institution content-type="normalized">Universidade do Estado do Amazonas</institution>
                <addr-line>
                    <named-content content-type="city">Manaus</named-content>
                    <named-content content-type="state">AM</named-content>
                </addr-line>
                <country country="BR">Brasil</country>
                <institution content-type="original">Universidade do Estado do Amazonas, Manaus, AM, Brasil</institution>
            </aff>
            ...
        </contrib-group>
        ...
    </article-meta>
    ...
     

.. code-block:: xml

     <xref ref-type="bibr" rid="B13">John 2003</xref>


.. code-block:: xml

    <p>Check in <xref ref-type="fig" rid="f01">Figure</xref>:</p>
    <p>
        <fig id="f01">
            <caption>
                <title>Environmental <italic>in situ</italic> conditions during the study period.</title>
            </caption>
            <graphic xlink:href="0074-0276-mioc-0074-0276140068-gf01"/>
        </fig>
    </p>
 
.. note:: Não envolver a tag ``<xref>`` em ``<sup>``.


Para casos em que não há label explícito para relacionar o autor à afiliação, deve ser inserido em :ref:`elemento-contrib` um elemento ``<xref>`` "fechado". Veja:


.. code-block:: xml
    
  ...
  <article-meta>
    ...
    <contrib-group>
      <contrib contrib-type="author">
        <name>
            <surname>Broering</surname>
            <given-names>Laurent Wiliam</given-names>
        </name>
        <xref ref-type="aff" rid="aff1"/>
      </contrib>
    </contrib-group>
    <aff id="aff1">
      <institution content-type="normalized">Fundação Getúlio Vargas</institution>
      <institution content-type="orgname">Fundação Getúlio Vargas</institution>
      <institution content-type="orgdiv1">EAESP</institution>
      <addr-line>
        <named-content content-type="city">São Paulo</named-content>
        <named-content content-type="state">SP</named-content>
      </addr-line>
      <country country="BR">Brazil</country>
      <institution content-type="original">Fundação Getúlio Vargas - FGV-EAESP, Av. 9 de Julho, 2029, Bela Vista, 01313-902, São Paulo, SP, Brazil.</institution>
    </aff>
  ...

.. note:: Não inserir label caso não exista no PDF.


.. _elemento-label:
 
<label>
-------

Aparece em
  :ref:`elemento-aff`,
  :ref:`elemento-corresp`, 
  :ref:`elemento-fn`,
  :ref:`elemento-fig`,
  :ref:`elemento-table-wrap`,
  :ref:`elemento-disp-formula`,
  :ref:`elemento-media`,
  :ref:`elemento-supplementary-material`,
  :ref:`elemento-list`,
  ``list-item``,
  :ref:`elemento-ref`,
  ``glossary``,
  :ref:`elemento-app`,
  :ref:`elemento-def-list`
  :ref:`elemento-verse-group`

Ocorre
  Zero ou mais vezes


A tag ``<label>`` é responsável pela identificação numérica ou alfabética 
que faz a ligação entre etiquetas.

Exemplos:
 
.. code-block:: xml
 
    <aff id="aff01">
        <label>a</label>
        ...
    </aff>


.. code-block:: xml

    <corresp id="c01">
       <label>*</label>
       ...
    </corresp>


.. code-block:: xml

    <fig id="f01">
        <label>Figure 1</label>
        ...
    </fig>
    

.. code-block:: xml

    <table-wrap id="t01">
        <label>Table 1</label>
        ...
    </table-wrap>
 

.. code-block:: xml

    <ref id="B01">1</ref>
        <label>1</label>
        ...
    </ref>
 

.. code-block:: xml

    <app>
        <label>Apêndice</label>
        ...
    </app>
 
 
.. _elemento-p:

<p>
---
 
Aparece em
  :ref:`elemento-abstract`,
  :ref:`elemento-ack`,
  :ref:`elemento-app`,
  :ref:`elemento-body`,
  :ref:`elemento-boxed-text`,
  ``<def>``,
  :ref:`elemento-disp-quote`,
  :ref:`elemento-fn`,
  ``<list-item>``,
  :ref:`elemento-ref-list`,
  :ref:`elemento-sec`,
  :ref:`elemento-trans-abstract`

 
Ocorre
  Uma ou mais vezes
 

Esta tag identifica parágrafos. Deve ser inserida no documento sem nenhum 
tipo de atributo.


.. _sugestao-atribuicao-id:

Sugestão de atribuição de @id
=============================
 
Para a composição do ``@id``, combine o prefixo do tipo do elemento e um número 
inteiro, como segue:
 

+------------------------+---------------------------+---------+---------------------+
| Elemento XML           | Descrição                 | Prefixo | Exemplo             |
+========================+===========================+=========+=====================+
| aff                    | Afiliação                 | aff     | aff1, aff2, ...     |
+------------------------+---------------------------+---------+---------------------+
| app                    | Apêndice                  | app     | app1, app2, ...     |
+------------------------+---------------------------+---------+---------------------+
| author-notes/fn |      | Notas de rodapé do artigo | fn      | fn1, fn2, ...       | 
| fn-group/fn            |                           |         |                     |
+------------------------+---------------------------+---------+---------------------+
| boxed-text             | Caixa de texto            | bx      | bx1, bx2, ...       |
+------------------------+---------------------------+---------+---------------------+
| corresp                | Correspondência           | c       | c1, c2, ...         |
+------------------------+---------------------------+---------+---------------------+
| def-list               | Lista de Definições       | d       | d1, d2, ...         |
+------------------------+---------------------------+---------+---------------------+
| disp-formula           | Equações                  | e       | e1, e2, ...         |
+------------------------+---------------------------+---------+---------------------+
| fig                    | Figuras                   | f       | f1, f2, ...         |
+------------------------+---------------------------+---------+---------------------+
| glossary               | Glossário                 | gl      | gl1, gl2, ...       |
+------------------------+---------------------------+---------+---------------------+
| media                  | Media                     | m       | m1, m2, ...         |
+------------------------+---------------------------+---------+---------------------+
| ref                    | Referência bibliográfica  | B       | B1, B2, ...         |
+------------------------+---------------------------+---------+---------------------+
| sec                    | Seções                    | sec     | sec1, sec2, ...     |
+------------------------+---------------------------+---------+---------------------+
| sub-article            | sub-artigo                | S       | S1, S2, ...         |
+------------------------+---------------------------+---------+---------------------+
| supplementary-material | Suplemento                | suppl   | suppl1, suppl2, ... |
+------------------------+---------------------------+---------+---------------------+
| table-wrap-foot/fn     | Notas de rodapé de tabela | TFN     | TFN1, TFN2, ...     |
+------------------------+---------------------------+---------+---------------------+
| table-wrap             | Tabela                    | t       | t1, t2, ...         |
+------------------------+---------------------------+---------+---------------------+


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
  5. specific-use="sps-1.2"
 
Ocorre
  Uma vez
 

A tag :ref:`elemento-article` representa o elemento raiz do XML, e deve conter 
obrigatoriamente os atributos ``@dtd-version``, ``@article-type``, ``@xml:lang``, 
``@xmlns:xlink="http://www.w3.org/1999/xlink"`` e ``@specific-use``.

O atributo ``@xmlns:mml="http://www.w3.org/1998/Math/MathML"`` é opcional e 
deve ser utilizado quando equações :term:`MathML` forem identificadas no 
documento.

Para ``@dtd-version`` utilizar os valores 1.0 ou 3.0 conforme a :term:`DTD`, 
explicitada em :ref:`xml-doctype`. Para ``@article-type`` define-se a tipologia 
de artigos, os valores que podem ser utilizados são:
 
+--------------------+----------------------------------------------------------+
| Valor              | Descrição                                                |
+====================+==========================================================+
|                    | resumo - uma apresentação precisa e resumida de uma      |
| abstract           | obra sem agregar interpretação ou crítica, acompanhado   |
|                    | de uma referência bibliográfica da obra original.        |
+--------------------+----------------------------------------------------------+
|                    | exposição ou declaração relevante que pode ou não ter    |
| announcement       | relação com o artigo publicado.                          |
|                    |                                                          |
+--------------------+----------------------------------------------------------+
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
|                    | políticas do editor de uma revista, geralmente sobre     |
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
 
     <article xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:mml="http://www.w3.org/1998/Math/MathML" dtd-version="1.0" specific-use="sps-1.2" article-type="research-article" xml:lang="en">
 


O atributo ``@specific-use`` identifica a versão do schema SciELO PS.

.. _elemento-front:

<front>
=======

Aparece em
  :ref:`elemento-article`
 
Ocorre
  Uma vez


Em ``<front>`` devem ser identificados os metadados do periódico, título, 
autoria, afiliação, resumo, palavras-chave, DOI, volume, número, suplemento, 
paginação, indicação da licença Creative Commons, data de publicação, 
seção de cabeçalho, histórico de datas, dados de correspondência, 
notas de autor, informações de resenhas de livros, contagem de elementos e 
dados de financiamento (se houver).
 

.. _elemento-journal-meta:

<journal-meta>
--------------

Aparece em
  :ref:`elemento-front`
 
Ocorre
  Uma vez


Em ``<journal-meta>`` faz-se a identificação dos metadados do periódico.
 
.. note:: Consulte o :ref:`arquivo de metadados dos periódicos <journal-meta-csv>` 
          como referência na identificação dos elementos.


.. _elemento-journal-id:
 
<journal-id>
^^^^^^^^^^^^

Aparece em
  :ref:`elemento-journal-meta`
 
Atributos obrigatórios
  1. journal-id-type='publisher-id'
 
Ocorre
  Uma ou mais vezes


Especifica o título padronizado do periódico.

Os valores permitidos para o atributo ``@journal-id-type`` são:

+---------------+-----------------------------------------+
| Valor         | Descrição                               |
+===============+=========================================+
| publisher-id  | Acrônimo do periódoco na coleção SciELO |
+---------------+-----------------------------------------+
| nlm-ta        | Título abreviado no :term:`PubMed`      |
+---------------+-----------------------------------------+
 
Artigos de periódicos indexados no :term:`PubMed`, devem apresentar adicionalmente 
o título abreviado do periódico no :term:`PubMed` por meio do elemento 
``<journal-id @journal-id-type="nlm-ta">``, conforme o exemplo:
 

.. code-block:: xml
   
    ...
    <journal-meta>
        ...
        <journal-id journal-id-type="publisher-id">mioc</journal-id>
        <journal-id journal-id-type="nlm-ta">Mem Inst Oswaldo Cruz</journal-id>
        ...
    </journal-meta>
    ...

Para verificar se o periódico está indexado no :term:`PubMed` consulte o link 
http://www.ncbi.nlm.nih.gov/pubmed/advanced


.. note:: Consulte o :ref:`arquivo de metadados dos periódicos <journal-meta-csv>` 
          como referência na identificação dos elementos.


.. _elemento-journal-title-group:
 
<journal-title-group>
^^^^^^^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-journal-meta`
 
Ocorre
  Uma vez
 

Abrange tags que representam os metadados identificadores da revista.
 
Exemplo:

.. code-block:: xml
 
    ...
    <journal-meta>
        ...
        <journal-title-group>
            <journal-title>Brazilian Journal of Otorhinolaryngology</journal-title>
            <abbrev-journal-title abbrev-type="publisher">Braz J Otorhinolaryngol.</abbrev-journal-title>
            ...
        </journal-title-group>
        ...
    </journal-meta>
    ...
 

.. _elemento-journal-title:
 
<journal-title>
^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-journal-title-group`
 
Ocorre
  Uma vez


Neste item é incluído o título longo do periódico de acordo com seu registro 
no ISSN. 

.. note:: Consulte o :ref:`arquivo de metadados dos periódicos <journal-meta-csv>` 
          como referência na identificação dos elementos.
 
Exemplo:

.. code-block:: xml

    ...
    <journal-meta>
        ...
        <journal-title-group>
            <journal-title>Brazilian Journal of Medical and Biological Research</journal-title>
            ...
        </journal-title-group>
        ...
    </journal-meta>
    ...
 

.. _elemento-abbrev-journal-title:

<abbrev-journal-title>
^^^^^^^^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-journal-title-group`
 
Atributos obrigatórios
  1. abbrev-type="publisher"
 
Ocorre
  Uma vez
 

Nesta tag é incluída a forma abreviada do título do periódico de acordo 
com seu registro no ISSN. 

.. note:: Consulte o :ref:`arquivo de metadados dos periódicos <journal-meta-csv>` 
          como referência na identificação dos elementos.

Exemplo:
 
.. code-block:: xml
 
    <journal-title-group>  
        <abbrev-journal-title abbrev-type="publisher">Braz. J. Med. Biol. Res.</abbrev-journal-title>
    </journal-title-group>
 

.. _elemento-issn:
 
<issn>
^^^^^^

Aparece em
  :ref:`elemento-journal-meta`, :ref:`elemento-element-citation`
 
Atributos obrigatórios em :ref:`elemento-front`
  1. pub-type='ppub' ou pub-type='epub'
 
Ocorre
  Uma ou mais vezes


O ISSN é um código numérico, único, que identifica uma publicação seriada 
a qual é definida pela norma :term:`ISO 3297:2007`. Normalmente cada tipo de 
suporte utilizado pelo periódico possui um número específico. 

É possível também encontrar esta informação em :ref:`elemento-back` dentro de 
:ref:`elemento-element-citation` nas referências, mas não se faz o uso de 
nenhum atributo neste caso.

.. note:: Consulte o :ref:`arquivo de metadados dos periódicos <journal-meta-csv>` 
          como referência na identificação dos elementos.

Os valores permitidos para o atributo ``@pub-type`` são:

+-------+-------------------------+
| Valor | Descrição               |
+=======+=========================+
| ppub  | ISSN da versão impressa |
+-------+-------------------------+
| epub  | ISSN da versão digital  |
+-------+-------------------------+
 
No caso de estarem disponíveis, ambos os ISSNs deverão ser identificados, 
conforme o exemplo:
 
.. code-block:: xml
    
    ...
    <journal-meta>
        ...
        <issn pub-type="epub">1808-8686</issn>
        <issn pub-type="ppub">1808-8694</issn>
        ...
    </journal-meta>
    ...


.. _elemento-publisher:
 
<publisher>
^^^^^^^^^^^

Aparece em
  :ref:`elemento-journal-meta`
 
Ocorre
  Uma vez


O nome da instituição responsável pela publicação do periódico deve ser 
especificado de acordo com o registro na SciELO. 

.. note:: Consulte o :ref:`arquivo de metadados dos periódicos <journal-meta-csv>` 
          como referência na identificação dos elementos.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <journal-meta>
        ...
        <publisher>
            <publisher-name>Instituto Oswaldo Cruz, Ministério da Saúde</publisher-name>
        </publisher>
        ...
    </journal-meta>
    ...
 

.. _elemento-article-meta:
     
<article-meta>
--------------

Aparece em
  :ref:`elemento-front`
 
Ocorre
  Uma vez


Contém os metadados do artigo. Seus elementos básicos são :term:`DOI`, seção 
(de acordo com o sumário do periódico), título(s) do artigo, autor (es) e 
suas respectivas afiliações e notas, data de publicação, volume, número e 
paginação do artigo, resumo(s), palavras-chave, histórico, indicação da licença
de uso Creative Commons e contagem de elementos e dados de financiamento (se houver).

 
.. _elemento-article-id:

<article-id>
^^^^^^^^^^^^

Aparece em
  :ref:`elemento-article-meta`
 
Atributos obrigatórios
  1. pub-id-type='doi'
 
Ocorre
  Uma ou mais vezes


Cada artigo deve possuir um identificador único, e para tal a SciELO utiliza 
o identificador :term:`DOI` do artigo. 
 
Exemplo:
 
.. code-block:: xml
    
    ...
    <article-meta>
        ...
        <article-id pub-id-type="doi">10.1590/0074-0276130047</article-id>
        ...
    </article-meta>
    ...
     

.. _elemento-article-categories:
 
<article-categories>
--------------------

Aparece em
  :ref:`elemento-article-meta`
 
Ocorre
  Uma vez


Em ``<article-categories>`` classifica-se o artigo de acordo com a seção 
que aparece no sumário do periódico. Esta classificação pode ser temática 
ou por tipologia do documento.
 
 
.. _elemento-subj-group:

<subj-group>
^^^^^^^^^^^^

Aparece em
  :ref:`elemento-article-categories`
 
Atributos obrigatórios
  1. subj-group-type="heading"
 
Ocorre
  Uma vez
 

Designa a seção do documento e serve para organizar documentos em grupos 
por assunto. É obrigatória a presença de uma e somente uma ocorrência do
elemento ``<subj-group>`` com o atributo ``@subj-group-type="heading"``. 
Em ``<subject>`` atribui-se a seção em que o artigo foi classificado 
(consultar o sumário para melhor identificação) e para :term:`ahead-of-print` 
deve ser adotado sempre a seção ``Articles``. Ver exemplo de :ref:`ahead-of-print`
 
 
Exemplos:
 
Seção temática:
 
.. code-block:: xml
 
    ...
    <article-categories>
        <subj-group subj-group-type="heading">
            <subject>Biotechnology</subject>
        </subj-group>
    </article-categories>
    ...


Seção por tipo de documento:
 
.. code-block:: xml
 
    ...
    <article-categories>
        <subj-group subj-group-type="heading">
            <subject>Original Article</subject>
        </subj-group>
    </article-categories>
    ...
 
Para ahead-of-print:
 
.. code-block:: xml
 
    ...
    <article-categories>
        <subj-group subj-group-type="heading">
            <subject>Articles</subject>
        </subj-group>
    </article-categories>
    ...
 

.. note:: Para documentos como editoriais, erratas, cartas ao editor etc que não 
          apresentam título, mas apenas a seção, é preciso repetir o título da 
          seção no front e marcá-lo com as tags de título.


.. _elemento-title-group:

<title-group>
-------------

Aparece em
  :ref:`elemento-article-meta`
 
Ocorre
  Uma vez


Esta tag é utilizada para especificar o título ou um conjunto de títulos 
do artigo. Nele são identificados :ref:`elemento-article-title` e 
:ref:`elemento-trans-title-group`.
 
 
.. _elemento-article-title:

<article-title>
^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-title-group`, 
  :ref:`elemento-element-citation`
 
Ocorre
  zero ou uma vez


Esta tag pode ser utilizada para especificar o título do artigo em si 
em :ref:`elemento-article-meta`, ou para especificar um título de documento 
nas referências em :ref:`elemento-element-citation`. Em ambos os casos, o 
atributo ``@xml:lang`` não deve ser utilizado.

.. note:: O elemento ``<article-title>`` é obrigatório em :ref:`elemento-title-group`, .

 
Exemplo:
 
.. code-block:: xml
 
    ...
    <title-group>
        <article-title>The teaching of temporomandibular disorders and  orofacial pain at undergraduate level in Brazilian dental schools</article-title>
    </title-group>
    ...

.. note:: Se o título do artigo ou da referência possuir um subtítulo, ele deve 
          ser marcado junto a tag ``<article-title>``. Não se deve marcar 
          nenhum texto separadamente em outras tags 
          (a mesma regra se aplica a :ref:`elemento-trans-title`).
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <title-group>
        <article-title>Correlação entre sintomas e tempo de evolução do câncer do trato aerodigestivo superior com o estádio inicial e avançado</article-title>
    </title-group>
    ...


.. note:: Se o título da seção for igual ao título do artigo (exemplo de alguns 
          editoriais, erratas, cartas ao editor), repetir a informação no front 
          e marcá-la com as tags de título. 


.. _elemento-trans-title-group:
 
<trans-title-group>
^^^^^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-title-group`
 
Atributos obrigatórios
  1. xml:lang
 
Ocorre
  Zero ou mais vezes


Esta tag é utilizada para apresentar o título traduzido ou um conjunto de 
títulos traduzidos do artigo. O atributo ``@xml:lang`` é obrigatório 
e deve ser utilizado para especificar o idioma traduzido do título.


.. _elemento-trans-title:

<trans-title>
^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-trans-title-group`
 
Ocorre 
  Uma ou mais vezes


Marca o título traduzido, dentro da tag :ref:`elemento-trans-title-group`.


Exemplo:
 
.. code-block:: xml
 
    ...
    <title-group>
        <article-title>Between spiritual wellbeing and spiritual distress: possible related factors in elderly patients with cancer</article-title>
        <trans-title-group xml:lang="pt">
            <trans-title>Entre o bem-estar espiritual e a angústia espiritual: possíveis fatores relacionados a idosos com cancro</trans-title>
        </trans-title-group>
        <trans-title-group xml:lang="es">
            <trans-title>Entre el bienestar espiritual y el sufrimiento espiritual: posibles factores relacionados en ancianos con câncer</trans-title>
        </trans-title-group>
    </title-group>
    ...
          

.. _elemento-contrib-group:
 
<contrib-group>
---------------

Aparece em
  :ref:`elemento-article-meta`
 
Ocorre
  Uma vez


Representa o grupo dos que contribuiram para a elaboração do artigo. 
Os tipos de contribuintes mais frequentes são de autores pessoais, 
instituições e grupos de pesquisa. A tag pode ou não envolver a 
informação de afiliação, sendo obrigatória na identificação do contribuidor 
do tipo autores (author) sejam institucionais ou não. Os principais 
elementos de ``<contrib-group>`` são: :ref:`elemento-contrib`, 
:ref:`elemento-xref`, :ref:`elemento-collab`, :ref:`elemento-aff` e 
:ref:`elemento-role`.


.. _elemento-contrib:
 
<contrib>
^^^^^^^^^

Aparece em
  :ref:`elemento-contrib-group`
 
Atributos obrigatórios
  1. contrib-type
 
Ocorre
  Uma ou mais vezes


Em ``<contrib>`` especifica-se o indivíduo ou instituição que contribuiu para 
o artigo. Pode ser anônimo ou ter um ou vários autores, inclusive autores 
institucionais. Tags como :ref:`elemento-name`, :ref:`elemento-collab`, :ref:`elemento-on-behalf-of`, 
:ref:`elemento-xref`, :ref:`elemento-role` e ``<anonymous>`` podem ser encontradas neste elemento. 
 
O atributo ``@contrib-type`` pode possuir os valores:

+------------+----------------------------------------------------------------+
| Valor      | Descrição                                                      |
+============+================================================================+
| author     | Autor do conteúdo                                              |
+------------+----------------------------------------------------------------+
| compiler   | Compilador - pessoa que montou um trabalho composto de várias  |
|            | fontes                                                         |
+------------+----------------------------------------------------------------+
| editor     | Editor do conteúdo                                             |
+------------+----------------------------------------------------------------+
| translator | Tradutor do conteúdo                                           |
+------------+----------------------------------------------------------------+

 
Exemplo:
 
.. code-block:: xml
 
    ...
    <contrib-group>
        <contrib contrib-type="author">
            <name>
                <surname>Freitas</surname>
                <given-names>Ismael Forte</given-names>
                <suffix>Júnior</suffix>
            </name>
            <xref ref-type="aff" rid="aff01">1</xref>
        </contrib>
        ...
    </contrib-group>
    ...
 
.. note:: Observar normas para entrada de nomes (*AACR2* - Código de Catalogação 
          Anglo Americano e/ou Currículo Lattes dos autores, avaliar formas 
          de entrada autorizadas).

.. note:: Para artigos que apresentam assinatura, como editoriais, apresentação etc. repetir autores de <sig-block> em front/contrib caso não exista informação de autor.

.. _elemento-collab:
 
<collab>
^^^^^^^^

Aparece em
  :ref:`elemento-contrib`
 
Ocorre
  Zero ou mais vezes


Utilizada para identificar uma autoria institucional individual ou grupo. 

 
.. _elemento-on-behalf-of:

<on-behalf-of>
^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-contrib-group`, 
  :ref:`elemento-contrib`
 
Ocorre
  Zero ou mais vezes


Utiliza-se quando um autor age como representante de um grupo ou 
organização. Ou seja, quando o autor diz ter escrito ou editado um trabalho 
em nome de uma organização. 

 
Exemplo:

.. code-block:: xml

    ...
    <contrib-group>
        ...
        <contrib>
            <name>
                <surname>Proietti</surname>
                <given-names>Fernando Augusto</given-names>
            </name>
            <xref ref-type="aff" rid="aff02">II</xref>
            <on-behalf-of>Interdisciplinary HTLV Research Group</on-behalf-of>
        </contrib>
        ...
    </contrib-group>
    ...
 
 
.. _elemento-role:

<role>
^^^^^^

Aparece em
  :ref:`elemento-collab`, 
  :ref:`elemento-contrib`, 
  :ref:`elemento-contrib-group`, 
  :ref:`elemento-element-citation`, 
  :ref:`elemento-person-group`, 
  :ref:`elemento-product`
 
Ocorre
  Zero ou mais vezes


A tag ``<role>`` (função ou papel) é usada para especificar o cargo 
(ou função) do contribuinte do documento.  

Exemplos:
 
.. code-block:: xml
 
    ...
    <contrib contrib-type="author">
        ...
        <name>
            <surname>Meader</surname>
            <given-names>CR</given-names>
            <prefix>Dr.</prefix>
            <suffix>Junior</suffix>
        </name>
        <xref ref-type="aff" rid="aff02">2</xref>
        <role>Pesquisador</role>
        ...
    </contrib>
    ...
 
 
.. code-block:: xml
 
    ...
    <element-citation publication-type="journal">
        ...
        <person-group person-group-type="author">
            <name>
                <surname>Petitti</surname>
                <given-names>DB</given-names>
                ...
            </name>
            <name>
                <surname>Crooks</surname>
                <given-names>VC</given-names>
                ...
            </name>
            <role>pesquisador</role>
            ...
        </person-group>
        ...
    </element-citation>
    ...
      

.. _elemento-name:
 
<name>
^^^^^^

Aparece em
  :ref:`elemento-contrib`, :ref:`elemento-person-group`
  
Ocorre
  Zero ou mais vezes


A tag ``<name>`` é utilizada para especificar o nome pessoal do contribuinte 
autoral. As tags possíveis em ``<name>`` são: :ref:`elemento-surname`, 
:ref:`elemento-given-names`, :ref:`elemento-prefix`, :ref:`elemento-suffix`.
 

.. note:: As tags possíveis em ``<name>`` devem seguir obrigatoriamente a 
          sequência de aparecimento citada acima.
 

.. _elemento-surname:
 
<surname>
^^^^^^^^^

Aparece em
  :ref:`elemento-name`
 
Ocorre
  Uma ou mais vezes


É utilizada para especificar sobrenome de autores. Aqui deve ser 
especificado o último nome do autor. Deve-se observar as regras para 
identificação de sobrenome de acordo com a norma adotada pelo periódico. 
A recomendação da SciELO é utilizar a norma *AACR2* Código de Catalogação 
Anglo Americano e/ou Currículo Lattes dos autores.
 
Exemplo:

.. code-block:: xml
 
    ...
    <name>
        <surname>Almeida</surname>
        <given-names>Antônio Golçalves de</given-names>
        ...
    </name>
    ...
 

.. _elemento-given-names:

<given-names>
^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-name`
 
Ocorre
  Zero ou mais vezes


Identifica o prenome do autor, ou seja, todos os nomes que não o sobrenome.
 
.. code-block:: xml
 
    ...
    <name>
        <surname>Santos</surname>
        <given-names>Ana Maria da Silva</given-names>
        ...
    </name>
    ...
 

.. _elemento-prefix:

<prefix>
^^^^^^^^

Aparece em
  :ref:`elemento-name`
 
Ocorre
  Zero ou mais vezes


Especifica o qualificador que precede o prenome do autor. Geralmente é 
utilizado para identificar qualificadores como "Prof. Dr.", "Dr.", "Sr",
"Presidente", "Embaixador" dentre outros.
 
Exemplo:

.. code-block:: xml

    ...
    <name>
        <surname>Oliveira</surname>
        <given-names>Marcos de</given-names>
        <prefix>Prof.</prefix>
        ...
    </name>
    ... 
 

.. _elemento-suffix:

<suffix>
^^^^^^^^

Aparece em
  :ref:`elemento-name`
 
Ocorre
  Zero ou mais vezes


Especifica sufixos do nome como as partículas "Neto", "Júnior", "Jr.", 
"Filho", "Sobrinho" etc.
 
Exemplo:

.. code-block:: xml
 
    ...
    <name>
        <surname>Santos</surname>
        <given-names>João da Silva</given-names>
        <suffix>Neto</suffix>
        ...
    </name>
    ...


.. _elemento-aff:

<aff>
-----

Aparece em
  :ref:`elemento-article-meta`

Atributos obrigatórios
  1. id (ver :ref:`sugestao-atribuicao-id`)
 
Ocorre
  Zero ou mais vezes


Considera-se como afiliação o vínculo institucional dos contribuintes do artigo 
naquele momento. 

Os dados de afiliação são importantes para localizar e mensurar a produção 
científica por país, estado, cidade, bem como por instituição e seus 
departamentos. Recomenda-se que os nomes das instituições das afiliações 
sejam especificadas em sua forma original, sem tradução ou abreviações de 
seus nomes. Ou seja, por exemplo, identificar preferencialmente 
**Universidade de São Paulo** a USP, ou University of São Paulo, ou 
Saint Paul University, entre outras possíveis formas. 
Por isso, quando ocorre no documento de existir mais de uma forma, usar a original.
 
Não configura vínculo institucional quando o dado é apresentado da seguinte 
forma: Doutor, Mestre ou Especialista em XXX pela Universidade YYY. Seria 
identificado como afiliação caso o dado esteja como Mestrando(a), Doutorando(a), 
Pós-Graduando(a) etc, configurando o vínculo com instituição naquele momento 
específico.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <aff id="aff01">
        <label>1</label>
        <institution content-type="orgname">Fundação Oswaldo Cruz</institution> 
        <institution content-type="orgdiv1">Escola Nacional de Saúde Pública Sérgio Arouca</institution>
        <institution content-type="orgdiv2">Centro de Estudos da Saúde do Trabalhador e Ecologia Humana</institution>   
        <addr-line>
            <named-content content-type="city">Manguinhos</named-content>
            <named-content content-type="state">RJ</named-content>
        </addr-line>
        <country country="BR">Brasil</country>
        <email>maurosilva@fiocruz.com</email>
        <institution content-type="original">Prof. da Fundação Oswaldo Cruz; da Escola Nacional de Saúde Pública Sérgio Arouca, do Centro de Estudos da Saúde do Trabalhador e Ecologia Humana. RJ - Manguinhos / Brasil. maurosilva@fiocruz.com </institution>
    </aff>
    ...
 

.. _elemento-institution:

<institution>
^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-aff`
 
Atributos obrigatórios
  1. content-type
 
Ocorre
  Zero ou mais vezes


Nesta tag especifica-se a instituição do autor, a qual pode ser dividida 
em até três níveis. Estes níveis serão definidos pelo atributo obrigatório 
``@content-type``, podendo possuir os seguintes valores:

+------------+--------------------------------------------------------------------+ 
| Valor      | Descrição                                                          |
+============+====================================================================+
| orgname    | Representando a instituição de nível hierárquico maior mencionado  |
|            | na afiliação.                                                      |
+------------+--------------------------------------------------------------------+ 
| orgdiv1    | Representando a primeira divisão da instituição mencionada em      |
|            | orgname.                                                           |
+------------+--------------------------------------------------------------------+ 
| orgdiv2    | Representando a segunda divisão da instituição mencionada em       |
|            | orgname.                                                           |
+------------+--------------------------------------------------------------------+ 
| normalized | Nome da instituição na forma normalizada pela SciELO.              |     
+------------+--------------------------------------------------------------------+ 
 

.. note:: No caso de mais divisões mencionadas em afiliações no PDF, 
          identifica-las somente na tag ``<institution content-type="original">``.
 

.. code-block:: xml
 
    ...
    <aff id="aff01">
        <institution content-type="orgname">
            Universidade de São Paulo
        </institution>
        <institution content-type="orgdiv1">
            Faculdade de Filosofia, Letras e Ciências Humanas
        </institution>
        <institution content-type="orgdiv2">
            Departamento de Vernáculos
        </institution>
        ...
    </aff>
    ...
 

Deve-se especificar a afiliação completa como aparece no documento 
original. 


.. code-block:: xml
 
     <institution content-type="original">Técnica de Cardiopneumologia. Unidade de
     Fisiopatologia Respiratória, Serviço de Pneumologia, Centro Hospitalar Lisboa
     Norte, Lisboa, Portugal. mara@scielo.org</institution>

 
.. _elemento-addr-line:
     
<addr-line>
^^^^^^^^^^^

Aparece em
  :ref:`elemento-aff`
 
Ocorre
  Zero ou mais vezes

Em ``<addr-line>``, especifica-se os dados de endereço da instituição 
vinculada ao autor, e deve aparecer quando a informação for descrita no 
artigo dentro de :ref:`elemento-aff`. Pode conter somente informações de 
estado e cidade.
 

.. _elemento-named-content:
 
<named-content>
^^^^^^^^^^^^^^^
 
Aparece em
  :ref:`elemento-addr-line`
 
Atributos obrigatórios
  1. content-type
 
Ocorre
  Zero ou mais vezes


Esta tag representa as informações de endereço que aparecem em afiliação e 
portanto irá dentro da tag de :ref:`elemento-addr-line` e obrigatoriamente 
terá o atributo ``@content-type``, podendo possuir os seguintes valores: 


+---------+------------+ 
| Valor   | Descrição  |
+=========+============+
| city    | Cidade     |
+---------+------------+
| state   | Estado     |
+---------+------------+
 

.. code-block:: xml
    
    ...
    <addr-line>
        <named-content content-type="city">
            São José do Rio Preto
        </named-content>
        <named-content content-type="state">
            São Paulo
        </named-content>
        ...
    </addr-line>
    ...
 

.. _elemento-country:

<country>
^^^^^^^^^

Aparece em
  :ref:`elemento-aff`

Atributos obrigatórios
  1. country
 
Ocorre
  Uma vez


Identifica o país da afiliação.
 
A tag deve possuir o atributo ``@country`` e nele deve ser atribuído o código 
do país de acordo com a Norma *ISO 3166*, de dois caracteres alfabéticos.

Para consultar o código do país consulte o link: 
https://www.iso.org/obp/ui/#iso:pub:PUB500001:en


Exemplo:


.. code-block:: xml

    ...
    <aff id="aff01">
        ...
        <country country="BR">Brasil</country>
        ...
    </aff>
    ...

.. note:: O uso desse elemento, ``<country>``, é obrigatório 


.. _elemento-author-notes:
 
<author-notes>
--------------       

Aparece em
  :ref:`elemento-article-meta`
 
Ocorre
  Zero ou mais vezes


A tag de notas de autor deve ser utilizada para identificar informações como 
correspondência, contribuição igualitária, conflitos de interesses, 
ou seja, notas sobre autor.

Exemplo:
 
.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <author-notes>
            <corresp id="c01"><bold>Correspondence:</bold> Maria Silva, Avenida Senador Felinto Muller,s/n - Cidade Universitária, 79070-192 Campo Grande - MS Brasil,<email>maria.ra@hotmail.com</email></corresp>
            <fn fn-type="conflict">
                <p>Conflict of interest: none</p>
            </fn>     
        </author-notes>
        ...
    </article-meta>
    ...
 
 
.. _elemento-fn:

<fn>
----

Representa um complemento ou um comentário explicativo do que está sendo 
citado no texto, e deve ser identificado de acordo com sua natureza 
ao referenciar autores ou as demais partes do texto.

.. _elemento-fn-notas-autores:

Notas de autor
^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-author-notes`

Atributos obrigatórios
  1. fn-type
 
Ocorre
  Zero ou mais vezes


Notas de rodapé de autores são notas inseridas em :ref:`elemento-author-notes` 
e que obrigatoriamente possuem o atributo ``@fn-type``. 

Os valores possíveis para o atributo ``@fn-type`` são:
 
+---------------------------+--------------------------------------------------+
| Valor                     | Descrição                                        |
+===========================+==================================================+
| author                    | Outro tipo de nota relacionado a autor           |
+---------------------------+--------------------------------------------------+
| con                       | Informação de contribuição                       |
+---------------------------+--------------------------------------------------+
| conflict                  | Declaração de conflito de Interesse              |
+---------------------------+--------------------------------------------------+
| current-aff               | Afiliação atual do autor                         |
+---------------------------+--------------------------------------------------+
| deceased                  | Pessoa morreu desde que o artigo foi escrito     |
+---------------------------+--------------------------------------------------+
| edited-by                 | Autor é o editor                                 |
+---------------------------+--------------------------------------------------+
| equal                     | Informação de contribuição igualitária           |
+---------------------------+--------------------------------------------------+
| on-leave                  | Autor está ausente (sabático ou outro)           |
+---------------------------+--------------------------------------------------+
| participating-researchers | Autor foi um pesquisador para o artigo           |
+---------------------------+--------------------------------------------------+
| present-address           | Endereço atual do autor                          |
+---------------------------+--------------------------------------------------+
| previously-at             | Afiliação anterior do autor                      |
+---------------------------+--------------------------------------------------+
| study-group-members       | Autor foi um membro do grupo de estudos para a   |
|                           | pesquisa                                         |
+---------------------------+--------------------------------------------------+
| other                     | Especifica aquelas notas diferentes das          |
|                           | relacionados acima. É possível também ter este   |
|                           | tipo de nota em :ref:`elemento-fn-group` em      |
|                           | :ref:`elemento-back`                             |
+---------------------------+--------------------------------------------------+
| presented-at              | Trabalho apresentado em Conferência, Colóquio etc|
+---------------------------+--------------------------------------------------+
| presented-by              | Informação de trabalho apresentado pelo autor    |
+---------------------------+--------------------------------------------------+
 

.. code-block:: xml
 
    ...
    <author-notes>
        <corresp id="c01">
            <label>*</label>
            <bold>Correspondence</bold>: Dr. Edmundo Figueira Departamento de Fisioterapia, Universidade FISP - Hogwarts,  Brasil. E-mail: <email>contato@contato.com</email>
        </corresp>           
        <fn fn-type="conflict">
            <p>Não há conflito de interesse entre os autores do artigo.</p>
        </fn>
        <fn fn-type="equal">
            <p>Todos os autores tiveram contribuição igualitária na criação do artigo.</p>
        </fn>
    </author-notes>
    ...
 

.. _elemento-fn-notas-gerais:

Notas gerais
^^^^^^^^^^^^

Aparece em
  :ref:`elemento-fn-group`

Atributos obrigatórios
  1. fn-type

Ocorre
  Uma ou mais vezes


Representa um complemento ou um comentário explicativo do que está sendo 
citado no texto.
 
As notas que devem ser consideradas para entrar como nota de rodapé de
:ref:`elemento-back`, são quaisquer notas que não fazem nenhum tipo de
referência aos autores, as quais deverão ser identificadas em
:ref:`elemento-fn-notas-autores`.
 
Notas em :ref:`elemento-back` devem ser identificadas dentro do grupo 
:ref:`elemento-fn-group`.
 
Consulte a :ref:`sugestao-atribuicao-id` para instruções sobre a composição do 
atributo ``@id``.
 
Para notas que apresentam uma etiqueta de identificação (1, 2, a, b, ``*``, e etc)
marque com a tag :ref:`elemento-label`. A tag :ref:`elemento-label` não
pode estar dentro de :ref:`elemento-p`.

Os valores possíveis para o atributo ``@fn-type`` são:
 
+-------------------------+--------------------------------------------------+
| Valor                   | Descrição                                        |
+=========================+==================================================+
| abbr                    | Representa abreviaturas de termos e nomes        |
|                         | próprios utilizadas ao longo do texto. Caso      |
|                         | esteja falando de abreviaturas de nomes dos      |
|                         | autores, inserir nota em                         |
|                         | :ref:`elemento-author-notes` em                  |
|                         | :ref:`elemento-front`                            |
+-------------------------+--------------------------------------------------+
| com                     | Representa nota de algum tipo de comunicado      |
|                         | relevante para a realização do artigo            |
+-------------------------+--------------------------------------------------+
| financial-disclosure    | Declaração de financiamento ou negação e         |
|                         | aceitação de recursos recebidos em apoio às      |
|                         | pesquisa em que um artigo é baseado. Serve também|
|                         | para informações de financiamento que possuem    |
|                         | um número de contrato ou que só informam se "sim"|
|                         | ou "não" houve financiamento                     |
+-------------------------+--------------------------------------------------+
| supported-by            | Indica que a pesquisa sobre a qual o artigo é    |
|                         | baseado foi apoiada por alguma entidade,         |
|                         | instituição ou pessoa física. Considerar neste   |
|                         | tipo, informações de financiamento que não       |
|                         | possuem números de contrato                      |
+-------------------------+--------------------------------------------------+
| presented-at            | Indica que o artigo foi apresentado em algum     |
|                         | evento científico                                |
+-------------------------+--------------------------------------------------+
| supplementary-material  | Indica ou descreve o material suplementar do     |
|                         | artigo                                           |
+-------------------------+--------------------------------------------------+
| other                   | Especifica aquelas notas diferentes das          |
|                         | relacionados acima. É possível também ter este   |
|                         | tipo de nota em :ref:`elemento-author-notes`     |
+-------------------------+--------------------------------------------------+
 

Exemplo:
 
.. code-block:: xml

    ... 
    <fn-group>
        <fn fn-type="financial-disclosure" id="fn01">
            <label>1</label>
            <p>Declaração de financiamento: sim</p>
        </fn>
        <fn fn-type="presented-at" id="fn02">
            <label>**</label>
            <p>Artigo foi apresentado na XVIII Conferência Internacional de Biblioteconomia 2014</p>
        </fn>
    </fn-group>
    ...
 

.. _elemento-fn-notas-tabela:

Nota de Tabela
^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-table-wrap-foot`


Atributos obrigatórios
  1. id

Ocorre
  Uma ou mais vezes

Notas de rodapé de tabelas são notas inseridas em :ref:`elemento-table-wrap-foot` e que obrigatoriamente possuem o atributo @id.
Consulte a :ref:`sugestao-atribuicao-id` para instruções sobre a composição do atributo ``@id``.


Exemplo:
 
.. code-block:: xml

    ...
    <table-wrap id="t05">
      ... 
      <table-wrap-foot>
        <fn id="TFN1">
          <label>*</label>
          <p>All diagnoses at admission (sepsis, cardiovascular, respiratory, neurological, gastrointestinal, and emergency surgery) were grouped except for elective surgery.</p>
        </fn>
      </table-wrap-foot>
    </table-wrap>
    ...


.. _elemento-corresp:

<corresp>
---------
 
Aparece em
  :ref:`elemento-author-notes`
 
Ocorre
  Zero ou mais vezes


Esta tag representa as informações de correspondência de um dos autores 
do artigo. Pode ou não possuir um :ref:`elemento-label` e também o atributo 
``@id``. É possível marcar o ``<email>`` caso inserido.
 
Consulte a :ref:`sugestao-atribuicao-id` para instruções sobre a composição do 
atributo ``@id``.
 
Exemplo:

.. code-block:: xml
 
    ...
    <author-notes>
        ...
        <corresp id="c01">Dr. Edmundo Figueira Departamento de Fisioterapia, Universidade FISP - São Paulo, Brasil. E-mail: <email>contato@contato.com</email></corresp>
        ...
    </author-notes>
    ...
 
.. note:: Esta tag não necessita da inserção de parágrafo :ref:`elemento-p`.
 
 
.. _elemento-pub-date:

<pub-date>
----------

Aparece em
  :ref:`elemento-article-meta`
 
Atributos obrigatórios
  1. pub-type='epub' ou pub-type='epub-ppub'
 
Ocorre
  Uma vez


Para a marcação da data de publicação do artigo/fascículo utiliza-se a 
tag ``<pub-date>`` a qual pode conter os elementos :ref:`elemento-day`, 
:ref:`elemento-month`, :ref:`elemento-season` e obrigatoriamente 
:ref:`elemento-year`. Esta tag deve estar acompanhada do atributo ``@pub-type``.
 
A data de publicação pode ser do tipo ``epub-ppub`` se houver uma versão 
impressa do fascículo, apenas ``epub`` para publicação digital ou em 
``ahead-of-print``.
 
Exemplo de marcação de data de publicação nas versões impressa e digital:
 
.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <pub-date pub-type="epub-ppub">
            <day>17</day>
            <month>03</month>
            <year>2014</year>
        </pub-date>
        ...
    </article-meta>
    ...

 
Os valores de dia, mês e ano devem ser representados segundo a data de publicação do fascículo, geralmente apresentado no sumário do número.
 
Exemplo de marcação de data de publicação na versão digital:
 
.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <pub-date pub-type="epub">
            <season>Jan-Feb</season>
            <year>2014</year>
        </pub-date>
        ...
    </article-meta>
    ...
 

.. _elemento-season:

<season>
^^^^^^^^

Aparece em
  :ref:`elemento-pub-date`, 
  :ref:`elemento-product`, 
  :ref:`elemento-element-citation`

Ocorre 
 Zero ou uma vez 


Esta tag pode ser encontrada em :ref:`elemento-front` 
(ver :ref:`elemento-pub-date` e :ref:`elemento-product`) ou em 
:ref:`elemento-back`, representando informações das estações do ano em um referência.


.. code-block:: xml

    ...
    <back>
        ...
        <ref-list>
            <ref>
                ...
                <season>Outono</season>
                ...
            </ref>
        </ref-list>
        ...
    </back>


.. code-block:: xml

    ...
    <front>
        ...
        <article-meta>
            ...
            <pub-date pub-type="epub">
                <season>Nov-Dec</season>
                <year>2013</year>
            </pub-date>
            ...
        </article-meta>
        ...
    </front>
    ...
          

.. note:: Para abreviatura dos meses que devem ser inseridos na data de 
          publicação dos fascículos, utilizar siglas em inglês com 3 
          caracteres, separados por hífen. As abreviaturas são: Jan, Feb, Mar,
          Apr, May, Jun, Jul, Aug, Sep, Oct, Nov e Dec.


.. _elemento-year:

<year>
^^^^^^

Aparece em
  :ref:`elemento-pub-date`, :ref:`elemento-product`, 
  :ref:`elemento-element-citation`

Ocorre 
  1. Uma vez em :ref:`elemento-front`
  2. Zero ou mais vezes em :ref:`elemento-back`


Identifica ano em referências, pode representar o ano de publicação de um 
documento, o ano de fabriação de um software, o ano da criação de uma 
base de dados e assim por diante. Também utilizada em :ref:`elemento-front` 
para identificar ano da publicação de um artigo 
(ver :ref:`elemento-pub-date`) ou de um produto (ver :ref:`elemento-product`).


.. _elemento-month:

<month>
^^^^^^^

Aparece em
  :ref:`elemento-pub-date`, :ref:`elemento-product`, 
  :ref:`elemento-element-citation`

Ocorre 
  1. Zero ou uma vez em :ref:`elemento-front`
  2. Zero ou mais vezes em :ref:`elemento-back`

Identifica o mês em referências, pode representar o mês de publicação de um 
periódico científico, o mês da realização de um relatório e assim por diante. 
Também utilizada em :ref:`elemento-front` para identificar o mês da publicação 
de um artigo (ver :ref:`elemento-pub-date`) ou de um produto 
(ver :ref:`elemento-product`).

O valor deve ser um número inteiro de 1-12.

Intervalos de meses, e.g. ``Jan-Mar``, devem ser identificados em :ref:`elemento-season`. 


.. _elemento-day:

<day>
^^^^^

Aparece em
  :ref:`elemento-pub-date`, :ref:`elemento-product`,
  :ref:`elemento-element-citation`

Ocorre 
  1. Zero ou uma vez em :ref:`elemento-front`
  2. Zero ou mais vezes em :ref:`elemento-back`


Identifica o dia em referências, pode representar o dia de publicação de 
um periódico científico, o dia da realização de um relatório e assim por 
diante. Também utilizada em :ref:`elemento-front` para identificar mês da 
publicação de um artigo (ver :ref:`elemento-pub-date`) ou de um produto 
(ver :ref:`elemento-product`).


.. _elemento-volume:

<volume>
--------

Aparece em
  :ref:`elemento-article-meta`, :ref:`elemento-element-citation`
 
Ocorre
  1. Uma vez em :ref:`elemento-front`
  2. Zero ou mais vezes em :ref:`elemento-back`
 

Representa o volume de uma publicação.
 
Caso haja suplemento de volume em :ref:`elemento-front`, este deverá ser 
identificado em :ref:`elemento-issue`. 

Exemplo ``v10s1``:
 
.. code-block:: xml
 
    ...
    <front>
        ...
        <article-meta>
            ...
            <volume>10</volume>
            <issue>suppl 1</issue>
            ...
        </article-meta>
        ...
    </front>
    ...
 
 
.. _elemento-issue:

<issue>
-------
 
Aparece em
  :ref:`elemento-article-meta`, :ref:`elemento-element-citation`
 
Ocorre
  1. Uma vez em :ref:`elemento-front`
  2. Zero ou mais vezes em :ref:`elemento-back`

 
Em caso de suplemento de número em :ref:`elemento-front`, exemplo: ``v10n5s1``:
 
.. code-block:: xml
 
    ...
    <front>
        ...
        <article-meta>
            ...
            <volume>10</volume>
            <issue>5 suppl 1</issue>
            ...
        </article-meta>
        ...
    </front>
    ...
 
Em caso de :term:`ahead-of-print`, especificar valores zerados, como segue:
 
.. code-block:: xml
 
    ...
    <front>
        ...
        <article-meta>
            ...
            <volume>00</volume>
            <issue>00</issue>
            ...
        </article-meta>
        ...
    </front>
    ...

.. note:: Para informações de suplemento em :ref:`elemento-front` não se deve 
          utilizar a tag ``<supplement>``.
 
 
.. _elemento-fpage:

<fpage>
-------

Aparece em
  :ref:`elemento-article-meta`,
  :ref:`elemento-element-citation`
 
Ocorre
  Zero ou uma vez
 

Designa-se a paginação inicial do artigo. No caso de :term:`ahead-of-print`, 
a informação deve ser preenchida com ``00``.
 
Exemplo:

.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <fpage>17</fpage>
        <lpage>21</lpage>
        ...
    </article-meta>
    ...
 
 
.. _elemento-lpage:

<lpage>
-------

Aparece em
  :ref:`elemento-article-meta`, 
  :ref:`elemento-element-citation`
 
Ocorre
  Zero ou uma vez

 
Designa-se a paginação final do artigo. No caso de :term:`ahead-of-print`, 
a informação deve ser preenchida com ``00``.
 
Exemplo:

.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <fpage>396</fpage>
        <lpage>452</lpage>
        ...
    </article-meta>
    ...
 

.. _elemento-elocation-id:

<elocation-id>
--------------

Aparece em
  :ref:`elemento-article-meta`,
  :ref:`elemento-element-citation`
 
Ocorre
  Zero ou uma vez 
 

Esta tag irá identificar uma paginação eletrônica, pode ser encontrada também 
em :ref:`elemento-element-citation`. Ela só deverá ser usada quando só houver 
um único número de paginação eletrônica, caso haja o intervalo de páginas 
deve-se optar pelo uso de :ref:`elemento-fpage` e :ref:`elemento-lpage`.
 
Exemplo:

.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <volume>00</volume>
        <issue>00</issue>
        <elocation-id>0102961</elocation-id>
        ...
    </article-meta>
    ...


.. note:: ``elocation-id`` só deve ser identificado quando não houver informação de 
          :ref:`elemento-fpage`.
 

.. _elemento-product:

<product>
---------

Aparece em
  :ref:`elemento-article-meta`
 
Atributos obrigatórios  
  1. product-type
 
Ocorre
  Zero ou mais vezes


Em ``<product>`` devem ser inseridas as informações do produto resenhado. 
É importante salientar que esta tag só deverá ser utilizada quando 
:ref:`elemento-article` possuir o atributo ``@article-type="book-review"`` ou 
``@article-type="product-review"``.

Os valores possíveis para ``@product-type`` são: 

+-----------+---------------------------------+
| Valor     | Descrição                       |
+===========+=================================+
| article   | referência de artigo            |
+-----------+---------------------------------+
| book      | referência de livro             |
+-----------+---------------------------------+
| chapter   | referência de capítulo de livro |
+-----------+---------------------------------+
| other     | outros tipos                    |
+-----------+---------------------------------+
| software  | referência de software          |
+-----------+---------------------------------+

 

.. code-block:: xml

    ...
    <article-meta>
        ...
        <product product-type="book">
            <person-group person-group-type="author">
                <name>
                    <surname>ONFRAY</surname>
                    <given-names>Michel</given-names>
                </name>
            </person-group>
            <source>La comunidad filosófica: manifiesto por una universidad popular</source>
            <year>2008</year>
            <publisher-name>Gedisa</publisher-name>
            <publisher-loc>Barcelona</publisher-loc>
            <size units="pages">155</size>
            <isbn>9788497842525</isbn>                          
            <inline-graphic>1234-5678-rctb-45-05-690-gf01.tif</inline-graphic>
        </product>
        <history>
            ...
        </history>
        ...
    </article-meta>
    ...

 
.. note:: A ordem das tags é importante! A tag ``<product>`` deve estar 
          inserida antes de :ref:`elemento-history` ou depois de 
          :ref:`elemento-fpage`.
               

.. _elemento-person-group:

<person-group>
^^^^^^^^^^^^^^ 

Aparece em
  :ref:`elemento-product`,
  :ref:`elemento-element-citation`
  
Atributos obrigatórios 
  1. person-group-type

Ocorre 
  Zero ou mais vezes


Identifica o grupo ou o indivíduo criador/elaborador do documento. 
As tags :ref:`elemento-collab`, :ref:`elemento-role`, 
:ref:`elemento-name` e :ref:`elemento-etal`, no caso de existirem, devem ser 
identificadas apenas em ``person-group``. 

Os valores possíveis para o atributo ``@person-group-type`` são:

+-----------+---------------+
| Valor     | Descrição     |
+===========+===============+
| author    | valor padrão  |
+-----------+---------------+
| compiler  | compilador    |
+-----------+---------------+
| editor    | editor        |
+-----------+---------------+
| translator| tradutor      |
+-----------+---------------+

Exemplo:
 
.. code-block:: xml

    ...
    <ref>
        <element-citation publication-type="book">
            <person-group person-group-type="author">
                <name>
                    <surname>Silva</surname>
                    <given-names>Jaqueline Figueiredo da</given-names>
                </name>
                <collab>Instituto Brasil Leitor</collab>
                ...
            </person-group>
            ...
        </element-citation>
        ...
    </ref>
    ...


.. _elemento-etal:

<etal>
^^^^^^

Aparece em
  :ref:`elemento-person-group`
  :ref:`elemento-product`

Ocorre 
  Zero ou uma vez


Esta deve deve aparecer apenas em :ref:`elemento-person-group` e é usada 
quando existirem mais de três autores, onde indica-se apenas o primeiro, 
acrescentando-se a expressão et al. que significa "entre outros". 

Esta informação aparece primordialmente em referências. 

.. note:: Quando a informação aparecer no texto da referência, não é 
          necessário envolver o texto "et al." com a tag <etal></etal>, 
          basta inserir a tag na forma ``<etal/>``.


Exemplo:

.. code-block:: xml

    ...
    <ref>
        <element-citation publication-type="book">
            <person-group person-group-type="author">
                <name>
                    <surname>Borba</surname>
                    <given-names>Quincas</given-names>
                </name>
                <etal/>
                ...
            </person-group>
            ...
        </element-citation>
        ...
    </ref>
    ...


.. _elemento-size:

<size>
^^^^^^

Aparece em
  :ref:`elemento-product`,
  :ref:`elemento-element-citation`

Atributos obrigatórios
  1. units="pages"

Ocorre 
  Zero ou mais vezes
 

Identifica a quantidade total de páginas de um documento mencionado numa 
referência. Deve ser utilizada com o atributo ``@units="pages"``.


.. _elemento-page-range:

<page-range>
^^^^^^^^^^^^

Aparece em
  :ref:`elemento-product`,
  :ref:`elemento-element-citation`
  
Ocorre 
  Zero ou uma vez


Identifica um intervalo de paginação mencionados numa referência.

Exemplo:

.. code-block:: xml

    ...
    <ref>
        <element-citation publication-type="book">
            ...
            <fpage>300</fpage>
            <lpage>420</lpage>
            <page-range>300-301, 305, 407-420</page-range>
            ...
        </element-citation>
        ...
    </ref>
    ...

.. note:: A inserção do intervalo de paginação deve ser inserido após à
          informação de última página :ref:`elemento-lpage`.


.. _elemento-isbn:

<isbn>
^^^^^^

Aparece em
  :ref:`elemento-product`,
  :ref:`elemento-element-citation`

Ocorre 
  Zero ou mais vezes


Identifica o :term:`ISBN` de um livro e é identificado numa referência ou produto.


.. _elemento-source:

<source>
^^^^^^^^

Aparece em
  :ref:`elemento-product`,
  :ref:`elemento-element-citation`

Ocorre 
  Zero ou mais vezes


Identifica o título da fonte principal de uma referência ou de um produto. 
O atributo ``@xml:lang`` não deve ser utilizado.


.. _elemento-edition:

<edition>
^^^^^^^^^

Aparece em
  :ref:`elemento-product`,
  :ref:`elemento-element-citation`
  
Ocorre 
  Zero ou mais vezes

Representa a edição de um documento de uma referência, também pode 
identificar a versão de um software ou base de dados.


.. _elemento-publisher-name:

<publisher-name>
^^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-product`, 
  :ref:`elemento-element-citation`, 
  :ref:`elemento-publisher`
  
Ocorre 
  Zero ou mais vezes


Representa o nome da casa publicadora ou editora numa referência.


.. _elemento-publisher-loc:

<publisher-loc>
^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-product`, 
  :ref:`elemento-element-citation`, 
  :ref:`elemento-publisher-loc`
  
Ocorre 
  Zero ou mais vezes


Identifica o local de uma casa publicadora ou editora.


.. _elemento-history:

<history>
---------

Aparece em
  :ref:`elemento-article-meta`
 
Ocorre
  Zero ou uma vez


Agrupa as datas em que o artigo foi recebido, aceito ou revisado. Contém 
obrigatoriamente tags :ref:`elemento-date`.
 

.. _elemento-date:
 
<date>
^^^^^^

Aparece em
  :ref:`elemento-history`
 
Atributos obrigatórios
  1. date-type="received" ou date-type="accepted" ou date-type="rev-recd"
 
Ocorre
  Uma ou mais vezes 


Em ``<date>`` deve constar obrigatoriamente a tag :ref:`elemento-year`. 
Usa-se o atributo ``@date-type`` para especificar o tipo do recebimento.

Os valores possíveis para o atributo ``@date-type`` são:

+------------+------------+
| Valor      | Descrição  |
+============+============+
| received   | recebido   |
+------------+------------+
| accepted   | aceito     |
+------------+------------+
| rev-recd   | revisado   |
+------------+------------+

.. code-block:: xml

    ...
    <article-meta>
        ...
        <history>
            <date date-type="received">
                <day>15</day>
                <month>03</month>
                <year>2013</year>
            </date>
            <date date-type="rev-recd">
                <day>06</day>
                <month>11</month>
                <year>2013</year>
            </date>  
            <date date-type="accepted">
                <day>12</day>
                <month>05</month>
                <year>2014</year>
            </date>  
        </history>
        ...
    </article-meta>
    ...
 
 
.. _elemento-permissions:

<permissions>
-------------

Aparece em
  :ref:`elemento-article-meta`
 
Ocorre
  Uma vez


A permissão é um conjunto de condições sob as quais o conteúdo do artigo 
pode ser usado, acessado e distribuído.
 
 
.. _elemento-license:

<license>
^^^^^^^^^

Aparece em
  :ref:`elemento-permissions`
 
Atributos obrigatórios
  1. license-type="open-access"
  2. xlink:href
 
Ocorre
  Uma vez


Define a licença de uso adotada pelo artigo, por meio de referência à URL onde 
o texto da licença está disponível.

Cada tipo de licença define regras que regulam o uso, distribuição e adaptação 
da obra. Para mais informações consultar: http://creativecommons.org/


Os valores possíveis para ``@xlink:href`` são:

+--------------------------------------------------------+-------------------------+
| Valor                                                  | Descrição               |
+========================================================+=========================+
| http://creativecommons.org/licenses/by/4.0/            | CC-BY versão 4.0        |
+--------------------------------------------------------+-------------------------+
| http://creativecommons.org/licenses/by/3.0/            | CC-BY versão 3.0        |
+--------------------------------------------------------+-------------------------+
| http://creativecommons.org/licenses/by-nc/4.0/         | CC-BY-NC versão 4.0     |
+--------------------------------------------------------+-------------------------+
| http://creativecommons.org/licenses/by-nc/3.0/         | CC-BY-NC versão 3.0     |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by-nc-nd/3.0/     | CC-BY-NC-ND versão 3.0  |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by-nc-nd/4.0/     | CC-BY-NC-ND versão 4.0  |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by/3.0/igo/       | BY/IGO versão 3.0       |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by-nc/3.0/igo/    | BY-NC/IGO versão 3.0    |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by-nc-nd/3.0/igo/ | BY-NC-ND/IGO versão 3.0 |
+--------------------------------------------------------+-------------------------+


Além da referência à URL, o texto da licença deve ser adicionado na tag
``<license-p>``.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <permissions>
            ...
            <license license-type="open-access"
                     xlink:href="http://creativecommons.org/licenses/by/4.0/">
                <license-p>This is an open-access article distributed under the terms of the Creative Commons Attribution License, which permits unrestricted use, distribution, and reproduction in any medium, provided the original work is properly cited.</license-p>
            </license>
        </permissions>
        ...
    </article-meta>
    ...
 
.. note:: O texto de ``<license-p>`` deve ser inserido na língua principal do artigo.
 
 
.. _elemento-copyright:

<copyright>
^^^^^^^^^^^

Aparece em
  :ref:`elemento-permissions`
 
Ocorre
  Zero ou uma vez


É possível além de :ref:`elemento-license` acrescentar outras informações 
de direitos autorais através de duas tags, são elas:
 
* ``<copyright-statement>`` para identificar a instituição a quem pertence 
  os direitos. Normalmente a informação descrita aqui vem junto com o 
  símbolo de "copyright".
* ``<copyright-year>`` para identificar o ano do direito autoral.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <permissions>
            <copyright-statement>&#x00A9; 2013 Elsevier Editora Ltda.</copyright-statement>
            <copyright-year>2013</copyright-year>
            <license license-type="open-access" 
                     xlink:href="http://creativecommons.org/licenses/by/4.0/">
                <license-p>This is an Open Access article distributed under the terms of the Creative Commons Attribution Non-Commercial License, which permits unrestricted non-commercial use, distribution, and reproduction in any medium, provided the original work is properly cited.</license-p>
            </license>
        </permissions>
        ...
    </article-meta>
    ...
 
 
.. _elemento-abstract:

<abstract>
----------

Aparece em
  :ref:`elemento-article-meta`
 
Ocorre
  Zero ou mais vezes


Tag que identifica o resumo do artigo e não deve conter informação de 
atributo ``@xml:lang``. Embora em via de regra esse elemento ocorra 
zero ou mais vezes, ele se faz obrigatório quando :ref:`elemento-article` for declarado
com o atributo ``@article-type="research-article"`` ou ``@article-type="review-article"``.
Em ``<abstract>`` deve ser inserido um elemento ``title`` para especificar o título do resumo.

Os resumos apresentados nos artigos publicados na SciELO normalmente 
apresentam-se em dois formatos:
 
* Estruturado: Quando possui seções 
  (Ex.: Introdução, Objetivos, Métodos e Resultado). Cada grupo apresentado 
  no resumo será identificado como seção e cada seção terá seu título.
 
  Exemplo:
   
  .. code-block:: xml

      ...
      <article-meta>
          ...
          <abstract>
            <title>Resumo</title>
              <sec>
                  <title>Objetivo</title>
                  <p>Verificar a sensibilidade e especificidade das curvas de fluxo-volume na detecção de obstrução da via aérea central (OVAC), e se os critérios qualitativos e quantitativos da curva se relacionam com a localização, o tipo e o grau de obstrução.</p>
              </sec>
              <sec>
                  <title>Métodos</title>
                  <p>Durante quatro meses foram selecionados, consecutivamente, indivíduos com indicação para broncoscopia. Todos efetuaram avaliação clínica, preenchimento de escala de dispneia, curva de fluxo-volume e broncoscopia num intervalo de uma semana. Quatro revisores classificaram a morfologia da curva sem conhecimento dos dados quantitativos, clínicos e broncoscopicos. Um quinto revisor averiguou os critérios morfológicos e quantitativos.</p>
              </sec>        
          </abstract>
          ...
      </article-meta>
      ...

* Simples: Quando apresenta de forma sucinta os principais pontos do 
  texto sem a divisão por seções. 
 
  Exemplo:
 
  .. code-block:: xml
   
      ...
      <article-meta>
          ...
          <abstract>
            <title>Resumo</title>
              <p>Verificar a sensibilidade e especificidade das curvas de fluxo-volume na detecção de obstrução da via aérea central (OVAC), e se os critérios qualitativos e quantitativos da curva se relacionam com a localização, o tipo e o grau de obstrução. Métodos: Durante quatro meses foram selecionados, consecutivamente, indivíduos com indicação para broncoscopia. Todos efetuaram avaliação clínica, preenchimento de escala de dispneia, curva de fluxo-volume e broncoscopia num intervalo de uma semana. Quatro revisores classificaram a morfologia da curva sem conhecimento dos dados quantitativos, clínicos e broncoscopicos. Um quinto revisor averiguou os critérios morfológicos e quantitativos.</p>
          </abstract>
          ...
      </article-meta>
      ...

 
.. _elemento-trans-abstract:

<trans-abstract>
----------------

Aparece em
  :ref:`elemento-article-meta`
 
Atributos obrigatórios
  1. xml:lang
 
Ocorre
  Zero ou mais vezes
 
Esta tag deve conter o resumo traduzido do artigo, podendo apresentar os 
formatos simples ou estruturado, da mesma maneira que o elemento :ref:`elemento-abstract`. 
Deve ser inserida imediatamente após :ref:`elemento-abstract` e obrigatoriamente 
deve conter o atributo ``@xml:lang``.

Em ``<trans-abstract>`` deve ser inserida uma informação de etiqueta ``title``.
 
 Exemplo:
   
.. code-block:: xml
    
    ...
    <article-meta>
        ...
        <trans-abstract xml:lang="en">
            <title>Abstract</title>
            <sec>
                <title>Objective</title>
                <p>To analyze the association between socioeconomic situation, clinical characteristics referred and the family history of cardiovascular disease, with the Self-perceived health of young adults education and their implications for clinical characteristics observed.</p>
            </sec>
            <sec>
                <title>Method</title>
                <p>Analytical study conducted with 501 young adults who are students in countryside city in the Brazilian Northeast. We used binary logistic regression.</p>
            </sec>        
        </trans-abstract>
        ...
    </article-meta>
    ...


* Simples: Quando apresenta de forma sucinta os principais pontos do 
  texto sem a divisão por seções. 
 
  Exemplo:
 

.. code-block:: xml
   
    ...
    <article-meta>
        ...
        <trans-abstract xml:lang="en">
            <title>Abstract</title>
            <p>In this paper we discuss the tutoring model adopted by the Public Institutions of Higher Education that integrate the Open University of Brazil (Universidade Aberta do Brasil - UAB) program. The starting point is the research and the actions developed by the authors in the past decade that are directly related to distance education in Brazil. The focus is on the classroom tutors who are responsible for assisting students in the presential center where they have support and who are selected through publishe.. notes in the virtual notice board of the institutions that offer higher education courses in a distinct mode of classroom teaching.</p>
        </trans-abstract>
        ...
    </article-meta>
    ...


.. _elemento-kwd-group:

<kwd-group>
-----------

Aparece em
  :ref:`elemento-article-meta`
 
Atributos obrigatórios
  1. xml:lang
 
Ocorre
  Zero ou mais vezes


Identifica o grupo de palavras-chave do artigo por idioma. Obrigatoriamente deve 
conter o atributo ``@xml:lang``.
Em ``<kwd-group>`` deve ser inserida uma informação de etiqueta ``title``. 

.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <kwd-group xml:lang="pt">
            <title>Palavra-chave</title>
            <kwd>Broncoscopia</kwd>
        </kwd-group>
        ...
    </article-meta>
    ...
 
 
.. _elemento-kwd:

<kwd>   
^^^^^

Aparece em
  :ref:`elemento-kwd-group`
 
Ocorre
  Uma ou mais vezes


Esta tag é inserida obrigatoriamente dentro da tag :ref:`elemento-kwd-group` e 
identifica cada palavra-chave individualmente.
 
Exemplo:

.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <kwd-group xml:lang="pt">
            <title>Palavras-chave</title>
            <kwd>Broncoscopia</kwd>
            <kwd>Curvas de fluxo-volume expiratório máximo</kwd>
            <kwd>sensibilidade e especificidade</kwd>
            <kwd>Neoplasias pulmonares</kwd>    
        </kwd-group>
        <kwd-group xml:lang="en">
            <title>Keywords</title>
            <kwd>Bronchoscopy</kwd>
            <kwd>Maximal expiratory flow-volume curves</kwd>
            <kwd>Sensitivity and specificity</kwd>
            <kwd>Lung neoplasms</kwd>
        </kwd-group>
        ...
    </article-meta>
    ...
 
 
.. _elemento-funding-group:

<funding-group>
---------------
 
Aparece em
  :ref:`elemento-article-meta`
 
Ocorre
  Zero ou uma vez


Somente quando há número de contrato explicitado no artigo. As informações de 
financiamento podem aparecer nas tags :ref:`elemento-fn` ou :ref:`elemento-ack`.
 
.. note:: ``<funding-group>`` deve ser inserida entre as tags 
          :ref:`elemento-kwd-group` e :ref:`elemento-counts`.
 
 
.. _elemento-award-group:

<award-group>
^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-funding-group`
 
Ocorre
  Zero ou mais vezes


Um artigo pode ter diversos financiadores. Cada grupo de dados de 
financiamento será identificado pela tag ``<award-group>``.
 

.. _elemento-funding-source:
 
<funding-source>
^^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-award-group`
 
Ocorre
  Uma ou mais vezes


Esta tag deve ficar dentro de :ref:`elemento-award-group` e nela será 
especificado o órgão e/ou instituição financiadora:
 
Exemplo:

.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <funding-group>           
            <award-group>
                <funding-source>CNPq</funding-source>
                <award-id>1685X6-7</award-id>
            </award-group>
        </funding-group>
        ...
    </article-meta>
    ...
 

Existem casos em que há mais que uma instituição financiadora para um único número de contrato.

Exemplo:

.. code-block:: xml

    ...
    <article-meta>
       ...
       <funding-group>
          <award-group>
             <funding-source>CNPq</funding-source>
             <funding-source>FAPESP</funding-source>
             <award-id>#09/06953-4</award-id>
          </award-group>
       </funding-group>
       ...
    </article-meta>
    ...

.. _elemento-award-id:
 
<award-id>
^^^^^^^^^^

Aparece em
  :ref:`elemento-award-group`
 
Ocorre
  Uma ou mais vezes


Esta tag deve ficar dentro de :ref:`elemento-award-group` e nela será 
especificado o número de contrato estipulado pela instituição financiadora.
 
Exemplo:

.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <funding-group>           
            <award-group>
                <funding-source>CNPq</funding-source>
                <award-id>00001</award-id>
                <award-id>00002</award-id>
            </award-group>
            <award-group>
                <funding-source>FAPESP</funding-source>
                <award-id>0000X</award-id>
            </award-group>
        </funding-group>
        ...
    </article-meta>
    ...
     
 
 
.. _elemento-funding-statement:

<funding-statement>
^^^^^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-funding-group`
 
Ocorre
  Zero ou uma vez


Representa os dados de financiamento exatamente como apresentado na nota de rodapé.

Está tag só deverá ser inserida quando as informações de financiamento forem 
apresentadas em notas de rodapé (:ref:`elemento-fn`). 
 
Exemplo:
 
.. code-block:: xml
    
    <front>
        ...
        <article-meta>
            ...
            <kwd-group>
                ...
            </kwd-group>
            <funding-group>           
                <award-group>
                    <funding-source>Coordenação de Aperfeiçoamento de Pessoal de Nível Superior</funding-source>
                    <award-id>04/08142-0</award-id>
                </award-group>
                <funding-statement>This study was supported in part by Coordenação 
                de Aperfeiçoamento de Pessoal de Nível Superior (Capes — Brasília, 
                Brazil), Fundação de Amparo à Pesquisa do Estado de São Paulo (FAPESP — 
                Grant no. 04/08142-0; São Paulo, Brazil)</funding-statement>
            </funding-group>    
            ...
        </article-meta>
        ...
    </front>
    ...
    <back>
        ...
        <fn-group>
            <fn id="fn01" fn-type="financial-disclosure">
                <p>This study was supported in part by Coordenação de Aperfeiçoamento 
                de Pessoal de Nível Superior (Capes — Brasília, Brazil), Fundação 
                de Amparo à Pesquisa do Estado de São Paulo (FAPESP — 
                Grant no. 04/08142-0; São Paulo, Brazil)</p>
            </fn>
        </fn-group>
        ...
    </back>
 

.. note:: nota de rodapé com informação de instituição financiadora e número de contrato
          deve ser identificado dentro de :ref:`elemento-back` em :ref:`elemento-fn-group` com o 
          tipo ``@fn-type="financial-disclosure"`` e em :ref:`elemento-front`.
 
.. note:: Notas SEM NÚMERO DE CONTRATO, ficam apenas em :ref:`elemento-back` mas com 
          tipo ``@fn-type="supported-by"``.
 
 
.. _elemento-counts:

<counts>
--------

Aparece em
  :ref:`elemento-article-meta`
 
Ocorre
  Uma vez


Na elaboração do XML alguns dados são importantes para determinar a 
quantidade de elementos presentes no artigo, por isso utiliza-se a tag 
``<counts>`` para contabilizar o número exato de tabelas, figuras, 
referências, equações e páginas presentes no arquivo. Esta tag deve ser 
inserida como último item de :ref:`elemento-article-meta`.
 
Os elementos que identificam os totais são:

* ``<fig-count>``: Total de figuras no documento
* ``<table-count>``: Total de tabelas no documento
* ``<equation-count>``: Total de equações do documento
* ``<ref-count>``: Total de referências no documento
* ``<page-count>``: Total de páginas do artigo
 
Exemplo:

.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <counts>
            <fig-count count="5"/>
            <table-count count="3"/>
            <equation-count count="10"/>
            <ref-count count="26"/>
            <page-count count="6"/>
        </counts>
    </article-meta>
    ...
 
.. note:: A ordem dos elementos é importante.
.. note:: No caso de o documento não apresentar alguns dos elementos contabilizados,
          o valor dos respectivos atributos ``@count`` deve ser ``0``. e.g.
          ``<equation-count count="0"/>``.

 
.. _elemento-body:

<body>
======

Aparece em
  :ref:`elemento-article`

Ocorre
  Uma vez


O body compreende o conteúdo e desenvolvimento do artigo.
 
.. note:: Informamos que as tabelas, figuras e equações que não estão em 
          ``app-group``, devem ser inseridas obrigatoriamente após 
          a primeira chamada no texto. Para material suplementar, analisar e 
          identificar conforme o PDF.
 
.. _elemento-sec:

<sec>
-----
Aparece em
  :ref:`elemento-body`

Ocorre
  Zero ou mais vezes

 
O corpo textual do artigo pode ser constituído por seções. 
Cada uma delas possui um elemento ``<title>`` seguido de um ou mais 
:ref:`elemento-p`.

:term:`Seções de primeiro nível` podem ser qualificadas de acordo com seu tipo por 
meio do atributo ``@sec-type``, cujos valores possíveis são:

+------------------------+------------------------------------------------+
| Valor                  | Descrição                                      |
+========================+================================================+
| cases                  | relatos/estudos de caso                        |
+------------------------+------------------------------------------------+
| conclusions            | conclusões/considerações finais/Final Remarkes |
+------------------------+------------------------------------------------+
| discussion             | discussões                                     |
+------------------------+------------------------------------------------+
| intro                  | introdução/sinopse                             |
+------------------------+------------------------------------------------+
| materials              | materiais                                      |
+------------------------+------------------------------------------------+
| methods                | metodologia/método                             |
+------------------------+------------------------------------------------+
| results                | resultados                                     |
+------------------------+------------------------------------------------+
| supplementary-material | material suplementar                           |
+------------------------+------------------------------------------------+

 
Exemplo:
 
.. code-block:: xml
 
    ...
    <body>
        ...
        <sec sec-type="intro">
            <title>Introduction</title>
            <p>Central airway obstruction (CAO) is a pathological process that leads to airflow limitation at the level of the glottis, subglottis, trachea, and main bronchi. Correct diagnosis and treatment of CAO is an area of interest and concern for health professionals,given that this disease has the potential to cause significant morbidity and mortality.</p>
            ...
        </sec>
        ...
    </body>
    ...
 

No caso de seções combinadas, ou seja, quando o título for composto por mais 
de um desses itens, o valor do atributo ``@sec-type`` deverá corresponder a 
cada um respectivamente, separados pelo caractere ``|``.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <body>
        ...
        <sec sec-type="materials|methods">
            <title>Materials and Methods</title>
            <p>Between November of 2009 and April of 2010, we conducted a prospective, observational, cross-sectional study. The target population consisted of patients for whom bronchoscopy was clinically indicated. The patients were consecutively selected for the sample on the...</p>
            ...
        </sec>
        ...
    </body>
    ...

 
As seções podem ser compostas por uma ou mais subseções, neste caso, 
cada subseção deverá ser marcada com tag ``<sec>`` dentro da seção maior.
 
Exemplo:
 
.. code-block:: xml

    ...
    <body>
        ...
        <sec sec-type="methods">
            <title>Methodology</title>
            <sec>
                <title>Methodology in Science</title>
                <p>Each patient underwent a brief physical examination, and the degree of dyspnea was determined by the Medical Research Council (MRC) 5-point scale.</p>
                ...
            </sec>
        </sec>
        ...
    </body>
    ...

 
No caso da seção não possuir nenhum tipo padrão pode-se inserir a tag sem o 
atributo ``@sec-type``. 

Exemplo:
 
.. code-block:: xml
 
    ...
    <body>
        ...
        <sec>
            <title>Biologia Marinha</title>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi pharetra lacinia orci at adipiscing.</p>
            ...
        <sec>
        ...
    </body>
    ...

 
Para seções que apresentam marcador de numeração, identificar o dado dentro da tag <title>.
Exemplo:

.. code-block:: xml

    ...
    <body>
        ...
        <sec sec-type="intro">
            <title>1. Introdução</title>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris non sollicitudin nulla.</p>
            ...
        </sec>
        ...
    </body>
    ...


.. note:: Não inserir a tag <label> para <sec>.


.. _elemento-disp-formula:
     
<disp-formula>
--------------

Aparece em
  :ref:`elemento-body`,
  :ref:`elemento-p`,
  ``<th>``,
  ``<td>``,
  :ref:`elemento-app`,
  :ref:`elemento-supplementary-material`

Atributos obrigatórios
  1. id (ver :ref:`sugestao-atribuicao-id`)
 
Ocorre
  Zero ou mais vezes


Tag para identificar equações em parágrafos no texto, podem ser 
apresentadas como imagem ou codificadas e serão identificadas pela tag 
``<disp-formula>``. Se a equação for capturada como imagem, deve-se incluir o 
nome do arquivo em ``<graphic>``:
 
 
Exemplo:

.. code-block:: xml
 
    ...        
    <p>The Eh measurements were recalculated to the standard hydrogen potential (Standard Hydrogen Electrode - SHE), using the following <xref ref-type="disp-formula" rid="e01">equation 1</xref>(in mV):</p>
    <disp-formula id="e01">
        <graphic xlink:href="1234-5678-rctb-45-05-0110-e01.tif"/>
    </disp-formula>
    ...
 
Exemplo:
 
.. code-block:: xml
 
    <!-- codificar: σˆ2 -->

    ... 
    <xref ref-type="disp-formula" rid="e07">Equation 3</xref>
    <disp-formula>
        <mml:math id="e03">
            <mml:mrow>
                <mml:msup>
                    <mml:mover accent="true">
                        <mml:mi>σ</mml:mi>
                        <mml:mo>ˆ</mml:mo>
                    </mml:mover>
                    <mml:mn>2</mml:mn>
                </mml:msup>
            </mml:mrow>
        </mml:math>
    </disp-formula>
    ...
 

.. _elemento-inline-graphic:
 
<inline-graphic>
----------------
 
Aparece em
  :ref:`elemento-product`, 
  :ref:`elemento-body`,
  :ref:`elemento-p`,
  :ref:`elemento-sec`,
  ``th``,
  ``td``
 
Ocorre
  Zero ou mais vezes


Elemento utilizado para identificar equações em imagem que estejam posicionadas em linha, ou seja, em meio a um parágrafo.
 
Consulte a :ref:`sugestao-atribuicao-id` para instruções sobre a composição do atributo ``@id``.
 
Exemplo:

.. code-block:: xml
 
    ...
    <p>We also used an enrichment factor for surface waters (EF<sub>w</sub>) based on the equation:<inline-graphic xlink:href="1234-5678-rctb-45-05-0110-e01.tif"/>. The EF<sub>s</sub> and EF<sub>w</sub> quantified the concentration of the element of interest (C<sub>i</sub>) in the sample, in relation to the (natural) geochemical background.</p>
    ...


.. _elemento-inline-formula:
 
<inline-formula>
----------------
 
Aparece em
  :ref:`elemento-product`, 
  :ref:`elemento-body`,
  :ref:`elemento-p`,
  :ref:`elemento-sec`,
  ``th``,
  ``td``
 
Ocorre
  Zero ou mais vezes


Elemento utilizado para identificar equações codificadas em linha. Nesse caso, a codificação pode ser feita de acordo com :term:`W3C` em linguagem :term:`MathML` 
(http://www.w3.org/TR/MathML3/), sendo o elemento base ``<mml:math>`` ou com outros tipos de codificação, exemplo: caracteres ASCII, TeX ou LaTeX.
 
**Exemplo**: para codificar  σˆ2*
 
.. code-block:: xml

    ... 
    <inline-formula>
        <mml:math id="e03">
            <mml:mrow>
                <mml:msup>
                    <mml:mover accent="true">
                        <mml:mi>σ</mml:mi>
                        <mml:mo>ˆ</mml:mo>
                    </mml:mover>
                    <mml:mn>2</mml:mn>
                </mml:msup>
            </mml:mrow>
        </mml:math>
    </inline-formula>
    ...
 
 
.. _elemento-table-wrap:

<table-wrap>
------------

Aparece em
  :ref:`elemento-app`,
  ``app-group``,
  :ref:`elemento-body`,
  :ref:`elemento-glossary`,
  :ref:`elemento-p`,
  :ref:`elemento-sec`,
  :ref:`elemento-supplementary-material`,


Atributos obrigatórios
  1. id (ver :ref:`sugestao-atribuicao-id`)
 
Ocorre
  Zero ou mais vezes


É utilizada para especificar todas as partes de uma única tabela, incluindo 
:ref:`elemento-label`, :ref:`elemento-caption` ou :ref:`elemento-table-wrap-foot`. 
 
 
.. _elemento-table-wrap-foot:

<table-wrap-foot>
^^^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-table-wrap`

Ocorre
  Zero ou mais vezes


Em ``<table-wrap-foot>`` é possível fazer a identificação de nota de rodapé de 
tabela por meio de tags :ref:`elemento-fn`, que devem apresentar obrigatoriamente o 
atributo ``@id``.
 
Consulte a :ref:`sugestao-atribuicao-id` para instruções sobre a composição do 
atributo ``@id``.
 
A nota de rodapé poderá ser relacionada com alguma informação no corpo da tabela.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <table-wrap id="t01">
        <label>Table 1</label>
        <caption>
            <title>Título da tabela.</title>
        </caption>
        <table>
            ...
        </table>
        <table-wrap-foot>
            <fn id="TFN01">
                <label>*</label>
                <p>text</p>
            </fn>
        </table-wrap-foot>
    </table-wrap>
    ...
 

.. elemento-table:

<table>
^^^^^^^
 
Aparece em
  :ref:`elemento-table-wrap`

Ocorre
  Uma vez


Tabela codificada conforme o padrão :term:`NISO JATS table model`, com a adição 
das regras:

* O primeiro nível da estrutura não pode conter o elemento ``<tr>``, i.e. 
  ``//table/tr``.
* Elemento ``<th>`` apenas como descendente de ``<thead>``.
* Elemento ``<td>`` apenas como descendente de ``<tbody>``.


Toda a formatação para exibição deve ser realizada conforme descrito no guia 
`Table Formatting <http://jats.nlm.nih.gov/publishing/tag-library/1.0/n-unw2.html#pub-tag-table-format>`_.


.. _elemento-supplementary-material:

<supplementary-material>
------------------------

Aparece em
  :ref:`elemento-article-meta`,
  :ref:`elemento-p`,
  :ref:`elemento-app`

Atributos obrigatórios
  1. id (ver :ref:`sugestao-atribuicao-id`)
  2. xlink:href
  3. mimetype
  4. mime-subtype
 
Ocorre
  Zero ou mais vezes


O material suplementar é um documento que não faz parte do texto do artigo, 
mas que serviu como apoio para sua elaboração.
Em ``<supplementary-material>`` é possível especificar tabelas, figuras, 
dados brutos de planilha, banco de dados de genomas, quiz, equações, links, 
diálogos, listas, licenças e objetos multimídia como áudio e vídeo.
 
O material suplementar pode estar em :ref:`elemento-front`, dentro de 
:ref:`elemento-article-meta`, em :ref:`elemento-body` como seção ou entre 
parágrafos ou em :ref:`elemento-back`, onde só poderá ser identificado caso 
esteja especificado dentro do grupo de apêndices ``app-group``.
 
Seus atributos obrigatórios são:
 
* ``@id``: Utilizado como um identificador único no documento e ganha maior 
  importância quando há mais que um material suplementar e/ou quando o material 
  suplementar é referenciado no corpo do texto. Nesse caso é necessário relacionar 
  a chamada no texto com o "id" do material suplementar.
* ``@mimetype``: Utilizado para especificar o tipo de mídia como "vídeo" ou "aplicação".
* ``@mime-subtype``: Utilizado para especificar o formato da mídia.
* ``@xlink:href``: Utilizado para indicar do nome completo do arquivo, tais como: pdf, vídeo, zip etc.
 

.. code-block:: xml

    ...
    <front>
        ...
        <article-meta>
            ...
            <fpage>237</fpage>
            <lpage>259</lpage>
            <supplementary-material id="suppl01" mimetype="application" mime-subtype="pdf" xlink:href="1234-5678-rctb-45-05-0110-suppl01.pdf"/>
            ...
        </article-meta>
        ...
    </front>
    <body>
        ...
        <p>
            <supplementary-material id="suppl02" mimetype="image" mime-subtype="tiff" xlink:href="11234-5678-rctb-45-05-0110-suppl01.tif">
                <label>Fig 1.</label>
                <caption>
                    <title>Supplementary material A</title>
                </caption>
            </supplementary-material>
        </p>
        ...
        <p> 
            <supplementary-material id="suppl03" mimetype="application" mime-subtype="pdf" xlink:href="1234-5678-rctb-45-05-0110-suppl01.pdf"/>
        </p>
        ...
    </body>
    <back>
        <app-group>
            <app>
                <label>S-1</label>
                <supplementary-material id="suppl04" mimetype="image" mime-subtype="tiff" xlink:href="11234-5678-rctb-45-05-0110-suppl01.tif">
                    <label>Fig 1.</label>
                    <caption>
                        <title>Supplementary material A</title>
                    </caption>
                </supplementary-material>
            </app>
            <app>
                <label>S-2</label>
                <supplementary-material id="suppl05" mimetype="image" mime-subtype="tiff" xlink:href="11234-5678-rctb-45-05-0110-suppl02.tif"/>
            </app>
        </app-group>
        ...
    </back>
    ...


.. note:: Esta tag em :ref:`elemento-front` obrigatoriamente deve ser inserida abaixo das 
          informações de paginação ou antes de :ref:`elemento-history`.


.. _elemento-inline-supplementary-material:

<inline-supplementary-material>
-------------------------------

Aparece em
  :ref:`elemento-article-meta`, 
  :ref:`elemento-p`, 
  :ref:`elemento-app`
 
Atributos obrigatórios
  1. xlink:href
  2. mimetype
  3. mime-subtype
 
Ocorre
  Zero ou mais vezes

Esta tag tem a mesma função da tag :ref:`elemento-supplementary-material`, mas é 
utilizada quando a menção do material suplementar está em linha, ou seja descrita 
em um parágrafo.

Seus atributos obrigatórios são:

* ``@mimetype:``: Utilizado para especificar o tipo de mídia como “vídeo”, “aplicação” dentre outros.
* ``@mime-subtype``: Utilizado para especificar o formato da mídia.
* ``@xlink:href``: Utilizado para indicar do nome completo do arquivo, tais como: pdf, vídeo, zip e etc.


.. note:: Para consultar valores dos atributos ``@mimetype`` e ``@mime-subtype``, 
          consultar http://www.iana.org/assignments/media-types/media-types.xhtml

Exemplo 1:

.. code-block:: xml

    <p>Devido a esse elevado percentual de dados omissos, possivelmente não influenciaram no resultado final do <inline-supplementary-material xlink:href="0103-507X-rbti-26-02-0130-suppl1.pdf" mimetype="application" mime-subtype="pdf">Material Suplementar</inline-supplementary-material></p>


Exemplo 2:

.. code-block:: xml

    <p>Nunc faucibus orci ut bibendum mollis. Nunc rutrum ullamcorper neque sit amet venenatis. Praesent mattis <inline-supplementary-material xlink:href="0103-507X-rbti-26-02-0130-suppl1.pdf" mimetype="video" mime-subtype="avi"/> elit id augue tincidunt, sit amet ornare nibh laoreet. Morbi et odio a libero facilisis dapibus id vitae orci.</p>


.. _elemento-disp-quote:

<disp-quote>
------------

Aparece em
  :ref:`elemento-p`
 
Ocorre
  Zero ou mais vezes


Quando há no texto uma citação de outra fonte utiliza-se a tag 
``<disp-quote>``. Geralmente essa informação é apresentada com algum 
recuo, possui mais de três linhas e fonte de tamanho diferente, tendo essa 
informação já destacada a identificação deve ser:
 
Exemplo:
 
.. code-block:: xml
 
    <p>In the face of the failure of the transmission argument Wright would, apparently, endorse the view that Caution could still provide an adequate route to an anti-realist account of necessity, as can be gathered from the following passage:</p>
    <p>
        <disp-quote>
            <p>We suppose (i) that a priori judgement will play a part in the operation of any coherent system of belief, and (ii) that non-cognitivism about necessity had probably better grant a role for judgements of necessity as co-ordinate to (some) a priori judgements. If supposition (i) is wrong, then global Caution about necessitated judgements is, after all, at the service of the non-cognitivist about necessity</p>
        </disp-quote>
    </p>
    <p>I disagree. In the previous section we saw that showing that Caution is an incoherent attitude is not an easy matter.</p>
 
 
.. _elemento-ext-link:

<ext-link>
----------

Aparece em
  :ref:`elemento-p`,
  :ref:`elemento-element-citation`, 
  :ref:`elemento-comment`,

Atributos obrigatórios
  1. ext-link-type="uri"
  2. xlink:href
 
Ocorre
  Zero ou mais vezes

Utilizado para especificar referências a recursos disponíveis na internet.

Exemplo:
 
.. code-block:: xml
 
    ...
    <p>Neque porro quisquam est <ext-link ext-link-type="uri" xlink:href="http://www.scielo.org">www.scielo.org</ext-link> qui dolorem ipsum quia</p>
    ...
 
.. note:: O prefixo ``http://`` deve estar sempre presente no ``@xlink:href``.
 
 
.. _elemento-list:

<list>
------

Aparece em
  :ref:`elemento-p`, ``<list-item>``, :ref:`elemento-disp-quote`

Atributos obrigatórios
  1. list-type

Ocorre
  Zero ou mais vezes


Uma lista contendo dois ou mais itens. Pode conter opcionalmente um elemento
``<title>`` ou um elemento ``<label>``, exclusivamente.

O elemento ``<label>`` deve ser utilizado para identificar a etiqueta que pode 
acompanhar a lista. São consideradas etiqueta: legenda de equação, figura, 
referência, etc. 
 
O atributo ``@list-type`` especifica o prefixo a ser utilizado no marcador da 
lista. Os valores possíveis são:

+----------------+-------------------------------------------------------------------+
| Valor          | Descrição                                                         |
+================+===================================================================+
| order          | Lista ordenada, cujo prefixo utilizado é um número ou letra       |
|                | dependendo do estilo.                                             |
+----------------+-------------------------------------------------------------------+
| bullet         | Lista desordenada, cujo prefixo utilizado é um ponto, barra ou    |
|                | outro símbolo.                                                    |
+----------------+-------------------------------------------------------------------+
| alpha-lower    | Lista ordenada, cujo prefixo é um caractere alfabético minúsculo. |
+----------------+-------------------------------------------------------------------+
| alpha-upper    | Lista ordenada, cujo prefixo é um caractere alfabético maiúsculo. |
+----------------+-------------------------------------------------------------------+
| roman-lower    | Lista ordenada, cujo prefixo é um numeral romano minúsculo.       |
+----------------+-------------------------------------------------------------------+
| roman-upper    | Lista ordenada, cujo prefixo é um numeral romano maiúsculo.       |
+----------------+-------------------------------------------------------------------+
| simple         | Lista simples, sem prefixo nos itens.                             |
+----------------+-------------------------------------------------------------------+
 
 
Exemplo::
 

  Lista Numérica:

  1. Nullam gravida tellus eget condimentum egestas.
    1.1. Curabitur luctus lorem ac feugiat pretium.
  2. Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.
 
Deve ser identificada como:

.. code-block:: xml
 
    ...
    <list list-type="order">
        <title>Lista Númerica</title>
        <list-item>
            <p>Nullam gravida tellus eget condimentum egestas.</p>
        </list-item>
        <list-item>
            <list list-type="order">
                <list-item>
                    <p>Curabitur luctus lorem ac feugiat pretium.</p>
                </list-item>
            </list>
        </list-item>
        <list-item>
            <p>Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.</p>
        </list-item>
    </list>
    ...
 
.. note:: Note que o marcador não deve ser identificado como parte do texto no 
          elemento ``<list-item>``.

 
.. _elemento-caption:

<caption>
---------
 
Aparece em
  :ref:`elemento-disp-formula`,
  :ref:`elemento-fig`, 
  :ref:`elemento-table-wrap`,
  :ref:`elemento-media`,
  :ref:`elemento-supplementary-material`

Ocorre
  Zero ou mais vezes


Tag que representa uma descrição de tabela, figura ou objeto similar.
 
Obrigatoriamente dentro de ``<caption>`` deve-se conter a tag de ``<title>`` 
com a descrição textual da legenda dos objetos mencionados.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <fig id="f03">
        <label>Figura 3</label>
        <caption>
            <title>Percentual de atividade mitocondrial (método MTT) das células dos diferentes grupos experimentais em relação às células do grupo controle</title>
        </caption>
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
    </fig>
    ...
 

.. _elemento-fig:

<fig>
-----

Aparece em
  :ref:`elemento-p`,
  :ref:`elemento-app`,
  :ref:`elemento-supplementary-material`

Atributos obrigatórios
  1. id (ver :ref:`sugestao-atribuicao-id`)
 
Ocorre
  Zero ou mais vezes


As figuras de um artigo são identificadas por meio da tag ``<fig>``. 
Com essa tag é possível especificar label, caption, graphic, links, e objetos 
multimídia como vídeo, áudio e filme.
 
As imagens podem ter ou não legendas. Para imagens sem legendas é necessário 
marcá-la como ``<fig>`` e identificá-la com a tag ``<graphic>``.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <fig id="f01">
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
    </fig>
    ...
 
A tag ``<graphic>`` é utilizada para identificar alguns tipos de 
arquivos. Seus atributos são:
 
* **@xlink:href:** utilizado para especificar o nome completo da imagem referenciada
 
Para figuras com legendas a marcação deve envolver toda a informação de 
imagem, inclusive sua descrição, com a tag ``<fig>``. Dentro de ``<fig>`` 
serão identificados o rótulo da figura :ref:`elemento-label` e mais a tag de 
:ref:`elemento-caption` com a tag ``<title>`` com o título da figura.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <fig id="f01">
        <label>Fig. 1</label>
        <caption>
            <title>título da imagem</title>
        </caption>
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
    </fig>
    ...
 
Essa tag pode ter os seguintes atributos: ``@fig-type``, ``@id``, ``@xml:lang``. 
Os atributos mais frequentes são:
 
* **@fig-type:** utilizado para especificar o tipo de imagem. Os tipos 
  podem ser muitos como: Graphic, Cartoon, Chart, Diagram, Drawing, Exihibit, 
  Illustration, Map etc. Contudo o tipo só será definido caso o label da 
  figura apresente um tipo diferente de "fig." "figure".
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <fig fig-type="map" id="f01">
        <label>Map 1</label>
        <caption>
            <title>Título do Mapa<title>
        </caption>
    </fig>
    ...
 
Se a figura não possuir um tipo específico, deve-se manter a tag sem o atributo.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <fig id="f01">
        <label>Fig 1</label>
        <caption>
            <title>Título da Figura<title>
        </caption>
    </fig>
    ...
 
* **@id:** identificador da tag. É possível fazer referência cruzada no 
  documento; esse atributo deve ter valor único no arquivo e é possível 
  fazer link relacionado a um "rid".
 
 
Exemplo:

.. code-block:: xml
 
    ...
    <fig id="f01">
        <label>FIGURE 1</label>
        <caption>
            <title>Título da figura</title>
        </caption>
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
    </fig>

 
 
.. _elemento-attrib:

<attrib>
--------

Aparece em
  :ref:`elemento-boxed-text`
  :ref:`elemento-fig`
  ``<graphic>``
  :ref:`elemento-media`
  :ref:`elemento-supplementary-material`
  :ref:`elemento-table-wrap`
  :ref:`elemento-verse-group`

Ocorre

  Zero ou mais vezes


Elemento utilizado para identificar a descrição da fonte, nome de autor de poesias, agradecimentos, material de direitos autorais, ou outras informações. Geralmente utilizado para especificação de fonte de imagens e para identificar o autor de uma poesia ou verso.


Exemplo em figura:
 
.. code-block:: xml

    ...
    <fig id="f02" fig-type="other">
      <label>Figure 2</label>
        <caption>
          <title>Produtividade das variantes lexicais para a questão 132 do QSL segundo a região administrativa</title>
        </caption>
        <graphic xlink:href="0103-507X-rbti-26-02-0130-g02.tif"/>
        <attrib>Fonte: Banco de dados do ALiB (2013).</attrib>
    </fig>

.. note:: em figuras o elemento :ref:`elemento-attrib` deve ser inserido abaixo de ``<graphic>``.


Exemplo em versos:

.. code-block:: xml

    ...
    <verse-group>
        <verse-line>Porque quando te não vejo, deixastes de existir.</verse-line>
        <verse-line>E se se tem saudades do que não existe,</verse-line>
        <verse-line>Sinto-a em relação a cousa nenhuma;</verse-line>
        <verse-line>Não é do navio, é de nós, que sentimos saudade.</verse-line>
        <attrib>(Alberto Caeiro, O guardador de rebanhos e outros poemas).</attrib>
    </verse-group>
    ...


.. _elemento-media:

<media>
-------

Aparece em
  :ref:`elemento-p`,
  :ref:`elemento-fig`,
  :ref:`elemento-app`,

Atributos obrigatórios
  1. mime-subtype
  2. xlink:href
  3. mime-type
 
Ocorre
  Zero ou mais vezes


A tag ``<media>`` é utilizada para especificar arquivos multimídia como:

- vídeo
- áudio
- filmes
- animações
 
Atributos
 
- ``@id``

Para composição do ``@id`` de ``<media>`` utiliza-se o seguinte padrão:
``m`` + o número de ordem da media:

**Exemplo:** m01... m10, m11;

- **@mimetype:** utilizado para especificar o tipo de mídia como "vídeo" ou "aplicação".

- **@mime-subtype:** utilizado para especificar o formato da mídia.

Exemplo:
 
.. code-block:: xml
 
    <media mimetype="video" 
           mime-subtype="mp4" 
           xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/>
 

- @mimetype
    utilizado para especificar o tipo de mídia como "vídeo" ou "aplicação".
 
Exemplo:
 
.. code-block:: xml
 
    <media mimetype="video" 
           mime-subtype="mp4" 
           xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/>
 

- **@xlink:href:** indica o link de um arquivo multimídia.
 
Exemplo:
 
.. code-block:: xml
 
    <media mimetype="video"  
           mime-subtype="mp4" 
           xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/>
 

Exemplo:
 
*Em parágrafo:*
 
.. code-block:: xml
 
    <p>Within the limitations of this study, it may be concluded that remaining 
    tooth wall thickness did not influence the fatigue resistance of 
    molars restored with CAD/CAM ceramic inlays <media mimetype="video"  
    mime-subtype="mp4" xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/></p>
 

*Em figuras:*
 
.. code-block:: xml
 
    <p>
        <fig id="f01">
            <label>Figure 1</label>
            <caption>
                <title>descrição da fig.<title>
            </caption>
            <media xlink:href="1234-5678-rctb-45-05-0110-m01.avi" mimetype="video" mime-subtype="avi"/>
        </fig>
    </p>
 

*Em :ref:`elemento-sec` do tipo material suplementar:*
 
.. code-block:: xml
 
    <sec sec-type="supplementary-material">
        <title>Supplementary Material</title>
        <supplementary-material id="m1">
            <caption>
                <title>legenda</title>
            </caption>
            <media mimetype="application" mime-subtype="pdf" xlink:href="1234-5678-rctb-45-05-0110-m01.pdf"/>
        </supplementary-material>
    </sec>
 
 
.. _elemento-sig-block:

<sig-block>
-----------

Aparece em
  :ref:`elemento-body`

Ocorre
  Zero ou uma vez


Tag que identifica um bloco de assinatura(s), normalmente utilizada em 
documentos do tipo editorial. A tag de ``<sig-block>`` deve obrigatoriamente 
conter a tag ``<sig>``. É possível formatar o texto do bloco de assinatura 
com negrito ``<bold>`` ou itálico ``<italic>``. Para as quebras de linhas 
deve-se usar a tag ``<break/>`` como mostram os exemplos a seguir:

Exemplo 1:
 
.. code-block:: xml
 
    ...
    <sig-block>
        <sig>
            <bold>Harry Weasley</bold>
            <break/>
            <italic>Editor Chefe</italic>
            <break/>
            Profeta Diário
            <break/>
        </sig>
    </sig-block>
    ...


**Exemplo 2:**

.. code-block:: xml
 
    <sig-block>
        <sig>
            <bold>Harry Weasley</bold>
            <italic>Editor Chefe<italic>
            Profeta Diário
        </sig>
    </sig-block>
 

.. note:: Para arquivos que apresentam apenas uma assinatura ao final do documento, é preciso repetir os nomes que constam na assinatura em front\contrib e marcá-los como autores.

 
.. _elemento-back:

<back>
======

Aparece em
  :ref:`elemento-article`

Ocorre
  Zero ou uma vez

O ``<back>`` é a parte final do documento que compreende lista de referências e demais
dados referentes a pesquisa como: notas de rodapé, agradecimentos, apêndice,
material suplementar, anexos e glossário.
 

.. _elemento-ack:

<ack>
-----

Aparece em
  :ref:`elemento-back`

Ocorre
  Zero ou mais vezes

A seção de agradecimentos quando aparecer no documento deve ser marcada dentro
de :ref:`elemento-back`.
 
É em agradecimentos que frequentemente os dados de financiamento da pesquisa são 
indicados, como descrito em :ref:`elemento-funding-group`
em :ref:`elemento-front`.
 
Todo o conteúdo de agradecimentos deverá ser identificado com a tag ``<ack>``, 
caso haja o título "Agradecimentos" ou "Acknowledgment" identifique-o com a tag
``<title>``. Em ``<ack>`` é possível especificar um ou mais parágrafos
:ref:`elemento-p`.

Exemplo:
 
.. code-block:: xml

    ...
    <back>
        <ack>
            <title>Agradecimentos</title>
            <p>Texto de agradecimentos, pode ou não conter dados de financiamento</p>
        </ack>
    </back>
    ...

.. note:: Não inserir a tag :ref:`elemento-sec` para identificação da seção
          agradecimentos.


.. _elemento-ref-list:

<ref-list>
----------

Aparece em
  :ref:`elemento-back`

Ocorre
  Zero ou mais vezes

  O conjunto de referências biliográficas de um artigo é representado pela tag
  ``<ref-list>``. Esse elemento deve conter, obrigatoriamente, três tags: 
  :ref:`elemento-ref`, :ref:`elemento-mixed-citation` e
  :ref:`elemento-element-citation`.

Em ``<ref-list>`` deve ser inserida uma informação de etiqueta ``title``.

Exemplo:
 
.. code-block:: xml

    ...
    <ref-list>
        <title>Referência Bibliográfica</title>
        <ref id="B1">
            ...
        </ref>
        ...
    </ref-list>
    ...


.. _elemento-ref:

<ref>
-----

Aparece em
  :ref:`elemento-ref-list`

Atributos obrigatórios
  1. id (ver :ref:`sugestao-atribuicao-id`)

Ocorre
  Uma ou mais vezes


Existem diversos tipos de referências e normas para apresentá-las num documento 
textual (:term:`ABNT`, :term:`Vancouver`, :term:`APA`, :term:`ISO` e 
OTHER). Independente da norma usada, a representação dos elementos
essenciais em XML de uma referência devem ser identificados corretamente.
 

Exemplo:

.. code-block:: xml
 
    ...
    <ref-list>
        <title></title>
        <ref id="B1">
            <label>1</label>
            <mixed-citation>. Aires M, Paz AA, Perosa CT. Situação de saúde e grau de dependência de pessoas idosas institucionalizadas. <italic>Rev Gaucha Enferm.</italic> 2009;30(3):192-9.</mixed-citation>
            <element-citation publication-type="journal">
                <person-group person-group-type="author">
                    <name>
                        <surname>Aires</surname>
                        <given-names>M</given-names>
                    </name>
                    <name>
                        <surname>Paz</surname>
                        <given-names>AA</given-names>
                    </name>
                    <name>
                        <surname>Perosa</surname>
                        <given-names>CT</given-names>
                    </name>
                </person-group>
                <article-title>Situação de saúde e grau de dependência de pessoas idosas institucionalizadas</article-title>
                <source>Rev Gaucha Enferm</source>
                <year>2009</year>
                <volume>30</volume>
                <issue>3</issue>
                <fpage>192</fpage>
                <lpage>199</lpage>
            </element-citation>
        </ref>
        ...
    </ref-list>
    ...
  

.. _elemento-mixed-citation:

<mixed-citation>
^^^^^^^^^^^^^^^^

Tag utilizada para identificar uma referência bibliográfica conforme consta no
PDF;
 

.. _elemento-element-citation:

<element-citation>
^^^^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-ref`

Atributos obrigatórios
  1. publication-type

Ocorre
  Uma ou mais vezes


A tag ``<element-citation>`` apresenta a identificação detalhada de cada
referência bibliográfica, e deve aparecer apenas como filha do elemento 
:ref:`elemento-ref`. Além disso deve apresentar o atributo ``@publication-type``, 
que indica o tipo de publicação da referência. 

Os valores que podem ser utilizados para o atributo ``@publication-type`` são:

+-----------+------------------------------------------------------------------+
| Valor     | Descrição                                                        |
+===========+==================================================================+
| book      | Utilizada para referenciar livros. Pode Também representar       |
|           | somente uma parte ou capítulo de um livro.                       |
+-----------+------------------------------------------------------------------+
| confproc  | Utilizada para referenciar documentos relacionados à eventos     |
|           | científicos: atas, anais, resultados, proceedings, convenção,    |
|           | conferência entre outros.                                        |
+-----------+------------------------------------------------------------------+
| database  | Utilizada para referenciar bases de dados.                       |
+-----------+------------------------------------------------------------------+
| journal   | Utilizada para referenciar publicações seriadas, editadas em     |
|           | unidades sucessivas, com designações numéricas e/ou cronológicas |
|           | e destinada a ser continuada indefinidamente.                    |
+-----------+------------------------------------------------------------------+
| patent    | Utilizada para referenciar patentes.                             |
+-----------+------------------------------------------------------------------+
| report    | Utilizada para referencias de um relatório técnico, normalmente  |
|           | de autoria institucional.                                        |
+-----------+------------------------------------------------------------------+
| software  | Utilizada para referenciar um software em suportes como CDs,     |
|           | DVD's, suporte online, dispositivos usb e etc.                   |
+-----------+------------------------------------------------------------------+
| thesis    | Utilizada para referenciar monografias, dissertações ou teses    |
|           | para obtenção de um grau acadêmico, tais como livre-docência,    |
|           | doutorado, mestrado, bacharelado, licenciatura, etc.             |
+-----------+------------------------------------------------------------------+
| webpage   | Utilizada para identificar informações de web sites e blogs      |
+-----------+------------------------------------------------------------------+
| legal-doc | Utilizada para referenciar normas jurídicas.                     |
+-----------+------------------------------------------------------------------+
| newspaper | Utilizada para referenciar artigos de jornal.                    |
+-----------+------------------------------------------------------------------+ 
| other     | Utilizada para referenciar tipos não previstos pelo SciELO PS.   |
+-----------+------------------------------------------------------------------+


.. note::

  * Nunca manter uma informação toda com formatação <italic>, <bold>, etc,
    dentro de alguma tag;
  * Evitar pontuação dentro da marcação em :ref:`elemento-element-citation`
    (ponto final, vírgula etc);
  * Todas as informaçoes de uma referência devem ser marcadas, caso não exista
    uma tag específica para uma informação inserir esta em
    :ref:`elemento-comment`.


Exemplos:
 
.. code-block:: xml

    <!-- Journal Sample -->

    ...
    <ref-list>
        <ref id="B01">
            <label>1</label>
            <mixed-citation>ARRETCHE, M. Federalism and territorial equality: a contradiction in terms? Dados, Rio de Janeiro, v. 5, n. 02, 2010 . Disponível em: &lt;http://socialsciences.scielo.org.</mixed-citation>
            <element-citation publication-type="journal">
                <person-group person-group-type="author">
                    <name>
                        <surname>ARRETCHE</surname>
                        <given-names>M</given-names>
                    </name>
                </person-group>
                <article-title>Federalism and territorial equality: a contradiction in terms?</article-title>
                <source>Dados</source>
                <publisher-loc>Rio de Janeiro</publisher-loc>
                <volume>5</volume>
                <issue>02</issue>
                <year>2010</year>
                <ext-link ext-link-type="uri" xlink:href="http://socialsciences.scielo.org">http://socialsciences.scielo.org</ext-link>
            </element-citation>
        </ref>
    <ref-list> 
    ...


.. code-block:: xml

    <!-- Book Chapter Sample --> 

    ...
    <ref-list>
        <ref id="B02">
            <label>2</label>
            <mixed-citation>Calkins BM, Mendeloff AI. The epidemiology of idiopathic inflammatory bowel disease. In: Kirsner JB, Shorter RG, eds. Inflammatory bowel disease, 4th ed. Baltimore: Williams &amp; Wilkins. 1995:31-68.</mixed-citation>
            <element-citation publication-type="book">
              <person-group person-group-type="author">
                <name>
                    <surname>Calkins</surname>
                    <given-names>BM</given-names>
                </name>
                <name>
                    <surname>Mendeloff</surname>
                    <given-names>AI</given-names>
                </name>
              </person-group>
                <chapter-title>The epidemiology of idiopathic inflammatory bowel
                disease.</chapter-title>
                <person-group person-group-type="editor">
                    <name>
                        <surname>Kirsner</surname>
                        <given-names>JB</given-names>
                    </name>
                    <name>
                        <surname>Shorter</surname>
                        <given-names>RG</given-names>
                    </name>
                </person-group>
                <source>Inflammatory bowel disease</source>
                <edition>4th ed</edition>
                <publisher-loc>Baltimore</publisher-loc>
                <publisher-name>Williams &amp; Wilkins</publisher-name>
                <year>1995</year>
                <fpage>31</fpage>
                <lpage>68</lpage>
            </element-citation>
        </ref>
    </ref-list>
    ...

.. code-block:: xml
 
    <!-- Book Sample --> 

    ...
    <ref-list>
        <ref id="B03">
            <label>3</label>
            <mixed-citation>LÉVY, Pierre. As tecnologias da inteligência: o 
            futuro do pensamento na era da informática. Edição especial. Rio de 
            Janeiro: Editora 34. 2001. 208 p.</mixed-citation>
        <element-citation publication-type="book">
            <person-group person-group-type="author">
                <name>
                    <surname>LÉVY</surname>
                    <given-names>Pierre</given-names>
                </name>               
            </person-group>
            <source>As tecnologias da inteligência: o futuro do pensamento na 
            era da informática</source>
            <edition>edição especial</edition>
            <publisher-loc>Rio de Janeiro</publisher-loc>
            <publisher-name>Editora 34</publisher-name>
            <year>2001</year>            
            <size units="pages">208</size>            
        </element-citation>
        </ref>
    </ref-list>
    ...
 
.. code-block:: xml
 
    <!-- Webpage Sample -->
    
    ...
    <ref id="B04">
        <label>4</label>
        <mixed-citation>COB - Comitê Olímpico Brasileiro. Desafio para o corpo. Disponível em: http://www.cob.org.br/esportes/esporte.asp?id=39. (Acesso em 10 abr 2010)</mixed-citation>
        <element-citation publication-type="webpage">
            <person-group person-group-type="author">
                <collab>COB -Comitê Olímpico Brasileiro</collab>
            </person-group>
            <source>Desafio para o corpo</source>
            <comment>Disponível em: <ext-link ext-link-type="uri" xlink:href="http://www.cob.org.br/esportes/esporte.asp?id=39">http://www.cob.org.br/esportes/esporte.asp?id=39</ext-link></comment>
            <date-in-citation content-type="access-date">10 abr 2010</date-in-citation>
        </element-citation> 
    </ref>
    ...

.. note:: Quando a referência apresentar URL com texto (Disponível em: ou 
          Available from:) identificar conforme o exemplo acima.
 
.. code-block:: xml

    <!-- Webpage Sample 2 -->
  
    <ref id="B21">
        <label>21</label>
        <mixed-citation>Fugh-Berman A. PharmedOUT [Internet]. Washington: Georgetown University, Department of Physiology and Biophysics; c2006 [cited 2007 Mar 23]. Available from: http://www.pharmedout.org/.</mixed-citation>
        <element-citation publication-type="webpage"> 
            <person-group person-group-type="author">
                <name>
                    <surname>Fugh-Berman</surname>
                    <given-names>A</given-names>
                </name>
            </person-group>
            <source>PharmedOUT [Internet]</source>
            <publisher-loc>Washington</publisher-loc>
            <publisher-name>Georgetown University, Department of Physiology and Biophysics</publisher-name>
            <year>c2006</year>
            <date-in-citation>cited 2007 Mar 23</date-in-citation>
            <comment>Available from: <ext-link ext-link-type="uri" xlink:href="http://www.pharmedout.org">http://www.pharmedout.org</ext-link></comment>
        </element-citation>
    </ref>

.. code-block:: xml

    <!-- Report Sample -->

    ...
    <ref-list>
        <ref id="B05">
            <label>5</label>
            <mixed-citation>World Health Organization. Control of the leishmaniases. Geneva: WHO; 2010.(Technical Report Series; 949)</mixed-citation>
            <element-citation publication-type="report">
                <person-group person-group-type="author">
                    <collab>World Health Organization</collab>
                </person-group>
                <article-title>Control of the leishmaniases</article-title>
                <publisher-loc>Geneva</publisher-loc>
                <publisher-name>WHO</publisher-name>
                <year>2010</year>
                <comment>(Technical Report Series; 949)</comment>
            </element-citation>
        </ref>
    </ref-list> 
    ...
 
.. code-block:: xml

    <!-- Report Sample -->

    ...
    <ref-list>
        <ref id="B1">
            <mixed-citation>Water HP, Boshuizen HC, Perenboom RJ. Health expectancy of the Dutch population. Bilthoven (Netherlands): National Institute of Public Health and Environmental Protection (NL); 1995. 21 p. Report No.: 431501009</mixed-citation>
            <element-citation publication-type="report">
                <person-group person-group-type="author">
                    <name>
                        <surname>Water</surname>
                        <given-names>HP</given-names>
                    </name>
                    <name>
                        <surname>Boshuizen</surname>
                        <given-names>HC</given-names>
                    </name>
                    <name>
                        <surname>Perenboom</surname>
                        <given-names>RJ</given-names>
                    </name>
                </person-group>
                <source>Health expectancy of the Dutch population</source>
                <publisher-loc>Bilthoven (Netherlands)</publisher-loc>
                <publisher-name>National Institute of Public Health and Environmental Protection (NL)</publisher-name>
                <year>1995</year>
                <size units="pages">21</size>
                <pub-id pub-id-type="other">Report No.: 431501009</pub-id>
            </element-citation>
        </ref>
    </ref-list>
    ...

.. note:: Para referências que apresentam informações de coleção ou série 
          exemplo, "Technical Report Series; 949" deve ser identificado com a 
          tag ``<comment>``. Não confundir com referência bibliográfica do 
          tipo "report" que apresenta número de relatório (Report No.: 431501009), 
          para esses casos, identificar com a tag ``<pub-id pub-id-type="other">``.

.. code-block:: xml
 
    <!-- Confproc (proceedings) Sample -->

    ...
    <ref-list>
        <ref id="B06">
            <label>6</label>
            <mixed-citation>World Health Organization (WHO). Ultrasound in schistosomiasis. A pratical guide to the standardized use of ultrasonography for the assessment of schistosomiasis-related morbidity. Second International Workshop. 22 October, 1996, Niamey, Niger.</mixed-citation>
            <element-citation publication-type="confproc">
                <person-group person-group-type="author">
                    <collab>World Health Organization (WHO)</collab>
                </person-group>
                <source>Ultrasound in schistosomiasis. A pratical guide to the standardized use of ultrasonography for the assessment of schistosomiasis-related morbidity</source>
                <comment>Second International Workshop</comment>
                <day>22</day>
                <month>10</month>
                <publisher-loc>Niamey, Niger</publisher-loc>
                <year>1996</year>
            </element-citation>
        </ref>
    </ref-list> 
    ...


  .. code-block:: xml
 
    <!-- Confproc (proceedings) Sample -->
    
    ...
    <ref id="B42">
        <label>42</label>
        <mixed-citation>Kornilaki, E., & Nunes, T. (1997). What do young children understand about division? In Proceedings of the 21th Annual International Conference of Psychology of Mathematics Education. Lahti, Finland: University of Helsinki.
        </mixed-citation>
        <element-citation publication-type="confproc">
          <person-group person-group-type="author">
            <name>
              <surname>Kornilaki</surname>
              <given-names>E.</given-names>
            </name>
            <name>
              <surname>Nunes</surname>
              <given-names>T.</given-names>
            </name>
          </person-group>
          <year>1997</year>
          <source>What do young children understand about division?</source>
          <conf-name>Proceedings of the 21th Annual International Conference of Psychology of Mathematics Education</conf-name>
          <conf-loc>Lahti, Finland</conf-loc>
          <publisher-name>University of Helsinki</publisher-name>
        </element-citation>
      </ref>
      ...


.. code-block:: xml

    <!-- Thesis Sample -->
 
    ...
    <ref-list>
        <ref id="B07">
            <label>7</label>
            <mixed-citation>Milani RM. Análise dos resultados imediatos da operação para revascularização do miocárdio sem pinçamento total da aorta [Dissertação de mestrado]. Curitiba: Universidade Federal do Paraná; 2000.</mixed-citation>
            <element-citation publication-type="thesis">
                <person-group person-group-type="author">
                    <name>
                        <surname>Milani</surname>
                        <given-names>RM</given-names>
                    </name>
                </person-group>
                <source>Análise dos resultados imediatos da operação para revascularização do miocárdio sem pinçamento total da aorta</source>
                <comment>Dissertação de mestrado</comment>
                <publisher-loc>Curitiba</publisher-loc>
                <publisher-name>Universidade Federal do Paraná</publisher-name>
                <year>2000</year>
            </element-citation>
        </ref>
    </ref-list>
    ...

.. code-block:: xml
 
    <!-- Patent Sample -->

    ...
    <ref-list>
        <ref id="B08">
            <label>8</label>
            <mixed-citation>EMBRAPA. Medidor digital multissensor de temperatura para solos. BR n. PI 8903105-9, 30 maio 1995.</mixed-citation>
            <element-citation publication-type="patent">
                <person-group person-group-type="author">
                    <collab>EMBRAPA</collab>
                </person-group>
                <source>Medidor digital multissensor de temperatura para solos</source>
                <patent country="BR">PI 8903105-9</patent>
                <day>30</day>
                <month>05</month>
                <year>1995</year>
            </element-citation>
        </ref>
    </ref-list>
    ...

.. code-block:: xml
 
    <!-- Software Sample -->

    ...
    <ref-list>     
        <ref id="B09">
            <label>9</label>
            <mixed-citation>MICROSOFT. Project for Windows 95: project planning software. Version 4.1. [S.l.]: Microsoft Corporation, 1995. 1 CD-ROM.</mixed-citation>
            <element-citation publication-type="software">
                <person-group person-group-type="editor">
                    <collab>MICROSOFT</collab>
                </person-group>
                <source>Project for Windows 95: project planning software</source>
                <edition>Version 4.1</edition>
                <publisher-name>Microsoft Corporation</publisher-name>
                <year>1995</year>
                <comment>1 CD-ROM</comment>
            </element-citation>
        </ref>
    <ref-list>
    ...

.. code-block:: xml
 
    <!-- Database Sample -->

    ...
    <ref-list>
        <ref id="B10">
            <label>10</label>
            <mixed-citation>FUNDAÇÃO TROPICAL DE PESQUISAS E TECNOLOGIA “ANDRÉ TOSELLO”. Base de Dados Tropical. 1985. Disponível em: <http://www.bdt.fat.org.br/acaro/sp/>. Acesso em: 30 maio 2002.</mixed-citation>
            <element-citation publication-type="database">
                <person-group person-group-type="author">
                    <collab>FUNDAÇÃO TROPICAL DE PESQUISAS E TECNOLOGIA “ANDRÉ TOSELLO”</collab>
                </person-group>
                <source>Base de Dados Tropical</source>
                <year>1985</year>
                <comment>Disponível em: <ext-link ext-link-type="uri" xlink:href="http://www.bdt.fat.org.br/acaro/sp/">http://www.bdt.fat.org.br/acaro/sp/</ext-link></comment>
                <date-in-citation content-type="access-date">30 maio 2002</date-in-citation>
            </element-citation>
        </ref>
    </ref-list>
    ...


.. note:: Deve-se levar em consideração que muitas vezes as referências são
          contruídas de forma incorreta, o que dificulta a marcação de seus
          elementos.
          No caso de referências que não apresentam informações como data de publicação ou título, a referência deve ser considerada como "incomplete".

.. _elemento-element-chapter-title:

<chapter-title>
^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-element-citation`

Ocorre 
  Zero ou mais vezes

Identifica um capítulo de um documento numa referência.

Exemplo:

.. code-block:: xml
    
    ...
    <element-citation>
        <chapter-title>Anjo da morte</chapter-title>
    </element-citation>
    ...

.. note:: Representa o capítulo 24 do livro ‘As feiticeiras de East End’.


.. _elemento-pub-id:

<pub-id>
^^^^^^^^

Aparece em
  :ref:`elemento-element-citation`
  

Atributos obrigatórios 
  ``@pub-id-type``

Ocorre 
  Zero ou mais vezes

Identifica o tipo de identificador (id) de um documento em uma referência.
Deve possuir o atributo ``@pub-id-type`` com os seguintes possíveis valores:

+--------+----------------------------------------+
| Valor  | Descrição                              |
+========+========================================+
| pmid   | :term:`PubMed` ID                      |
+--------+----------------------------------------+
| pcmid  | :term:`PubMed` Central ID              |
+--------+----------------------------------------+
| doi    | Número DOI registrado no Crossref      |
+--------+----------------------------------------+
| pii    | Identificador do editor                |
+--------+----------------------------------------+
| other  | qualquer outro identificador           |
+--------+----------------------------------------+

Exemplo:

.. code-block:: xml

    ...
    <element-citation>
        <pub-id pub-id-type="pmid">15867408</pub-id>
    </element-citation>
    ...


.. _elemento-date-in-citation:

<date-in-citation>
^^^^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-element-citation`
 
Atributos obrigatórios 
 ``@content-type``

Ocorre 
  Zero ou mais vezes

Esta tag identifica a data de citação em uma referência. Deve sempre possuir 
o atributo ``@content-type`` com os tipos de data de acesso e data de
atualização do documento.

Exemplo 1:

.. code-block:: xml

    ...
    <element-citation>
        <date-in-citation content-type="access-date">cited 2007 Feb 21</date-in-citation>
    </element-citation>
    ...

Exemplo 2:

.. code-block:: xml

    ...
    <element-citation>
        <date-in-citation content-type="updated">2006 Jul 20</date-in-citation>
    </element-citation>
    ...


.. _elemento-comment:

<comment>
^^^^^^^^^

Aparece em
  :ref:`elemento-element-citation`

Ocorre 
  Zero ou mais vezes

Tag pode servir para marcar alguma informações juntamente com uma URL 
(ver tag :ref:`elemento-ext-link`)e também para identificar dados que não
possuem tagueamento específico em uma referência.

Exemplo:

.. code-block:: xml

    ...
    <element-citation>
        <comment>1 CD-ROM: color, 4 3/4 in.</comment> 
    </element-citation>
    ...


.. _elemento-conf-name:

<conf-name>
^^^^^^^^^^^

Aparece em
  :ref:`elemento-element-citation`
  
Ocorre 
 Zero ou mais vezes

Identifica o nome de uma conferência, congresso, reunião, palestra, seminário e
etc mencionado em uma referência.

Exemplo:

.. code-block:: xml

    ...
    <element-citation>
        <conf-name>Proceedings of the 23rd International Summer School of Brain Research</conf-name>
    </element-citation>
    ...


.. _elemento-conf-loc:

<conf-loc>
^^^^^^^^^^

Aparece em
  :ref:`elemento-element-citation`
  
Ocorre 
  Zero ou mais vezes

Identifica o local, país, cidade, estado, província, e local físico como uma
assembléia, anfiteatro e etc de uma conferência, congresso, reunião, palestra,
seminário e etc mencionado em uma referência.

Exemplo:

.. code-block:: xml

    ...
    <element-citation>
        <conf-loc>Dallas, TX</conf-loc>
    </element-citation>
    ...


.. _elemento-conf-date:

<conf-date>
^^^^^^^^^^^

Aparece em
  :ref:`elemento-element-citation`
  
Ocorre 
  Zero ou mais vezes

Trata-se de uma tag para identificar a data de uma conferência, evento e etc.
Pode ser composta por um período por exemplo: 2003 Aug 25-29.

Exemplo:

.. code-block:: xml

    ...
    <element-citation>
        <conf-date>2002 Jul 28-Aug 2</conf-date>
    </element-citation>
    ...


.. _elemento-patent:

<patent>
^^^^^^^^

Aparece em
  :ref:`elemento-element-citation`
  
Atributos obrigatórios 
  ``@country``

Ocorre 
  Zero ou uma vez

Tag utilizada para identificar um número de patente. Deve possuir o atributo 
``@country`` e nele deve ser atribuído o código do país de acordo com a 
Norma ISO 3166, com dois caracteres alfabéticos.

Para consultar ao código do país consulte o link da norma ISO: https://www.iso.org/obp/ui/#iso:pub:PUB500001:en

Exemplo de patente americana:

.. code-block:: xml

    ...
    <element-citation>
        <patent country="US">US 6,980,855</patent>
    </element-citation>
    ...



.. _elemento-fn-group:

<fn-group>
----------

Aparece em
  :ref:`elemento-back`

Ocorre
  Zero ou uma vez

A tag de grupo de notas é um elemento de :ref:`elemento-back` e deve conter todo
o grupo de notas de rodapé mencionadas no documento que não representem notas de
autor, as quais deverão ser identificadas em :ref:`elemento-author-notes`. Pode
possuir uma ou mais notas :ref:`elemento-fn`.
 
Exemplo:
 
.. code-block:: xml

    ...
    <back>
        ...
        <fn-group>
            <fn fn-type="supported-by" id="fn01">
                <label>*</label>
                <p>Vivamus sodales fermentum lorem, consectetur mollis lacus sollicitudin quis</p>
            </fn>
            <fn fn-type="presented-at" id="fn02">
                <label>*</label>
                <p>Donec et urna sed orci volutpat sollicitudin. Vestibulum quis tempor lacus. Nunc cursus, mi sed auctor pellentesque, orci tellus tincidunt arcu, eu imperdiet augue ligula eget justo.</p>
            </fn>
        </fn-group>
        ...
    </back>
    ...


.. _elemento-app:

<app>
-----

Aparece em
  :ref:`elemento-back`

Atributos obrigatório 
  1. id (Ver :ref:`sugestao-atribuicao-id`)
 
Ocorre
  Zero ou uma vez

Utilizado para indicar a presença de um apêndice ao documento. Para a marcação
básica de um apêndice devemos levar em consideração duas tags importantes, a de
grupo de apêndice ``app-group`` e de apêndice propriamente dito
``<app>``. Obrigatoriamente deve ser inserida uma informação de
etiqueta :ref:`elemento-label` em ``<app>``.

 
Exemplo:
  
  app01... app10, app11;
 
Exemplo de Apêndice com texto:
 
.. code-block:: xml
 
    ...
    <app-group>
          <app id="app01">
              <label>Apêndice</label>
              <p>Vivamus fermentum elit et pellentesque iaculis. Curabitur egestas rhoncus purus quis iaculis. Sed laoreet id leo eu tristique. Etiam hendrerit nibh in tincidunt mattis. Sed et volutpat nulla, eget semper tellus. Nullam imperdiet fringilla diam, nec mollis elit sagittis a. Nam euismod sagittis posuere.</p>
          </app>
    </app-group>
    ...


Exemplo de Apêndice com imagem (Pode ser imagem de figura, tabela, quadro, equação e etc):
 
.. code-block:: xml
 
    ...
    <app-group>
        <app id="app01">               
              <label>Appendix 1</label>
              <title>Questionnaire for SciELO</title>    
              <graphic xlink:href="1234-5678-rctb-45-05-0110-app01.tif"/>         
        </app>
    </app-group>
    ...

Exemplo de Apêndice com link externo (ext-link do tipo uri):
 
.. code-block:: xml
 
    ...
    <app-group>
        <app id="app01">                
            <label>Appendix 1</label>
            <p>Para mais informações <ext-link ext-link-type="uri" xlink:href="http://www.scielo.org">clique aqui</ext-link> para verificar o pdf.</p>
        </app>
    </app-group>
    ...
 
Exemplo de Apêndice com tabela:
 
.. code-block:: xml
 
    ...
    <app-group>
      <app id="app01">
      <label>Appendix</label>        
            <table-wrap>
              <label>Table 1</label>
              <caption>
                  <title>Título da tabela</title>
              </caption>
              <table frame="hsides" rules="all">
                  <colgroup width="XX%">
                      <col/>
                      <col/>
                      <col/>
                  </colgroup>
                  <thead>
                      <tr>
                           <th style="background-color:#e5e5e5">xxxxx</th>
                           <th style="background-color:#e5e5e5">xxxxx</th>
                           <th style="background-color:#e5e5e5">xxxxxx</th>
                      </tr>
                  </thead>
                  <tbody>
                      <tr>
                           <td align="center">xxxxx</td>
                           <td align="center">xxxx</td>
                           <td align="center">xxxx</td>
                      </tr>
                  </tbody>
              </table>
            </table-wrap>             
      </app>
    </app-group>
    ...

Exemplo de Apêndice misto (figura mais tabela)
 
.. code-block:: xml

    ... 
    <app-group>
        <app id="app01">               
            <label>Appendix 1</label>
            <title>Questionnaire for SciELO</title>    
            <graphic xlink:href="1234-5678-rctb-45-05-0110-app01.tif"/>         
        </app>
        <app id="app02">
            <label>Appendix 2</label>      
            <table-wrap>
                <label>Supplementary Table S1</label>
                <caption>
                    <title>Título da tabela</title>
                </caption>
                <table frame="hsides" rules="all">
                    <colgroup width="XX%">
                        <col/>
                        <col/>
                        <col/>
                    </colgroup>
                    <thead>
                        <tr>
                            <th style="background-color:#e5e5e5">xxxxx</th>
                            <th style="background-color:#e5e5e5">xxxxx</th>
                            <th style="background-color:#e5e5e5">xxxxxx</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td align="center">xxxxx</td>
                            <td align="center">xxxx</td>
                            <td align="center">xxxx</td>
                        </tr>
                    </tbody>
                </table>
            </table-wrap>        
        </app>
    </app-group>
    ...
 
Exemplo de Apêndice misto (texto mais figura):
 
.. code-block:: xml
 
    ...
    <app-group>
        <app id="app01">               
            <label>Appendix 1</label>
            <title>Questionnaire for student inclusion</title>    
            <graphic xlink:href="1234-5678-rctb-45-05-0110-app01.tif"/>
        </app>     
        <app id="app02">
            <label>Appendix 2</label>
            <p>Pellentesque sollicitudin, purus nec ultricies tristique, purus nisi imperdiet enim, nec mollis augue odio sit amet augue. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut cursus ipsum non nisi faucibus suscipit. Cras ut venenatis tellus.</p>       
        </app>
    </app-group>
    ...
 
Exemplo de Apêndice com vídeo:

.. code-block:: xml
 
    ...
    <app-group>
          <app id="app01">
              <label>suplemento eletrônico</label>
              <supplementary-material id="suppl01">
              <media xlink:href="1234-5678-rctb-45-05-0110-m01.avi" mimetype="video" mime-subtype="avi"/>
              </supplementary-material>
          </app>
    </app-group>
    ...
 
.. note:: Obrigatoriamente o elemento :ref:`elemento-app` deve estar inserido em ``<app-group>``.,


.. _elemento-def-list:
 
<def-list>
----------

Aparece em
  :ref:`elemento-app`
  ``app-group``
  :ref:`elemento-body`
  :ref:`elemento-boxed-text`
  ``<def-list>`` 
  :ref:`elemento-glossary`
  ``<list-item>``
  :ref:`elemento-p`
  :ref:`elemento-ref-list`
  :ref:`elemento-sec`


Ocorre
  Zero ou mais vezes



Utilizada quando há uma lista de termos e suas respectivas definições.
A lista de definições deve ser apresentada como texto e apresenta os seguintes elementos:

``<title>``, ``<term-head>``, ``<def-head>``, ``<def-item>``, ``<def-list>``.


Em ``<def-item>`` utilizar os seguintes elementos:

- <term> : Utilizado para identificar a palavra, frase, equação etc que está sendo definido ou descrito.

- <def> : Descrição, explicação da palavra ou frase identificada em <term>. Nesse elemento deve ser inserido, obrigatoriamente, o elemento :ref:`elemento-p`.

 
Consulte a :ref:`sugestao-atribuicao-id` para instruções sobre a composição do 
atributo ``@id``.
 

Exemplo em body:
 
.. code-block:: xml

  <body>
    <def-list id="d1">
      <def-item>
        <term>Angina pectoris (Angina de peito)</term>
        <def>
          <p>Sensação de angústia, de opressão torácica, devido a um fornecimento insuficiente de oxigênio ao coração.</p>
        </def>
      </def-item>
      <def-item>
        <term>Antagonista</term>
        <def>
            <p>É uma droga ou um composto que opõe os efeitos fisiológicos de outro composto. Em nível de receptor, é uma entidade química que opõe as respostas associadas à ativação do receptor, normalmente induzidas por outro agente bioativo.</p>
        </def>
      </def-item>
      <def-item>
        <term>Biodisponibilidade</term>
          <def>
            <p>Termo que expressa a taxa ou concentração de fármaco que atinge a circulação sistêmica a partir do seu sítio de administração.</p>
          </def>
      </def-item>
    </def-list>
  </body>


Exemplo sublista de definições:
 
.. code-block:: xml
 
    ...
    <def-list id="d2">
      <label>Glossário</label>          
      <def-item>
        <term>I</term>
        <def>
          <p>moment of inertia</p>
        </def>
      </def-item>
      <def-item>
        <term>V</term>
        <def>
          <p>shear force</p>
        </def>
      </def-item>
        <def-list>
          <def-item>
            <term>D<sub>E</sub>50</term>
            <def>
              <p>Dose do fármaco necessária para atingir 50% do efeito farmacológico desejado</p>
            </def>
          </def-item>
          <def-item>
            <term>Depuração</term>
            <def>
              <p>Indica a taxa de remoção de uma substância do sangue quando ele atravessa um órgão, por ex., fígado ou rim.</p>
            </def>
          </def-item>
        </def-list>
    </def-list>
    ...


.. _elemento-glossary:
 
<glossary>
----------

Aparece em
  :ref:`elemento-app`,
  :ref:`elemento-back`,
  :ref:`elemento-boxed-text`,
  ``<glossary>``


Ocorre
  Zero ou mais vezes


Elemento ``<glossary>`` é utilizado com a finalidade de descrever um glossário para documento. O conteúdo desse elemento geralmente é uma lista de definições, apresentando elementos de ``<def-list>``. Nesse caso, utilizar as regras de :ref:`elemento-def-list`.

Consulte a :ref:`sugestao-atribuicao-id` para instruções sobre a composição do atributo ``@id``.


Exemplo em back:
 
.. code-block:: xml

  <back>
    <glossary id="gl1">
      <label>Glossário</label>
      <def-list>
        <def-item>
          <term>PEL</term>
          <def>
            <p>Passivo Externo Líquido</p>
          </def>
        </def-item>
        <def-item>
          <term>PEL1</term>
          <def>
            <p>Passivo Externo Líquido1</p>
          </def>
        </def-item>
        <def-item>
          <term>PEL2</term>
          <def>
            <p>Passivo Externo Líquido2</p>
          </def>
        </def-item>
        <def-item>
          <term>DCCA</term>
          <def>
            <p>déficit acumulado na conta corrente do balanço de pagamentos</p>
          </def>
        </def-item>
      </def-list>
    </glossary>
  </back>


Exemplo em apêndice:
 
.. code-block:: xml

  <back>
    <app-group>
      <app>
      <label>Glossário</label>
        <glossary id="gl2">
          <def-list>
            <def-item>
              <term>Metabólito</term>
              <def>
                <p>É qualquer intermediário ou produto resultante do metabolismo.</p>
              </def>
            </def-item>
            <def-item>
              <term>Potência</term>
              <def>
                <p>É a dose de uma droga requerida para produzir um efeito específico de dada intensidade, comparada a um padrão de referência</p>
              </def>
            </def-item>
            <def-item>
              <term>Relação estrutura-atividade</term>
              <def>
                <p>É a relação entre estrutura química e atividade farmacológica para uma série de composto</p>
              </def>
            </def-item>
          </def-list>
        </glossary>
      </app>
    </app-group>
  </back>


Exemplo em boxed-text:
 
.. code-block:: xml

  ...
  <boxed-text id="bx2">
    <sec>
      <title>Box 1. De Humanis corporis fabrica libri septem, or the <italic>Fabrica</italic>, and others.</title>
      <p><italic>De humani corporis fabrica libri septem,  </italic> the <italic>Fabrica</italic>,1<sup>st  </sup>edition, came to light in 1543, by the printer Johannes Oporinus, from Basel. It is one of the most influential books on human anatomy, and considered one of the great scientific and artistic oeuvre of mankind. The <italic>Fabrica</italic> is illustrated with detailed illustrations, printed with woodcut engravings, in Venice, with the identity of the artist is uncertain.</p>
      <p>The <italic>Fabrica,</italic> 2<sup>nd</sup> edition, released in 1555, dedicated to Charles V, is considered more sumptuous than the 1<sup>st  </sup>one. There are also corrections, decrease of redundancies, as well as inclusion of physiological experiments, by means of nervous section, e.g., section of the recurrent nerve, with consequent laryngeal paralysis.</p>
      <p><italic>De Humani corporis fabrica librorum Epitome</italic>, the <italic>Epitome</italic>, printed in 1543, was intended by Vesalius to be a very brief descriptive book, being a remarkable condensation of the 1<sup>st</sup> edition of the main book. It has 6 chapters, the 5<sup>th</sup> concerned with "The brain and the nervous system".  </p>
    </sec>
    <glossary>
      <def-list id="d1">
        <title>Nomenclature</title>
        <def-item>
          <term>u</term>
          <def>
            <p>time domain vertical displacement</p>
          </def>
        </def-item>
        <def-item>
          <term>û</term>
          <def>
            <p>frequency domain vertical displacement</p>
          </def>
        </def-item>
        <def-item>
          <term>E</term>
          <def>
            <p>Young´s Modulus</p>
          </def>
        </def-item>
      </def-list>
    </glossary>
  </boxed-text>
 ...


No elemento ``glossary`` pode ser inserido o atributo ``@id``.  
Consulte a Sugestão de atribuição de @id para instruções sobre a composição do atributo @id.
 
O glossário pode ser apresentado como imagem, utilizando a tag ``<graphic>``,
ou como texto.

.. note:: Não inserir pontuação nos elementos ``<term>`` ou ``<def>``.


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
 

.. _elemento-front-stub:

<front-stub>
------------

Aparece em
  :ref:`elemento-sub-article`, 
  :ref:`elemento-response`.


Tags obrigatórias
  ``<subject>``
  :ref:`elemento-article-title`


Ocorre

Uma vez


Tag utilizada em :ref:`elemento-sub-article` a qual herda os metadados do xml principal, 
portanto não inserir as tags :ref:`elemento-journal-meta` e :ref:`elemento-article-meta`. 
Nessa tag deve ser inserido apenas as informações que são diferentes das que 
constam no artigo principal, ou seja, não é necessário inserir informações como 
:ref:`elemento-volume`, :ref:`elemento-issue`, :ref:`elemento-fpage` :ref:`elemento-lpage` e :ref:`elemento-elocation-id`, 
:ref:`elemento-pub-date`, :ref:`elemento-permissions`, :ref:`elemento-funding-group`, :ref:`elemento-history`.


Exemplo da tag completa:

.. code-block:: xml
 
    ...
    <sub-article article-type="translation" xml:lang="en" id="S1">
        <front-stub>
            <subj-group subj-group-type="heading">
                <subject>Letter to the Editor</subject>
            </subj-group>
        </front-stub>
        ...
    </sub-article>
    ...


.. note:: Para arquivos traduzidos inserir em ``<front-stub>`` apenas os dados 
          traduzidos, ou seja, se há afiliação traduzida identificar autores e 
          afiliações, caso contrário, não identificar nenhum dado de autor e afiliação.


.. _elemento-response:

<response>
----------

Aparece em
  :ref:`elemento-article`,
  :ref:`elemento-sub-article`


Atributos obrigatórios
  1. response-type
  2. id
  3. xml:lang


Ocorre
  Zero ou mais vezes


Utilizada para apresentar uma resposta ao artigo principal que está diretamente relacionado ao artigo principal, por exemplo, resposta de uma carta ou apresenta opinião contrária de um artigo publicado.
Para esse elemento, recomendamos utilizar também a tag :ref:`elemento-front-stub`.

Para ``@response-type``, os valores que podem ser utilizados são:

+------------------------+-----------------------------------------+
| Valor                  | Descrição                               |
+========================+=========================================+
| addendum               | Adendo - Informação adicional           |
+------------------------+-----------------------------------------+
| discussion             | Discussão relacionado a um número       |
|                        | específico                              |
+------------------------+-----------------------------------------+
| reply                  | resposta a um artigo                    |
+------------------------+-----------------------------------------+

Exemplo da tag completa:

.. code-block:: xml
 
    ...
    <article>
      ...
      <response response-type="reply" xml:lang="en" id="R1">
          ...
      </response>
    </article>
    ...



.. _elemento-verse-group:

<verse-group>
-------------

Aparece em
  :ref:`elemento-app`, 
  ``app-group``, 
  :ref:`elemento-body`, 
  :ref:`elemento-boxed-text`, 
  :ref:`elemento-disp-quote`, 
  :ref:`elemento-p`, 
  :ref:`elemento-ref-list`, 
  :ref:`elemento-sec`, 
  :ref:`elemento-supplementary-material`, 
  :ref:`elemento-verse-group`

Ocorre
  Zero ou mais vezes


Elemento utilizado para apresentar poemas, versos ou músicas. Nesse elemento 
também pode ser inserido a tag :ref:`elemento-attrib` para identificação do autor e :ref:`elemento-label` para identificação do título do poema, verso etc.


Exemplo verse-group:

.. code-block:: xml
 
    ...
    <verse-group>
      <label>Porque é que um sono agita</label>
        <verse-line>E, num fiel regresso</verse-line>
        <verse-line>Ao que já era bruma,</verse-line>
        <verse-line>Sonolento me apresso</verse-line>
        <verse-line>Para coisa nenhuma.</verse-line>
        <attrib>Fernando Pessoa</attrib>
    </verse-group>
    ...


.. _elemento-boxed-text:

<boxed-text>
------------

Aparece em
  :ref:`elemento-app`, 
  ``app-group``, 
  :ref:`elemento-body`, 
  :ref:`elemento-boxed-text`, 
  :ref:`glossary`, 
  :ref:`elemento-p`, 
  :ref:`elemento-ref-list`, 
  :ref:`elemento-sec`


Atributos obrigatórios
  1. id


Ocorre
  Zero ou mais vezes


É utilizado para identificação de um texto ou objeto que faz parte do artigo, mas não do corpo do texto.
É possível apresentar um texto com seções, figura, tabela etc.


Exemplo com seções:

.. code-block:: xml
 
    ...
    <boxed-text id="bx1">
        <sec>
            <title>Box 1 Use of antidepressants and suicidality in young individuals</title>
            <p>In 2004, the FDA made the decision to include a black box warning about the risk of suicidality associated with antidepressant use among individuals under 25 years of age<xref ref-type="bibr" rid="B26">26</xref>.</p>
            <p>Based on the fact that for the treatment of depressive disorders the number needed to treat (NNT) in this age group is at least 10 and the number needed to harm (number needed to harm, NNH) is 112, it was concluded that the benefits associated with the use of antidepressants outweigh the potential risks.</p>
        </sec>
    </boxed-text>
    ...


Exemplo com figura:

.. code-block:: xml

    ... 
    <boxed-text id="bx1">
        <fig id="f12">
            <label>Figure</label>
            <caption>
                <title>Diagnostic algorithm for depressive episodes in children and adolescents</title>
            </caption>
            <graphic xlink:href="1516-4446-rbp-1516-4446-2012-S0022-gf01.jpg"/>
        </fig>
    </boxed-text>
    ...


.. _elemento-related-article:

<related-article>
-----------------

Aparece em
  :ref:`elemento-article-meta`,
  :ref:`elemento-front-stub`


Atributos obrigatórios
  1. related-article-type
  2. id

Ocorre
  Zero ou mais vezes


Elemento utilizado para indicar um artigo relacionado publicado ou não separadamente.
Essa tag deve ser inserida para artigos como: :ref:`errata` ou resposta de 
:ref:`artigo-comentado`.

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



Referências
===========

* ASSOCIAÇÃO BRASILEIRA DE NORMAS TÉCNICAS. NBR14724: informação e documentação: trabalhos acadêmicos: apresentação. Rio de Janeiro: NBR, 2011.
 
* ASSOCIAÇÃO BRASILEIRA DE NORMAS TÉCNICAS. NBR 6023: informação e documentação: referências: elaboração. Rio de Janeiro: NBR, 2002.
 
* JATS. Journal Article Tag Suite ANSI/NISO Z39.96-2012. Baltimore, USA: National Information Standards Organization, 2012. Disponível em:<http://jats.niso.org/>.
 
* JATS. Journal Article Tag Suite. Rockville Pike, USA: National Center for Biotechnology Information, 2013. Disponível em: <http://jats.nlm.nih.gov/>.
 
* JATS. Journal Publishing Tag Library NISO JATS Version 1.0. Rockville, USA: National Center for Biotechnology Information (NCBI), National Library of Medicine (NLM). 2012. Disponível em: <http://jats.nlm.nih.gov/publishing/tag-library/1.0/>.
 
* PubMed Central (NCBI). Sample PubMed Central Citations. Rockville Pike, USA: US National Library of Medicine National Institutes of Health. 2008. Disponível em: <http://www.ncbi.nlm.nih.gov/pmc/pmcdoc/tagging-guidelines/citations/v3/toc.html>.
 
* PubMed Central (NCBI). Elements: index of elements. Rockville Pike, USA: US National Library of Medicine National Institutes of Health. 2009. Disponível em: <https://www.ncbi.nlm.nih.gov/pmc/pmcdoc/tagging-guidelines/article/tags.html>.
