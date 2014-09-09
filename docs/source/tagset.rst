.. _xml-encoding:

encoding
========
Atributo que especifica a codificação de caracteres usada na elaboração do documento. 
Para o SciELO, todos os XMLs devem ser codificados em *utf-8*.
 
Para maiores detalhes leia a especificação do padrão XML 
(`2.8 Prolog and Document Type Declaration <http://www.w3.org/TR/2000/REC-xml-20001006#sec-prolog-dtd>`_).
 
.. code-block:: xml
 
    <?xml version="1.0" encoding="utf-8"?>
 

.. _xml-doctype:

<!DOCTYPE>
==========
 
A tag de declaração ``<!DOCTYPE>`` serve para indicar a :term:`DTD` 
a qual o XML é associado, ou seja, as regras estruturais do documento. 
O SciELO Publishing Schema utiliza como base o padrão *JATS 1.0*. 
 
Exemplo versão JATS 1.0:
 
.. code-block:: xml
 
    <!DOCTYPE article PUBLIC "-//NLM//DTD JATS (Z39.96) Journal Publishing DTD v1.0 20120330//EN" "JATS-journalpublishing1.dtd">
 

Exemplo versão PMC 3.0 (suporte por tempo indeterminado):
 
.. code-block:: xml
 
    <!DOCTYPE article PUBLIC "-//NLM//DTD Journal Publishing DTD v3.0 20080202//EN" "journalpublishing3.dtd">

 
Tags Flutuantes
===============

As chamadas tags flutuantes podem aparecer em todo o documento, ``<front>``, 
``<body>`` e ``<back>``.


.. _elemento-xref:

<xref>
------

Aparece em
  1. article/front/article-meta/title-group/article-title
  2. article/front/article-meta/trans-title-group/trans-title
  3. article/front/article-meta/contrib-group/contrib
  4. article/body/p
  5. article/body/sec/p
  6. article/body/p/table-wrap/table/thead/tr/th
  7. article/body/p/table-wrap/table/tbody/tr/td
  8. article/body/sec/p/table-wrap/table/thead/tr/th
  9. article/body/sec/p/table-wrap/table/tbody/tr/td
  #. article/back/app-group/app/table-wrap/table/thead/tr/th
  #. article/back/app-group/app/table-wrap/table/tbody/tr/td
  #. article/back/app-group/app/supplementary-material/table-wrap/table/thead/tr/th
  #. article/back/app-group/app/supplementary-material/table-wrap/table/tbody/tr/td
 
Atributos obrigatórios
  1. rid
  2. ref-type
 
Ocorre
  Zero ou mais vezes


Tag de Referência Cruzada usada para relacionar e/ou fazer link com alguma 
informação no texto. 
 
Os atributos obrigatórios para ``@xref`` são:
 
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

     <contrib-group>
    <contrib contrib-type="author">
                    <name>
                        <surname>Lacerda</surname>
                        <given-names>Marcus VG</given-names>
                    </name>
                    <xref ref-type="aff" rid="aff1">1</xref>
                </contrib-group>
            <aff id="aff1">
                <label>1</label>
                <institution content-type="orgname">Universidade do Estado do Amazonas</institution>
                <addr-line>
                    <named-content content-type="city">Manaus</named-content>
                    <named-content content-type="state">AM</named-content>
                </addr-line>
                <country>Brasil</country>
                <institution content-type="original">Universidade do Estado do Amazonas, Manaus, AM, Brasil</institution>
            </aff>
     
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
 

.. _elemento-label:
 
<label>
-------

Aparece em
  1. article/front/article-meta/aff
  2. article/front/article-meta/author-notes/corresp
  3. article/front/article-meta/author-notes/fn
  4. article/body/p/fig
  5. article/body/p/table-wrap
  6. article/body/p/disp-formula
  7. article/body/p/media
  8. article/body/p/supplementary-material
  9. article/body/p/list
  10. article/body/p/list/list-item
  11. article/body/sec/p/fig
  12. article/body/sec/p/table-wrap
  13. article/body/sec/p/disp-formula
  14. article/body/sec/p/media
  15. article/body/sec/p/supplementary-material
  16. article/body/sec/p/list
  17. article/body/sec/p/list/list-item
  18. article/back/ref-list/ref
  19. article/back/app-group/app/glossary
  20. article/back/glossary
  21. article/back/app-group/app
  22. article/back/app-group/app/table-wrap
  23. article/back/app-group/app/fig  
  24. article/back/app-group/app/glossary/desf-list
  25. article/back/glossary/def-list
  26. article/back/fn-group/fn
  27. article/back/app-group/app/supplementary-material/table-wrap
  28. article/back/app-group/app/supplementary-material/fig
 
Ocorre
  Zero ou mais vezes


A tag ``<label>`` é responsável pela identificação numérica ou alfabética 
que faz a ligação entre etiquetas.

Exemplos:
 
.. code-block:: xml
 

     <aff id="aff01">
          <label>a</label>
     
         <corresp id="c01">
            <label>*</label>

<fig id="f01">
          <label>Figure 1</label>

<table-wrap id="t01">
          <label>Table 1</label>
 
     <ref id="B01">1</ref>
          <label>1</label>
 
      <app>
          <label>Apêndice</label>
 
 
.. _elemento-p:

<p>
---
 
Aparece em
  1. article/front/article-meta/abstract
  2. article/front/article-meta/abstract/sec
  3. article/front/article-meta/trans-abstract
  4. article/front/article-meta/trans-abstract/sec
  5. article/front/article-meta/author-notes/fn
  6. article/body
  7. article/body/sec/title  
  8. article/body/p/table-wrap/table-wrap-foot/fn
  9. article/body/p/disp-quote
  10. article/body/p/list/list-item
  11. article/body/sec/p/table-wrap/table-wrap-foot/fn
  12. article/body/sec/p/disp-quote
  13. article/body/sec/p/list/list-item   
  14. article/body/sig-block/sig
  15. article/back/ack/title
  16. article/back/fn-group/fn
  17. article/back/app-group/app
  18. article/back/app-group/app/glossary/desf-list/def-item/def  
  19. article/back/glossary/desf-list/def-item/def
 
Ocorre
  Uma ou mais vezes
 

Esta tag identifica parágrafos. Deve ser inserida no documento sem nenhum 
tipo de atributo.


.. _regra-atribuicao-id:

Regra de atribuição de @id
==========================
 
Para a composição do ``@id``, combine um prefixo com uma numeração sequencial, 
como segue:
 

+------------------------+---------------------------+---------+-----------------------+
| Elemento XML           | Descrição                 | Prefixo | Exemplo               |
+========================+===========================+=========+=======================+
| aff                    | Afiliação                 | aff     | aff01, aff02, ...     |
+------------------------+---------------------------+---------+-----------------------+
| app                    | Apêndice                  | app     | app01, app02, ...     |
+------------------------+---------------------------+---------+-----------------------+
| corresp                | Correspondência           | c       | c01, c02, ...         |
+------------------------+---------------------------+---------+-----------------------+
| disp-formula           | Equações                  | e       | e01, e02, ...         |
+------------------------+---------------------------+---------+-----------------------+
| fig                    | Figuras                   | f       | f01, f02, ...         |
+------------------------+---------------------------+---------+-----------------------+
| def-list               | Glossário                 | d       | d01, d02, ...         |
+------------------------+---------------------------+---------+-----------------------+
| table-wrap-foot/fn     | Notas de rodapé de tabela | TFN     | TFN01, TFN02, ...     |
+------------------------+---------------------------+---------+-----------------------+
| author-notes/fn |      | Notas de rodapé do artigo | fn      | fn01, fn02, ...       | 
| fn-group/fn            |                           |         |                       |
+------------------------+---------------------------+---------+-----------------------+
| table-wrap             | Tabela                    | t       | t01, t02, ...         |
+------------------------+---------------------------+---------+-----------------------+
| supplementary-material | Suplemento                | suppl   | suppl01, suppl02, ... |
+------------------------+---------------------------+---------+-----------------------+
| ref                    | Referência bibliográfica  | B       | B01, B02, ...         |
+------------------------+---------------------------+---------+-----------------------+
| media                  | Media                     | m       | m01, m02, ...         |
+------------------------+---------------------------+---------+-----------------------+
| sec                    | Seções                    | sec     | sec01, sec02, ...     |
+------------------------+---------------------------+---------+-----------------------+


.. _regra-nomeacao-imagem:

Regra de nomeação de imagens
============================
 
Para imagens (que podem ser figuras, equações, apêndices e etc) utilizar a 
seguinte estrutura de nomeação tanto nas imagens dentro do XML quanto para 
as imagens da pasta do pacote do fascículo ou lote de :term:`ahead-of-print`.
 
Para fascículo: 

    **ISSN**-**acrônimo**-**volume**-**número**-**paginação**-**nomedaimagem.extensãodaimagem**
 

Sendo:
 
* ISSN: Se houver mais de um, dar preferência ao impresso.
* Acrônimo: Sigla do periódico na SciELO
* Volume: Volume do fascículo
* Número: Número e/ou suplemento do fascículo (tratar como "n" e "s")
* Paginação: Manter a informação da primeira página contendo no mínimo 4 dígitos
* Nome da imagem: Prefixo com uma numeração sequencial 
  (ver :ref:`regra-atribuicao-id`)
 
Exemplo:
 
    *1807-5932-clin-69-05-0308-gf01.tif*
 

.. note:: Cada item deve ser separado por um hifén e obrigatoriamente deve-se 
          manter visível a extensão da imagem após o "ponto", optando 
          preferencialmente por imagens em formato *tif*.
 

Para ahead-of-print:
 
    **ISSN**-**acrônimo**-**númerodedoisemoprefixo.extensãodaimagem**
 
Exemplo:
 
    *0074-0276-mioc-00740276130057-gf01.tif*


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
 
Ocorre
  Uma vez
 

A tag ``<article>`` representa o elemento raiz do XML, e deve conter 
obrigatoriamente os atributos ``@dtd-version``, ``@article-type``, ``@xml:lang`` e
``@xmlns:xlink="http://www.w3.org/1999/xlink"``.

O atributo ``@xmlns:mml="http://www.w3.org/1998/Math/MathML"`` é opcional e 
deve ser utilizado apenas quando equações MathML forem identificadas no 
documento.

Para ``@dtd-version`` utilizar os valores 1.0 ou 3.0 conforme a :term:`DTD`, 
explicitada em :ref:`xml-doctype`. Para ``@article-type`` define-se a tipologia 
de artigos, os valores que podem ser utilizados são:
 
+--------------------+----------------------------------------------------------+
| Valor              | Descrição                                                |
+====================+==========================================================+
| research-article   | artigo original - abrange pesquisas, experiências        |
|                    | clínicas ou cirúrgicas ou outras contribuições originais.|
+--------------------+----------------------------------------------------------+
| letter             | cartas - comunicação entre pessoas ou instituições e     |
|                    | organizações por intercâmbio de cartas                   |
+--------------------+----------------------------------------------------------+
| article-commentary | comentários - uma nota crítica ou esclarecedora, escrita |
|                    | para discutir, apoiar ou debater um artigo ou outra      |
|                    | apresentação anteriormente publicada. Pode ser um artigo,| 
|                    | carta, editorial, etc. Estas publicações podem aparecer  |
|                    | como comentário, comentário editorial, ponto de vista,   |
|                    | etc.                                                     |
+--------------------+----------------------------------------------------------+
| brief-report       | comunicação breve - compreende breves relatos de         |
|                    | experiências, trabalhos ou projetos de investigação      |
|                    | em andamento.                                            |
+--------------------+----------------------------------------------------------+
| editorial          | editorial - uma declaração de opiniões, crenças e        |
|                    | políticas do editor de uma revista, geralmente sobre     |
|                    | assuntos de significado científico de interesse da       |
|                    | comunidade científica ou da sociedade.                   |
+--------------------+----------------------------------------------------------+
| in-brief           | press release - comunicação breve de linguagem           |
|                    | jornalística sobre um artigo ou tema.                    |
+--------------------+----------------------------------------------------------+
| case-report        | informe/relato de caso - descrição sumária de casos      |
|                    | especiais, que, por sua raridade despertam interesse     |
|                    | informativo para a coletividade.                         |
+--------------------+----------------------------------------------------------+
| report             | informe/relatório técnico - um informe que dá detalhes   |
|                    | de uma investigação ou resultado de um problema          |
|                    | científico. Pode também relatar um artigo científico,    |
|                    | o estado e posição atual de uma investigação científica  |
|                    | e o desenvolvimento da mesma.                            |
+--------------------+----------------------------------------------------------+
| note               | nota - relata resultados parciais ou preliminares de     |
|                    | investigação empírica.                                   |
+--------------------+----------------------------------------------------------+
| correction         | errata - corrige erros apresentados em artigos após      |
|                    | sua publicação online/impressa.                          |
+--------------------+----------------------------------------------------------+
| obituary           | obituário - anúncio de morte normalmente de              |
|                    | pesquisadores de notório saber de uma determinada        |
|                    | área para conhecimento de seus pares.                    |
+--------------------+----------------------------------------------------------+
| abstract           | resumo - uma apresentação precisa e resumida de uma      |
|                    | obra sem agregar interpretação ou crítica, acompanhado   |
|                    | de uma referência bibliográfica da obra original.        |
+--------------------+----------------------------------------------------------+
| review-article     | revisão - um artigo que se refere a um material          |
|                    | já publicado sobre um tema. Pode ser extenso quanto      |
|                    | à complexidade e ao intervalo de tempo do material       |
|                    | investigado.                                             |
+--------------------+----------------------------------------------------------+
| book-review        | resenha - análise críticas de livros e outras            |
|                    | monografias.                                             |
+--------------------+----------------------------------------------------------+
| product-review     | comentário de produto - Descrição, análise ou avaliação  |
|                    | de um produto, como um livro.                            |
+--------------------+----------------------------------------------------------+
| clinical-trial     | ensaio clínico - ensaio clínico que segue um plano ou    |
|                    | protocolo pré-definido e registrado.                     |
+--------------------+----------------------------------------------------------+
| retraction         | retratação - a retratação de um artigo científico é um   |
|                    | instrumento para corrigir o registro acadêmico publicado |
|                    | equivocadamente, por plágio, por exemplo.                |
+--------------------+----------------------------------------------------------+
| collection         | coleção - utilizada quando há um conjunto de cartas,     |
|                    | respostas, resenhas etc. O tipo collection é utilizado   |
|                    | em "article" do artigo principal e em ``<sub-article>``  |
|                    | ou ``<response>`` é identificado cada carta, resenha,    | 
|                    | resposta etc.                                            |
+--------------------+----------------------------------------------------------+


.. note:: O atributo ``@article-type`` identifica o tipo de documento. 
          Não confundir com a seção em que o documento aparece no sumário.
 

Para ``@xml:lang``, utilizar código de duas letras conforme norma *ISO 639-1*. 
Para uma lista completa dos códigos disponíveis e mais informações sobre a 
norma *ISO 639-1*, acesse http://www.mathguide.de/info/tools/languagecode.html.
 

Exemplo da tag completa versão JATS 1.0:
 
.. code-block:: xml
 
     <article xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:mml="http://www.w3.org/1998/Math/MathML" dtd-version="1.0" article-type="research-article" xml:lang="en">
 

Exemplo da tag completa versão PMC 3.0:
 
.. code-block:: xml

    <article xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:mml="http://www.w3.org/1998/Math/MathML" dtd-version="3.0" article-type="research-article" xml:lang="en">
 

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
notas de autor, informações de resenhas de livros.
 

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
  1. journal-id-type='nlm-ta' ou journal-id-type='publisher-id'
 
Ocorre
  Uma vez


Especifica o título padronizado do periódico.
 
Para o uso do título do periódico no Pubmed, 
utiliza-se ``@journal-id-type="nlm-ta"``:
 
.. code-block:: xml
 
    <journal-id journal-id-type="nlm-ta">
        Mem Inst Oswaldo Cruz
    </journal-id>
 

.. note:: Para verificar se o periódico está indexado no Medline 
          consulte o link http://www.ncbi.nlm.nih.gov/pubmed/advanced


Para o uso do acrônimo do periódico no SciELO, 
utiliza-se ``@journal-id-type="publisher-id"``:
 
.. code-block:: xml
 
    <journal-id journal-id-type="publisher-id">
        mioc
    </journal-id>


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
            <journal-title>
                Brazilian Journal of Otorhinolaryngology
            </journal-title>
            <abbrev-journal-title abbrev-type="publisher">
                Braz J Otorhinolaryngol.
            </abbrev-journal-title>
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
            <journal-title>
                Brazilian Journal of Medical and Biological Research
            </journal-title>
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
 
Atributo obrigatório
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
        <abbrev-journal-title abbrev-type="publisher">
            Braz. J. Med. Biol. Res.
        </abbrev-journal-title>
    </journal-title-group>
 

.. _elemento-issn:
 
<issn>
^^^^^^

Aparece em
  :ref:`elemento-journal-meta`, :ref:`elemento-element-citation`
 
Atributos obrigatórios em ``<front>``
  1. pub-type='ppub' ou pub-type='epub'
 
Ocorre
  Uma ou mais vezes


O ISSN é um código numérico, único, que identifica uma publicação seriada 
a qual é definida pela norma *ISO 3297:2007*. Normalmente cada tipo de 
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
            <publisher-name>
                Instituto Oswaldo Cruz, Ministério da Saúde
            </publisher-name>
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
de uso Creative Commons e contagem de elementos.

 
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
        <article-id pub-id-type="doi">
            10.1590/0074-0276130047
        </article-id>
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
deve ser adotado sempre a seção ``Articles``.
 
 
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
  :ref:`elemento-title-group`, :ref:`elemento-element-citation`
 
Ocorre
  Uma vez


Esta tag pode ser utilizada para especificar o título do artigo em si 
em :ref:`elemento-article-meta`, ou para especificar um título de documento 
nas referências em :ref:`elemento-element-citation`. Em ambos os casos, o 
atributo ``@xml:lang`` não deve ser utilizado.
 
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
 
     <title-group>
          <article-title>Correlação entre sintomas e tempo de evolução do câncer do trato aerodigestivo superior com o estádio inicial e avançado</article-title>
     </title-group>.


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
institucionais. Tags como ``<name>``, ``<collab>``, ``<on-behalf-of>``, 
``<xref>``, ``<role>`` e ``<anonymous>`` podem ser encontradas neste elemento. 
 
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
 
     <contrib contrib-type="author">
 
**Exemplo:**
 
.. code-block:: xml
 
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
 
.. note:: Observar normas para entrada de nomes (*AACR2* - Código de Catalogação 
          Anglo Americano e/ou Currículo Lattes dos autores, avaliar formas 
          de entrada autorizadas).
 

.. _elemento-collab:
 
<collab>
^^^^^^^^

Aparece em
  :ref:`elemento-contrib`, 
  :ref:`elemento-person-group` 
 
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

    <!-- CORRIGIR: Dados reais -->

    ...
    <contrib-group>
        ...
        <contrib>
            ...
            <on-behalf-of>
                Identificação de um grupo ou organização
            </on-behalf-of>
            ...
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
Anglo Americano e/ou Currículo Lattes dos autores).
 
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
  1. id
 
Ocorre
  Zero ou mais vezes


Considera-se como afiliação o vínculo institucional dos contribuintes do artigo. 
Os dados de afiliação são importantes para localizar e mensurar a produção 
científica por país, estado, cidade, bem como por instituição e seus 
departamentos. Recomenda-se que os nomes das instituições das afiliações 
sejam especificadas em sua forma original, sem tradução ou abreviações de 
seus nomes. Ou seja, por exemplo, identificar preferencialmente 
**Universidade de São Paulo** a USP, ou University of São Paulo, ou 
Saint Paul University, entre outras possíveis formas. 
Por isso, quando ocorre no documento de existir mais de uma forma, usar a original.
 
Para composição do atributo ``@id``, utiliza-se o seguinte padrão: 
``aff`` + o número de ordem da afiliação. (Ver :ref:`regra-atribuicao-id`)
 
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <aff id="aff01">
        <label>1</label>
        <institution content-type="orgname">
            Fundação Oswaldo Cruz
        </institution> 
        <institution content-type="orgdiv1">
            Escola Nacional de Saúde Pública Sérgio Arouca
        </institution>
        <institution content-type="orgdiv2">
            Centro de Estudos da Saúde do Trabalhador e Ecologia Humana
        </institution>   
        <addr-line>
            <named-content content-type="city">Manguinhos</named-content>
            <named-content content-type="state">RJ</named-content>
        </addr-line>
        <country>Brasil</country>
        <institution content-type="original">
            Prof. da Fundação Oswaldo Cruz; da Escola Nacional de Saúde Pública Sérgio Arouca, do Centro de Estudos da Saúde do Trabalhador e Ecologia Humana. RJ - Manguinhos / Brasil. <named-content content-type="email">maurosilva@fiocruz.com</named-content>
        </institution>
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

+---------+--------------------------------------------------------------------+ 
| Valor   | Descrição                                                          |
+=========+====================================================================+
| orgname | Representando a instituição de nível hierárquico maior mencionado  |
|         | na afiliação                                                       |
+---------+--------------------------------------------------------------------+ 
| orgdiv1 | Representando a primeira divisão da instituição mencionada em      |
|         | orgname                                                            |
+---------+--------------------------------------------------------------------+ 
| orgdiv2 | Representando a segunda divisão da instituição mencionada em       |
|         | orgname                                                            |
+---------+--------------------------------------------------------------------+ 
 

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
original. Caso o email esteja presente também deve ser marcado; ambas as tags 
possuem atributo obrigatório ``@content-type`` dos tipos: original, email ou country conforme segue no exemplo:


.. code-block:: xml
 
     <institution content-type="original">Técnica de Cardiopneumologia. Unidade de Fisiopatologia Respiratória, Serviço de Pneumologia, Centro Hospitalar Lisboa Norte, Lisboa, Portugal. 
     <named-content content-type="email">mara@scielo.org</named-content></institution>

 
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
 
Ocorre
  Uma vez


Identifica o país da afiliação.
 
A tag pode possuir o atributo ``@country`` e nele deve ser atribuído o código 
do país de acordo com a Norma *ISO 3166*, com dois caracteres alfabéticos.

Para consultar o código do país consulte o link: 
https://www.iso.org/obp/ui/#iso:pub:PUB500001:en


Exemplo:

.. code-block:: xml
 
    ...
    <aff id="aff01">
        ...
        <country>Brasil</country>
        ...
    </aff>
    ...


.. code-block:: xml

    ...
    <aff id="aff01">
        ...
        <country country="BR">Brasil</country>
        ...
    </aff>
    ...


.. note:: Para a próxima versão do SciELO PS este atributo passará a ser obrigatório.


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
            <corresp id="c01">
                <bold>Correspondence:</bold> Maria Silva, Avenida Senador Felinto Muller,s/n - Cidade Universitária, 79070-192 Campo Grande - MS Brasil,<email>maria.ra@hotmail.com</email>
            </corresp>
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
| corresp                   | Informação de correspondência                    |
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
|                           | ``<back>``                                       |
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
 
Para composição de ``@id`` de **notas** utiliza-se o seguinte padrão: "fn" + o 
número de ordem das notas. (Ver :ref:`regra-atribuicao-id`)
 
Para notas que apresentam uma etiqueta de identificação (1, 2, a, b, *, e etc)
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
 
Para composição de ``@id`` utiliza-se o seguinte padrão: "c" + o número de ordem da correspondência. 
(Ver :ref:`regra-atribuicao-id`)
 
Exemplo:

.. code-block:: xml
 
    ...
    <author-notes>
        ...
        <corresp id="c01">
            Dr. Edmundo Figueira Departamento de Fisioterapia, Universidade FISP - São Paulo, Brasil. E-mail: <email>contato@contato.com</email>
        </corresp>
        ...
    </author-notes>
    ...
 
.. note:: Esta tag não necessita da inserção de parágrafo ``<p>``.
 
 
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

 
Os valores de dia, mês e ano devem ser representados segundo o PDF do 
artigo/fascículo.
 
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
          Apr, Jun, Jul, Aug, Sep, Oct, Nov e Dec.


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
  2. Zero ou mais vezes em ``<back>``


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

+-----------+------------+
| Valor     | Descrição  |
+===========+============+
| book      |            |
+-----------+------------+
| software  |            |
+-----------+------------+
| article   |            |
+-----------+------------+
| issue     |            |
+-----------+------------+
| website   |            |
+-----------+------------+
| film      |            |
+-----------+------------+
| hardware  |            |
+-----------+------------+
 

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

+-----------+------------+
| Valor     | Descrição  |
+===========+============+
| author    |            |
+-----------+------------+
| compiler  |            |
+-----------+------------+
| director  |            |
+-----------+------------+
| editor    |            |
+-----------+------------+
| inventor  |            |
+-----------+------------+
| translator|            |
+-----------+------------+

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


Identifica um grupo de páginas mencionados numa referência.

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

.. note:: A inserção do grupo de páginas deve ser inserido posteriormente as 
          informações da primeira página do grupo :ref:`elemento-fpage` e de 
          última página do grupo :ref:`elemento-lpage`. (CORRIGIR! Não entendi nada!)


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
  :ref:`elemento-element-citation`
  
Ocorre 
  Zero ou mais vezes


Representa o nome da casa publicadora ou editora numa referência.


.. _elemento-publisher-loc:

<publisher-loc>
^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-product`,
  :ref:`elemento-element-citation`
  
Ocorre 
  Zero ou mais vezes


Identifica o local de uma casa publicadora ou editora numa referência.


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

+------------+-------------+
| Valor      | Descrição   |
+============+=============+
| received   |             |
+------------+-------------+
| accepted   |             |
+------------+-------------+
| rev-recd   |             |
+------------+-------------+

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

+-------------------------------------------------+----------------------+
| Valor                                           | Descrição            |
+=================================================+======================+
| http://creativecommons.org/licenses/by/4.0/     | CC-BY versão 4.0     |
+-------------------------------------------------+----------------------+
| http://creativecommons.org/licenses/by/3.0/     | CC-BY versão 3.0     |
+-------------------------------------------------+----------------------+
| http://creativecommons.org/licenses/by-nc/4.0/  | CC-BY-NC versão 4.0  |
+-------------------------------------------------+----------------------+
| http://creativecommons.org/licenses/by-nc/3.0/  | CC-BY-NC versão 3.0  |
+-------------------------------------------------+----------------------+


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
zero ou mais vezes, ele se faz obrigatório quando ``<article>`` for declarado
com o atributo ``@article-type="research-article"`` ou ``@article-type="review-article"``.

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
 
.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <kwd-group xml:lang="pt">
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
            <kwd>Broncoscopia</kwd>
            <kwd>Curvas de fluxo-volume expiratório máximo</kwd>
            <kwd>sensibilidade e especificidade</kwd>
            <kwd>Neoplasias pulmonares</kwd>    
        </kwd-group>
        <kwd-group xml:lang="en">
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
  Uma vez


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
 

.. _elemento-award-id:
 
<award-id>
^^^^^^^^^^

Aparece em
  :ref:`elemento-award-group`
 
Ocorre
  Uma vez


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
            </award-group>
            <award-group>
                <funding-source>CNPq</funding-source>
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
     
.. note:: Nunca insira mais de um número de contrato em um único 
          :ref:`elemento-award-group`, mesmo quando for de uma mesma instituição. 
 
 
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
                    <funding-source>Brazilian Ministry of Health/Secretariat of Health Surveillance/Department of STD, AIDS and Viral Hepatitis</funding-source>
                    <award-id>234/07</award-id>
                </award-group>
                <funding-statement>This study was supported by the Brazilian Ministry of Health/Secretariat of Health Surveillance/Department of STD, AIDS and Viral Hepatitis, through the Project of International Technical Cooperation AD/BRA/03/H34 between the Brazilian Government and the United Nations Office on Drugs and Crime (Process CSV 234/07).</funding-statement>
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
                <p>This study was supported by the Brazilian Ministry of Health/Secretariat of Health Surveillance/Department of STD, AIDS and Viral Hepatitis, through the Project of International Technical Cooperation AD/BRA/03/H34 between the Brazilian Government and the United Nations Office on Drugs and Crime (Process CSV 234/07).</p>
            </fn>
        </fn-group>
        ...
    </back>
 

.. note:: CORRIGIR: Revisar essas notas! ********
          No caso da nota de rodapé com informação de financiamento, sempre 
          mantê-la dentro de ``<back>`` em :ref:`elemento-fn-group` com o 
          tipo ``@fn-type="financial-disclosure"`` e em <front>.
 
.. note:: Notas SEM NÚMERO DE CONTRATO, ficam apenas em ``<back>`` mas com 
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
          :ref:`elemento-app-group`, devem ser inseridas obrigatoriamente após 
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

 
As seções podem ser compostas por uma ou mais :term:`subseções`, neste caso, 
cada :term:`subseção` deverá ser marcada com tag ``<sec>`` dentro da seção maior.
 
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

 
Pode possuir o atributo ``@id`` para criar referência cruzada 
:ref:`elemento-xref` com informações do texto.
 
Exemplo:
 
.. code-block:: xml

    ...
    <body>
        ...
        <sec sec-type="methods" id="sec01">
            <title>Methodology</title>
            <p>Each patient underwent a brief physical examination, and the degree of dyspnea was determined by the Medical Research Council (MRC) 5-point scale.</p>
            ...
        </sec>
        ...
    </body>
    ...
 
Para a composição do atributo ``@id``, utiliza-se o seguinte padrão: 
``sec`` + o número de ordem da seção. (Ver :ref:`regra-atribuicao-id`)
 
 
.. _disp-formula:
     
<disp-formula>
--------------

Aparece em
  :ref:`elemento-body`,
  :ref:`elemento-p`,
  ``<th>``,
  ``<td>``,
  ``<app>``,
  :ref:`elemento-supplementary-material`

Atributos obrigatórios
  1. id
 
Ocorre
  Zero ou mais vezes


Tag para identificar equações em parágrafos no texto, podem ser 
apresentadas como imagem ou codificadas e serão identificadas pela tag 
``<disp-formula>``. Se a equação for capturada como imagem, deve-se incluir o 
nome do arquivo em ``<graphic>``:
 
Para composição de ``@id`` utiliza-se o seguinte padrão: ``e`` + o número de 
ordem da equação. (Ver :ref:`regra-atribuicao-id`)
 
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


Também representa uma tag para identificar equações que estejam 
posicionadas em linha, ou seja, em meio a um parágrafo.
 
Para composição de ``@id`` utiliza-se o seguinte padrão: 
``e`` + o número de ordem da equação. (Ver :ref:`regra-atribuicao-id`)
 
Exemplo:

.. code-block:: xml
 
    ...
    <p>We also used an enrichment factor for surface waters (EF<sub>w</sub>) based on the equation:<inline-graphic xlink:href="1234-5678-rctb-45-05-0110-e01.tif"/>. The EF<sub>s</sub> and EF<sub>w</sub> quantified the concentration of the element of interest (C<sub>i</sub>) in the sample, in relation to the (natural) geochemical background.</p>
    ...

No caso de equações codificadas, deve-se observar as orientações de 
codificação recomendada pela :term:`W3C` em linguagem :term:`MathML` 
(http://www.w3.org/TR/MathML3/), sendo o elemento base ``<mml:math>``.
 
**Exemplo**: para codificar  σˆ2*
 
.. code-block:: xml
 
    <!-- codificar: σˆ2 -->

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
  ``<app>``,
  :ref:`elemento-app-group`,
  :ref:`elemento-body`,
  :ref:`elemento-glossary`,
  :ref:`elemento-p`,
  :ref:`elemento-sec`,
  :ref:`elemento-supplementary-material`,
  ``<table-wrap-group>``

Atributos obrigatórios
  1. id
 
Ocorre
  Zero ou mais vezes


É utilizada para especificar todas as partes de uma única tabela, incluindo 
:ref:`elemento-label`, :ref:`elemento-caption` ou :ref:`elemento-table-wrap-foot`. 
 
Para composição do atributo ``@id`` utiliza-se o seguinte padrão: 
``t`` + o número de ordem da tabela. (Ver :ref:`regra-atribuicao-id`)
 
 
.. _elemento-table-wrap-foot:

<table-wrap-foot>
^^^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-table-wrap`

Ocorre
  Zero ou mais vezes


Em ``<table-wrap-foot>`` é possível fazer a identificação de nota de rodapé de 
tabela por meio de tags ``<fn>``, que devem apresentar obrigatoriamente o 
atributo ``@id``.
 
Para composição do atributo ``@id`` do elemento ``<fn>``, utiliza-se o seguinte 
padrão: ``TFN`` + o número de ordem da nota de rodapé de table. 
(Ver :ref:`regra-atribuicao-id`)
 
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
  ``<inline-supplementary-material>``,
  ``<app>``

Atributos obrigatórios
  1. id
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
 
Para composição do atributo ``@id`` utiliza-se o seguinte padrão: 
``suppl`` + o número de ordem do suplemento. (Ver :ref:`regra-atribuicao-id`)
 
O material suplementar pode estar em :ref:`elemento-front`, dentro de 
:ref:`elemento-article-meta`, em :ref:`elemento-body` como seção ou entre 
parágrafos ou em :ref:`elemento-back`, onde só poderá ser identificado caso 
esteja especificado dentro do grupo de apêndices <app-group> (CORRIGIR: <app-group> não consta no SciELO PS como possível pai do elemento atual).
 
Seus atributos obrigatórios são:
 
* ``@id``: Utilizado como um identificador único no documento e ganha maior importância quando há mais que um material suplementar e/ou quando o material suplementar é referenciado no corpo do texto. Nesse caso é necessário relacionar a chamada no texto com o "id" do material suplementar.
* ``@mimetype``: Utilizado para especificar o tipo de mídia como "vídeo" ou "aplicação".
* ``@mime-subtype``: Utilizado para especificar o formato da mídia.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <supplementary-material id="suppl01" 
                            xlink:href="0000-0000-abcd-01-12-0001-suppl01.mp3" 
                            mimetype="audio"
                            mime-subtype="mpeg">
 
- **@xlink:href:** utilizado para indicar do nome completo do arquivo, tais como: pdf, vídeo, zip etc.
 

**Exemplo de material suplementar em <front>:**
 
..note:: Esta tag em <front> obrigatoriamente deve ser inserida abaixo das informações de paginação ou antes de <history>.
 
.. code-block:: xml
 
     <fpage>237</fpage>
     <lpage>259</lpage>
     <supplementary-material mimetype="application" mime-subtype="pdf" xlink:href="1234-5678-rctb-45-05-0110-suppl01.pdf"/>
 
**Exemplo de material suplementar em <body>:**
 
.. code-block:: xml
 
     <p>Descriptive analysis and the Pearson chi-squared test
were used to verify the association between categorical variables. The normality of the distribution of continuous variables was verified by drawing a histogram and plots (<xref ref-type="supplementary-material" rid="suppl01">Supplementary material A</xref>).</p>

<p>
     <supplementary-material id="suppl01">
         <label>Fig 1.</label>
             <caption><title>Supplementary material A</title></caption>
     <graphic xlink:href="1234-5678-rctb-45-05-0110-suppl01.tif"/>
     </supplementary-material>
</p>
 
<p>Os níveis de PCR, lactato, S<sub>2</sub> e DB não foram associados com readmissão. Esses dados estão disponíveis na tabela 1S do material eletrônico suplementar. <supplementary-material xlink:href="1234-5678-rctb-45-05-0110-suppl01.pdf"/></p>
 
     
 
**Exemplo de material suplementar em <back>:**
 
.. code-block:: xml
 
<app-group>
     <app>
<supplementary-material id="suppl01">
          <label>Fig 1.</label>
          <caption><title>Material Suplementar</title></caption>
                <graphic xlink:href="1234-5678-rctb-45-05-0110-suppl01.tif"/>
     </supplementary-material>
     </app>
<app-group>


<p>Devido a esse elevado percentual de dados omissos, possivelmente não influenciaram no resultado final do <inline-supplementary-material xlink:href="0103-507X-rbti-26-02-0130-s01.pdf" mimetype="application" mime-subtype="pdf">Material Suplementar</inline-supplementary-material></p>
 
 
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
 
    <!-- CORRIGIR: Exemplo não reflete a espec. -->

    <p>Mauris ac magna fermentum, pharetra tellus aliquam, tempor felis.</p>
    <disp-quote>
        <p>"Sed luctus quam a felis sagittis lacinia. Etiam auctor tincidunt nibh, sit amet convallis urna convallis nec. Nullam venenatis dapibus dapibus. Vivamus et arcu blandit, laoreet tellus eget, sodales sapien. Etiam fringilla turpis enim, sit amet porta velit faucibus eu."</p>
    </disp-quote>
    <p>Donec dapibus lacus urna, eu fringilla quam tempus eu.</p>
 
A tag ``<disp-quote>`` também é utilizada para epígrafes, citações em blocos 
e extratos dentro do texto.
 
 
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
  :ref:`elemento-p`, ``<list-item>``

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
  ``<disp-formula>``,
  :ref:`elemento-fig`, 
  :ref:`elemento-table-wrap`,
  :ref:`elemento-media`,
  :ref:`elemento-supplementary-material`,
  ``<app>``

Ocorre
  Zero ou mais vezes


Tag que representa uma descrição textual visível de uma tabela, figura ou 
objeto similar.
 
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
  ``<app>``,
  :ref:`elemento-supplementary-material`

Atributos obrigatórios
  1. id
 
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
 
* **@xlink:href:** utilizado para especificar um endereço ou links externos. 
  Portanto o @xlink:href deve conter nomes de imagens/arquivos e também o 
  nome completo de uma URL.
 
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
 
Para composição do atributo ``@id`` utiliza-se o seguinte padrão: 
``f`` + o número de ordem da figura. (Ver :ref:`regra-atribuicao-id`)
 
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

 
.. _elemento-media:

<media>
-------

Aparece em
  :ref:`elemento-p`,
  :ref:`elemento-fig`,
  ``<app>``,

Atributos obrigatórios
  1. mime-subtype
  2. xlink:href
 
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
 
    <p>Within the limitations of this study, it may be concluded that remaining tooth wall thickness did not influence the fatigue resistance of molars restored with CAD/CAM ceramic inlays <media mimetype="video"  mime-subtype="mp4" xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/></p>
 

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
 

*Em ``<sec>`` do tipo material suplementar:*
 
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
deve-se usar a tag ``<break/>``, ou ``<p>`` como mostram os exemplos a seguir:

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
            <p><bold>Harry Weasley</bold></p>
            <p><italic>Editor Chefe<italic></p>
            <p>Profeta Diário</p>
        </sig>
    </sig-block>
 
 
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
de :ref:`back`.
 
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
  ``<ref-list>``. Esse elemento deve conter, obrigatóriamente, três tags: 
  :ref:`elemento-ref`, :ref:`elemento-mixed-citation` e
  :ref:`elemento-element-citation`.


.. _elemento-ref:

<ref>
-----

Aparece em
  :ref:`elemento-ref-list`

Atributo Obrigatório 
  ``@id``

Ocorre
  (quando houver :ref:`elemento-ref-list`)
  Uma ou mais vezes

Existem diversos tipos de referências e normas para apresentá-las num documento 
textual (:term:`ABNT`, :term:`Vancouver`, :term:`APA`, :term:`ISO` e 
:term:`OTHER`). Independente da norma usada, a representação dos elementos
essenciais em xml de uma referência devem ser identificados corretamente.
 
Para composição de ``@id`` de referências utiliza-se o seguinte padrão:
"B" + o número de ordem das referências. (Ver :ref:`regra-atribuicao-id`) 

Exemplo:

.. code-block:: xml
 
    ...
    <ref-list>
        <ref id="B01">
            <mixed-citation>referência inteira sem marcação</mixed-citation>
            <element-citation publication-type="tipo da referência">elementos marcados um a um</element-citation>
        </ref>
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

A tag ``<element-citation>`` apresenta a identificação detalhada de cada
referência biliográfica. Essa tag deve apresentar o atributo
``@publication-type``. O atributo indica o tipo de referência, os valores que
podem ser utilizados para o atributo ``@publication-type`` são:

+-----------+------------------------------------------------------------------+
| Valor     | Descrição                                                        |
+===========+==================================================================+
| journal   | utilizada para referenciar publicações seriadas, editadas em     |
|           | unidades sucessivas, com designações numéricas e/ou cronológicas |
|           | e destinada a ser continuada indefinidamente                     |
+-----------+------------------------------------------------------------------+
| book      | utilizada para referenciar monografia/livro. Pode Também         |
|           | representar somente uma parte ou capítulo de um livro            |
+-----------+------------------------------------------------------------------+
| webpage   | utilizada para referencias de um relatório técnico, normalmente  |
|           | de autoria institucional                                         |
+-----------+------------------------------------------------------------------+
| thesis    | utilizada para referenciar TCC para obtenção de um grau          |
|           | acadêmico, tais como livre-docência, doutorado, mestrado,        |
|           | bacharelado, licenciatura, etc                                   |
+-----------+------------------------------------------------------------------+
| confproc  | utilizada para referenciar documentos relacionados com eventos   |
|           | científicos: atas, anais, resultados, proceedings, convenção,    |
|           | conferência entre outras denominações                            |
+-----------+------------------------------------------------------------------+
| patent    | utilizada para referenciar patentes                              |
+-----------+------------------------------------------------------------------+
| software  | utilizada para referenciar um software que pode estar em vários  |
|           | suportes, como CDs, DVDs, em suporte online, dispositivos usb e  |
|           | etc                                                              |
+-----------+------------------------------------------------------------------+
| database  | utilizada para referenciar bases de dados                        |
+-----------+------------------------------------------------------------------+

.. note::

  * Nunca manter uma informação toda com formatação <italic>, <bold>, etc,
    dentro de alguma tag;
  * Todas as referências devem conter informação de fonte principal
    :ref:`elemento-source`;
  * Evitar pontuação dentro da marcação em :ref:`elemento-element-citation`
    (ponto final, vírgula etc);
  * Todas as informaçoes de uma referência devem ser marcadas, caso não exista
    uma tag específica para uma informação insirir esta em
    :ref:`elemento-comment`.

Exemplos:
 
.. code-block:: xml

    <!-- Journal Sample -->

    ...
    <ref-list>
        <ref id="B01">
            <label>1</label>
            <mixed-citation>Referência conforme aparece no artigo</mixed-citation>
            <element-citation publication-type="journal">
                <person-group person-group-type="author">
                    <name>
                        <surname>Sobrenome</surname>
                        <given-names>Prenomes</given-names>
                    </name>
                    <name>
                        <surname>Sobrenome</surname>
                        <given-names>Prenomes</given-names>
                    </name>
                </person-group>
                <article-title>Título do artigo</article-title>
                <source>Nome do Periódico</source>
                <season>Estações do ano (ex.: Inverno) ou intervalo de meses (Ex.: Jan-Mar)</season>
                <month>Mês</month>
                <year>ano</year>
                <volume>volume</volume>
                <issue>número</issue>
                <fpage>página inicial</fpage>
                <lpage>página final</lpage>
                <issn>número do ISSN na revista</issn>   
                <pub-id pub-id-type="pmid">somente números</article-id>
                <pub-id pub-id-type="pcmid">somente números</article-id>
                <pub-id pub-id-type="doi">somente números</article-id>
                <pub-id pub-id-type="pii">somente números</article-id>
                <elocation-id>representa um número de página eletrônica</elocation-id>
            </element-citation>
        </ref>
    <ref-list> 
    ...

.. code-block:: xml

  <!-- Book Sample --> 

    ...
    <ref-list>
        <ref id="B02">
            <label>2</label>
            <mixed-citation>Referência conforme aparece no artigo</mixed-citation>    
            <element-citation publication-type="book">
                <person-group person-group-type="author">                  
                    <name>
                        <surname>Sobrenome</surname>
                        <given-names>Prenomes</given-names>
                    </name>
                </person-group>
                <source>Nome do Livro</source>
                <edition>edição (inserir informação ed. ou th. e etc conforme no pdf)</edition>
                <publisher-loc>Lugar de publicação do livro (cidade, estado, país e etc)</publisher-loc>
                <publisher-name>Nome da editora/Casa publicadora</publisher-name>
                <year>Ano de publicação da obra</year>
                <size units="page">quantidade total de páginas do livro</size>
                <isbn>número do ISBN do livro</isbn>
                <fpage>100</fpage>
                <lpage>120</lpage>
                <page-range>100-101, 105, 107-120</page-range>
            </element-citation>
        </ref>
     </ref-list>
     ...

.. code-block:: xml
 
    <!-- Book Chapter Sample --> 

    ...
    <ref-list>
        <ref id="B03">
            <label>3</label>
            <mixed-citation>Referência conforme aparece no artigo</mixed-citation>
            <element-citation publication-type="book">
                <person-group person-group-type="author">
                    <name>
                        <surname>Sobrenome</surname>
                        <given-names>Prenomes</given-names>
                    </name>
                    <etal/>
                </person-group>
                <source>Nome do livro</source>
                <edition>edição (inserir informação ed. ou th. e etc conforme no pdf)</edition>
                <publisher-loc>Lugar de publicação do livro (cidade, estado, país e etc)</publisher-loc>
                <publisher-name>Nome da editora/Casa publicadora</publisher-name>
                <year>ano de publicação da obra</year>
                <chapter-title>Parte do livro ou capítulo</chapter-title>
                <fpage>página inicial da parte</fpage>
                <lpage>página final da parte</lpage>
            </element-citation>
       </ref>
    </ref-list>
    ...
 
.. code-block:: xml
 
    <!-- Webpage Sample -->

    ...
    <ref-list>
        <ref id="B04">
            <label>4</label>
            <mixed-citation>Referência conforme aparece no artigo</mixed-citation>
            <element-citation publication-type="webpage">
                <source>Título do documento (pode ser nome do site) [Internet]</source>
                <publisher-loc>Lugar de publicação</publisher-loc>
                <publisher-name>Nome da mantenedoura/instituição</publisher-name>
                <year>ano</year>
                <date-in-citation content-type="access-date">data de acesso ao link</date-in-citation>
                <date-in-citation content-type="updated">data de uptated</date-in-citation>
                <comment>
                  Available from:
                  <ext-link ext-link-type="uri" xlink:href="http://www.scielo.org">
                    www.scielo.org
                  </ext-link>
                </comment>
            </element-citation>
        </ref>
    </ref-list> 
    ...

.. note:: Quando a referência apresentar URL com texto (Disponível em: ou 
          Available from:) identificar conforme o exemplo acima.
 
.. code-block:: xml

    <!-- Report Sample -->

    ...
    <ref-list>
        <ref id="B05">
              <label>5</label>
              <mixed-citation>Referência conforme aparece no artigo</mixed-citation>
              <element-citation publication-type="report">
                  <person-group person-group-type="author">
                      <collab>Nome da instituição organizadora</collab>
                  </person-group>     
                  <source>Título do Relatório</source>
                  <publisher-loc>Lugar de publicação, cidade, estado, país e etc</publisher-loc>
                  <publisher-name>Nome da casa publicadora</publisher-name>
                  <year>ano do relatório</year>
                  <month>mês do relatório</month>
                  <pub-id pub-id-type="other">Report No: XXXXXX</pub-id>
                  <comment>para outras informações mencionadas que fazem parte do relatório que não tenham tags específicas</comment>
              </element-citation>
        </ref>
    </ref-list> 
    ...
 
.. code-block:: xml
 
    <!-- Confproc (proceedings) Sample -->

    ...
    <ref-list>
        <ref id="B06">
            <label>6</label>
            <mixed-citation>Referência conforme aparece no artigo</mixed-citation>
            <element-citation publication-type="confproc">
                <person-group person-group-type="editor">
                    <name>
                        <surname>sobrenome</surname>
                        <given-names>Prenomes</given-names>
                    </name>
                    <name>
                        <surname>sobrenome</surname>
                        <given-names>Prenomes</given-names>
                    </name>
                </person-group>
                <source>título do documento usado referente a uma ou mais palestras do evento</source>
                <conf-name>Nome da conferência</conf-name>
                <conf-date>Data da conferência, pode ser composta por um período por, ex: 2003 Aug 25-29</conf-date>
                <conf-loc>Local físico da conferência (ex: anfiteatro, saguão…) mais nome da cidade, estado, país e etc</conf-loc>
                <publisher-loc>Lugar de publicação do apanhado informacional extraído da conferência</publisher-loc>
                <publisher-name>Nome da casa publicadora/Editora</publisher-name>
                <year>ano da composição do apanhado informacional extraído da conferência</year>
                <size units="page">quantidade total de páginas (se for impresso)</size>
                <comment>Outras informações da conferência que não tenham tags específicas</comment>
            </element-citation>
        </ref>
    </ref-list> 
    ...

.. code-block:: xml

    <!-- Thesis Sample -->
 
    ...
    <ref-list>
      <ref id="B07">
            <label>7</label>
            <mixed-citation>Referência conforme aparece no artigo</mixed-citation>
            <element-citation publication-type="thesis">
                <person-group person-group-type="author">
                    <name>
                        <surname>sobrenome</surname>
                        <given-names>Prenomes</given-names>
                    </name>
                </person-group>
                <source>título do trabalho acadêmico</source>
                <publisher-loc>local da publicação, cidade, estado, país etc</publisher-loc>
                <publisher-name>nome da casa publicadora (normalmente é a própria faculdade/universidade)</publisher-name>
                <year>ano de realização do trabalho</year>
                <size units="page">total de folhas do trabalho</size>
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
            <mixed-citation>Referência conforme aparece no artigo</mixed-citation>
            <element-citation publication-type="patent">
                <person-group person-group-type="author">
                    <name>
                        <surname>sobrenome</surname>
                        <given-names>Prenomes</given-names>
                    </name>
                    <collab>autor institucional</collab>
                </person-group>     
                <article-title>título do documento de patente</article-title>
                <source>identificado o nome do país autorizou a patente. Ex.: United States patent</source>
                <patent country="XX">XX Número da Patente</patent>
                <year>ano do documento da patente</year>
                <month>mês</month>
                <day>dia</day>
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
            <mixed-citation>Referência conforme aparece no artigo</mixed-citation>
            <element-citation publication-type="software">
                <person-group person-group-type="editor">
                    <name>
                        <surname>sobrenome</surname>
                        <given-names>Prenomes</given-names>
                    </name>
                    <name>
                        <surname>sobrenome</surname>
                        <given-names>Prenomes</given-names>
                    </name>
                </person-group>
                <source>título ou nome do software</source>
                <edition>Para software a versão pode ser considerada a edição ex: New version 4.0</edition>
                <publisher-loc>local de publicação/fabricação</publisher-loc>
                <publisher-name>nome da casa publicadora/distribuidora</publisher-name>
                <year>ano de criação do software</year>
                <comment>informações adicionais do software, ex.: informação de suporte: CDs, DVDs, e também especificações de cor, som, dimensões etc</comment>
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
            <mixed-citation>Referência conforme aparece no artigo</mixed-citation>
            <element-citation publication-type="database">
                <source>título da base de dados</source>
                <publisher-loc>local de publicação/país, cidade e/ou estado de origem da base de dados</publisher-loc>
                <publisher-name>nome da casa publicadora/mantenedora</publisher-name>
                <year>ano de criação da base</year>
                <comment>informações adicionais da base de dados</comment>
            </element-citation>
        </ref>
    </ref-list>
    ...
 
.. note:: Deve-se levar em consideração que muitas vezes as referências são
          contruídas de forma incorreta, o que dificulta a marcação de seus
          elementos.


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
  

Atributo Obrigatório 
  ``@pub-id-type``

Ocorre 
  Zero ou mais vezes

Identifica o tipo de identificador (id) de um documento em uma referência.
Deve possuir o atributo ``@pub-id-type`` com os seguintes possíveis valores:

+--------+------------------------------------------------------------------+
| Valor  | Descrição                                                        |
+========+==================================================================+
| pmid   |                                                                  |
+--------+------------------------------------------------------------------+
| pcmid  |                                                                  |
+--------+------------------------------------------------------------------+
| doi    | Número DOI registrado no Crossref                                |
+--------+------------------------------------------------------------------+
| pii    |                                                                  |
+--------+------------------------------------------------------------------+
| other  | qualquer outro identificador                                     |
+--------+------------------------------------------------------------------+

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
 
Atributo Obrigatório 
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
  
Atributo Obrigatório 
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


.. _elemento-app-group:

<app-group>
-----------

Aparece em
  :ref:`elemento-back`

Atributos obrigatório 
 ``@id``
 
Ocorre
 Zero ou uma vez

Utilizado para indicar a presença de um apêndice ao documento. Para a marcação
básica de um apêndice devemos levar em consideração duas tags importantes, a de
grupo de apêndice :ref:`elemento-app-group` e de apêndice propriamente dito
``<app>``. Obrigatoriamente deve ser inserido uma informação de
etiqueta :ref:`elemento-label` em ``<app>``.

Para composição de ``@id`` de **apêndice** utiliza-se o seguinte padrão: "app" + o
número de ordem do apêndice. (Ver :ref:`regra-atribuicao-id`)
 
Exemplo:
  
  app01... app10, app11;
 
Exemplo de Apêndice com texto:
 
.. code-block:: xml
 
    ...
    <app-group>
          <app>
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
        <app>                
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
          <app>
              <label>suplemento eletrônico</label>
              <supplementary-material id="suppl01">
              <media xlink:href="1234-5678-rctb-45-05-0110-m01.avi" mimetype="video" mime-subtype="avi"/>
              </supplementary-material>
          </app>
    </app-group>
    ...
 

.. _elemento-glossary:
 
<glossary>
----------

Aparece em
  :ref:`elemento-back`,
  ``<app>``
 
Ocorre
  Zero ou mais vezes

Utilizada quando há uma lista de termos e suas respectivas definições.
O glossário pode ser apresentado como imagem ou como texto com as identificações
de ``<term>``, ``<def-list>`` e ``<def>``. O 
glossário pode estar identificado em: ``<app>``, :ref:`elemento-back`,
e :ref:`elemento-sec`.
 
Para composição de ``@id`` de glossário utiliza-se o seguinte padrão:

  "d" + o número de ordem do glossário. (Ver :ref:`regra-atribuicao-id`)
 
Exemplo:

  d01... d10, d11;
 
Exemplo em apêndices:
 
.. code-block:: xml

    ... 
    <app-group>
        <app>
            <glossary>
                <title>nome do glossário</title>
                  <def-list id="d01">
                      <def-item>
                          <term> termo </term>
                          <def><p>definição</p></def>
                      </def-item>
                      <def-item>
                          <term>termo</term>
                          <def><p>definição</p></def>
                      </def-item>
                      <def-item>
                          <term>termo</term>
                          <def><p>definição</p></def>
                      </def-item>
                </def-list>
            </glossary>
        </app>
    </app-group>
    ...

Exemplo em back:
 
.. code-block:: xml
 
    ...
    <back>
        <glossary>
            <title>nome do glossário</title>
            <def-list id="d01">
                <def-item>
                    <term> termo </term>
                    <def><p>definição</p></def>
                </def-item>
                <def-item>
                    <term>termo</term>
                    <def><p>definição</p></def>
                </def-item>
                <def-item>
                    <term>termo</term>
                    <def><p>definição</p></def>
                </def-item>
            </def-list>
        </glossary>
        <ref-list>
    </back>
    ...

A tag :ref:`elemento-glossary` possui os seguintes atributos: 
``@content-type``, ``@id``, ``@specific-use`` e ``@xml:lang``. Porém o atributo
mais frequente é o ``@id``.
 
``@id``: identificador da tag. É possível fazer referência cruzada no documento;
esse atributo deve ter valor único no arquivo e é possível fazer link
relacionado a um "rid".

Para composição do ``@id`` de glossários utilizar o seguinte padrão:

  "d" + o número de ordem da figura
 
Exemplo: 
  
  d01... d10, d11;
 
O glossário pode ser apresentado como imagem, utilizando a tag ``<graphic>``,
ou como texto. Veja os exemplos abaixo:
 
Exemplo com imagem:
 
.. code-block:: xml
 
    ...
    <back>
        <glossary>
            <title>nome do glossário</title>
            <graphic xlink:href="1234-5678-rctb-45-05-0110-d01.tif"/>
        </glossary>
        ...
        <ref-list/>
        ...
    </back>
    ...

Exemplo com texto:
 
.. code-block:: xml
 
    ...
    <back>
        <glossary>
            <title>nome do glossário</title>
            <def-list id="d01">
                <def-item>
                    <term> termo </term>
                    <def><p>definição</p></def>
                </def-item>
                <def-item>
                    <term>termo</term>
                    <def><p>definição</p></def>
                </def-item>
                <def-item>
                    <term>termo</term>
                    <def><p>definição</p></def>
                </def-item>
            </def-list>
        </glossary>
        ...
        <ref-list/>
        ...
    </back>
    ...

Exemplo com duas listas de definições:
 
.. code-block:: xml
 
    <!-- Corrigir -->
    <back>
        <glossary>
            <title>nome do glossário</title>
            <glossary>
                <title>nome do glossário</title>
                <def-list id="d01">
                    <def-item>
                        <term> termo </term>
                        <def><p>definição</p></def>
                    </def-item>
                    <def-item>
                        <term>termo</term>
                        <def><p>definição</p></def>
                    </def-item>
                    <def-item>
                        <term>termo</term>
                        <def><p>definição</p></def>
                    </def-item>
                </def-list>
            </glossary>
            <glossary>
                <title>nome do glossário</title>
                <def-list id="d02">
                    <def-item>
                        <term> termo </term>
                        <def><p>definição</p></def>
                    </def-item>
                    <def-item>
                        <term>termo</term>
                        <def><p>definição</p></def>
                    </def-item>
                    <def-item>
                        <term>termo</term>
                        <def><p>definição</p></def>
                    </def-item>
                </def-list>
            </glossary>
        </glossary>
    </back>
 
Referências:
============

* ASSOCIAÇÃO BRASILEIRA DE NORMAS TÉCNICAS. NBR14724: informação e documentação: trabalhos acadêmicos: apresentação. Rio de Janeiro: NBR, 2011.
 
* ASSOCIAÇÃO BRASILEIRA DE NORMAS TÉCNICAS. NBR 6023: informação e documentação: referências: elaboração. Rio de Janeiro: NBR, 2002.
 
* JATS. Journal Article Tag Suite ANSI/NISO Z39.96-2012. Baltimore, USA: National Information Standards Organization, 2012. Disponível em:<http://jats.niso.org>.
 
* JATS. Journal Article Tag Suite. Rockville Pike, USA: National Center for Biotechnology Information, 2013. Disponível em: <http://jats​.nlm.nih.gov>.
 
* JATS. Journal Publishing Tag Library NISO JATS Version 1.0. Rockville, USA: National Center for Biotechnology Information (NCBI), National Library of Medicine (NLM). 2012. Disponível em: <http://jats.nlm.nih.gov/publishing/tag-library/1.0/>.
 
* PubMed Central (NCBI). Sample PubMed Central Citations. Rockville Pike, USA: US National Library of Medicine National Institutes of Health. 2008. Disponível em: <http://www.ncbi.nlm.nih.gov/pmc/pmcdoc/tagging-guidelines/citations/v3/toc.html>.
 
* PubMed Central (NCBI). Elements: index of elements. Rockville Pike, USA: US National Library of Medicine National Institutes of Health. 2009. Disponível em: <https://www.ncbi.nlm.nih.gov/pmc/pmcdoc/tagging-guidelines/article/tags.html>.
