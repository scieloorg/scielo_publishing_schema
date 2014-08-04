encoding
========
Atributo que especifica a codificação de caracteres usada na elaboração do documento. 
Para o SciELO, todos os XMLs devem ser codificados em *utf-8*.
 
Para maiores detalhes leia a especificação do padrão XML 
(`2.8 Prolog and Document Type Declaration <http://www.w3.org/TR/2000/REC-xml-20001006#sec-prolog-dtd>`_).
 
.. code-block:: xml
 
    <?xml version="1.0" encoding="utf-8"?>
 

<!DOCTYPE>
==========
 
A tag de declaração ``<!DOCTYPE>`` serve para indicar a *DTD* (Definição de Tipo de Documento)
a qual o XML é associado, ou seja, as regras estruturais do documento. 
O SciELO Publishing Schema utiliza como base o padrão *JATS 1.0*. 
 
Exemplo versão JATS 1.0:
 
.. code-block:: xml
 
    <!DOCTYPE article PUBLIC "-//NLM//DTD JATS (Z39.96) Journal Publishing DTD v1.0 20120330//EN" "JATS-journalpublishing1.dtd">
 

Exemplo versão PMC 3.0:
 
.. code-block:: xml
 
    <!DOCTYPE article PUBLIC "-//NLM//DTD Journal Publishing DTD v3.0 20080202//EN" "journalpublishing3.dtd">
 

<article>
=========

Aparece em
  1. /
 
Atributos obrigatórios
  1. dtd-version
  2. article-type
  3. xml:lang
 
Ocorre
  Uma vez
 

A tag ``<article>`` representa o elemento raiz do XML, e deve conter obrigatoriamente 
os atributos ``@dtd-version``, ``@article-type`` e ``@xml:lang``. 

Para ``@dtd-version`` utilizar os valores 1.0 ou 3.0, conforme a DTD explicitada em ``<!DOCTYPE>``.
Para ``@article-type`` define-se a tipologia de artigos, os valores que podem ser utilizados são:
 
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
| brief-communication| comunicação breve - compreende breves relatos de         |
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
norma *ISO 639-1*, acesse *http://www.mathguide.de/info/tools/languagecode.html.*
 

Exemplo da tag completa versão 1.0:
 
.. code-block:: xml
 
     <article xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:mml="http://www.w3.org/1998/Math/MathML" dtd-version="1.0" article-type="research-article" xml:lang="en">
 

Exemplo da tag completa versão 3.0:
 
.. code-block:: xml

    <article xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:mml="http://www.w3.org/1998/Math/MathML" dtd-version="3.0" article-type="research-article" xml:lang="en">
 
 
Tags Flutuantes
================
As chamadas tags flutuantes podem aparecer em todo o documento, <front>, <body> e <back>.
 
<xref>
------
Tag de Referência Cruzada usada para relacionar e/ou fazer link com alguma informação no texto. 
 
Os atributos obrigatórios para xref são:
 
- **@rid:** representa "a referência ao id" e é utilizado para fazer a ligação de elementos que possuem @id no arquivo. É imprescindível que haja um "@id" para cada "@rid" e ambos deverão ter o valor idêntico para sua relação.
 
- **@ref-type:**especifica o tipo de referência cruzada. Os valores para este atributo podem ser:
 
     aff: afiliação
     app: apêndice
     author-notes: notas de autor (ou relacionado a autor)
     bibr: referência bibliográfica
     boxed-text: caixa de texto
     contrib: contribuinte
     corresp: autor correspondente
     disp-formula: fórmula
     fig: figura ou grupos de figuras
     fn: nota de rodapé
     kwd: palavra-chave
     list: lista
     other: nenhum dos tipos listados
     sec: seção
     statement: declaração
     supplementary-material: material suplementar
     table: tabela ou grupo de tabelas
     table-fn: nota de rodapé de tabelas
 
**Alguns Exemplos:**
 
.. code-block:: xml
 
    <xref ref-type="aff" rid="aff1">1</xref>
     <aff id="aff01">1</aff>
     
     <xref ref-type="birb" rid="B01">1</xref>
      <ref id="B01">1</ref>

     <xref ref-type="fig" rid="f01">figure 1</xref>
      <fig id="f01">

     <xref ref-type="table" rid="t01">table 1</xref>
      <table-wrap id="t01">

     <xref ref-type="sec" rid="sec01">Seção Metodologia</xref>
      <sec sec-type="methods" id="sec01">

     <xref ref-type="app" rid="app01">Apêndice 1</xref>
      <app id="app01">
     
     <xref ref-type="supplementary-material" rid="suppl01">Material Suplementar A</xref>
     <supplementary-material id="suppl01">
 
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
 8. article/back/app-group/app/table-wrap/table/thead/tr/th
 9. article/back/app-group/app/table-wrap/table/tbody/tr/td
 10. article/back/app-group/app/supplementary-material/table-wrap/table/thead/tr/th
 11. article/back/app-group/app/supplementary-material/table-wrap/table/tbody/tr/td
 
Atributos obrigatórios
 1. rid
 2. ref-type
 
Ocorre
 Zero ou mais vezes
 
<label>
^^^^^^^^
A tag <label> é responsável pela identificação numérica ou alfabética que faz a ligação entre etiquetas.
 
**Alguns Exemplos**
 
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
 
<p>
^^^
 
Esta tag identifica parágrafos. Deve ser inserida no documento sem nenhum tipo de atributo.
 
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
 
Regra de atribuição de @id
==========================
 
Para a composição do @id, combine um prefixo com uma numeração sequencial, como segue:
 
- **Afiliações, prefixo "aff":** aff01, aff02,...aff15.;
- **Apêndice, prefixo "app":** app01, app02,...app15;
- **Correspondência, prefixo "c":** c01, c02,...c15.;
- **Equações, prefixo "e":** e01, e02,...e15;
- **Figuras, prefixo "f":** f01,f02,... f15;
- **Glossário, prefixo "d":** d01, d02,... d15;
- **Notas de rodapé de tabelas, prefixo "TFN":** TFN01, TFN02,..TFN15;
- **Notas de rodapé do artigo, prefixo "fn":** fn01, fn02..fn15;
- **Tabelas, prefixo "t"**: t01, t02. ...t15;
- **Suplemento, prefixo "suppl"**: suppl01, suppl02, … suppl15;
- **Referência bibliográfica , prefixo "B"**: B01, B02,..B15;
- **Media, prefixo "m"**: m01, m02,..m15;
- **Seções, prefixo "sec"**: sec01, sec02,..sec15;
 
Regra de nomeação de imagens
============================
 
Para imagens (que podem ser figuras, equações, apêndices e etc) utilizar a seguinte estrutura de nomeação tanto nas imagens dentro do XML quanto para as imagens da pasta do pacote do fascículo ou lote de ahead-of-print.
 
Para fascículo:
 
ISSN-acrônimo-volume-número-paginação-nomedaimagem.extensãodaimagem
 
Sendo:
 
**ISSN:** Se houver mais que um dar preferência ao impresso.
**Acrônimo:** Sigla do periódico na SciELO
**Volume:** Volume do fascículo
**Número:** número e/ou suplemento do fascículo (tratar como “n” e “s”)
**Paginação:** Manter a informação da primeira página contendo no mínimo 4 dígitos
**Nome da imagem:** prefixo com uma numeração sequencial (ver “Regra de atribuição de @id”)
 
**Exemplo:**
 
1807-5932-clin-69-05-0308-gf01.tif
 
.. note:: Cada item deve ser separado por um hifén e obrigatoriamente deve-se manter visível a extensão da imagem após o “ponto”, optando preferencialmente por imagens em formato .tif.
 
Para ahead-of-print
 
ISSN-acrônimo-númerodedoisemoprefixo.extensãodaimagem
 
**Exemplo:**
 
0074-0276-mioc-00740276130057-gf01.tif
 
.. note:: Esse número de ordem deve ser sequencial.
 
<front>
=======
No Front devem estar apresentados os seguintes dados:
Metadados do periódico, título, autoria, afiliação, resumo, palavras-chave, DOI, volume, número, suplemento, paginação, indicação da licença Creative Commons, data de publicação, seção de cabeçalho, histórico de datas, dados de correspondência, notas de autor, informações de resenhas de livros.
 
Aparece em
 1. article
 
Ocorre
 Uma vez
 
<journal-meta>
--------------
Em <journal-meta> faz-se a identificação dos metadados do periódico.
 
..note:: Confira a novidade criada pela equipe de TI SciELO, consulte link para preencher corretamente os metadados da revista em: http://static.scielo.org/sps/titles-tab-utf-8.csv

Aparece em
 1. article/front
 
Ocorre
 Uma vez
 
<journal-id>
^^^^^^^^^^^^
Especifica o título padronizado do periódico.
 
Aparece em
 1. article/front/journal-meta
 
Atributos obrigatórios
 1. journal-id-type='nlm-ta' ou journal-id-type='publisher-id'
 
Ocorre
 Uma vez
 
Para o uso do título do periódico no Pubmed, utiliza-se o valor "nlm-ta":
 
.. code-block:: xml
 
 <journal-id journal-id-type="nlm-ta">
   Mem Inst Oswaldo Cruz
 </journal-id>
 
 ..note:: Para verificar se o periódico está indexado no Medline consulte o link:http://www.ncbi.nlm.nih.gov/pubmed/advanced


Para o uso do acrônimo do periódico no SciELO, utiliza-se o valor "publisher-id":
 
.. code-block:: xml
 
 <journal-id journal-id-type="publisher-id">
   mioc
 </journal-id>
 
<journal-title-group>
^^^^^^^^^^^^^^^^^^^^^
 
Esta tag irá abranger tags que representam os metadados identificadores da revista.
 
.. code-block:: xml
 
 <journal-title-group>
   <journal-title>Brazilian Journal of Otorhinolaryngology</journal-title>
   <abbrev-journal-title abbrev-type="publisher">Braz J Otorhinolaryngol.
</abbrev-journal-title>
 </journal-title-group>
 
Aparece em
 1. article/front/journal-meta
 
Ocorre
 Uma vez
 
<journal-title>
^^^^^^^^^^^^^^^
Neste item é incluído o título longo do periódico de acordo com seu registro no ISSN. Pode-se consultar a forma adotada no site da coleção, na homepage do periódico.
 
Aparece em
 1. article/front/journal-meta/journal-title-group
 
Ocorre
 Uma vez
 
.. code-block:: xml
 
 <journal-title-group>
   <journal-title>Brazilian Journal of Medical and Biological Research</journal-title>
 </journal-title-group>
 
<abbrev-journal-title>
^^^^^^^^^^^^^^^^^^^^^
 
Nesta tag é incluída a forma abreviada do título do periódico de acordo com seu registro no ISSN. Pode-se consultar a forma adotada no site da coleção, na homepage do periódico. É obrigatório o uso do atributo **@abbrev-type** do tipo “publisher” conforme exemplo a seguir:
 
.. code-block:: xml
 
<journal-title-group>  
  <abbrev-journal-title abbrev-type="publisher">Braz. J. Med. Biol. Res.</abbrev-journal-title>
</journal-title-group>
 
Aparece em
 1. article/front/journal-meta/journal-title-group
 
Atributo obrigatório
 1. abbrev-type="publisher"
 
Ocorre
 Uma vez
 
<issn>
^^^^^^
O ISSN é um código numérico, único, que identifica uma publicação seriada a qual é definida pela norma ISO 3297:2007. Normalmente cada tipo de suporte utilizado pelo periódico possui um número específico. Pode-se consultar a forma adotada no site da coleção, na homepage do periódico. É possível também encontrar esta informação em <back> dentro de <element-citation> nas referências, mas não se faz o uso de nenhum atributo neste caso.
 
Aparece em
 1. article/front/journal-meta
 2. article/back/ref-list/ref/element-citation
 
Atributos obrigatórios em <front>
 1. pub-type='ppub'ou pub-type='epub'
 
Ocorre
 Uma ou mais vezes
 
*@pub-type="ppub"* para a versão impressa
.. code-block:: xml
 
 <issn pub-type="ppub">1808-8694</issn>
 
*@pub-type="epub"* para a versão digital
 
.. code-block:: xml
 
 <issn pub-type="epub">1808-8686</issn>
 
Ou ambos, *@pub-type="epub"* + *@pub-type="epub"*
 
.. code-block:: xml
 
 <issn pub-type="epub">1808-8686</issn>
 <issn pub-type="ppub">1808-8694</issn>
 
<publisher>
^^^^^^^^^^^
O nome da instituição responsável pela publicação do periódico deve ser especificado de acordo com o registro no SciELO. Pode-se consultar a forma adotada no site da coleção, na homepage do periódico.
 
Aparece em
 1. article/front/journal-meta
 
Ocorre
 Uma vez
 
.. code-block:: xml
 
 <publisher>
   <publisher-name>Instituto Oswaldo Cruz, Ministério da Saúde</publisher-name>
 </publisher>
 
     
<article-meta>
--------------
Contém os metadados do artigo. Seus elementos básicos são DOI, seção (de acordo com o sumário do periódico), título(s) do artigo, autor (es) e suas respectivas afiliações e notas, data de publicação, volume, número e paginação do artigo, resumo(s), palavras-chave, histórico, permissão de uso (licença)e contagem de elementos.

Aparece em
 1. article/front
 
Ocorre
 Uma vez
 
<article-id>
^^^^^^^^^^^^
Cada artigo deve ter um identificador único. O SciELO utiliza o padrão Digital Object Identifier (DOI), norma ISO 26324. O DOI é fornecido pela DOI Foundation. O atributo @pub-id-type='doi' é obrigatório nesta tag.
 
Aparece em
 1. article/front/article-meta
 
Atributos obrigatórios
 1. pub-id-type='doi'
 
Ocorre
 Uma ou mais vezes
 
.. code-block:: xml
 
 <article-id pub-id-type="doi">10.1590/0074-0276130047</article-id>
     
 
<article-categories>
--------------------
Em <article-categories> classifica-se o artigo de acordo com a seção que aparece no sumário do periódico. Esta classificação pode ser temática ou por tipologia do documento.
 
Aparece em
 1. article/front/article-meta
 
Ocorre
 Uma vez
 
<subj-group>
^^^^^^^^^^^^
 
Designa a seção do documento e serve para organizar documentos em grupo por assunto. É obrigatório o uso de atributo @subj-group-type na tag <subj-group> do tipo "heading" (cabeçalho). Em <subject> atribui-se a seção em que o artigo foi classificado (consultar o sumário para melhor identificação) e para ahead-of-print deve ser adotado sempre a seção “Articles”.
 
Aparece em
 1. article/front/article-meta/article-categories
 
Atributos obrigatórios
 1. subj-group-type="heading"
 
Ocorre
 Uma vez
 
**Exemplo:**
 
*Para seção temática:*
 
.. code-block:: xml
 
 <article-categories>
   <subj-group subj-group-type="heading">
     <subject>Biotechnology</subject>
   </subj-group>
 </article-categories>
 
*Para seção por tipo de documento:*
 
.. code-block:: xml
 
 <article-categories>
   <subj-group subj-group-type="heading">
     <subject>Original Article</subject>
   </subj-group>
 </article-categories>
 
*Para ahead-of-print:*
 
.. code-block:: xml
 
 <article-categories>
   <subj-group subj-group-type="heading">
     <subject>Articles</subject>
   </subj-group>
 </article-categories>
 
<title-group>
-------------
Esta tag é utilizada para especificar o título ou um conjunto de títulos de um artigo. Nele são identificados <article-title>, e <trans-title-group>.
 
Aparece em
 1. article/front/article-meta
 
Ocorre
 Uma vez
 
<article-title>
^^^^^^^^^^^^^^^
Esta tag pode ser utilizada para especificar o título do artigo em si em <article-meta>, ou para especificar um título de documento nas referências em <element-citation>. Em ambos os casos, o atributo @xml:lang não deve ser utilizado.
 
Aparece em
 1. article/front/article-meta/title-group
 2. article/back/ref-list/ref/element-citation
 
Ocorre
 Uma vez
 
.. code-block:: xml
 
 <title-group>
   <article-title>The teaching of temporomandibular disorders and  orofacial pain at undergraduate level in Brazilian dental schools
</article-title>
 </title-group>

.. note:: Se o título do artigo ou da referência possuir um subtítulo ele deve ser marcado junto a tag de <article-title>, não se deve marcar nenhum texto separadamente em outras tags (a mesma regra se aplica a <trans-title>).
 
**Exemplo:**
 
.. code-block:: xml
 
     <title-group>
          <article-title>Correlação entre sintomas e tempo de evolução do câncer do trato aerodigestivo superior com o estádio inicial e avançado <xref ref-type="fn" rid="fn01">*</xref> </article-title>
     </title-group>.
 
<trans-title-group>
^^^^^^^^^^^^^^^^^^^
Esta tag é utilizada para apresentar o título traduzido ou um conjunto de títulos traduzidos do artigo. O uso do atributo @xml:lang é obrigatório e deve ser utilizado para especificar o idioma traduzido do título.

Aparece em
 1.article/front/article-meta/title-group
 
Atributos obrigatórios
 1. xml:lang
 
Ocorre
 zero ou mais vezes

<trans-title>
^^^^^^^^^^^^^

Marca o título traduzido, dentro da tag <trans-title-group>.

**Exemplo:**
 
.. code-block:: xml
 
<title-group>
          <article-title>Between spiritual wellbeing and spiritual distress: possible related factors in elderly patients with cancer</article-title>
          <trans-title-group xml:lang="pt">
                <trans-title>Entre o bem-estar espiritual e a angústia espiritual: possíveis fatores relacionados a idosos com cancro</trans-title>
          </trans-title-group>
          <trans-title-group xml:lang="es">
                <trans-title>Entre el bienestar espiritual y el sufrimiento espiritual: posibles factores relacionados en ancianos con câncer</trans-title>
          </trans-title-group>
     </title-group>
 
          
Aparece em
 1.article/front/article-meta/title-group/trans-title-group
 
Ocorre (quando houver <trans-title-group>)
 Uma ou mais vezes
 
<contrib-group>
----------------
Representa o grupo dos que contribuiram para a elaboração do artigo. Os tipos de contribuintes mais frequentes são de autores pessoais, instituições e grupos de pesquisa. A tag pode ou não envolver a informação de afiliação, sendo obrigatória na identificação do contribuidor do tipo autores (author) sejam institucionais ou não. Os principais elementos de <contrib-group> são: <contrib>, <xref>, <collab>, <aff> e <role>.
 
Aparece em
 1.article/front/article-meta
 
Ocorre
 uma vez
 
<contrib>
^^^^^^^^^
Em <contrib> especifica-se o indivíduo ou instituição que contribuiu para o artigo. Pode ser anônimo ou ter um ou vários autores, inclusive autores institucionais. Tags como <name>, <collab>, <on-behalf-of>, <xref>, <role> e <anonymous> podem ser encontradas neste elemento. Um atributo deve ser inserido nesta tag:
 
- **@contrib-type:** Pode possuir os seguintes valores,
- author: autor(es) do conteúdo
- compiler: Compilador(es), pessoa(s) que montou um trabalho composto de várias fontes.
     - editor: Editor(es) do conteúdo.
     - translator: Tradutor(es) do conteúdo
 
.. code-block:: xml
 
     <contrib contrib-type="author">
 
**Exemplo:**
 
.. code-block:: xml
 
     <contrib-group>
          <contrib contrib-type="author">
                <name>
                     <surname>Último Sobrenome</surname>
                     <given-names>Prenomes</given-names>
                     <prefix>Qualificadores que antecendem o nome como Prof, Dr.,Marechal, dentre outros</prefix>
                     <suffix>Partículas do nome como Filho, Junior, Neto</suffix>
                </name>
                     <xref ref-type="aff" rid="aff01">Identificador da afiliação</xref>
     </contrib>
 
.. note:: Observar normas para entrada de nomes (AACR2 - Código de Catalogação Anglo Americano e/ou Currículo Lattes dos autores, avaliar formas de entrada autorizadas).
 
Aparece em
 1.article/front/article-meta/contrib-group
 
Atributos obrigatórios
 1. contrib-type
 
Ocorre
 Uma ou mais vezes
 
<collab>
^^^^^^^^
Utilizado para especificar um grupo de colaboradores (autores, editores, pesquisadores, instituição, laboratório etc que atuaram como colaboradores do trabalho). Pode ser identificada em <contrib>, <element-citation>, <person-group>, <product>.
 
Aparece em
 1. article/front/article-meta/contrib-group/contrib
 2. article/front/article-meta/product/person-group
 2. article/back/ref-list/ref/element-citation
 
Ocorre
 Zero ou mais vezes
 
<on-behalf-of>
^^^^^^^^^^^^^^
Utiliza-se quando um autor age como representante de um grupo ou organização. Ou seja, quando o autor diz ter escrito ou editado um trabalho em nome de uma organização. Essa tag pode ser encontrada em: <collab>, <contrib> e <contrib-group>.
 
.. code-block:: xml
 
     </name>
          <on-behalf-of>Identificação de um grupo ou organização</on-behalf-of>
     </contrib>
 
ou
.. code-block:: xml
 
     </contrib>
          <on-behalf-of>Identificação de um grupo ou organização</on-behalf-of>
     </contrib-group>
 
Aparece em
 1. article/front/article-meta/contrib-group
 2. article/front/article-meta/contrib-group/contrib
 
Ocorre
 Zero ou mais vezes
 
<role>
^^^^^^
A tag "role" (função ou papel) é usada para especificar o cargo (ou função) do contribuinte do documento. Essa tag pode ser encontrada nos seguintes elementos: <collab>, <contrib>, <contrib-group>, <element-citation>, <person-group>, <product>.
 
**Exemplos:**
 
*Em contrib:*
 
.. code-block:: xml
 
     <contrib contrib-type="author">
     <name>
     <surname>Meader</surname>
     <given-names>CR</given-names>
     <prefix>Dr.</prefix>
     <suffix>Junior</suffix>
 </name>
     <xref ref-type="aff" rid="aff02">2</xref>
     <role>Pesquisador</role>
 </contrib>
 
*Em referências:*
 
.. code-block:: xml
 
     <element-citation publication-type="journal">
     <person-group person-group-type="author">
          <name>
                <surname>Petitti</surname>
                <given-names>DB</given-names>
         </name>
          <name>
               <surname>Crooks</surname>
               <given-names>VC</given-names>
         </name>
         <role>pesquisador</role>
     </person-group>

      
Aparece em
 1. article/front/article-meta/contrib-group/contrib
 2. article/front/article-meta/product/person-group
 3. article/back/ref-list/ref/element-citation/person-group
 
Ocorre
 Zero ou mais vezes
 
<name>
^^^^^^
A tag <name> é utilizada para especificar o nome pessoal do contribuinte autoral e pode ser encontrada em:
<contrib>, <element-citation>, <person-group>, <product>.
 
As tags possíveis em <name> são:
 
     - <surname>;
     - <given-names>;
     - <prefix>;
     - <suffix>.
 
..note:: As tags possíveis dentro de <name> devem seguir obrigatoriamente a sequência de aparecimento citada acima.
 
Aparece em
 1. article/front/article-meta/contrib-group/contrib
 2. article/front/article-meta/product/person-group
 3. article/back/ref-list/ref/element-citation/person-group
 
 
Ocorre
 Zero ou mais vezes
 
<surname>
^^^^^^^^^^
É utilizada para especificar sobrenome de autores. Aqui deve ser especificado o último nome do autor. Deve-se observar as regras para identificação de sobrenome de acordo com a norma adotada pelo periódico. A recomendação do SciELO é utilizar a AACR2 Código de Catalogação Anglo Americano e/ou Currículo Lattes dos autores).
 
.. code-block:: xml
 
     <surname>Almeida</surname>
     <given-names>Antônio Golçalves de</given-names>
 
Aparece em
 1.article/front/article-meta/contrib-group/contrib
 2. article/back/ref-list/ref/element-citation/person-group
 3. article/front/article-meta/product/person-group
 
Ocorre (Quando houver <name>)
 Uma ou mais vezes
 
<given-names>
^^^^^^^^^^^^^
Identifica o prenome do autor, ou seja, o primeiro nome e também o nome(s) do(s) meio(s).
 
.. code-block:: xml
 
 <surname>Santos</surname>
     <given-names>Ana Maria da Silva</given-names>
 
Aparece em
 1. article/front/article-meta/contrib-group/contrib
 2. article/back/ref-list/ref/element-citation/person-group
 3. article/front/article-meta/product/person-group
 
Ocorre
 Zero ou mais vezes
 
<prefix>
^^^^^^^^
Especifica o qualificador que precede o prenome do autor. Geralmente é utilizado quando há qualificadores como "Prof. Dr., "Dr.","Sr","Presidente", "Embaixador" dentre outros.
 
<contrib contrib-type="author">
     <name>
     <surname>Oliveira</surname>
     <given-names>Marcos de</given-names>
     <prefix>Prof.</prefix>
     </name>
 
Aparece em
 1.article/front/article-meta/contrib-group/contrib
 2. article/back/ref-list/ref/element-citation/person-group
 3. article/front/article-meta/product/person-group
 
Ocorre
 Zero ou mais vezes
 
<suffix>
^^^^^^^^
Especifica sufixos do nome como as partículas "Neto", "Júnior", "Jr.", "Filho", "Sobrinho" etc.
 
.. code-block:: xml
 
     <contrib contrib-type="author">
     <name>
     <surname>Santos</surname>
     <given-names>João da Silva</given-names>
     <suffix>Neto</suffix>
     </name>
 
.. note:: para as tags que compõem <name> há uma ordem pré-estabelecida obrigatória:
 
.. code-block:: xml
 
     <name>
          <surname></surname>
          <given-names></given-names>
          <prefix></prefix>
          <suffix></suffix>
     </name>
 
Aparece em
 1. article/front/article-meta/contrib-group/contrib
 2. article/front/article-meta/product/person-group
 3. article/back/ref-list/ref/element-citation/person-group
 
 
Ocorre
 Zero ou mais vezes
 
<aff>
-----
Considera-se como afiliação o vínculo institucional do(s) contribuinte(s) do artigo. Os dados de afiliação são importantes para localizar e mensurar a produção científica por país, estado, cidade, bem como por instituição e seus departamentos. Recomenda-se que os nomes das instituições das afiliações sejam especificadas em sua forma original, sem tradução ou abreviações de seus nomes. Ou seja, por exemplo, identificar preferencialmente **Universidade de São Paulo** a USP, ou University of São Paulo, ou Saint Paul University, entre outras possíveis formas. Por isso, quando ocorre no documento de existir mais de uma forma, usar a original.
 
Pode possuir o atributo @id. Para composição de @id de **afiliação** utiliza-se o seguinte padrão: "aff" + o número de ordem da afiliação. (Ver Regra de atribuição de @id)
 
**Exemplo:** aff01... aff10, aff11;
 
**Exemplo completo de uma afiliação:**
 
.. code-block:: xml
 
     <aff id="aff01">
     <label>1</label>
     <institution content-type="orgname">Fundação Oswaldo Cruz</institution> 
<institution content-type="orgdiv1">Escola Nacional de Saúde Pública Sérgio Arouca</institution>
<institution content-type="orgdiv2">Centro de Estudos da Saúde do Trabalhador e Ecologia Humana</institution>   
     <addr-line>
     <named-content content-type="city">Manguinhos</named-content>
     <named-content content-type="state">RJ</named-content>
     </addr-line>
     <country>Brasil</country>
     <institution content-type="original">Prof. da Fundação Oswaldo Cruz; da Escola Nacional de Saúde Pública Sérgio Arouca, do Centro de Estudos da Saúde do Trabalhador e Ecologia Humana. RJ - Manguinhos / Brasil. <named-content        content-type="email">maurosilva@fiocruz.com</named-content></institution>
     </aff>

Aparece em
 1.article/front/article-meta
 
Ocorre
 Zero ou mais vezes
 
<institution>
^^^^^^^^^^^^^
Nesta tag especifica-se a instituição do autor, a qual pode ser dividida em até três níveis. Estes níveis serão definidos pelo atributo obrigatório @content-type, podendo possuir os seguintes valores:
 
- “orgname”: Representando a instituição de nível hierárquico maior mencionado na afiliação;
- “orgdiv1”: Representando a primeira divisão da instituição mencionada em orgname;
- “orgdiv2”: Representando a segunda divisão da instituição mencionada em orgname.
 
.. note:: No caso de mais divisões mencionadas em afiliações no PDF, identifica-las somente na tag <institution content-type="original">.
 
.. code-block:: xml
 
<institution content-type="orgname">Universidade de São Paulo</institution>
<institution content-type="orgdiv1">Faculdade de Filosofia, Letras e Ciências Humanas</institution>
<institution content-type="orgdiv2">Departamento de Vernáculos</institution>
 
Deve-se especificar a afiliação completa como aparece no documento original. Caso o email esteja presente também deve ser marcado; ambas as tags possuem atributo obrigatório @content-type dos tipos: original e/ou email, conforme segue no exemplo:
 
.. code-block:: xml
 
     <institution content-type="original">Técnica de Cardiopneumologia. Unidade de Fisiopatologia Respiratória, Serviço de Pneumologia, Centro Hospitalar Lisboa Norte, Lisboa, Portugal. <named-content content-type="email">mara@scielo.org</named-content></institution>

Aparece em
 1. article/front/article-meta/aff
 
Atributos obrigatórios
 1. content-type
 
Ocorre
 zero ou mais vezes
 
     
<addr-line>
^^^^^^^^^^^
Em <addr-line>, especifica-se os dados de endereço da instituição vinculada ao autor, e deve aparecer quando a informação for descrita no artigo dentro de <aff>. Pode conter somente informações de Estado e cidade.
 
 
Aparece em
 1. article/front/journal-meta/aff
 
Ocorre
 Zero ou mais vezes
 
<named-content>
^^^^^^^^^^^^^^^
 
Esta tag representa as informações de endereço que aparecem em afiliação e portanto irá dentro da tag de <addr-line> e obrigatoriamente terá o atributo @content-type cujos valores podem ser "city" ou "state", conforme exemplo a seguir:
 
.. code-block:: xml
 
     <addr-line>
     <named-content content-type="city">São José do Rio Preto</named-content>
     <named-content content-type="state">São Paulo</named-content>
     </addr-line>
 

Aparece em
 1. article/front/journal-meta/aff/addr-line
 
Atributos obrigatórios
 1. content-type
 
Ocorre
 Zero ou mais vezes


<country>
^^^^^^^^^

Identifica o país de uma afiliação e representa a única informação que deverá ser especificada fora da tag <addr-line>. 
 
A tag pode possuir o atributo @country e nele deve ser atribuído o código do país de acordo com a Norma ISO 3166, com dois caracteres alfabéticos.
Para consultar ao código do país consulte o link da norma ISO: https://www.iso.org/obp/ui/#iso:pub:PUB500001:en
**Exemplo:**

.. code-block:: xml
 
</addr-line>
     <country>Brasil</country>


**Exemplo com atributo:**

.. code-block:: xml

</addr-line>
     <country country="BR">Brasil</country>

..note:: Para a nova versão do SPS este atributo passará a ser obrigatório.

Aparece em
 1. article/front/journal-meta/aff
 
Ocorre
 Uma vez

 

 
<author-notes>
--------------       
A tag de notas de autor é um elemento de <front> e deve ser utilizada para identificar informações como correspondência, contribuição igualitária, conflitos de interesses, ou seja, notas sobre autor.
 
.. code-block:: xml
 
     <author-notes>
          <corresp id="c01">
                <bold>Correspondence:</bold> Maria Silva, Avenida Senador Felinto Muller,s/n - Cidade Universitária, 79070-192 Campo Grande - MS Brasil,<email>maria.ra@hotmail.com</email>
          </corresp>
          <fn fn-type="conflict">
                <p>Conflict of interest: none</p>
          </fn>     
     </author-notes>
 
Aparece em
 1. article/front/article-meta
 
Ocorre
 Zero ou mais vezes
 
<fn>
----
Foot Notes ou notas de rodapé de autores, são notas inseridas em <front> dentro de <author-notes> obrigatoriamente devem ter o atributo @fn-type que podem possuir os seguintes valores:
 
- **author** Outro tipo de nota relacionado a autor
- **con** Informação de contribuição
- **conflict** Declaração de conflito de Interesse
- **corresp** Informação de correspondência
- **current-aff** Afiliação atual do autor
- **deceased** Pessoa morreu desde que o artigo foi escrito
- **edited-by** Autor é o editor
- **equal** Informação de contribuição igualitária
- **on-leave** Autor está ausente (sabático ou outro)
- **participating-researchers** Autor foi um pesquisador para o artigo
- **present-address** Endereço atual do autor
- **previously-at** Afiliação anterior do autor
- **study-group-members** Autor foi um membro do grupo de estudos para a pesquisa
- **other:** especifica aquelas notas diferentes das relacionados acima. É possível também ter este tipo de nota em <fn-group> em <back>.
 
.. code-block:: xml
 
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
 
Aparece em
 1. article/front/article-meta/author-notes
 
Atributos obrigatórios
 1. fn-type
 
Ocorre
 Zero ou mais vezes
 
<corresp>
---------
 
Esta tag representa as informações de correspondência de um dos autores do artigo. Pode ou não possuir um <label> e também o atributo @id. É possível marcar o <email> caso inserido.
 
Para composição de @id de **correspondência** utiliza-se o seguinte padrão: "c" + o número de ordem da correspondência. (Ver Regra de atribuição de @id)
 
**Exemplo:** c01... c10, c11;


.. code-block:: xml
 
<author-notes>
          <corresp>
Dr. Edmundo Figueira Departamento de Fisioterapia, Universidade FISP - São Paulo, Brasil. E-mail: <email>contato@contato.com</email>
          </corresp>
</author-notes>
 
.. note:: Esta tag não necessita da inserção de parágrafo <p>.
 
Aparece em
 1. article/front/article-meta/author-notes
 
Ocorre
 Zero ou mais vezes
 
<pub-date>
----------
Para a marcação da data de publicação do artigo/fascículo utiliza-se a tag <pub-date> a qual pode conter os elementos <day>, <month>, <season> e obrigatoriamente <year>. Esta tag deve estar acompanhada do atributo @pub-type.
 
A data de publicação pode ser do tipo "epub-ppub" se houver uma versão impressa do fascículo, apenas "epub" para publicação digital ou em ahead-of-print.
 
**Exemplo de marcação de data de publicação nas versões impressa e digital:**
 
.. code-block:: xml
 
     <pub-date pub-type="epub-ppub">
           <day>17</day>
           <month>03</month>
           <year>2014</year>
     </pub-date>
 
Os valores de dia, mês e ano devem ser representados segundo o PDF do artigo/fascículo.
 
**Exemplo de marcação de data de publicação na versão digital:**
 
.. code-block:: xml
 
     <pub-date pub-type="epub">
          <season>Jan-Feb</season>
          <year>2014</year>
          </pub-date>

Aparece em
 1. article/front/article-meta
 
Atributos obrigatórios
 1. pub-type='epub' ou pub-type='epub-ppub'
 
Ocorre
 Uma vez
 
<season>
^^^^^^^^

Esta tag pode ser encontrada em <front> (ver <pub-date> e <product>) e em <back> representando informações das estações do ano em um referência.

**Exemplo em <back>:**

  ..code block::

      <season>Outono</season>

**Exemplo em <front>:**

      <season>Nov-Dec</season>
          

..note:: Para abreviatura dos meses que devem ser inseridos na data de publicação dos fascículos, utilizar siglas em inglês com 3 caracteres, separados por hífen.

Lista de Abreviatura de Meses para inserção:

Jan
Feb
Mar
Apr
Jun
Jul
Aug
Sep
Oct
Nov
Dec

Aparece em
  1. article/front/article-meta/pub-date
  2. article/front/article-meta/product
  3. article/back/ref-list/ref/element-citation  

Ocorre 
 Zero ou uma vez 

<year>
^^^^^^

Identifica ano em referências, pode representar o ano de publicação de um documento, o ano de fabriação de um software, o ano da criação de uma base de dados e assim por diante. Também utilizada em <front> para identificar ano da publicação de um artigo (ver tag <pub-date>) ou de um produto (ver tag <product>).

**Exemplo:**

  ..code block::

  <year>2014</year>

Aparece em
  1. article/front/article-meta/pub-date
  2. article/front/article-meta/product
  3. article/back/ref-list/ref/element-citation  

Ocorre 
 Uma vez <front>

Ocorre 
 Zero ou mais vezes em <back>

<month>
^^^^^^^

Identifica o mês em referências, pode representar o mês de publicação de um periódico científico, o mês da realização de um relatório e assim por diante. Também utilizada em <front> para identificar mês da publicação de um artigo (ver tag <pub-date>)ou de um produto (ver tag <product>).

**Exemplo:**

  ..code block::

    <month>Mar</month>

Aparece em
  1. article/front/article-meta/pub-date
  2. article/front/article-meta/product
  3. article/back/ref-list/ref/element-citation

Ocorre 
 Zero ou uma vez <front>

Ocorre 
 Zero ou mais vezes em <back>

<day>
^^^^^

Identifica o dia em referências, pode representar o dia de publicação de um periódico científico, o dia da realização de um relatório e assim por diante. Também utilizada em <front> para identificar mês da publicação de um artigo (ver tag <pub-date>) ou de um produto (ver tag <product>).

**Exemplo:**

  ..code block::

    <day>26</day>

Aparece em
  1. article/front/article-meta/pub-date
  2. article/front/article-meta/product
  3. article/back/ref-list/ref/element-citation

Ocorre 
 Zero ou uma vez <front>

Ocorre 
 Zero ou mais vezes em <back>

<volume>
--------
Representa o volume de uma publicação. A tag que pode ser apresentada em <front> e <element-citation>.
 
.. code-block:: xml
 
     <volume>10</volume>
     <issue>03</issue>
 
Caso haja suplemento de volume em <front>, exemplo: v10s1:
 
.. code-block:: xml
 
     <volume>10</volume>
     <issue>suppl 1</issue>
 
Aparece em
 1. article/front/article-meta
 2. article/back/ref-list/ref/element-citation
 
Ocorre
 Uma vez em front
 
Ocorre
 zero ou mais vezes em back
 
<issue>
-------
 
Tag que representa número de uma publicação e pode ser apresentada em <front> e <element-citation>.
 
.. code-block:: xml
 
     <volume>10</volume>
     <issue>05</issue>
 
Em caso de suplemento de número em <front>, exemplo: v10n5s1:
 
.. code-block:: xml
 
     <volume>10</volume>
     <issue>5 suppl 1</issue>  
 
..note:: Para informações de suplemento em <front> não se deve utilizar a tag <supplement>. Seguir os exemplos mencionados.
 
Em caso de ahead-of-print, especificar valores zerados, como segue:
 
.. code-block:: xml
 
     <volume>00</volume>
     <issue>00</issue>  
 
Aparece em
 1. article/front/article-meta
 2. article/back/ref-list/ref/element-citation
 
Ocorre
 Uma vez em front
 
Ocorre
 Zero ou mais vezes em back
 
<fpage>
-------
Designa-se a paginação inicial do artigo. No caso de ahead-of-print, a informação deve ser preenchida com 00.
 
.. code-block:: xml
 
     <fpage>17</fpage>
     <lpage>21</lpage>
 
Aparece em
 1. article/front/article-meta
 2. article/back/ref-list/ref/element-citation
 
Ocorre
 Uma vez em front
 
Ocorre
 Zero ou mais vezes em back
 
<lpage>
-------
 
Designa-se a paginação final do artigo. No caso de ahead-of-print, a informação deve ser preenchida com 00.
 
.. code-block:: xml
 
     <fpage>396</fpage>
     <lpage>452</lpage>
 
Aparece em
 1. article/front/article-meta
 2. article/back/ref-list/ref/element-citation
 
Ocorre
 Uma vez em front
 
Ocorre
 Zero ou mais vezes em back
 
<elocation-id>
--------------
Está tag irá identificar uma paginação eletrônica, pode ser encontrada também em <element-citation>. Ela só deverá ser usada quando só houver um único número de paginação eletrônica, caso haja o intervalo de páginas deve-se optar pelo uso de <fpage> e <lpage>.
 
.. code-block:: xml
 
<volume>00</volume>
     <issue>00</issue>
     <elocation-id>0102961</elocation-id>
 
Aparece em
 1. article/front/article-meta
 2. article/back/ref-list/ref/element-citation
 
Ocorre
 Uma vez em front (senão houver informações de <fpage> e <lpage>)
 
Ocorre
 Zero ou mais vezes em back

<product>
---------
Em <product> devem ser inseridas as informações do produto resenhado. É importante salientar que está tag só deverá ser utilizada quando o tipo de <article> for @article-type="book-review" ou @article-type="product-review". Para o atributo @product-type, os valores possíveis são: “book”, “software”, “article”, “issue”, “website”, “film” e “hardware”.
 
 .. code-block:: xml
 
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
<isbn>9788497842525</isbn>                          <inline-graphic>1234-5678-rctb-45-05-690-gf01.tif</inline-graphic>
</product>
<history>
 
.. note:: A ordem das tags é importante! A tag <product> deve estar inserida em front antes de <history> ou depois de </fpage>.
               
Aparece em
 1. article/front/article-meta
 
Atributos obrigatórios  
 1. product-type
 2. person-group-type (na tag <person-group>)
 
Ocorre
 Zero ou mais vezes

<person-group>
^^^^^^^^^^^^^^ 
Identifica o grupo ou o indivíduo criador/elaborador de um determinado documento. Obrigatoriamente as tags de <collab>, <role>, <name> e <etal/> se existentes devem constar dentro da tag. É necessário inserir o atributo @person-group-type que pode possuir os seguintes valores:

- author
- compiler
- director
- editor
- inventor
- translator 

**Exemplo:**
 
.. code-block:: xml

      <person-group person-group-type="author">
<name>
                 <surname>Silva</surname>
                 <given-names>Jaqueline Figueiredo da</given-names>
            </name>
         <collab>Instituto Brasil Leitor</collab>
       </person-group>

Aparece em
  1. article/front/article-meta/product
  2. article/back/ref-list/ref/element-citation
  

Atributo Obrigatório 
 1. person-group-type

Ocorre 
 Zero ou mais vezes

<etal>
^^^^^^
Esta deve deve constar dentro da <person-group> e é usada quando existirem mais de três autores, onde indica-se apenas o primeiro, acrescentando-se a expressão et al. que significa "entre outros". Esta informação aparece primordialmente em referências. 

..note:: Quando a informação aparecer no texto da referência, não é necessário envolver o texto “et al.” com a tag <etal></etal>, basta inserir a tag desta forma <etal/>.

**Exemplo: Quincas Borba, et al.**

  ..code block::

<person-group>
<name>
<surname>Borba</surname>
<given-names>Quincas</given-names>
</name>
<etal/>
</person-group>


Aparece em
 1. article/front/article-meta/product/person-group
 2. article/back/ref-list/ref/element-citation/person-group

Ocorre 
 Zero ou uma vez

<size>
^^^^^^
 
Identifica a quantidade total de páginas de um documento mencionado numa referência. Deve ser utilizada com o atributo @units com o tipo "page".

**Exemplo:**
 
.. code-block:: xml

     <size units="pages">359</size>

Aparece em
  1. article/front/article-meta/product
  2. article/back/ref-list/ref/element-citation
  

Atributo Obrigatório 
 1. units="page"

Ocorre 
 Zero ou mais vezes

<page-range>
^^^^^^^^^^^^
Identifica um grupo de páginas mencionados numa referência.

**Exemplo:**

  ..code block::

<fpage>300</fpage>
<lpage>420</lpage>
<page-range>300-301, 305, 407-420</page-range>

..note:: A inserção do grupo de páginas deve ser inserido posteriormente as informações da primeira página do grupo <fpage> e de última página do grupo <lpage>

Aparece em
   1. article/front/article-meta/product
   2. article/back/ref-list/ref/element-citation 
  
Ocorre 
 Zero ou uma vez

<isbn>
^^^^^^
Identifica O “International Standard Book Number” de um livro e é identificado numa referência ou produto.

**Exemplo:**

  ..code block::

    <isbn>853251622X</isbn>

Aparece em
  1. article/front/article-meta/product
  2. article/back/ref-list/ref/element-citation

Ocorre 
 Zero ou mais vezes

<source>
^^^^^^^^

Identifica o título da fonte principal de uma referência ou de um produto. O atributo @xml:lang não deve ser utilizado.

**Exemplo:**

  ..code block::

    <source>A insustentável leveza do ser</source>

**Exemplo:**

  ..code block::

   <source>Arch Neurol</source>


Aparece em
  1. article/front/article-meta/product
  2. article/back/ref-list/ref/element-citation  

Ocorre 
 Uma vez se houver <ref> e <product>

<edition>
^^^^^^^^^
Representa a edição de um documento de uma referência, também pode identificar a versão de um software ou base de dados.

**Exemplo 1: 2º edição de um livro**

  ..code block::

  <edition>2º ed<edition>

**Exemplo 2: Versão de software**

  ..code block::
 
  <edition>1.0 version<edition

Aparece em
  1. article/front/article-meta/product
  2. article/back/ref-list/ref/element-citation
  
Ocorre 
 Zero ou mais vezes

<publisher-name>
^^^^^^^^^^^^^^^^
Representa o nome da casa publicadora ou editora numa referência.

**Exemplo:**

  ..code block::

  <publisher-name>Rocco</publisher-name>

Aparece em
  1. article/front/article-meta/product
  2. article/back/ref-list/ref/element-citation
  
  
Ocorre 
 Zero ou mais vezes

<publisher-loc>
^^^^^^^^^^^^^^^
Identifica o local de uma casa publicadora ou editora numa referência.

**Exemplo:**

  ..code block::

  <publisher-loc>Rio de Janeiro, Ipanema</publisher-loc>

Aparece em
  1. article/front/article-meta/product
  2. article/back/ref-list/ref/element-citation
  
Ocorre 
 Zero ou mais vezes

<history>
---------
O histórico agrupa as datas em que o artigo foi recebido, aceito e/ou revisado. Contém obrigatoriamente as tags <date>.
 
Aparece em
 1. article/front/article-meta
 
Ocorre
 Zero ou uma vez
 
<date>
^^^^^^
Em <date> deve constar obrigatoriamente a tag <year>. Usa-se o atributo @date-type para especificar o tipo do recebimento (received), aceito (accepted) e revisado (rev-recd).


.. code-block:: xml
 
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
 
Aparece em
 1. article/front/article-meta/history
 
Atributos obrigatórios
 1. date-type="received" ou date-type="accepted" ou date-type="rev-recd"
 
Ocorre (se houver <history>)
 Uma ou mais vezes 
 
<permissions>
------------
A permissão é um conjunto de condições sob as quais o conteúdo dos artigos pode ser usado, acessados e distribuídos é uma tag obrigatória de <front> e contém a tag de <license>.
 
Aparece em
 1. article/front/article-meta
 
Ocorre
 Uma vez
 
<license>
^^^^^^^^^
Esta informação é obrigatória e está contida em <permissions>, possui também a tag <license-p>, informando o texto da licença adotada. Possui atributo @license-type e @xlink:href obrigatórios.
 
Para @license-type é obrigatório o valor “open-access”. Pode ser adotado os seguintes tipos de licença:"CC-BY-NC" (v3.0 e v4.0)", "CC-BY" (v3.0 e v4.0). Cada licença regula o uso, distribuição e adaptação da obra. Para mais informações consultar: http://creativecommons.org/
 
Para @xlink:href deve ser inserido a URL da licença adotada pelo periódico. As aceitas são as versões vigentes, 3.0 e 4.0.
 
Valores possíveis para @xlink:href:
 
http://creativecommons.org/licenses/by/4.0/
http://creativecommons.org/licenses/by/3.0/
http://creativecommons.org/licenses/by-nc/4.0/
http://creativecommons.org/licenses/by-nc/3.0/
 
*Exemplo:*
 
.. code-block:: xml
 
 <permissions>
     <license license-type="open-access" xlink:href="http://creativecommons.org/licenses/by-nc/4.0/">
     <license-p>Esta obra está licenciado sob uma Licença Creative Commons Atribuição-NãoComercial 4.0 Internacional.</license-p>
     </license>
 </permissions>
 
.. note:: O texto de <license-p> deve ser inserido na língua principal do artigo.
 
Aparece em
 1. article/front/article-meta/permissions
 
Atributos obrigatórios
 1. license-type="open-access"
 2. xlink:href
 
Ocorre
 Uma vez
 
<copyright>
^^^^^^^^^^
É possível além de <license> acrescentar outras informações de direitos autorais através de duas tags, são elas:
 
<copyright-statement> para identificar a instituição a quem pertence os direitos, normalmente a informação descrita aqui vem junto com o símbolo de “copyright”.
 
<copyright-year> para identificar o ano do direito autoral.
 
*Exemplo:*
 
.. code-block:: xml
 
     <permissions>
          <copyright-statement>&#x00A9; 2013 Elsevier Editora Ltda.</copyright-statement>
          <copyright-year>2013</copyright-year>
 
     <license license-type="open-access" xlink:href="http://creativecommons.org/licenses/by/3.0/">
     <license-p>This is an Open Access article distributed under the terms of the Creative Commons Attribution Non-Commercial License, which permits unrestricted non-commercial use, distribution, and reproduction in any medium, provided the original work is properly cited.</license-p>
     </license>
</permissions>
 
Aparece em
 1. article/front/article-meta/permissions
 
Ocorre
 Zero ou uma vez
 
<abstract>
---------
Tag que identifica o resumo do artigo e não deve conter informação de atributo @xml:lang. Os resumos apresentados nos artigos publicados no SciELO normalmente apresentam-se em dois formatos:
 
**estruturado**: Quando possui seções (Ex.: Introdução, Objetivos, Métodos e Resultado). Cada grupo apresentado no resumo será identificado como seção e cada seção terá seu título.
 
*Exemplo:*
 
.. code-block:: xml
 
     <abstract>
      <sec>
        <title>Objetivo</title>
          <p>Verificar a sensibilidade e especificidade das curvas de fluxo-volume na detecção de obstrução da via aérea central (OVAC), e se os critérios qualitativos e quantitativos da curva se relacionam com a localização, o tipo e o grau de obstrução.</p>
       </sec>
       <sec>
        <title>Métodos</title>
           <p>Durante quatro meses foram selecionados, consecutivamente, indivíduos com indicação para broncoscopia. Todos efetuaram avaliação clínica, preenchimento de escala de dispneia, curva de fluxo-volume e broncoscopia num intervalo de uma semana. Quatro revisores classificaram a morfologia da curva sem conhecimento dos
dados quantitativos, clínicos e broncoscopicos. Um quinto revisor averiguou os critérios morfológicos e quantitativos.</p>
       </sec>        
     </abstract>
     
**simples**: Quando apresenta de forma sucinta os principais pontos do texto sem a divisão por seções. Veja exemplo a seguir:
 
*Exemplo:*
 
.. code-block:: xml
 
     <abstract>
          <p>Verificar a sensibilidade e especificidade das curvas de fluxo-volume na detecção de obstrução da via aérea central (OVAC), e se os critérios qualitativos e quantitativos da curva se relacionam com a localização, o tipo e o grau de obstrução. Métodos: Durante quatro meses foram selecionados, consecutivamente, indivíduos com indicação para broncoscopia. Todos efetuaram avaliação clínica, preenchimento de escala de dispneia, curva de fluxo-volume e broncoscopia num intervalo de uma semana. Quatro revisores classificaram a morfologia da curva sem conhecimento dos
dados quantitativos, clínicos e broncoscopicos. Um quinto revisor averiguou os critérios morfológicos e quantitativos.</p>
     </abstract>
     
Aparece em
 1. article/front/article-meta
 
Ocorre
 Zero ou mais vezes
 
<trans-abstract>
----------------
 
Esta tag irá conter o resumo traduzido do artigo, podendo também possuir os formatos simples ou estruturado, deve ser inserida abaixo da tag de abstract e obrigatoriamente deve conter o atributo @xml:lang.
 
.. code-block:: xml
 
<trans-abstract xml:lang="en">
     <sec>
        <title>Objective:</title>
          <p>To assess the sensitivity and specificity of flow-volume curves in detecting central airway obstruction (CAO), and to determine whether their quantitative and qualitative criteria are associated with the location, type and degree of obstruction.</p>
       </sec>
       <sec>
        <title>Methods:</title>
           <p>Over a four-month period, we consecutively evaluated patients with bronchoscopy indicated. Over a one-week period, all patients underwent clinical evaluation, flow-volume curve, bronchoscopy, and completed a dyspnea scale. Four reviewers, blinded to quantitative and clinical data, and bronchoscopy results, classified the morphology of the curves. A fifth reviewer determined the morphological criteria, as well as the quantitative criteria.</p>
       </sec>        
     </trans-abstract>
 
.. code-block:: xml
 
<trans-abstract xml:lang="en">
     <p>To assess the sensitivity and specificity of flow-volume curves in detecting central airway obstruction (CAO), and to determine whether their quantitative and qualitative criteria are associated with the location, type and degree of obstruction.Over a four-month period, we consecutively evaluated patients with bronchoscopy indicated. Over a one-week period, all patients underwent clinical evaluation, flow-volume curve, bronchoscopy, and completed a dyspnea scale. Four reviewers, blinded to quantitative and clinical data, and bronchoscopy results, classified the morphology of the curves. A fifth reviewer determined the morphological criteria, as well as the quantitative criteria.</p>        
</trans-abstract>
 
Aparece em
 1. article/front/article-meta
 
Atributos obrigatórios
 1. xml:lang
 
Ocorre
 Zero ou mais vezes
 
<kwd-group>
-----------
Identifica o grupo por língua de palavras-chave descritas no artigo, terá sempre o atributo de @xml:lang atribuído.
 
.. code-block:: xml
 
     <kwd-group xml:lang="pt">
          <kwd>Broncoscopia</kwd>
     </kwd-group>
 
Aparece em
 1. article/front/article-meta
 
Atributos obrigatórios
 1. xml:lang
 
Ocorre
 Zero ou mais vezes
 
<kwd>   
^^^^^
Esta tag é inserida obrigatoriamente dentro da tag <kwd-group> e identifica cada palavra-chave individualmente <kwd>.
 
.. code-block:: xml
 
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
 
Aparece em
 1. article/front/article-meta/kwd-group
 
Atributos obrigatórios
 1. xml:lang
 
Ocorre (Quando houver <kwd-group>)
 Uma ou mais vezes
 
<funding-group>
--------------
 
Somente quando há número de contrato explicitado no artigo, os dados de financiamento devem ser especificados com <funding-group> sempre dentro de <front>. Obrigatoriamente esta tag deve ser inserida acima da tag de <counts>.
 
.. code-block:: xml
 
     <funding-group>           
       Tags de financiamento...
    </funding-group>
 
A informação de financiamento pode ocorrer em:
- *notas de rodapé <fn>*
- *agradecimentos <ack>*
 
.. note::<funding-group> deve ser inserido logo após as palavras-chave.
 
Aparece em
 1. article/front/article-meta
 
Ocorre
 Zero ou uma vez
 
<award-group>
^^^^^^^^^^^^^
Um artigo pode ter diversos financiadores. Cada grupo de dados de financiamento será identificado pela tag <award-group>.
 

Aparece em
 1. article/front/article-meta/funding-group
 
Ocorre
 Zero ou mais vezes
 
<funding-source>
^^^^^^^^^^^^^^^^
Esta tag deve ficar dentro de <award-group> e nela será especificado o órgão e/ou instituição financiadora:
 
.. code-block:: xml
 
     <funding-group>           
          <award-group>
                <funding-source>CNPq</funding-source>
                <award-id>1685X6-7</award-id>
          </award-group>
 </funding-group>
 
Aparece em
 1. article/front/article-meta/funding-group/award-group
 
Ocorre
 Zero ou mais vezes
 
<award-id>
^^^^^^^^^^
Esta tag deve ficar dentro de <award-group> e nela será especificado
o número de contrato estipulado pela instituição financiadora.
 
.. code-block:: xml
 
     Quando houver para uma instituição mais de um número de contrato:
 
.. code-block:: xml
 
     <funding-group>           
          <award-group>
                <funding-source>CNPQ</funding-source>
                <award-id>00001</award-id>
          </award-group>
     <award-group>
                <funding-source>CNPQ</funding-source>
                <award-id>00002</award-id>
          </award-group>
          <award-group>
                <funding-source>FAPESP</funding-source>
                <award-id>0000X</award-id>
          </award-group>
     </funding-group>
     
.. note:: Nunca insira dois ou mais números de contrato de uma mesma instituição em um único <award-group>, cada número deverá pertencer a seu próprio grupo <award-group>.
 
Aparece em
 1. article/front/article-meta/funding-group/award-group
 
Ocorre
 Zero ou mais vezes
 
<funding-statement>
^^^^^^^^^^^^^^^^^^
 
Está tag só deverá ser inserida quando as informações de financiamento forem apresentadas em notas de rodapé. Representa os dados de financiamento exatamente como foi apresentado na nota de rodapé.
 
*Exemplo informações de financiamento em nota de rodapé <fn>:*
 
.. code-block:: xml
 
     <front>
     <...>
     </kwd-group>
     <funding-group>           
          <award-group>
                <funding-source>CNPQ</funding-source>
                <award-id>00001</award-id>
          </award-group>
     <award-group>
                <funding-source>CNPQ</funding-source>
                <award-id>00002</award-id>
          </award-group>
     <funding-statement>Dados de financiamento como foi apresentado na nota de rodapé</funding-statement>
     </funding-group>    
     <...>
     <back>
     <...>
     <fn-group>
          <fn fn-type="financial-disclosure">
                <p>CNPQ contract 00001 e 00002</p>
          </fn>
     </fn-group>
     </back>
 
.. note:: No caso da nota de rodapé com informação de financiamento, sempre mantê-la dentro de <back> em <fn-group> com o tipo @fn-type "financial-disclosure" e em <front>.
 
.. note:: Notas SEM NÚMERO DE CONTRATO, ficam apenas em <back> mas com tipo @fn-type="supported-by".
 
Aparece em
 1. article/front/article-meta/funding-group
 
Ocorre
 Zero ou uma vez
 
<counts>
--------
Na elaboração do XML alguns dados são importantes para determinar a quantidade de elementos presentes no artigo, por isso utiliza-se a tag <counts> para contabilizar o número exato de tabelas, figuras, referências, equações e páginas presentes no arquivo. Esta tag deve ser inserida como último item de <article-meta>.
 
.. code-block:: xml
 
     <counts>
          <fig-count count="**número de figuras no artigo**"/>
          <table-count count="**número de tabelas no artigo**"/>
          <equation-count count="**número de equações do artigo**"/>
          <ref-count count="**número de referências no artigo**"/>      
          <page-count count="**número de páginas do artigo**"/>
   </counts>
 
.. note:: A sequência das tags de “count” deve ser exatamente a mencionada nos exemplos citados, sua ordem é mandatória.
 
.. code-block:: xml
 
     <counts>
          <fig-count count="5"/>
<table-count count="3"/>
<equation-count count="10"/>
<ref-count count="26"/>
<page-count count="6"/>
  </counts>
 
Aparece em
 1. article/front/article-meta
 
Ocorre
 Uma vez
 
<body>
======
O body compreende o conteúdo e desenvolvimento do artigo.
 
Aparece em
 1. article/body
Ocorre
 Uma vez
 
<sec>
-----
 
O corpo textual do artigo pode ser constituído por seções. Cada uma delas possui um elemento <title> seguido de um ou mais <p>.
 
Quando seus títulos forem:
- **cases:** relatos/estudos de caso
- **conclusions:** conclusões/considerações finais/Final Remarkes
- **discussion:** discussões
- **intro:** introdução/sinopse
- **materials:** materiais
- **methods:** metodologia/método
- **results:** resultados
- **supplementary-material:** material suplementar
 
Terá que ser inserido um atributo @sec-type com o valor correspondente.
 
**Exemplo:**
 
.. code-block:: xml
 
     <sec sec-type="intro">
     <title>Introduction</title>
     <p>Central airway obstruction (CAO) is a pathological process that leads to airflow limitation at the level of the glottis, subglottis, trachea, and main bronchi. Correct diagnosis and treatment of CAO is an area of interest and concern for health professionals,given that this disease has the potential to cause
significant morbidity and mortality.</p>
     </sec>
 
No caso de seções combinadas, ou seja, quando o título for composto por mais de um desses itens, o valor do atributo @sec-type deverá corresponder a cada um respectivamente, separados pelo caractere  `|` (pipe).
 
Exemplo:
 
.. code-block:: xml
 
     <sec sec-type="materials|methods">
     <title>Materials and Methods</title>
       <p>Between November of 2009 and April of 2010, we conducted a prospective, observational, cross-sectional study. The target population consisted of patients for whom bronchoscopy was clinically indicated. The patients were consecutively selected for the sample on the...</p>
</sec>
 
Estas seções podem ser composta por uma ou mais **subseções**, neste caso, cada subseção deverá ser marcada com tag <sec> dentro da seção maior.
 
**Exemplo:**
 
.. code-block:: xml
 
     <sec sec-type="methods">
          <title>Methodology</title>
                <sec>
                     <title>Methodology in Science</title>
                        <p>Each patient underwent a brief physical
examination, and the degree of dyspnea was determined by the Medical Research Council (MRC) 5-point scale.</p>
     </sec>
</sec>
 
No caso da seção não possuir nenhum tipo padrão pode-se inserir a tag sem o atributo @sec-type. Exemplo:
 
.. code-block:: xml
 
<sec>
          <title>Biologia Marinha</title>
<p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi pharetra lacinia orci at adipiscing.</p>
     <sec>
 
Pode possuir um @id para criar referência cruzada <xref> com informações do texto.
 
**Exemplo:**
 
.. code-block:: xml
 
     <sec sec-type="methods" id=”sec01”>
 
Para composição de @id de **seçao** utiliza-se o seguinte padrão: "sec" + o número de ordem da seção. (Ver Regra de atribuição de @id)
 
**Exemplo:** sec01... sec10, sec11;
 
Aparece em
 1. body

Ocorre
 Zero ou mais vezes
     
<disp-formula>
--------------
Tag para identificar equações em parágrafos no texto, podem ser apresentadas como imagem ou codificadas e serão identificadas pela tag <disp-formula>. Se a equação for capturada como imagem, deve-se incluir o nome do arquivo em <graphic>:
 
Para composição de @id de **equações** utiliza-se o seguinte padrão: "e" + o número de ordem da equação. (Ver Regra de atribuição de @id)
 
**Exemplo:** e01... e10, e11;
 
.. code-block:: xml
 
     <p>was the reference electrode.
The Eh measurements were recalculated to the standard hydrogen potential (Standard Hydrogen Electrode - SHE), using the following <xref ref-type="disp-formula" rid="e01">equation 1</xref>
(in mV):</p>
     <disp-formula id="e01">
      <graphic xlink:href="1234-5678-rctb-45-05-0110-e01.tif"/>
     </disp-formula>
 
**Exemplo**: para codificar  σˆ2*
 
.. code-block:: xml
 
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
 
Aparece em
 1. article/body
 2. article/body/p
 3. article/body/sec/p  
 4. article/body/p/table-wrap/thead/tr/th
 5. article/body/p/table-wrap/tbody/tr/td
 6. article/body/sec/tile/p/table-wrap/thead/tr/th
 7. article/body/sec/tile/p/table-wrap/tbody/tr/td
 8. article/back/app-group/app
 9. article/back/app-group/app/supplementary-material

Atributos obrigatórios
 1. @id
 
Ocorre
 Zero ou mais vezes
 
<inline-graphic>
----------------
 
Também representa uma tag para identificar equações que estejam posicionadas em linha, ou seja, em meio a um parágrafo.
 
Para composição de @id de **equações** utiliza-se o seguinte padrão: "e" + o número de ordem da equação. (Ver Regra de atribuição de @id)
 
**Exemplo:** e01... e10, e11;
 
.. code-block:: xml
 
**Exemplo:**
 
<p>We also used an enrichment factor for surface
waters (EF<sub>w</sub>) based on the equation:<inline-graphic xlink:href="1234-5678-rctb-45-05-0110-e01.tif"/>. The EF<sub>s</sub> and EF<sub>w</sub> quantified the concentration of the element of interest (C<sub>i</sub>) in the sample, in relation to the (natural) geochemical background.</p>
 
No caso de equações codificadas, deve-se observar as orientações de codificação recomendada pela W3C em linguagem MathML (http://www.w3.org/TR/MathML3/), sendo o elemento base <mml:math>.
 
**Exemplo**: para codificar  σˆ2*
 
.. code-block:: xml
 
     <inline-formula>
     <mml:math>
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
 
Aparece em
 1. article/article-meta/product
 2. article/body
 3. article/body/p
 4. article/body/sec  
 5. article/body/table-wrap/thead/tr/th
 6. article/body/table-wrap/tbody/tr/td
 7. article/back/app-group/app/table-wrap/thead/tr/th
 8. article/back/app-group/app/table-wrap/tbody/tr/td
 
Ocorre
 Zero ou mais vezes
 
<table-wrap>
^^^^^^^^^^^^
É utilizada para especificar uma tabela, incluindo <label>, <caption> e <table-wrap-foot>. 
 
Para composição de @id de **tabela** utiliza-se o seguinte padrão: "t" + o número de ordem da tabela. (Ver Regra de atribuição de @id)
 
**Exemplo:** t01... t10, t11;
 
**Exemplo:**
 
.. code-block:: xml
 
     <table-wrap id="t01">
 
Aparece em
 1. article/body/p
 2. article/body/sec/p  
 3. article/back/app-group/app
 4. article/back/app-group/app/glossary
 5. article/back/app-group/app/supplementary-material
 6. article/back/glossary
 

Atributos obrigatórios
 1. id
 
Ocorre
 Zero ou mais vezes
 
<table-wrap-foot>
^^^^^^^^^^^^^^^^^
Em <table-wrap-foot> é possível fazer a identificação de nota de rodapé de tabela(<fn>). A tag <fn> deve apresentar o atributo de @id com a seguinte estrutura:
 
Para composição de @id de **nota de rodapé de table** utiliza-se o seguinte padrão: "TFN" + o número de ordem da nota de rodapé de table. (Ver Regra de atribuição de @id)
 
**Exemplo:** TFN01... TFN10,TFNf11;
 
A nota de rodapé poderá ser relacionada com alguma informação no corpo da tabela.
 
**Exemplo**:
 
.. code-block:: xml
 
     <table-wrap id="t01">
     <label>Table 1</label>
     <caption>
     <title>Título da tabela.</title>
     </caption>
     <table>
     <...>
     </table>
     <table-wrap-foot>
     <fn id="TFN01">
     <label>*</label>
     <p>text</p>
     </fn>
     </table-wrap-foot>
     </table-wrap>
 
Aparece em
 1. article/body/p/table-wrap
 2. article/body/sec/p/table-wrap
 3. article/back/app-group/app/table-wrap
 4. article/back/app-group/app/glossary/table-wrap
 5. article/back/glossary/table-wrap
 6. article/back/app-group/app/supplementary-material/table-wrap

Ocorre
Zero ou mais vezes
 
<table>
^^^^^^^
A tabela é dividida em cabeçalho/títulos <thead> e corpo/dados da tabela <tbody>.
 
São elementos de <table>:
 
- **col:** identifica uma coluna (possui atributos);
- **colgroup:** identifica o total de colunas da tabela (possui atributos);
- **thead:** identifica o cabeçalho;
- **tfoot:** identifica a nota de rodapé da tabela;
- **tbody:** identifica o corpo da tabela;
- **tr:** identifica uma linha da tabela.
 
Aparece em
 1. article/body/p/table-wrap
 2. article/body/sec/p/trable-wrap
 3. article/back/app-group/app/table-wrap
 4. article/back/app-group/app/glossary/table-wrap
 5. article/back/glossary/table-wrap
 6. article/back/app-group/app/supplementary-material/table-wrap  

Ocorre (quando houver <table-wrap>)
 Uma vez
 
<thead>
^^^^^^^
Utilizada para apresentar o cabeçalho/título de uma tabela, pode conter alguns atributos para que a formatação fique de acordo com o PDF. Para fazer a identificação dos dados de cabeçalho deve ser utilizada as tags <tr> e <th>.
 
**<tr>**: A tag <tr> é utilizada para fazer a identificaçao de uma linha da tabela. <tr> faz a identificação das tags <td> e <th> onde: <td> especifica os dados da tabela em <tbody> e <th> identifica os dados da tabela em <thead>. Portanto, para cabeçalhos / títulos a estrutura deve ser a seguinte:
 
.. code-block:: xml
 
     <thead>
     <tr>
      <th>dado</th>
      <th>dado</th>
      <th>dado</th>
     </tr>
     </thead>
 
Aparece em
 1. article/body/p/table-wrap/table
 2. article/body/sec/p/trable-wrap/table
 3. article/back/app-group/app/table-wrap/table
 4. article/back/app-group/app/glossary/table-wrap/table
 5. article/back/glossary/table-wrap/table
 6. article/back/app-group/app/supplementary-material/table-wrap/table  

Ocorre
 Zero ou mais vezes
 
**<th>**: REESCREVER O <TH>.
 
<tbody>
^^^^^^^
A tag <tbody> é utilizada para identificar do corpo da tabela. A tag <tr> em <tbody> indica a presença de uma linha.
 
Para a especificação de dados em <tr> para o corpo da tabela, é necessário utilizar a tag <td>. Essa tag é utilizada para identificar a células/dados que ficam no corpo da tabela.
 
A tag <td> pode conter uma série de informações tais como: email, hr, break, italic, underline, bold, roman, sub, sup, inline-formula, list, mml:math, p, graphic, media, sc, inline-supplementary-material, disp-formula-group, disp-formula, inline-graphic, fn, xref etc.
 
**Exemplo:**
 
.. code-block:: xml
 
     <tbody>
     <tr>
     <td align="center">célula<sup>3</sup></td>
     <td align="center">célula</td>
     <td align="center">célula</td>
     </tr>
     <tr>
     <td align="center">célula</td>
     <td align="center">célula</td>
     <td align="center">célula</td>
     </tr>
     <tr>
     <td align="center">célula<xref ref-type="table-fn" rid="TFN01">*</xref></td>
     <td align="center">célula</td>
     <td align="center">célula</td>
     </tr>
     </tbody>
 </table>
     <table-wrap-foot>
     <fn id="TFN01">
     <label>*</label>
     <p>text</p>
     </fn>
     </table-wrap-foot>
 </table-wrap>
 
.. note:: as tags <thead>, <tbody>, <tr>, <th> e <td> possuem atributos de estilo os quais podem ser consultados em:
http://jats.nlm.nih.gov/publishing/tag-library/1.0
 
**Exemplo:**
 
.. code-block:: xml
 
<table-wrap id="t01">
    <label>Tabela 1</label>
         <caption>
             <title>Correlação de Spearman entre Ideb, PIB, População e Custo-Aluno, referentes ao Sub-Banco de Dados do Nível da Escola com Dados - 2009</title>
       </caption>
   <table>
       <colgroup>
            <col/>
            <col/>
       </colgroup>
       <thead>
            <tr>
                <th align="center">Variável</th>
                 <th align="center">Ideb
  2009</th>
            </tr>
       </thead>
       <tbody>
           <tr>
              <td align="center">%BPBF</td>
              <td align="center">-0,54</td>
          </tr>
          <tr>
              <td align="center">População</td>
              <td align="center">0,08</td>
          </tr>
          <tr>
              <td align="center">PIB p/c 2009</td>
              <td align="center">0,45</td>
           </tr>
          <tr>
              <td align="center">CA 2009</td>
              <td align="center">0,54</td>
          </tr>
       </tbody>
   </table>
   <table-wrap-foot>
       <fn id="TFN01">
           <p>Notas: Ideb 2009 = Índice de Desenvolvimento da Educação Básica 2009.</p>
       </fn>
   </table-wrap-foot>
</table-wrap>
 
     
     <table-wrap id="t02">
          <label>Table 2</label>
          <caption>
          <title>Título da tabela.</title>
           </caption>
          <table frame="hsides" rules="all">
                <colgroup width="33%">
                <col/>
                <col/>
                <col/>
                </colgroup>
          <thead> dados do cabeçalho da tabela
                <tr>
                <th style="background-color:#e5e5e5">xxxxx</th>
                <th style="background-color:#e5e5e5">xxxxx</th>
                <th style="background-color:#e5e5e5">xxxxxx</th>
                </tr>
          </thead>
          <tbody>
                <tr>
                <td align="center">xxx<xref ref-type="fn" rid="TFN02">(1)</xref></td>
                <td align="center">xxxx</td>
                <td align="center">xxxx</td>
                </tr>
                <tr>
                <td align="center">xxxxx</td>
                <td align="center">xxxx</td>
                <td align="center">xxxx</td>
                </tr>
                <tr>
                <td align="center">xxxxx</td>
                <td align="center">xxxx</td>
                <td align="center">xxxx</td>
                </tr>
          </tbody>
          </table>
          <table-wrap-foot>
          <fn id="TFN02">
          <label>(1)</label>
          <p>Data are reported as number with percent in parentheses unless otherwise indicated</p>
          </fn>
          </table-wrap-foot>
          </table-wrap></p>

..note:: o label da <table-wrap-foot> pode fazer relação com algum símbolo dentro da tabela, que será identificado com xref do tipo "fn" com rid seguindo o da sua nota correspondente (TFN02). 

Aparece em
 1. article/body/p/table-wrap/table
 2. article/body/sec/p/table-wrap/table
 3. article/back/app-group/app/table-wrap/table
 4. article/back/app-group/app/glossary/table-wrap/table
 5. article/back/glossary/table-wrap/table 
 5. article/back/app-group/app/supplementary-material/table-wrap/table 

Ocorre
 Zero ou mais vezes
 
<supplementary-material>
------------------------
O material suplementar é um documento que não faz parte do texto do artigo, mas que serviu como apoio para sua elaboração.
Em <supplementary-material> é possível especificar tabelas, figuras, dados brutos de planilha, banco de dados de genomas, quiz, equações, links, diálogos, listas, licenças e objetos multimídia como áudio e vídeo.
 
Para composição de @id de **suplemento** utiliza-se o seguinte padrão: "suppl" + o número de ordem do suplemento. (Ver Regra de atribuição de @id)
 
**Exemplo:** suppl01... suppl10, suppl11;
 
O material suplementar pode estar em <front>, dentro de <article-meta>, em <body> como seção ou entre parágrafos e em <back> só poderá ser identificado caso esteja especificado dentro do grupo de apêndices <app-group>.
 
Seus atributos mais frequentes são:
 
- **@id:** utilizado como um identificador único no documento e ganha maior importância quando há mais que um material suplementar e/ou quando o material suplementar é referenciado no corpo do texto. Nesse caso é necessário relacionar a chamada no texto com o "id" do material suplementar.
- **@mimetype:** utilizado para especificar o tipo de mídia como "vídeo" ou "aplicação".
- **@mime-subtype:** utilizado para especificar o formato da mídia.
 
**Exemplo:**
 
.. code-block:: xml
 
     <supplementary-material xlink:href="0000-0000-abcd-01-12-0001-suppl01.mp3" mime-subtype="mpeg" mimetype="audio">
 
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
 
Aparece em
 1. article/front/article-meta
 2. article/body/p
 3. article/body/sec/p
 4. article/body/p/inline-supplementary-material
 3. article/body/sec/p/inline-supplementary-material
 4. article/back/app-group/app

Atributos obrigatórios
 1. id
 2. xlink:href
 3. mimetype
 4. mime-subtype

 
Ocorre
  Zero ou mais vezes
 
<disp-quote>
------------
Quando há no texto uma citação de outra fonte utiliza-se a tag <disp-quote>. Geralmente essa informação é apresentada com algum recuo, possui mais de três linhas e fonte de tamanho diferente, tendo essa informação já destacada a identificação deve ser:
 
**Exemplo:**
 
.. code-block:: xml
 
     <p> Mauris ac magna fermentum, pharetra tellus aliquam, tempor felis. </p>
     <disp-quote>
                <p>"Sed luctus quam a felis sagittis lacinia. Etiam auctor tincidunt nibh, sit amet convallis urna convallis nec. Nullam venenatis dapibus dapibus. Vivamus et arcu blandit, laoreet tellus eget, sodales sapien. Etiam fringilla turpis enim, sit amet porta velit faucibus eu."</p>
     </disp-quote>
     <p>Donec dapibus lacus urna, eu fringilla quam tempus eu.</p>
 
A tag <disp-quote> também é utilizada para epígrafes, citações em blocos e extratos dentro do texto.
 
Aparece em
 1. article/body/p
 2. article/body/sec/p
 
Ocorre
 Zero ou mais vezes
 
<ext-link>
----------
Utilizado para especificar links de URLs. Ao fazer a identificação da URL com <ext-link>, o link abrirá em uma nova aba.
 
**Atributos**
 
@ext-link-type
@xlink:href     
 
Para o atributo @ext-link-type utilizar o valor “uri”.
 
Em @xlink:href deve ser inserido a URL do arquivo referenciado (http://…)e entre a tag.
 
**Exemplo:**
 
.. code-block:: xml
 
     <p>Neque porro quisquam est <ext-link ext-link-type="uri" xlink:href="http://www.scielo.org">www.scielo.org</ext-link> qui dolorem ipsum quia</p>
 
.. note:: O prefixo "http://" deve estar sempre presente no xlink:href.
 
Aparece em
 1. article/body/p
 2. article/body/sec/p
 3. article/back/ref-list/ref/element-citation
 4. article/back/ref-list/ref/element-citation/comment
 5. article/back/app-group/app/p

Atributos obrigatórios
 1. ext-link-type="uri"
 2. xlink:href
 
Ocorre
 Zero ou mais vezes
 
<list>
------
Para uma sequência de dois ou mais itens em lista, possuindo ou não uma determinada ordenação, usa-se a tag <list>.
 
<list> deve apresentar as seguintes tags:
 
- list-item (1 ou mais)
- label     (0 ou 1)    
- title     (0 ou 1)
 
**<list-item>**
Utilizada para identificar um item de uma lista.
A tag list-item pode identificar as tags que seguem:
 
- <p> (1 ou mais)
- <def-list> (0 ou 1)
- <list> (0 ou 1)
**<label>**
Opcional - se constar no PDF, identificar.
 
**<title>**
Opcional - se constar no PDF, identificar.
 
.. note:: Somente uma das tags citadas acima (<label> e <title>) podem ser utilizadas dentro de uma lista (tag <list>), não se pode usar as duas tags ao mesmo tempo.
 
**@list-type:** indica o tipo de lista apresentada.
 
**Exemplos:**
 
- **order:** lista ordenada, cujo prefixo utilizado é um número;
- **bullet:**   lista com marcadores, prefixo utilizado é um ícone de "bola";
- **alpha-lower:** lista ordenada, cujo prefixo é um caractere alfabético minúsculo;
- **alpha-upper:** lista ordenada, cujo prefixo é um caractere alfabético maiúsculo;
- **roman-lower:** lista ordenada, cujo prefixo é um numeral romano minúsculo;
- **roman-upper:** lista ordenada, cujo prefixo é um numeral romano maiúsculo;
- **simple**: simples ou lista simples, sem prefixo antes de cada item ou com um traço.
 
**Exemplos:**
 
Tipo ordenada (ordem numérica):
 
**Exemplo no texto:**
 
Lista Númerica
1 Nullam gravida tellus eget condimentum egestas.
2 Curabitur luctus lorem ac feugiat pretium.
3 Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.
 
**Exemplo no XML:**
 
.. code-block:: xml
 
<list list-type=“order”>
 <title>Lista Númerica</title>
  <list-item>
    <p>Nullam gravida tellus eget condimentum egestas.</p>
  </list-item>
  <list-item>
<p>Curabitur luctus lorem ac feugiat pretium.</p>
  </list-item>
  <list-item>
<p>Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.</p>
  </list-item>
 
Tipo ícone com "marcadores":
 
**Exemplo no texto:**
 
Nullam gravida tellus eget condimentum egestas.
Curabitur luctus lorem ac feugiat pretium.
Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.
 
Exemplo no XML:
 
.. code-block:: xml
 
<list list-type=“bullet”>
  <list-item>
    <p>Nullam gravida tellus eget condimentum egestas.</p>
  </list-item>
  <list-item>
<p>Curabitur luctus lorem ac feugiat pretium.</p>
  </list-item>
  <list-item>
<p>Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.</p>
  </list-item>
 
Tipo caracter alfabético minúsculo:
 
**Exemplo no texto:**
 
- Lista 3
a Nullam gravida tellus eget condimentum egestas.
b Curabitur luctus lorem ac feugiat pretium.
c Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.
 
Exemplo no XML:
 
.. code-block:: xml
 
<list list-type=“alpha-lower”>
 <label>Lista 3</label>
  <list-item>
    <p>Nullam gravida tellus eget condimentum egestas.</p>
  </list-item>
  <list-item>
<p>Curabitur luctus lorem ac feugiat pretium.</p>
  </list-item>
  <list-item>
<p>Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.</p>
  </list-item>
 
Tipo caracter alfabético maiúsculo:
 
**Exemplo no texto:**
 
A Nullam gravida tellus eget condimentum egestas.
B Curabitur luctus lorem ac feugiat pretium.
C Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.
 
**Exemplo no XML:**
 
.. code-block:: xml
 
<list list-type=“alpha-upper”>
  <list-item>
    <p>Nullam gravida tellus eget condimentum egestas.</p>
  </list-item>
  <list-item>
<p>Curabitur luctus lorem ac feugiat pretium.</p>
  </list-item>
  <list-item>
<p>Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.</p>
  </list-item>
 
Tipo número romano minúsculo:
 
**Exemplo no texto:**
 
i Nullam gravida tellus eget condimentum egestas.
ii Curabitur luctus lorem ac feugiat pretium.
iii Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.
 
**Exemplo no XML:**
 
.. code-block:: xml
 
<list list-type=“roman-lower”>
  <list-item>
    <p>Nullam gravida tellus eget condimentum egestas.</p>
  </list-item>
  <list-item>
<p>Curabitur luctus lorem ac feugiat pretium.</p>
  </list-item>
  <list-item>
<p>Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.</p>
  </list-item>
 
Tipo número romano maiúsculo:
 
**Exemplo no texto:**
 
I Nullam gravida tellus eget condimentum egestas.
II Curabitur luctus lorem ac feugiat pretium.
III Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.
 
**Exemplo no XML:**
 
.. code-block:: xml
 
<list list-type=“alpha-upper”>
  <list-item>
    <p>Nullam gravida tellus eget condimentum egestas.</p>
  </list-item>
  <list-item>
<p>Curabitur luctus lorem ac feugiat pretium.</p>
  </list-item>
  <list-item>
<p>Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.</p>
  </list-item>
 
Tipo sem prefixo:
 
**Exemplo no texto:**
 
Nullam gravida tellus eget condimentum egestas.
Curabitur luctus lorem ac feugiat pretium.
Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.
 
**Exemplo no XML:**
 
<list list-type=“simple”>
  <list-item>
    <p>Nullam gravida tellus eget condimentum egestas.</p>
  </list-item>
  <list-item>
<p>Curabitur luctus lorem ac feugiat pretium.</p>
  </list-item>
  <list-item>
<p>Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.</p>
  </list-item>
 
Aparece em
 1. article/body/p
 2. article/body/sec/p

Ocorre
 Zero ou mais vezes
 
<caption>
---------
 
Tag que representa uma descrição textual visível de uma tabela, figura ou objeto similar.
 
Obrigatoriamente dentro de <caption> deve-se conter a tag de <title> com a descrição textual da legenda dos objetos mencionados.
 
**Exemplo:**
 
.. code-block:: xml
 
<fig id="f03">
 <label>Figura 3</label>
     <caption>
<title>Percentual de atividade mitocondrial (método MTT) das células dos diferentes grupos experimentais em relação às células do grupo controle</title>
</caption>
     <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
</fig>
 
Aparece em
 1. article/body/p/disp-formula
 2. article/body/p/fig
 3. article/body/p/table-wrap
 4. article/body/p/media
 5. article/body/p/supplementary-material
 6. article/body/sec/p/disp-formula
 7. article/body/sec/p/fig
 8. article/body/sec/p/table-wrap
 9. article/body/sec/p/media
 10. article/body/sec/p/supplementary-material
 11. article/back/app-group/app
 12. article/back/app-group/app/fig
 13. article/back/app-group/app/table-wrap
 14. article/back/app-group/supplementary-material

Ocorre
 Zero ou mais vezes


<fig>
-------
As figuras de um artigo são identificadas por meio da tag <fig>. Com essa tag é possível especificar label, caption, graphic, links, e objetos multimídia como vídeo, áudio e filme.
 
As imagens podem ter ou não legendas. Para imagens sem legendas é necessário marcá-la como <fig> e identificá-la com a tag <graphic>.
 
**Exemplo:**
 
.. code-block:: xml
 
     <fig id="f01">
     <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
     </fig>
 
A tag <graphic> é utilizada para identificar alguns tipos de arquivos. Seus atributos são:
 
- **@xlink:href:** utilizado para especificar um endereço ou links externos. Portanto o @xlink:href deve conter nomes de imagens/arquivos e também o nome completo de uma URL.
 
Para figuras com legendas a marcação deve envolver toda a informação de imagem, inclusive sua descrição, com a tag <fig>. Dentro de <fig> serão identificados o rótulo da figura <label> e mais a tag de <caption> com a tag <title> com o título da figura.
 
**Exemplo:**
 
.. code-block:: xml
 
     <fig id="f01">
 <label>Fig. 1</label>
     <caption><title>título da imagem</title></caption>
     <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
     </fig>
 
Essa tag pode ter os seguintes atributos: @fig-type, @id, @xml:lang. Os atributos mais frequentes são:
 
- **@fig-type:** utilizado para especificar o tipo de imagem. Os tipos podem ser muitos como: Graphic, Cartoon, Chart, Diagram, Drawing, Exihibit, Illustration, Map etc. Contudo o tipo só será definido caso o label da figura apresente um tipo diferente de "fig." "figure".
 
**Exemplo:**
 
.. code-block:: xml
 
     <fig fig-type="map" id="f01">
     <label>Map 1</label>
     <caption>
      <title>Título do Mapa<title>
     </caption>
 
Se a figura não possuir um tipo específico, deve-se manter a tag sem o atributo.
 
**Exemplo:**
 
.. code-block:: xml
 
     <fig id="f01">
     <label>Fig 1</label>
     <caption>
          <title>Título da Figura<title>
     </caption>
 
- **@id:** identificador da tag. É possível fazer referência cruzada no documento; esse atributo deve ter valor único no arquivo e é possível fazer link relacionado a um "rid".
 
Para composição de @id de **figuras** utiliza-se o seguinte padrão: "f" + o número de ordem da figura. (Ver Regra de atribuição de @id)
 
**Exemplo:** f01... f10, f11;
 
.. code-block:: xml
 
     <fig id="f01">
     <label>FIGURE 1</label>
          <caption>
                <title>Título da figura</title>
          </caption>
      <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
     </fig>

Aparece em
 1. article/body/p
 2. article/body/sec/p
 3. article/back/app-group/app  
 4. article/back/app-group/app/supplementary-material

Atributos obrigatórios
 1. id
 
Ocorre
 Zero ou mais vezes
 
<media>
-----
A tag <media> é utilizada para especificar arquivos multimídia como:
 
- vídeo
- áudio
- filmes
- animações
 
Atributos
 
- @id
Para composição do @id de **media** utiliza-se o seguinte padrão:
"m" + o número de ordem da media:
 

**Exemplo:** m01... m10, m11;

- **@mimetype:** utilizado para especificar o tipo de mídia como "vídeo" ou "aplicação".

- **@mime-subtype:** utilizado para especificar o formato da mídia.
 
**Exemplo:**
 
.. code-block:: xml
 
<media mimetype="video"  mime-subtype="mp4" xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/>
 
- @mimetype
    utilizado para especificar o tipo de mídia como "vídeo" ou "aplicação".
 
**Exemplo:**
 
.. code-block:: xml
 
<media mimetype="video" mime-subtype="mp4" xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/>
 
- **@xlink:href:** indica o link de um arquivo multimídia.
 
**Exemplo:**
 
.. code-block:: xml
 
     <media mimetype="video"  mime-subtype="mp4" xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/>
 
**Exemplo:**
 
*Em parágrafo:*
 
.. code-block:: xml
 
<p>Within the limitations of this study, it may be concluded that remaining tooth wall thickness did not influence the fatigue resistance of molars restored with CAD/CAM ceramic inlays
<media mimetype="video"  mime-subtype="mp4" xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/></p>
 
*Em figuras:*
 
.. code-block:: xml
 
<p>
 <fig id="f01">
     <label>Figure 1</label>
     <caption><title>descrição da fig.<title></caption>
          <media xlink:href="1234-5678-rctb-45-05-0110-m01.avi" mimetype="video" mime-subtype="avi"/>
      </fig>
</p>
 
*Em <sec> do tipo material suplementar:*
 
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
 
Aparece em
 1. article/body/p
 2. article/body/sec/p
 3. article/body/p/fig
 4. article/body/sec/p/fig
 5. article/back/app-group/app  
 6. article/back/app-group/app/fig

Atributos obrigatórios
 1. mime-subtype
 2. xlink:href
 
Ocorre
 Zero ou mais vezes
 
<sig-block>
-----------
Tag que identifica um bloco de assinatura(s), normalmente utilizada em documentos do tipo editorial. A tag de <sig-block> deve obrigatoriamente conter a tag <sig>. É possível formatar o texto do bloco de assinatura com negrito <bold> ou itálico <italic>. Para as quebras de linhas deve-se usar a tag <break/>, ou <p> como mostram os exemplos a seguir:
 
.. code-block:: xml
 
**Exemplo 1:**
 
<sig-block>
<sig>
<bold>Harry Weasley</bold><break/>
<italic>Editor Chefe</italic><break/>
Profeta Diário<break/>
</sig>
</sig-block>
.. code-block:: xml
 
**Exemplo 2:**
 
<sig-block>
<sig>
<p><bold>Harry Weasley</bold></p>
<p><italic>Editor Chefe<italic></p>
<p>Profeta Diário</p>
</sig>
</sig-block>
 
Aparece em
 1. article/body
Ocorre
 Zero ou uma vez
 
<back>
======
O back é a parte final do documento que compreende lista de referências e demais dados referentes a pesquisa como: notas de rodapé, agradecimentos, apêndice, material suplementar, anexos e glossário.
 
Aparece em
 1. article
Ocorre
 Zero ou uma vez
 
<ack>
-----
A seção de agradecimentos quando aparecer no documento deve ser marcada dentro de <back>.
 
É em agradecimentos que frequentemente os dados de financiamento da pesquisa são indicados, como descrito em <funding-group> em <front>.
 
Todo o conteúdo de agradecimentos deverá ser identificado com a tag <ack>, caso haja o título "Agradecimentos" ou "Acknowledgment" identifique-o com a tag <title>. Em <ack> é possível especificar um ou mais parágrafos <p>.
 
**Exemplo:**
 
.. code-block:: xml
 
     <back>
          <ack>
                <title>Agradecimentos</title>
                <p>Texto de agradecimentos, pode ou não conter dados de financiamento</p>
     </ack>
 
.. note:: Não inserir a tag <sec> para identificação da seção agradecimentos. 
 
Aparece em
 1. article/back

Ocorre
 Zero ou mais vezes


<ref-list>
----------

 O conjunto de referências biliográficas de um artigo é representado pela tag <ref-list>. Esse elemento deve conter, obrigatóriamente, três tags: <ref>, <mixed-citation> e <element-citation>.

Aparece em
 1. article/back

Ocorre
 Zero ou mais vezes

 
<ref>
-----
Existem diversos tipos de referências e normas para apresentá-las num documento textual (ABNT, Vancouver, APA, ISO e OTHER). Independente da norma usada, a representação dos elementos essenciais em xml de uma referência devem ser identificados corretamente.
 
Para composição de @id de **referências** utiliza-se o seguinte padrão: "B" + o número de ordem das referências. (Ver Regra de atribuição de @id)
 
**Exemplo:** B01... B10, B11;
 
Aparece em
 1. article/back/ref-list

Ocorre (quando houver <ref-list>)
 Uma ou mais vezes
 
Atributo Obrigatório 
 1. id

.. code-block:: xml
 
<ref-list>
   <ref id="B01">
      <mixed-citation>referência inteira sem marcação</mixed-citation>
      <element-citation publication-type=“tipo da referência”>elementos marcados um a um</element-citation>
   </ref>
</ref-list>
 
- <ref>
Na tag <ref> deve ser inserido um @id para cada referência citada;
 
     - <mixed-citation>
Tag utilizada para identificar uma referência bibliográfica conforme consta no PDF;
 
- <element-citation>
A tag element-citation apresenta a identificação detalhada de cada referência biliográfica. Essa tag deve apresentar o atributo @publication-type. O atributo indica o tipo de referência.
     
Tipos de publicação - **@publication-type:**:
 
- **journal:** utilizada para referenciar publicações seriadas, editadas em unidades sucessivas, com designações numéricas e/ou cronológicas e destinada a ser continuada indefinidamente.   
- **book:** utilizada para referenciar monografia/livro. Pode também representar somente uma parte ou capítulo de um livro.
- **webpage:** utilizada para referencias de um relatório técnico, normalmente de autoria institucional.
- **thesis:** utilizada para referenciar TCC para obtenção de um grau acadêmico, tais como livre-docência, doutorado, mestrado, bacharelado, licenciatura, etc.
- **confproc :** utilizada para referenciar documentos relacionados com eventos científicos: atas, anais, resultados, proceedings, convenção, conferência entre outras denominações.
- **patent:** utilizada para referenciar patentes.
- **software:** utilizada para referenciar um software que pode estar em vários suportes, como CDs, DVDs, em suporte online, dispositivos usb e etc.
- **database:** utilizada para referenciar bases de dados.


**IMPORTANTE:**
 
- Nunca manter uma informação toda com formatação <italic>, <bold> etc, dentro de alguma tag;
- Todas as referências devem conter informação de fonte principal <source>;
- Evitar pontuação dentro da marcação em element-citation (ponto final, vírgula etc);
- Todas as informaçoess de uma referência devem ser marcadas, caso nao haja nenhuma tag específica para uma informação insira em <comment>.


**Exemplos:**
 
*Para journal:*
 
.. code-block:: xml
 
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
                <season>Estações do ano (ex.: Inverno)</season>
<month>Mês ou intervalo de meses (Ex.: Jan-Mar)</month>
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
 
*Para book:*
 
.. code-block:: xml
 
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
 
*Para chapter-title (capítulo de livro):*
 
.. code-block:: xml
 
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
 
*Para webpage*:
 
.. code-block:: xml
 
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
     <comment>Available from:<ext-link ext-link-type="uri" xlink:href="http://www.scielo.org">www.scielo.org
     </ext-link></comment>
     </element-citation>
     </ref>
 
.. note:: Quando a referência apresentar URL com texto (Disponível em: ou Available from) identificar conforme o exemplo acima.

*Para report:*
 
.. code-block:: xml
 
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
 
*Para confproc (proceedings):*
 
.. code-block:: xml
 
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
 
*Para thesis:*
 
.. code-block:: xml
 
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
 
*Para patent:*
 
.. code-block:: xml
 
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
 
*Para software:*
 
.. code-block:: xml
 
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
 
*Para database:*
 
.. code-block:: xml
 
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
 
.. note:: Deve-se levar em consideração que muitas vezes as referências são contruídas de forma incorreta, o que dificulta a marcação de seus elementos.

<chapter-title>
^^^^^^^^^^^^^^^

Identifica um capítulo de um documento numa referência.

**Exemplo:**

  ..code block::

  <chapter-title>Anjo da morte</chapter-title>

..note:: Representa o capítulo 24 do livro ‘As feiticeiras de East End’.

  Aparece em
  1. article/back/ref-list/ref/element-citation  

Ocorre 
 Zero ou mais vezes

<pub-id>
^^^^^^^^

Identifica o tipo de identificador (id) de um documento em uma referência. Deve possuir o atributo @pub-id-type com os seguintes possíveis valores:

- pmid
- pcmid
- doi
 -pii
- other

**Exemplo:**

  ..code block::

  <pub-id pub-id-type="pmid">15867408</pub-id>

Aparece em
  1. article/back/ref-list/ref/element-citation
  

Atributo Obrigatório 
 1. pub-id-type

Ocorre 
 Zero ou mais vezes


<date-in-citation>
^^^^^^^^^^^^^^^^^^
Esta tag identifica a data de citação em uma referência. Deve sempre possuir o atributo @content-type com os tipos de data de acesso e data de atualização do documento.

**Exemplo 1:**

  ..code block::

<date-in-citation content-type="access-date">cited 2007 Feb 21</date-in-citation>

**Exemplo 2:**

  ..code block::

<date-in-citation content-type="updated">2006 Jul 20
</date-in-citation>

Aparece em
  1. article/back/ref-list/ref/element-citation
 
Atributo Obrigatório 
 1. content-type="access-date"
 2. content-type="updated" 

Ocorre 
 Zero ou mais vezes

<comment>
^^^^^^^^^

Tag pode servir para marcar alguma informações juntamente com uma URL (ver tag <ext-link>)e também para identificar dados que não possuem tagueamento específico em uma referência.

**Exemplo:**

  ..code block::
 
  <comment>1 CD-ROM: color, 4 3/4 in.</comment> 

Aparece em
  1. article/back/ref-list/ref/element-citation
  

Ocorre 
 Zero ou mais vezes

<conf-name>
^^^^^^^^^^^
Identifica o nome de uma conferência, congresso, reunião, palestra, seminário e etc mencionado em uma referência.

**Exemplo:**

  ..code block::

<conf-name>Proceedings of the 23rd International Summer School of Brain Research</conf-name>

Aparece em
  1. article/back/ref-list/ref/element-citation
  
Ocorre 
 Zero ou mais vezes

<conf-loc>
^^^^^^^^^^
Identifica o local, país, cidade, estado, província, e local físico como uma assembléia, anfiteatro e etc de uma conferência, congresso, reunião, palestra, seminário e etc mencionado em uma referência.

**Exemplo:**

  ..code block::

  <conf-loc>Dallas, TX</conf-loc>

Aparece em
  1. article/back/ref-list/ref/element-citation
  
Ocorre 
 Zero ou mais vezes

<conf-date>
^^^^^^^^^^^
Trata-se de uma tag para identificar a data de uma conferência, evento e etc. Pode ser composta por um período por exemplo: 2003 Aug 25-29.

**Exemplo:**

  ..code block::

  <conf-date>2002 Jul 28-Aug 2</conf-date>

Aparece em
  1. article/back/ref-list/ref/element-citation
  
Ocorre 
 Zero ou mais vezes


<patent>
^^^^^^^^
Tag utilizada para identificar um número de patente. Deve possuir o atributo @country e nele deve ser atribuído o código do país de acordo com a Norma ISO 3166, com dois caracteres alfabéticos.

Para consultar ao código do país consulte o link da norma ISO: https://www.iso.org/obp/ui/#iso:pub:PUB500001:en

**Exemplo de patente americana:**

  ..code block::

    <patent country="US">US 6,980,855</patent>

Aparece em
  1. article/back/ref-list/ref/element-citation
  
Atributo Obrigatório 
  1. country

Ocorre 
 Zero ou uma vez

<fn-group>
----------
A tag de grupo de notas é um elemento de <back> e deve conter todo o grupo de notas de rodapé mencionadas no documento que não representem notas de autor, as quais deverão ser identificadas em <author-notes>. Pode possuir uma ou mais notas <fn>.
 
**Exemplo:**
 
.. code-block:: xml
 
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
 
Aparece em
 1. article/back
Ocorre
 Zero ou uma vez
 
<fn>
----
Nota de rodapé representa um complemento ou um comentário explicativo do que está sendo citado no texto
 
As notas que devem ser consideradas para entrar como nota de rodapé de <back>, são quaisquer notas que não fazem nenhum tipo de referência aos **autores**, as quais deverão ser identificadas em <author-notes>.
 
Notas em <back> devem estar dentro de um grupo de notas de rodapé: <fn-group>. Os atributos de <fn> são: @fn-type e @id, esta última deve ser única para cada nota.
 
Para composição de @id de **notas** utiliza-se o seguinte padrão: "fn" + o número de ordem das notas. (Ver Regra de atribuição de @id)
 
**Exemplo:** fn01... fn10, fn11;
 
Para notas que apresentam uma etiqueta de identificação (1, 2, a, b, *, e etc) marque com a tag <label>. Essa tag de <label> não pode estar dentro de <p>.

**Exemplo:**
 
.. code-block:: xml
 
     <fn-group>
          <fn fn-type="supported-by" id="fn01">
                <label>*</label>
                     <p>A pesquisa do artigo foi apoiada pelo SEBRAE.</p>
          </fn>
     </fn-group>
 
É possível ter quantas notas forem necessárias dentro da tag de grupo de notas <fn-group>.
 
**Exemplo:**
 
.. code-block:: xml
 
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
 
Também é possível ver notas de rodapé mais simples sem etiqueta <label> ou identificação @id ou ambos.
 
**Exemplo:**
 
.. code-block:: xml
 
     <fn-group>
          <fn fn-type="other">    
                <p>Proin feugiat mattis felis eu placerat.</p>
          </fn>
     </fn-group>
 
Os tipos de <fn> são:
 
- **abbr:** representa abreviaturas de termos e nomes próprios utilizadas ao longo do texto. Caso esteja falando de abreviaturas de nomes dos autores, inserir nota em <author-notes> em <front>.
- **com:** representa nota de algum tipo de comunicado relevante para a realização do artigo.
- **financial-disclosure:** declaração de financiamento ou negação e aceitação de recursos recebidos em apoio à pesquisa em que um artigo é baseado. Serve também para informações de financiamento que possuem um número de contrato ou que só informam se "sim" ou "não" houve financiamento.
- **supported-by:** indica que a pesquisa sobre a qual o artigo é baseado foi apoiada por alguma entidade, instituição ou pessoa física. Considerar neste tipo, informações de financiamento que não possuem números de contrato.
- **presented-at:** indica que o artigo foi apresentado em algum evento científico.
- **supplementary-material:** indica ou descreve o material suplementar do artigo.
- **other:** especifica aquelas notas diferentes das relacionados acima. É possível também ter este tipo de nota em <author-notes> em <front>.
 
**Exemplos:**
 
.. code-block:: xml
 
     <fn-group>
          <fn fn-type="presented-at">
                <label>1</label>
                     <p>Artigo apresentado na primeira conferência SciELO 15 anos, realizada dia 25 de outubro de 2013.</p>
          </fn>
          <fn fn-type="financial-disclosure">
                <label>2</label>
                     <p>Trabalho foi financiado pelo CNPq / Contract: 012345X.</p>
          </fn>
          <fn fn-type="supported-by">
                <label>*</label>
                     <p>Este artigo teve apoio e parceria da Instituição, SciELO - Scientific Eletronic Library Online e da FAP/UNIFESP.</p>
          </fn>
     </fn-group>
 
Aparece em
 1. article/front/article-meta/author-notes
 2. article/back/fn-group 

Atributos obrigatórios
 1. fn-type
 
Ocorre em front
 Zero ou mais vezes

Ocorre em back (quando houver <fn-group>)
 Uma ou mais vezes
 
<app-group>
-----------
Utilizado para indicar a presença de um apêndice ao documento. Para a marcação básica de um apêndice devemos levar em consideração duas tags importantes, a de grupo de apêndice <app-group> e de apêndice propriamente dito <app>. Obrigatoriamente deve ser inserido uma informação de etiqueta <label> em <app>.

Para composição de @id de **apêndice** utiliza-se o seguinte padrão: "app" + o número de ordem do apêndice. (Ver Regra de atribuição de @id)
 
**Exemplo:** app01... app10, app11;
 
**Exemplo de Apêndice com texto:**
 
.. code-block:: xml
 
     <app-group>
     <app>
          <label>Apêndice</label>
     <p>Vivamus fermentum elit et pellentesque iaculis. Curabitur egestas rhoncus purus quis iaculis. Sed laoreet id leo eu tristique. Etiam hendrerit nibh in tincidunt mattis. Sed et volutpat nulla, eget semper tellus. Nullam imperdiet fringilla diam, nec mollis elit sagittis a. Nam euismod sagittis posuere.</p>
     </app>
     </app-group>


**Exemplo de Apêndice com imagem (Pode ser imagem de figura, tabela, quadro, equação e etc):**
 
.. code-block:: xml
 
     <app-group>
     <app id="app01">               
     <label>Appendix 1</label>
          <title>Questionnaire for SciELO</title>    
     <graphic xlink:href="1234-5678-rctb-45-05-0110-app01.tif"/>         
     </app>
     </app-group>
 
**Exemplo de Apêndice com link externo (ext-link do tipo uri):**
 
.. code-block:: xml
 
     <app-group>
     <app>                
     <label>Appendix 1</label>
      <p>Para mais informações <ext-link ext-link-type="uri" xlink:href="http://www.scielo.org">clique aqui</ext-link> para verificar o pdf.</p>                  
     </app>
     </app-group>
 
**Exemplo de Apêndice com tabela:**
 
.. code-block:: xml
 
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
 
**Exemplo de Apêndice misto (figura mais tabela)**
 
.. code-block:: xml
 
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
 
**Exemplo de Apêndice misto (texto mais figura)**
 
.. code-block:: xml
 
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
 
**Exemplo de Apêndice com vídeo:**
.. code-block:: xml
 
     <app-group>
          <app>
           <label>suplemento eletrônico</label>
          <supplementary-material id="suppl01">
          <media xlink:href="1234-5678-rctb-45-05-0110-m01.avi" mimetype="video" mime-subtype="avi"/>
          </supplementary-material>
          </app>
     </app-group>
 
Aparece em
 1. article/back

Atributos obrigatório para <app>
 1. id
 
Ocorre
 Zero ou uma vez
 
<glossary>
---------
Utilizada quando há uma lista de termos e suas respectivas definições. O glossário pode ser apresentado como imagem ou como texto com as identificações de <term>, <def-list> e <def>. O glossário pode estar identificado em: <app>, <back>, e <sec>.
 
Para composição de @id de **glossário** utiliza-se o seguinte padrão: "d" + o número de ordem do glossário. (Ver Regra de atribuição de @id)
 
**Exemplo:** d01... d10, d11;
 
**Exemplo:**
 
*Em apêndices:*
 
.. code-block:: xml
 
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
 
*Em back:*
 
.. code-block:: xml
 
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
 
A tag <glossary> possui os seguintes atributos: @content-type, @id, @specific-use e @xml:lang. Porém o atributo mais frequente é o @id.
 
- **@id:** identificador da tag. É possível fazer referência cruzada no documento; esse atributo deve ter valor único no arquivo e é possível fazer link relacionado a um "rid".
 Para composição do "ID" de **glossários** utilizar o seguinte **padrão:** "d" + o número de ordem da figura –
 
 **Exemplo:** d01... d10, d11;
 
O glossário pode ser apresentado como imagem, utilizando a tag <graphic>, ou como texto. Veja os exemplos abaixo:
 
*Imagem:*
 
.. code-block:: xml
 
     <back>
     <glossary>
     <title>nome do glossário</title>
     <graphic xlink:href="1234-5678-rctb-45-05-0110-d01.tif"/>
     </glossary>
     <ref-list>
     </back>
 
*Texto:*
 
.. code-block:: xml
 
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
 
*Glossário com duas listas de definições:*
 
.. code-block:: xml
 
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
     </back>
 
Aparece em
 1. article/back
 1. article/back/app-group/app
 
Ocorre
 Zero ou mais vezes
 
Referências:
============
ASSOCIAÇÃO BRASILEIRA DE NORMAS TÉCNICAS. NBR14724: informação e
documentação: trabalhos acadêmicos: apresentação. Rio de Janeiro: NBR, 2011.
 
ASSOCIAÇÃO BRASILEIRA DE NORMAS TÉCNICAS. NBR 6023: informação e
documentação: referências: elaboração. Rio de Janeiro: NBR, 2002.
 
JATS. Journal Article Tag Suite ANSI/NISO Z39.96-2012. Baltimore, USA: National Information Standards Organization, 2012. Disponível em:<http://jats.niso.org>.
 
JATS. Journal Article Tag Suite. Rockville Pike, USA: National Center for Biotechnology Information, 2013. Disponível em: <http://jats​.nlm.nih.gov>.
 
JATS. Journal Publishing Tag Library NISO JATS Version 1.0. Rockville, USA: National Center for Biotechnology Information (NCBI), National Library of Medicine (NLM). 2012. Disponível em: <http://jats.nlm.nih.gov/publishing/tag-library/1.0/>.
 
PubMed Central (NCBI). Sample PubMed Central Citations. Rockville Pike, USA: US National Library of Medicine National Institutes of Health. 2008. Disponível em: <http://www.ncbi.nlm.nih.gov/pmc/pmcdoc/tagging-guidelines/citations/v3/toc.html>.
 
PubMed Central (NCBI). Elements: index of elements. Rockville Pike, USA: US National Library of Medicine National Institutes of Health. 2009. Disponível em: <https://www.ncbi.nlm.nih.gov/pmc/pmcdoc/tagging-guidelines/article/tags.html>.
