================================================================
SciELO Publishing Schema - Guia de uso dos elementos e atributos
================================================================

Versão preliminar do documento sujeita a modificações, Abril 2014

encoding
========
A declaração de codificação (encoding) identifica a codificação usada para representar os caracteres no documento. Esta deve ser a primeira especificação a aparecer no documento XML. Para iniciar o XML SciELO usa-se:

  .. code-block:: xml

    <?xml version="1.0" encoding="utf-8"?>

doctype
=======
DOCTYPE é a abreviação de "Document Type". No doctype informa-se quais regras devem ser seguidas e o que é ou não permitido dentro da estrutura de um determinado XML e de um (X)HTML. A estrutura utilizada como guia para o XML SciELO é a JATS (Z39.96) Journal Publishing DTD v1.0 ou `SciELO Publishing Schema v1.0 <http://scieloorg.github.io/scielo_publishing_schema/>`_. Quando XML é criado dentro da estrutura prevista no DOCTYPE o documento é validado. Se há algo divergente, o problema é identificado a partir do confronto entre a estrutura do doctype de referência e do XML criado.


**Nota:** o Doctype valida a estrutura do documento XML e não seu conteúdo.

  .. code-block:: xml

    <!DOCTYPE article PUBLIC "-//NLM//DTD JATS (Z39.96) Journal Publishing DTD v1.0 20120330//EN" "JATS-journalpublishing1.dtd">


article
=======
@dtd-version
------------
a versão utilizada de DOCTYPE. O SciELO PS está na versão 1.0 mas também aceita-se a DTD da JATS v1.0

@article-type
-------------
define-se a tipologia de artigos aceita na estrutura do SciELO PS  1.0. Os tipos de artigos são:

- **research-article (artigo original):** abrange pesquisas, experiências clínicas ou cirúrgicas ou outras contribuições originais.

- **letter (cartas):** comunicação entre pessoas ou instituições e organizações por intercâmbio de cartas

- **article-commentary (comentários):** uma nota crítica ou esclarecedora escrita para discutir, apoiar ou debater um artigo ou outra apresentação anteriormente publicada. Pode ser um artigo, carta, editorial, etc. Estas publicações podem aparecer como comentário, comentário editorial, ponto de vista, etc.

- **brief-communication (comunicação breve):** compreende breves relatos de experiências, trabalhos ou projetos de investigação em andamento.

- **editorial (editorial):** uma declaração de opiniões, crenças e políticas do editor de uma revista, geralmente sobre assuntos de significado científico de interesse da comunidade científica ou da sociedade.

- **in-brief (press release):** comunicação breve de linguagem jornalística sobre um artigo ou tema.

- **case-report (informe/relato de caso):** descrição sumária de casos especiais, que, por sua raridade despertam interesse informativo para a coletividade.

- **report (informe/relatório técnico):** um informe que dá detalhes de uma investigação ou resultado de um problema científico. Pode também relatar um artigo científico, o estado e posição atual de uma investigação científica e o desenvolvimento da mesma.

- **note (nota):** relata resultados parciais ou preliminares de investigação empírica.

- **correction (errata):** corrige erros apresentados em artigos após sua publicação online/impressa.

- **obituary (obituário):** anúncio de morte normalmente de pesquisadores de notório saber de uma determinada área para conhecimento de seus pares.

- **abstract (resumo):** uma apresentação precisa e resumida de uma obra sem agregar interpretação ou crítica, acompanhado de uma referência bibliográfica da obra original.

- **review (revisão):** um artigo que se refere a um material já publicado sobre um tema. Pode ser extenso quanto à complexidade e ao intervalo de tempo do material investigado.

- **book-review (resenha):** análise críticas de livros e outras monografias.

- **clinical-trial (ensaio clínico):** ensaio clínico que segue um plano ou protocolo pré-definido e registrado.

- **retraction (retratação):** a retratação de um artigo científico é um instrumento para corrigir o registro acadêmico publicado equivocadamente, por plágio, por exemplo.

- **collection (coleção):** utilizada quando há um conjunto de cartas, respostas, resenhas etc. O tipo collection é utilizado em "article" do artigo principal e em <sub-article> ou <response> é identificado cada carta, resenha, resposta etc.

@xml:lang
---------
Identica idioma e pode estar presente em praticamente todos os elementos. É mais frequente nos elementos <article>, <article-title>, <name>, <abstract> e <element-citation>. 
Deve-se informar o idioma do elemento utilizando código de duas letras conforme norma ISO 639. Em alguns casos, pode-se usar um classificador quando a língua apresenta variações, como zh-Hant para chinês tradicional e zh-Hans para Chinês simplificado. Abaixo lista de códigos mais comuns:

- **en:** inglês
- **fr:** francês
- **pt:** português
- **es:** espanhol
- **ge:** alemão
- **af:** africâner

 Demais códigos podem ser consultados em http://www-01.sil.org/iso639-3/codes.asp?order=639_1&letter=e

  .. code-block:: xml

    <article 
      xmlns:xlink="http://www.w3.org/1999/xlink" 
      xmlns:mml="http://www.w3.org/1998/Math/MathML" 
      dtd-version="1.0" 
      article-type="research-article" 
      xml:lang="en">


Front
=====
O Front de cada artigo contém os dados principais do documento que compõe a sua referência bibliográfica e que serão também utilizados para a criação do sumário do respetivo número do periódico recuperação de autoria, recuperação do documento e especificação de afiliação. Esses dados alimentam a base e possibilitam a indexação, interoperabilidade na Web, geração de indicadores bibliométricos e interface com os demais serviços oferecidos pelo SciELO.

No Front devem estar apresentados os seguintes dados: metadados do periódico, título(s), autoria, afiliação, resumo(s), palavras-chave, DOI, registro de ensaio clínico (quando houver), paginação, indicação da licença Creative Commons, seção temática ou de tipo de documento a que o documento pertence, histórico (datas de submissão, de aceite e publicação em ahead of print, se houver), dados de correspondência, nota de autor (quando houver).


  .. code-block:: xml

    <front>...</front>

journal-meta
------------
Em journal-meta faz-se a identificação do periódico como um todo. Este item contem os elementos:

journal-id
^^^^^^^^^^
Especifica o tipo de identificação do periódico. No caso do SciELO PS, temos dois tipos: "nlm-ta" onde usa-se a forma abreviada do título do periódico registrada no Pubmed, caso o mesmo seja indexado nesta base de dados ou "publisher-id" onde usa-se o acrônimo do periódico no SciELO.

Para especificação de periódico do tipo "nlm-ta"


  .. code-block:: xml

    <journal-meta>
      <journal-id journal-id-type="nlm-ta">Título do Periódico no Pubmed/Medline</journal-id> 

Para especificação de periódico do tipo "publisher-id"


  .. code-block:: xml

    <journal-id journal-id-type="publisher-id">Acrônimo do Periódico no SciELO</journal-id>

journal-title-group
^^^^^^^^^^^^^^^^^^^
Neste item são incluídas a forma curta (abreviada) e longa do título do periódico de acordo com seu registro no ISSN. O título abreviado sempre Terá como atributo o tipo "publisher".


  .. code-block:: xml

    <journal-title-group>
        <journal-title>Título do Periódico</journal-title>
        <abbrev-journal-title abbrev-type="publisher">Título Abreviado do Periódico</abbrev-journal-title>
    </journal-title-group>

ISSN
^^^^
O ISSN é um código numérico, único, que identifica uma publicação seriada a qual é definida pela norma ISO 3297:2007. Normalmente cada tipo de suporte utilizado pelo periódico possui um número específico. Os tipos de ISSN previstos no SciELO PS  são:

*@pub-type="ppub"* para a versão impressa


  .. code-block:: xml

    <issn pub-type="ppub">ISSN impresso</issn>

*@pub-type="epub"* para a versão digital


  .. code-block:: xml

    <issn pub-type="epub">ISSN eletrônico</issn>

publisher
^^^^^^^^^
O nome da instituição responsável pela publicação do periódico deve ser especificado de acordo com o registro no SciELO. Pode-se consultar a forma adotada no site da coleção, na homepage do periódico.


  .. code-block:: xml

    <publisher>
           <publisher-name>Nome da Instituição responsável pelo Periódico</publisher-name>
    </publisher>
    </journal-meta>
      
article-meta
------------
Contem os metadados do artigo. Seus elementos básicos são DOI, seção (de acordo com o sumário do periódico), título(s) do artigo, autores e suas respectivas afiliações e notas, se houver, data de publicação, volume, número e paginação do artigo, resumo(s), histórico, permissão de uso, palavras-chave e contagem de elementos. 

article-id (doi)
^^^^^^^^^^^^^^^^
Cada artigo deve ter um identicador único. O SciELO utiliza o padrão Digital Object Identifier (DOI), norma ISO 26324. O DOI é fornecido pela DOI Foundation.  O SciELO adota a seguinte estrutura para montagem do DOI:
- Número do provedor junto à Fundação DOI. No caso do SciELO o número é 10.1590/
- ISSN do periódico
- Ano de publicação
- Fascículo
- Página inicial do artigo
Contudo esta estrutura não é mandatória. Cada periódico pode adotar uma metodologia para construção do número de DOI, sendo que apenas os elementos referentes ao provedor e ISSN do periódico devem ser fixos. Por exemplo, após o ISSN pode-se adotar o número de registro do artigo no sistema de submissão. O importante é usar um esquema de geração do DOI que garanta que o número não se repita.
  

  .. code-block:: xml

    <article-id pub-id-type="doi">10.1590/ISSNxxxxxxxx</article-id>
     
Para ahead-of-print também inclui-se outra identificação que será utilizada para criar o link do artigo. Este identificador foi criado para evitar conflitos no link do artigo quando o mesmo for incluido em um fascículo regular. Normalmente usa-se o número de ordem do artigo no lote de envio. O conteúdo é numérico e limitado a cinco dígitos.    


  .. code-block:: xml

    <article-id pub-id-type="other">00001</article-id>

subject 
-------
Em subject classifica-se o artigo de acordo com a seção em que ele aparece no sumário do periódico. É a partir da identificação dessa informação que pode-se agrupar artigos que possuem uma mesma característica e/ou tratam do mesmo assunto. Esta classificação pode ser temática ou por tipologia. 
Por padrão adota-se para grupo de assuntos o tipo "heading" (cabeçalho) e, em assunto atribui-se a seção em que o artigo foi classificado.

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

title-group
----------- 
Title-group é utilizado para especificar o título ou um conjunto de títulos de um artigo. Nele são identificados <article-title>, <subtitle>, <alt-title> e <trans-title-group>. 

article-title
^^^^^^^^^^^^^
Article-title pode ser utilizado em duas situações: para especificar o título do artigo em si ou para especificar um título de documento(artigo, livro etc.) nas referências bibliográficas em <element-citation>. O atributo @xml:lang deve ser utilizado para especificar o idioma do título.
A marcação de título deverá seguir a estrutura abaixo:
 

  .. code-block:: xml

    <title-group>
        <article-title xml:lang="pt">título do artigo</article-title>
            <subtitle>subtítulo do artigo, se houver</article-title>
        <alt-title alt-title-type="short">título alternativo, se houver (em alguns casos o periódico adota um título curto para representar o artigo</article-title>
    </title-group>

trans-title-group
-----------------
Trans-title-group pode ser utilizado para apresentar o título ou um conjunto de títulos traduzidos de um artigo e pode conter os mesmo elementos do grupo de títulos, tais como <trans-title>, <trans-subtitle>, <alt-title>. 
Também pode ser utilizada para representar o título paralelo de um periódico em outro idioma dentro de <journal-meta>.


  .. code-block:: xml

    <title-group>
        <article-title xml:lang="pt">Título do artigo no idioma portugês</article-title>
    <trans-title-group xml:lang="en">
          <trans-title>Título traduzido para o idioma inglês, se houver</trans-title>
        </trans-title-group>
        <trans-title-group xml:lang="es">
          <trans-title>Título traduzido para o idioma es, se houver</trans-title>
     </trans-title-group>
     </title-group>
 
Freqüentemente são inseridas notas ao título que devem ser identificadas com a tag <xref ref-type="fn">. Ver item "notas de rodapé".

**Exemplo:**

 
  .. code-block:: xml

        <title-group>
        <article-title xml:lang="en">Título do artigo <xref ref-type="fn" rid="fn01">*</xref> </article-title>
    </title-group>.
    [...]
    <fn id="fn01">*</fn>


autores individuais e institucionais 
------------------------------------

contrib-group
^^^^^^^^^^^^^
Os que contribuiram (contribuintes) para a elaboração do artigo são identificados em <contrib-group> e podem ser encontradas em <front> ou <front-stub>. Os tipos de contribuintes mais frequentes são de autores, instituições e grupos de pesquisa. A tag pode ou não envolver a informação de afiliação, sendo obrigatória na identificação do contribuidor do tipo "autores" sejam institucionais ou não. Os principais elementos de <contrib-group> são: <contrib>, <xref>, <collab>, <aff>, <role> e <address>.

contrib
^^^^^^^
Em <contrib> especifica-se quem contribuiu para o artigo. Pode ser anônimo ou  ter um ou vários autores, inclusive autores institucionais. Tags como <name>, <contrib-id>, <collab>, <on-behalf-of>, <xref>, <role>, <ext-link>, <email>, <anonymous> podem ser encontradas neste elemento. Alguns atributos podem ser inseridos nesta tag. São eles:

- **@contrib-type:** utilizado para especificar o tipo do contribuinte. O tipo mais comum é "author", mas também pode ser "editor", "organizer", "illustrator", "translator" entre outros, se assim for indicado no artigo.

- **@corresp:** especifica se o autor é ou não o indicado para correspondência. Os valores para esse atributo devem ser "yes" ou "no".

  .. code-block:: xml

    <contrib contrib-type="author" corresp="yes">

- **@equal-contrib:** informa se todos os autores contribuíram igualmente para a pesquisa. Os valores para esse atributo devem ser "yes" ou "no".


  .. code-block:: xml

    <contrib contrib-type="author" equal-contrib="no">

- **@deceased:** especifica se o contribuinte faleceu quando uma parte do documento ou o documento foi publicado. Os valores para esse atributo devem ser "yes" ou "no".

  .. code-block:: xml

    <contrib contrib-type="author" deceased="yes">

**Exemplo:**

  .. code-block:: xml

    <contrib-group>
        <contrib contrib-type="author">
          <name>
          <surname>Último Sobrenome</surname>
          <given-names>Prenome</given-names>
      <prefix>Qualificadores que antecendem o nome como Prof.Dr, Dr., Capitão etc</prefix>
          <suffix>Partículas como Filho, Junior, Neto se houver</suffix>
          </name>
          <xref ref-type="aff" rid="aff1">Identificador da afiliação</xref> 
        </contrib>

**Nota:** Observar normas para nomes latinos (AACR2 - Código de Catalogação Anglo Americano e/ou Currículo Lattes dos autores, avaliar formas de entrada autorizadas)em <surname> e <given-names>.

collab
^^^^^^
Utilizado para especificar um grupo de colaboradores (autores, editores, pesquisadores, instituição, laboratório etc que atuaram como colaboradores do trabalho). Pode ser identificada em <contrib>, <element-citation>, <mixed-citation>, <person-group>, <product>, <related-article> e <related-object>. Collab possui atributos e os mais utilizados são @collab-type e @id:

- **@collab-type**: utilizado para definir o tipo de colaborador.

**Exemplo:** committee, assignee, authors, editors, compilers, guest-editors, inventors e translators.

- **@id:** identificador da tag. Esse atributo deve ter valor único no arquivo e é possível fazer link relacionado a um "rid"."    


on-behalf-of
^^^^^^^^^^^^
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

xref
^^^^
Tag de Referência Cruzada usada para relacionar e/ou fazer link com alguma informação no texto. Essa tag pode ser encontrada em: <aff>, <article-title>,  <bold>, <collab>, <comment>, <contrib>, <contrib-group>, <italic>, <license-p>, <named-content>, <on-behalf-of>, <p>, <product>, <sub>, <sup>, <td>, <term>, <term-head>, <th>, <title>, <trans-subtitle>, <trans-title> entre outros. Atributos mais frequentes para xref são:
 
- **@alt:** atributo de acessibilidade, é utilizado para descrever o conteúdo referenciado. A descrição deve ser feita no campo de valor do atributo.

**Exemplo:**
 
  .. code-block:: xml

    <xref alt="imagem de uma microfotografia" rid=" …>

- **@rid:** significa "referente ao id" e é utilizado para fazer a ligação de elementos que possuem @id no arquivo. É imprescindível que haja um "id" para cada "rid" e ambos deverão ter o mesmo valor.

**Exemplo:**
 

  .. code-block:: xml

    <xref ref-type="aff" rid="aff1">xx</xref>
         <aff id="aff1">xx</aff>
       <...>
      <p>xxxxxx<xref ref-type="birb" rid="B01">xx</xref>
       <...>
    <back>
      <ref id="B01">xx</ref>
    </back>


- **@ref-type:** especifica o tipo de referência cruzada. Os tipos mais comuns são:

  - **aff**: afiliação
  - **app**: apêndice
  - **author-notes**: notas de autor (ou relacionado a autor)
  - **bibr**: referência bibliográfica
  - **boxed-text**: caixa de texto
  - **contrib**: contribuint
  - **corresp**: autor correspondente
  - **disp-formula**: fórmula
  - **fig**: figura ou grupos de figuras
  - **fn**: nota de rodapé
  - **kwd**: palavra-chave
  - **list**: lista
  - **other**: nenhum dos tipos listados
  - **sec**: seção
  - **statement**: declaração
  - **supplementary-material**: material suplementar
  - **table**: tabela ou grupo de tabelas
  - **table-fn**: nota de rodapé de tabelas

role
^^^^
A tag "role" (rol ou papel) é usada para especificar o papel (ou função) do contribuinte do documento. Essa tag pode ser encontrada nos seguintes elementos: <collab>, <contrib>, <contrib-group>, <element-citation>, <mixed-citation>, <person-group>, <product>, <related-article>, <related-object>.
Contudo, a tag "role" aparece com maior frequência em <contrib>, <element-citation> e em <person-group>. **Exemplos:**

*Em contrib:*

  .. code-block:: xml

    <contrib contrib-type="author">
      <name>
     <surname>Último Sobrenome</surname>
     <given-names>Prenome</given-names>
     <prefix>Qualificadores que antecendem o nome como Prof., Dr., Capitão etc</prefix>
     <suffix>Partículas como Filho, Junior, Neto se houver</suffix>
   </name>
       <xref ref-type="aff" rid="aff2">identificador da afiliação</xref>
    <role>Pesquisador</role>
   </contrib>

*Em referências:*

  .. code-block:: xml

    <ref id="B01">
    <label>1</label>
    <mixed-citation>Referência conforme aparece no artigo</mixed-citation>
    <element-citation publication-type="journal">
        <person-group person-group-type="author">
            <name>
                <surname>Sobrenome</surname>
                <given-names>Nome</given-names>
            </name>
            <name>
                <surname>Sobrenome</surname>
                <given-names>Nome</given-names>
            </name>
        <role>pesquisador</role>
        </person-group>
        <article-title xml:lang="en">Título do artigo</article-title>
        <source>Periódico</source>
        <month>Mês</month>
        <year>ano</year>
        <volume>vol</volume>
        <issue>número</issue>
        <fpage>página inicial</fpage>
        <lpage>página final</lpage>        
    </element-citation>
    </ref>

Name
^^^^
A tag <name> (nome) é utilizada para especificar o nome pessoal do contribuinte e pode ser encontrada em: <contrib>, <element-citation>, <mixed-citation>, <name-alternatives>, <person-group>, <principal-award-recipient>, <principal-investigator>, <product>, <related-article>, <related-object>. Em <name> é possível inserir alguns atributos como @content-type, @id, @name-style, @specific-use, @xml:base e @xml:lang, porém os atributos mais utilizados são: @name-style e @xml:lang. Essa tag identifica prenomes, sobrenomes prefixos e sufixos.
 

- **@name-style:** atributo opcional, @name-style indica o tipo de nome, por exemplo, se ocidental ou oriental.

*Ocidental:*


  .. code-block:: xml

    <name name-style="western">
      <surname>Baker</surname>
      <given-names>John M.</given-names>
    </name>

*Oriental:*


  .. code-block:: xml

    <name name-style="eastern" xml:lang="ja-Jpan">
   <surname>園田</surname>
   <given-names>直子</given-names>
   </name>

- **@xml:lang:** atributo opcional utilizado para especificar o idioma em que o nome está escrito. Geralmente é utilizado para nomes orientais. Exmeplo:


  .. code-block:: xml

    <name name-style="eastern" xml:lang="ja-Jpan">
    <surname>園田</surname>
      <given-names>直子</given-names>
    </name>

Surname
^^^^^^^^
Esta tag pode estar inserida em <name> e também em <string-name>. É utilizada para especificar sobrenome de autores. Aqui deve ser especificado o último nome do autor. Deve-se observar as regras para identificação de sobrenome de autor de acordo com a norma bibliográfica adotada pelo periódico. A recomendação do SciELO é utilizar as Anglo-American Cataloguing Rules( AACR2).


Given-names
^^^^^^^^^^^
Given-names identifica o prenome do autor, ou seja, o primeiro nome e também o nome(s) do(s) meio(s). 

 .. code-block:: xml

   <surname>Santos</surname>
     <given-names>Ana Maria da Silva</given-names>

prefix
^^^^^^
Especifica o qualificador que precede o prenome do autor. Geralmente é utilizado quando há qualificadores como "Prof. Dr., "Dr.","Sr","Presidente", "Embaixador" etc.

suffix
^^^^^^
Especifica sufixos do nome como as partículas "Neto", "Júnior", "Jr.", "Filho", "Sobrinho" etc.


  .. code-block:: xml

    <contrib contrib-type="author">
    <name>
          <surname>Santos</surname>
          <given-names>João da Silva</given-names>
          <suffix>Neto</suffix>
    </name>


**IMPORTANTE:** para as tags que compõem <name> há uma ordem pré-estabelecida:

 
  .. code-block:: xml

    <contrib-group>    
    <contrib contrib-type="author">
         <name>
            <surname>Último Sobrenome</surname> 
            <given-names>Prenome</given-names>
        <prefix>Qualificadores que antecendem o nome como Prof. Dr., Dr., etc</prefix>
            <suffix>Partículas como Filho, Junior, Neto se houver</suffix>
         </name>
       <xref ref-type="aff" rid="aff2">identificador da afiliação</xref>
    <xref ref-type="corresp" rid="cor01">*</xref>
    </contrib>
        <contrib contrib-type="author">
          <name>
            <surname>Silva</surname>
            <given-names>José Eduardo Nogueira da</given-names>
    <prefix>Professor Doutor</prefix>
            <suffix>Sobrinho</suffix>
          </name>
    <on-behalf-of>Comissão de Ensino de Juiz de Fora</on-behalf-of>
    <xref ref-type="aff" rid="aff3">III</xref>
    </contrib>
    <contrib contrib-type="author">
            <collab>Antônio Rodrigues</collab>        
    <xref ref-type="aff" rid="aff4">IV</xref>
    </contrib>    
    </contrib-group>

Caso alguma tag esteja fora de ordem os validadores apontarão erro.

affiliation 
-----------
Considera-se como afiliação o vínculo institucional do(s) contribuinte(s) do artigo. Os dados de afiliação são importantes para localizar e mensurar a produção científica por país, estado, cidade, bem como por instituição e seus departamentos. Recomenda-se que as afiliações sejam especificadas em sua língua original, ou seja, se autor for da Espanha, por exemplo, deve-se manter a instituição em espanhol. Este elemento é composto de:
 
label
^^^^^
A tag <label>xx</label> é responsável pela identificação numérica ou alfabética que faz a ligação entre o autor e afiliação.
 
institution
^^^^^^^^^^^
<institution> especifica-se a instituição do autor, a qual pode ser dividida em até quatro níveis. Para cada nível atribui-se um tipo sendo (orgname) para o maior nível institucional e (orgdiv1) para o menor, seguindo no máximo três níveis, ou seja, podemos especificar até no máximo (orgdiv3).
 
addr-line
^^^^^^^^^
Em <addr-line>, literalmente "linha de endereço", especifica-se o estado e cidade da instituição vinculada ao autor / contribuinte. 


  .. code-block:: xml

    <addr-line>
          <named-content content-type="city">São José do Rio Preto</named-content>
          <named-content content-type="state">São Paulo</named-content>
        </addr-line>

A única informação que deverá ser especificada fora da tag <addr-line> será país. Para isso utiliza-se a tag <country>.


  .. code-block:: xml

    <country>Brasil</country>

Após identificar todos os itens acima, deve-se especificar a afiliação como a mesma estiver no artigo. Caso o email esteja presente ele deve ser marcado conforme segue:


  .. code-block:: xml

    <institution content-type="original">xxxxxx<named-content content-type="email">xxxx@xxx.xx</named-content></institution>

**Exemplo:**


  .. code-block:: xml

    <aff id="aff1">
        <label>identificador de afiliação</label>
        <institution content-type="orgdiv1">Divisão, departamento etc da instituição de afiliação</institution>
        <institution content-type="orgname">Instituição de afiliação</institution>
        <addr-line>
          <named-content content-type="city">cidade</named-content>
          <named-content content-type="state">estado</named-content>
        </addr-line>
        <country>país</country>
        <institution content-type="original">Preservação da afiliação na forma como foi incluída no artigo<named-content
            content-type="email">email, se houver</named-content></institution>
    </aff>

author-notes
------------         
Em alguns artigos existem informações extras sobre os autores(contribuintes), como correspondência, contribuição igualitária entre outros. Para especificar esses dados utiliza-se a tag <author-notes>.
Todas as notas presentes no rodapé do texto que possuem ligação direta com o(s) autor(es)também devem ser marcadas. Para consultar os tipos de nota de rodapé disponíveis, ver item "notas de rodapé".
 

  .. code-block:: xml

    <author-notes>
            <corresp>           
            <corresp id="cor01">
            <label>*</label>
                  <bold>Correspondence</bold>: Dr. xxxxxxx Departamento de xxxx, Universidade xxxxx - São Paulo,  Brasil. E-mail: <email>xxxxx@XXX.com</email>
            </corresp>
            </corresp>
            <fn fn-type="conflict">
            <p>xxxxx</p>
            </fn>
          <fn fn-type="equal">
            <p>Contribuição igualitária dos autores</p>
            </fn>
      </author-notes>


pub-date
--------
Para a marcação da data de publicação do artigo/fascículo utiliza-se a tag <pub-date> a qual pode conter os elementos <day>, <month>, <season> e obrigatoriamente <year>. Esta tag deve estar acompanhada do atributo @pub-type. 
A data de publicação pode ser do tipo "epub-ppub" se houver uma versão impressa do fascículo, apenas "epub" para publicação digital ou em ahead-of-print ou "collection" quando trata-se de um fascículo composto de artigos publicados anteriormente em ahead-of-print. 
Neste último caso, serão apresentadas duas datas de publicação, uma para designar a data de publicação do artigo em ahead-of-print e outra para indicar a data que o artigo foi movido para o fascículo ("collection").

**Exemplo de identificação de data de publicação de artigo publicado em ahead-of-print e movido para fascículo:**


  .. code-block:: xml

    <pub-date pub-type="epub">
            <day>01</day>
            <month>1</month>
            <year>2013</year>
         </pub-date>
         <pub-date pub-type="collection">            
            <month>11</month>
            <year>2013</year>
         </pub-date> 

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

**IMPORTANTE:** O único elemento obrigatório em <pub-date> é o ano. Contudo, se o periódico publicar números, a informação de mês <month>, intervalos de meses ou estações <season> devem estar presentes neste elemento.


volume e issue
--------------
Volume e issue podem ser apresentados em <front> para designar volume e número do fascículo, bem como em referências bibliográficas em <element-citation> para especificar volume e número do artigo citado no corpo do texto. 


  .. code-block:: xml

    <volume>xx</volume>
    <issue>xx</issue>

Considerando como exemplo o fascículo (v10n5) o preenchimento das tags seria:

  .. code-block:: xml

    <volume>10</volume>
    <issue>5</issue>

Caso haja suplemento de número (v10s1):


  .. code-block:: xml

    <volume>10</volume>
    <issue>suppl 1</issue>

Em caso de suplemento de número (v10n5s1):


  .. code-block:: xml

    <volume>10</volume>
    <issue>5 suppl 1</issue>  

Em caso de ahead-of-print, especificar como segue:


  .. code-block:: xml

    <volume>00</volume>
    <issue>00</issue>  

fpage/lpage
-----------
Designa-se a paginação inicial e final do artigo. No caso de ahead-of-print, a informação deve ser preenchida com zero.
 

  .. code-block:: xml

    <fpage>xx</fpage>
    <lpage>xx</lpage>



history 
-------
O histórico agrupa as datas em que o artigo foi recebido,aceito e/ou revisado. Contem obrigatoriamente as tags <date>, <day>, <month> e <year>. 
Em <date> usa-se o atributo @date-type para especificar a data de recebimento (received), aceito (accepted) e revisado (rev-recd).


  .. code-block:: xml

    <history>
        <date date-type="received">
           <day>xx</day>
           <month>xx</month>
           <year>xxx</year>
            </date>
        <date date-type="accepted">
           <day>xx</day>
           <month>xx</month>
           <year>xxxx</year>
        </date>
        <date date-type="rev-recd">
           <day>xx</day>
           <month>xx</month>
           <year>xxxx</year>
        </date>
     </history>


license 
-------
A Licença é um conjunto de condições sob as quais o conteúdo pode ser usado, acessado e distribuído. Esta informação é obrigatória e está contida em <permissions>.

@license-type
^^^^^^^^^^^^^
Especifica-se o tipo de licença adotada pelo artigo. Os mais comuns no SciELO são:"CC-BY-NC", "CC-BY", CC-BY-NC-SA e CC-BY-SA. Cada licença regula o uso, distribuição e adaptação da obra. Para mais informações consultar: http://creativecommons.org/ 

license-p
^^^^^^^^^ 
Informa-se o texto da licença adotada. 


  .. code-block:: xml

    <permissions>
    <license license-type="open-access" xlink:href="http://creativecommons.org/licenses/by/4.0/">
    <license-p>Licença adotada</license-p>
    </license>
    </permissions>

abstracts
---------
Cada artigo pode apresentar resumos em diversos idiomas. Por esta razão o atributo de idioma @xml:lang é obrigatório neste elemento.
Os resumos apresentados nos artigos publicados no SciELO normalmente apresentam-se em dois formatos: 

estruturado
^^^^^^^^^^^
quando segue a estrutura do artigo principal (Introdução, Objetivos, Métodos e Resultado). Cada grupo apresentado no resumo será identificado como seção e cada seção terá seu título. Se houver resumo traduzido, o mesmo será apresentado logo abaixo do resumo no idioma principal. Veja exemplo a seguir:
  

  .. code-block:: xml

    <abstract xml:lang="en">
    <sec>
    <title>Introduction</title>
    <p>xxxxxxx</p>
    </sec>
    <sec>
    <title>Conclusion</title>
    <p>xxxxxxx</p>
    </sec>            
    </abstract>
    <trans-abstract xml:lang="pt">
    <sec>
    <title>Introdução</title>
    <p>xxxxxxx</p>
    </sec>
    <sec>
    <title>Conclusão</title>
    <p>xxxxxxx</p>
    </sec>            
    </trans-abstract>


simples
^^^^^^^
Quando apresenta de forma sucinta os principais pontos do texto sem seguir a estrutura do artigo. Se houver resumo traduzido, o mesmo será apresentado logo abaixo do resumo no idioma principal. Veja exemplo a seguir:

  .. code-block:: xml

    <abstract xml:lang="en">
            <p>xxxxxxx</p>
         </abstract>
    <trans-abstract xml:lang="pt">
            <p>xxxxxxx, se houver</p>
         </trans-abstract>


kwd-group
--------- 
Identificadas em grupos de palavras-chave <kwd-group>, terá sempre o atributo de @xml:lang atribuído. Quando houver tradução, deve-se acrescentar um grupo para palavras traduzidas <trans-kwd-group>. Cada palavra-chave será identificada individualmente por meio da tag <kwd>.


  .. code-block:: xml

    <kwd-group xml:lang="en">
            <kwd>tendon injuries</kwd>
             <kwd>evaluation studies</kwd>
    </kwd-group>
    <trans-kwd-group xml:lang="pt">
            <kwd>traumatismos dos tendões</kwd>
            <kwd>estudos de avaliação</kwd>
    </trans-kwd-group>
    

funding-group 
-------------
Normalmente presente em "agradecimentos" <ack> ou em notas de rodapé <fn>, os dados de financiamento são especificados em <funding-group> e apresentam os dados de financiamento/apoio à pesquisa por pessoas jurídicas, ong's, oscip's (em alguns casos de pessoa física) e órgãos de fomento em geral. Esta tag só será utilizada quando houver a informação de número de contrato explicitado no artigo. 
Um artigo pode ter diversos financiadores. Cada grupo de dados de financiamento será identificado pela tag <award-group> e nela serão especificados o órgão financiador <funding-source> e o número de contrato <award-id>. O grupo de financiamento deve ser inserido logo após as palavras-chave.

Quando está presente em agradecimentos <ack> o dado de financiamento será identificado como segue:


  .. code-block:: xml

    <funding-group>            
             <award-group>
               <funding-source>Nome da instituição financiadora</funding-source>
               <award-id>número do contrato</award-id>
             </award-group>
   </funding-group>

*Em nota de rodapé <fn>:*


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
        <p>CNPQ contract 00001</p>
    </fn>
        </fn-group>
    </back>

**IMPORTANTE:** No caso da nota de rodapé com informação de financiamento, sempre mantê-la dentro de <back> em <fn-group> com o tipo @fn-type "financial-disclosure" e em <front>. Notas SEM NÚMERO DE CONTRATO, ficam apenas em <back> mas com tipo @fn-type "supported-by".

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
         
**IMPORTANTE:** Nunca insira dois ou mais números de contrato de uma mesma instituição em um único <award-group>, cada número deverá pertencer a seu próprio grupo <award-group>.

counts 
------
Na elaboração do XML alguns dados são importantes para determinar a quantidade de elementos presentes no artigo, por isso utiliza-se a tag <counts> para contabilizar o número exato de tabelas, figuras, referencias, equações e páginas presentes no arquivo.
 

  .. code-block:: xml

    <counts>
            <table-count count="número de tabelas no artigo"/>
            <ref-count count="número de referências no artigo"/>
            <fig-count count="número de figuras no artigo"/>
            <page-count count="número de equações do artigo"/>
            <page-count count="número de páginas do artigo"/>
   </counts>

Body
====
O body compreende o corpo do artigo e é estruturado normalmente com os tópicos: introdução, metodologia, desenvolvimento, discussão, recomendações, conclusão (nem todas seções são formalmente apresentadas e algumas são agrupadas ou suprimidas). 


section 
-------
Elemento usualmente presente em artigos científicos, as seções <sec> organizam o conteúdo de forma a especificar as etapas da pesquisa/trabalho e facilitar o seu entendimento. 
Os elementos mais comuns de uma seção são: <sec> neste caso usada para representar uma subseção, <p>, <title>, <fig>, <table-wrap>, <disp-formula>, <list> e <disp-quote>.
Os tipos mais comuns de seção devem ser identificados utilizando o atributo @sec-type.

- **cases:** relatos/estudos de caso
- **conclusions:** conclusões/comentários
- **discussion:** discussões
- **intro:** introdução/Sipnose
- **materials:** materiais
- **methods:** metodologia/método
- **results:** resultados
- **supplementary-material:** material suplementar

 
  .. code-block:: xml

    <sec sec-type="intro">
         <title>Introduction</title>
         <p>xxxxxxxxxxxxxxxxxx</p>
      <p>xxxxxxxxxxxxxxxxxx</p>
    </sec>

As seções podem ser combinadas:

- **materials|methods:** materiais e métodos
- **results|discussion:** discussão e resultados
- **results|discussion|conclusions:** conclusões, discussões e resultados                             

 
  .. code-block:: xml

    <sec sec-type="materials|methods">
         <title>Materials and Methods</title>
         <p>xxxxxxxxxxxxxxxxxx</p>
      <p>xxxxxxxxxxxxxxxxxx</p>
    </sec>
 

Cada seção pode ser composta por uma ou mais **subseções**, neste caso,  cada subseção deverá ser marcada com tag <sec> dentro da seção maior.


  .. code-block:: xml

    <sec sec-type="methods">
        <title>Methodology</title>
        <sec>
            <title>Methodology in Science</title>
                      <p>xxxxxxxxxxxx.</p>
          </sec>
    </sec>
      

equations 
---------
As equações podem ser apresentadas como imagem ou codificadas e serão identificadas pela tag <disp-formula> e <inline-formula>, esta última usada para que a equação seja posicionada em linha, ou seja, em meio a um parágrafo. Se a equação for capturada como imagem, deve-se incluir o nome do arquivo em <grafic>:


  .. code-block:: xml

    <p>xxxxxxxxx<xref ref-type="disp-formula" rid="e01">equação 1</xref>
    </p>
    <disp-formula id="e01">
           <graphic xlink:href="nome da equação em imagem"/>
    </disp-formula>
    

No caso de equações codificadas, deve-se observar as orientações de codificação recomendada pela W3C em linguagem MathML (http://www.w3.org/TR/MathML3/), sendo o elemento base <mml:math>. Mais informação sobre a forma de codificação consulte: http://www.ncbi.nlm.nih.gov/pmc/pmcdoc/tagging-guidelines/article/tags.html#el-math  

**Exemplo**: para codificar  σˆ2* 


  .. code-block:: xml

    <xref ref-type="disp-formula" rid="e07">Equation 7</xref>
     <inline-formula>
    <mml:math id="e07">
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

Tables 
------

Table-wrap
^^^^^^^^^^
<table-wrap> é utilizada para especificar uma tabela, incluindo labels, caption e footnotes. Essa tag pode estar inserida em: <app>, <app-group>, <body>, <boxed-text>, <disp-quote>, <fig>, <floats-group>, <glossary>, <named-content>, <notes>, <p>, <sec>, <supplementary-material> e  <table-wrap-group>. Possuem atributos opcionais utilizados principalmente para determinar a forma de apresentação da tabela, tais como:  @content-type; @orientation; @position; @specific-use; @xml:base; @xml:lang. Apenas o atributo de @id é obrigatório e deve seguir a estrutura abaixo: 

- **@id:** tabelas = "t" + o número de ordem da tabela = t01, t02... t10.

**Exemplo:**


  .. code-block:: xml

    <table-wrap id="t01">


table-wrap-foot
^^^^^^^^^^^^^^^
Em table-wrap-foot é possível fazer a identificação de nota de rodapé de tabela(<fn>). A tag <fn> deve apresentar o atributo de @id com a seguinte estrutura:

Notas de rodapé de tabelas = "tfn" + o número de ordem da nota + o número da tabela que esta sendo trabalhada = TFN01t01, TFN02t01;

A nota de rodapé poderá ser relacionado com alguma informação no corpo da tabela.


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
     <fn id="TFN01t01">
       <label>*</label>
         <p>text</p>
       </fn>
      </table-wrap-foot>
    </table-wrap>

table
^^^^^
A tabela é dividida  em cabeçalho/títulos <thead> e corpo/dados da tabela <tbody> e pode conter o atributos @style  para definir a aparência/separações da tabela, além de @border (borda), cellpadding.

São elementos de <table>:

- **col:** identifica uma coluna (possui atributos);
- **colgroup:** identifica o total de colunas da tabela (possui atributos);
- **thead:** identifica o cabeçalho;
- **tfoot:** identifica a nota de rodapé da tabela;
- **tbody:** identifica o corpo da tabela;
- **tr:** identifica uma linha da tabela.


Alguns atributos podem ser acrescentados, tais como: @border, @cellpadding, @cellspacing, @content-type, @frame, @id, @rules e @width.


**Exemplo:**

- **@border:** especifica a espessura da borda em pixels para a tabela. O valor "0" é utilizado para indicar que a tabela não possui borda e se não acrescentar o atributo @border a tabela irá apresentar uma borda de espessura padrão.
- **@cellpadding:** define uma quantidade de espaços (em pixels)entre o dado (conteúdo) e a borda de uma célula.
- **@cellspacing:** define a largura de espaços (em pixels) entre células de uma tabela.
- **@content-type:** identifica o assunto ou o tipo de conteúdo que está sendo apresentado.
- **@id**: identificador da tag. Esse atributo deve ter valor único
- **@rules** define as regras para o desenho entre linhas e colunas (all - todas as linhas e colunas, cols - apenas entre colunas, groups - entre grupos, none- nenhuma regra para a tabela, rows - apenas em linhas)
- **@width:** define a largura total da tabela em pixels.
- **@frame:** indica qual dos lados da tabela deve seguir determinada regra. 

Os valores para este atributo são:

**above:** em cima, apenas. (top)
**below:** em baixo, apenas. (bottom)
**border:** regra para a borda, (todos os lados)
**hsides:** apenas para lados horizontais (topbot)
**lhs:** apenas para o lado esquerdo
**rhs:** apenas para o lado direito
**void:** sem linha, nenhuma borda
**vsides:** regra para os lados verticais, apenas lados (sides)

**Nota:** Todos esses atributos são opcionais.

thead
^^^^^
Utilizada para apresentar o cabeçalho/título de uma tabela, pode conter alguns atributos para que a formatação fique de acordo com o PDF. Os atributos para essa tag são: @align, @char, @charoff, @content-type, @id, @style, @valign, @xml:base. Para fazer a identificação dos dados de cabeçalho deve ser utilizada as tags <tr> e <th>.

**<tr>**: A tag <tr> é utilizada para fazer a identificaçao de uma linha da tabela. Essa tag pode apresentar os seguintes atributos: align, char, charoff, content-type, id, style, valign, xml:base. <tr> faz a identificação das tags <td> e <th> onde: <td> especifica os dados da tabela em <tbody> e <th> identifica os dados da tabela em <thead>. Portanto, para cabeçalhos / títulos a estrutura deve ser a seguinte:


  .. code-block:: xml

    <thead>
     <tr>
           <th>dado</th>
           <th>dado</th>
           <th>dado</th>
     </tr>
    </thead>


**<th>**: A tag <th> possui alguns atributos, que são opcionais, tais como: @abbr, @align, @axis, @char, @charoff, @colspan, @content-type, @headers, @id, @rowspan, @scope, @style, @valign e @xml:base. Ao optar por não inserir nenhum atributo na tag <th> os dados da tabela ganham uma formatação automaticamente: os dados ficam centralizados e em negrito.

tbody
^^^^^
A tag <tbody> é utilizada para identificar do corpo da tabela. A tag <tr> em <tbody> indica a presença de uma linha. Essa tag possui alguns atributos que são opcionais: @align, @char, @caroff, @content-type, @id, @style, @valign e @xml:base.

Para a especificação de dados em <tr> para o corpo da tabela, é necessário utilizar a tag <td>. Essa tag é utilizada para identificar a células/dados que ficam no corpo da tabela. <td> possui alguns atributos que são opcionais, como: @abrr, @align, @axis, @char, @charoff, @colspan, @content-type, @headers, @id, @rowspan, @scote, @style, @valign e xml:base.

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
     <td align="center">célula<xref ref-type="table-fn" rid="TFN01t01">*</xref></td>
     <td align="center">célula</td>
     <td align="center">célula</td>
      </tr>
    </tbody>
   </table>
    <table-wrap-foot>
     <fn id="TFN01t01">
       <label>*</label>
         <p>text</p>
       </fn>
    </table-wrap-foot>
   </table-wrap>

**Nota:** as tags <thead>, <tbody>, <tr>, <th> e <td> também possuem atributos de estilo os quais podem ser consultados em:
http://jats.nlm.nih.gov/publishing/tag-library/1.0/n-2gn0.html
http://jats.nlm.nih.gov/publishing/tag-library/1.0/n-vk60.html
http://jats.nlm.nih.gov/publishing/tag-library/1.0/n-mad0.html
http://jats.nlm.nih.gov/publishing/tag-library/1.0/n-xi60.html

**Exemplo:**


  .. code-block:: xml

    <p>        
    <table-wrap id="t01">
               <label>Table 1</label>
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
                    <th style="background-color:#e5e5e5"> xxxxx</th>
                    <th style="background-color:#e5e5e5"> xxxxx</th>
                    <th style="background-color:#e5e5e5"> xxxxxx</th>
                     </tr>
                  </thead>
              <tbody>
                     <tr>
                    <td align="center"> xxxxx</td>
                    <td align="center">xxxx</td>
                    <td align="center">xxxx</td>
                     </tr>
                     <tr>
                     <td align="center"> xxxxx</td>
                     <td align="center">xxxx</td>
                     <td align="center">xxxx</td>
                     </tr>
                     <tr>
                     <td align="center"> xxxxx</td>
                     <td align="center">xxxx</td>
                     <td align="center">xxxx</td>
                     </tr>
              </tbody>
               </table>
        </table-wrap>
     </p>
           <p>xxxxxxxxxxxxxxxxxxx(<xref ref-type="table" rid="t02">Table 2</xref>).</p>
    <p>
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
                    <th style="background-color:#e5e5e5"> xxxxx</th>
                    <th style="background-color:#e5e5e5"> xxxxx</th>
                    <th style="background-color:#e5e5e5"> xxxxxx</th>
                     </tr>
               </thead>
              <tbody>
                 <tr>
                    <td align="center">xxx<xref ref-type="fn" rid="TFN01t02">(1)</xref></td>
                    <td align="center">xxxx</td>
                    <td align="center">xxxx</td>
                     </tr>
                     <tr>
                    <td align="center"> xxxxx</td>
                    <td align="center">xxxx</td>
                    <td align="center">xxxx</td>
                     </tr>
                     <tr>
                    <td align="center"> xxxxx</td>
                    <td align="center">xxxx</td>
                    <td align="center">xxxx</td>
                     </tr>
               </tbody>
               </table>
               <table-wrap-foot>
               <fn id="TFN01t02">
              <label>(1)</label> <!-- o label pode fazer relação com algum símbolo dentro da tabela, que será identificado com xref do tipo "fn" com rid seguindo o da sua nota correspondente (TFN01t02) -->
              <p> xxxxxx</p>
               </fn>
               </table-wrap-foot>
            </table-wrap></p>

supplement material 
--------------------
O material suplementar é um documento que não faz parte do texto do artigo, mas que serviu como apoio para sua elaboração.
Em <supplementary-material> é possível especificar tabelas, figuras, dados brutos de planilha, banco de dados de genomas, quiz, equações, links, URLs, diálogos, financiamento (statement), listas, licenças e objetos multimídia como áudio, vídeo e filme.
O material suplementar pode estar em dois blocos: em **front**, dentro de <article-meta> e em **body** como seção ou entre parágrafos. O <supplementary-material> só poderá ser identificado em <back> caso esteja identificado dentro do grupo de apêndices <app-group> ou do apêndice <app>.
Seus atributos mais frequentes são:

- **@content-type:** indica-se o tipo de conteúdo que será apresentado como material suplementar. 

**Exemplo:**

  .. code-block:: xml

    <supplementary-material content-type="gene">

- **@id:** utilizado como um identificador único no documento e ganha maior importância quando há mais que um material suplementar e/ou quando o material suplementar é referenciado no corpo do texto. Nesse caso é necessário relacionar a chamada no texto com o "id" do material suplementar.
- **@mime-type:** utilizado para especificar o tipo de mídia como "vídeo" ou "aplicação".
- **@mime-subtype:** utilizado para especificar o formato da mídia.

**Exemplo:**

  .. code-block:: xml

    <supplementary-material xlink:href="nomedoarquivo.mp3" **mime-subtype="mp3"** mimetype="video">

- **@xlink:href:** utilizado para indicar do nome completo do arquivo, tais como: pdf, vídeo, zip etc.

- **@position:** utilizado quando é necessário indicar a posição de tabelas e figuras no documento. Para isso é atribuído os seguintes valores:

  - **float:** a tabela/figura não está fixa, pode abrir em qualquer parte do texto e fora dele.
  - **anchor:** Tab e Fig devem ser apresentadas na posição em que está indicada no texto, não podendo ser removida.
  - **background:** com o valor "background" a imagem deve ser apresentada como plano de fundo no texto.
  - **margin:** indica que imagem deve estar na margem do documento.


- **@xml:lang:** usado para indicar o idioma do material suplementar apresentado. Os valores mais frequentes para esse documento são: "en" (inglês), "pt" (português), "es" (espanhol).

**Exemplo de material suplementar em <front>:**

(Após paginação indicar o material suplementar.)


  .. code-block:: xml

    <fpage>xx</fpage>
   <lpagexx</lpage>
    <supplementary-material mime-type="application" mime-sub-type="pdf" xlink:href="nomedoarquivo.pdf"/>

**Exemplo de material suplementar em <body>:**

(Em qualquer parte do corpo do texto)


  .. code-block:: xml

    <p>xxxx</p>
    <supplementary-material id="suppl01">
       <label>Fig 1.</label>
          <caption>
             <p>descrição da figura</p>
          </caption>
       <graphic mimetype="image" xlink:href="nomedoarquivo.tif"/>
    </supplementary-material>
    <p>xxxxxxxxxx<xref ref-type="supplementary-material" rid="sp01">Material Suplementar</xref>xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx</p>


.. note::

  xref do tipo "supplementary-material" é utilizado para fazer link com a informação de material suplementar no artigo.


disp-quote 
----------
Quando há no texto uma citação de outra fonte utiliza-se a tag <disp-quote>. Geralmente essa informação é apresentada com algum recuo, possui mais de três linhas e fonte de tamanho diferente, tendo essa informação já destacada a identificação deve ser:

**Exemplo:**


  .. code-block:: xml

     <p>xxxx</p>
        <disp-quote>
                 <p>"Sed luctus quam a felis sagittis lacinia. Etiam auctor tincidunt nibh, sit amet convallis urna convallis nec. Nullam venenatis dapibus dapibus. Vivamus et arcu blandit, laoreet tellus eget, sodales sapien. Etiam fringilla turpis enim, sit amet porta velit faucibus eu."</p>
          </disp-quote>
     <p>xxxx</p>

A tag <disp-quote> também é utilizada para epígrafes, citações em blocos e extratos dentro do texto.

**Exemplo:**


  .. code-block:: xml

    <p>xxxx</p>
        <disp-quote>
            <preformat>On the night of the day on which this cruel deed was done, I was aroused from sleep by the cry of fire. The curtains of my bed were in flames. The whole house was blazing. It was with great difficulty that my wife, a servant, and myself, made our escape from the conflagration. The destruction was complete. My entire worldly wealth was swallowed up, and I resigned myself thenceforward to despair.</preformat>
          <attrib>Edgar Allan Poe, The Black Cat</attrib>
        </disp-quote>
     <p>xxxxx</p>

A tag <disp-quote> pode ser inserida em: <app>, <app-group>, <bio>, <body>, <boxed-text>, <disp-quote>, <fig>, <glossary>, <license-p>, <named-content>, <notes>, <p>, <ref-list>, <sec>, <styled-content>, <supplementary-material>, <table-wrap>

ext-link 
--------
Utilizada para especificar URLs, links ativos. Ao fazer a identificação da URL com <ext-link>, o link abrirá em uma nova aba. 

**Exemplo:**


  .. code-block:: xml

    <p>xxx <ext-link ext-link-type="uri" xlink:href="http://www.scielo.org">www.scielo.org</ext-link> xxxxx</p>

**IMPORTANTE:** O prefixo "http://" deve estar sempre presente. Caso não venha no texto se deve acrescentar dentro da tag de ext-link, para assegurar que o link funcione corretamente.

list 
----
Para uma sequência de dois ou mais itens, possuindo ou não uma determinada ordenação, usa-se a tag <list>. 

**@list-type:** indica o tipo de lista apresentada. Abaixo as mais comuns:

  - **order:** lista ordenada, cujo prefixo utilizado é um número;
  - **bullet:**     lista com marcadores, prefixo utilizado é um ícone de "bola";
  - **alpha-lower:** lista ordenada, cujo prefixo é um caractere alfabético minúsculo;
  - **alpha-upper:** lista ordenada, cujo prefixo é um caractere alfabético maiúsculo;
  - **roman-lower:** lista ordenada, cujo prefixo é um numeral romano minúsculo;
  - **roman-upper:** lista ordenada, cujo prefixo é um numeral romano maiúsculo;
  - **simple: simples ou lista simples, sem prefixo antes de cada item ou com um traço.

**@prefix-word:** palavra ou frase a ser adicionada ao início de cada item em uma lista, por exemplo, "Step", "Procedure", etc.

A tag <list-item> e a tag <p> sãou tilizadas para cada item na lista de itens, dentro da tag <list list-type="xxx">.

Obs: Se a lista possuir um título, poderá ter uma tag <title> ou <label> antes de <list-item>.

**Exemplo:**


  .. code-block:: xml

    <p>
    <list list-type="bullet">
    <list-item>
    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit.</p>
    </list-item>
    <list-item>
    <p>Curabitur pretium magna quis metus malesuada, at sodales tortor sagittis.</p>
    </list-item>
    <list-item>
    <p>Nam interdum tellus nec nulla posuere, a iaculis eros tempor.</p>
    </list-item>
    </list>
   </p>

Figuras 
-------
As figuras de um artigo são identificadas por meio da tag <fig>. Com essa tag é possível especificar label, caption, graphic, links, listas, diálogo, citações e objetos multimídia como vídeo, áudio e filme.

As imagens podem ter ou não legendas. Para imagens sem legendas é necessário marcá-la como <fig> e identificá-la com a tag <graphic>.


**Exemplo:**

  .. code-block:: xml

    <fig id="f01">
       <graphic xlink:href="nomedaimagem.tif"/>
     </fig>

A tag <graphic> é utilizada para idenfiticar alguns tipos de arquivos. Seus atributos mais frequentes são:


- **@xlink:href:** utilizado para especificar um endereço ou links externos. Portanto o @xlink:href deve conter nomes de imagens/arquivos e também o nome completo de uma URL.

- **@mimetype:** utilizado para especificar o tipo de mídia como "vídeo" ou "aplicação".

- **@mime-subtype:** utilizado para especificar o formato da mídia.

**Exemplo:**


  .. code-block:: xml

    <graphic xlink:href="nomedoarquivo.avi" **mime-subtype="avi"** mimetype="video"/>

Para figuras com legendas a marcação deve envolver toda a informação de imagem, inclusive sua descrição, com a tag <fig>. Dentro de <fig> serão identificados o rótulo da figura <label> e sua descrição através da tag <caption>.

**Exemplo:**


  .. code-block:: xml

    <fig id="f01">
   <label>Fig. 1</label>
     <caption>Aqui é identificada a descrição/legenda da imagem</caption>
     <graphic xlink:href="nomedaimagem"/>
    </fig>

Essa tag pode ter os seguintes atributos: @fig-type, @id, @orientatoin, @position, @xml:lang, @xml:base, @specific-use. Os atributos mais frequentes são:


- **@fig-type:** utilizado para especificar o tipo de imagem. Os tipos podem ser muitos como: Graphic, Cartoon, Chart, Diagram, Drawing, Exihibit, Illustration, Map etc. Contudo o tipo só será definido caso o label da figura apresente um tipo diferente de "fig." "figure". 
**Exemplo:**


  .. code-block:: xml

    <figfig-type="map" id="f01">
      <label>Map 1</label>
        <caption>
           <p>xxxx</p>
        </caption>

Se a figura apresentar o label como "fig." ou "figure" atribuir o valor "other" para fig-type, ou não especificar o type.

**Exemplo:**


  .. code-block:: xml

    <figfig-type="other" id="f01">
      <label>Fig 1</label>
        <caption>
             <p>xxxx</p>
        </caption>
ou


  .. code-block:: xml

    <fig id="f01">
      <label>Fig 1</label>
        <caption>
             <p>xxxx</p>
        </caption>

- **@id:** identificador da tag. É possível fazer referência cruzada no documento; esse atributo deve ter valor único no arquivo e é possível fazer link relacionado a um "rid". 
Para composição do "ID" de **figuras** utiliza-se o seguinte padrão:
"f" + o número de ordem da figura –

**Exemplo:** f01... f10, f11;


  .. code-block:: xml

    <fig id="f01">
         <label>FIGURE 1</label>
               <caption>
               <title>Título da figura</title>
               </caption>
           <graphic xlink:href="xxxx-xxxx-acronimo-vol-nº-pag-gf01"/>
    </fig>

Media 
-----
A tag <media> é utilizada para especificar arquivos multimídia como vídeo, áudio, filmes, animações etc.
Essa tag possui os seguintes atributos: @content-type, @id, @mime-subtype, @mimetype, @orientation, @position, @specific-use, @xlink:actuate, @xlink:href, @xlink:role, @xlink:show, @xlink:title, @xmlns:xlink, @xml:base, @xml:lang. Os atributos mais frequentes são:

- **@content-type:** define-se o tipo de conteúdo que será apresentado em <media>.

**Exemplo:**


  .. code-block:: xml

    <media content-type="video">


- **@id:** identificador da tag. Esse atributo deve ter valor único no arquivo e é possível fazer link relacionado a um "rid".


- **@mime-subtype:** utilizado para especificar o formato de mídia apresentado.

**Exemplo:**


  .. code-block:: xml

    <media mimetype="video"  **mime-subtype="mp4"** xlink:href="nomedoarquivo.mp4"/>


- **@mimetype:** utilizado para especificar o tipo de mídia como "vídeo" ou "aplicação".

**Exemplo:**


  .. code-block:: xml

    <media **mimetype="video"** mime-subtype="mp4" xlink:href="nomedoarquivo.mp4"/>


- **@position: ** utilizado quando é necessário especificar a posição de tabelas e figuras no documento. Para isso é atribuído os seguintes valores:

  - **float:** a tabela/figura não está fixa, pode abrir em qualquer parte do texto e fora dele.
  - **anchor:** Tab e Fig devem ser apresentadas na posição em que está indicada no texto, não podendo ser removida.
  - **background:** com o valor "background" a imagem deve ser apresentada como plano de fundo no texto.
  - **margin::** indica que imagem deve estar na margem do documento.


- **@xlink:href:** indica a direção de um arquivo multimídia.

**Exemplo:**


  .. code-block:: xml

    <media mimetype="video"  mime-subtype="mp4" xlink:href="nomedoarquivo.mp4"/>

A tag <media> pode ser encontrada em: <app>, <app-group>, <body>, <boxed-text>, <disp-formula>, <disp-quote>, <fig>, <fig-group>, <floats-group>, <p>, <sec>, <supplementary-material> etc. Contudo, <media> aparece com frequência entre parágrafos, em material suplementar e em figuras.


**Exemplo:**

*Em parágrafo:*


  .. code-block:: xml

    <p>text <media mimetype="video"  mime-subtype="mp4" xlink:href="nomedoarquivo.mp4"/> text</p>

*Em figuras:*


  .. code-block:: xml

    <fig id="f01">
        <label>Figure 1</label>
      <caption>descrição da fig.</caption>
    <alternatives>
    <media xlink:href="nomedoarquivo.avi" mimetype="video" mime-subtype="avi"/>
        </alternatives>
    </fig>

*Em material suplementar:*


  .. code-block:: xml

    <sec sec-type="supplementary-material">
   <title>Supplementary Material</title>
   <supplementary-material id="sm1">
     <caption>
      <title>legenda</title>
     </caption>
   <media mimetype="application" mime-subtype="pdf" xlink:href="nomedoarquivo.pdf"/>
    </supplementary-material>

Nesse último exemplo, o material suplementar pode estar dentro de uma seção do tipo material suplementar ou entre parágrafos.


  .. code-block:: xml

    <sec>
    <p>xxxx</p>
    </sec>
       <sec sec-type="conclusions">
          <title>Conclusion</title>
             <p>xxxx</p>
        <media xlink:href="nome do arquivo de video.extensãoi" mimetype="video" mime-subtype="informação da extensão ex.: mp3, avi etc."/>
        <p>xxxxx <xref ref-type="app" rid="app01">Appendix 1</xref> <!-- Link (xref) com apêndice em back --></p>
         <p>xxxx</p>
       <fig id="f01">
        <label>Figure 1</label>
        <caption>
        <p>xxxxxx</p>        
        </caption>
        <media xlink:href="nome do arquivo de video.extensãoi" mimetype="video" mime-subtype="informação da extensão ex.: mp3, avi etc."/>
        <graphic xlink:href="xxxx-xxxx-acronimo-vol-nº-pag-gf02"/>
         </fig>
         <!-- acima, exemplo de vídeo em figura -->
          </sec>
         <sec sec-type="conclusions">
             <title>Final remarks</title>
             <p>xxxx <xref ref-type="sec" rid="sec01">Supplementary material</xref> xxxx.</p>
          </sec>
          <sec sec-type="supplementary-material" id="sp01"> <!-- Material suplementar também pode estar em <back> dentro de <app-group> a sequência do pdf deve ser respeitada. Verificar as estruturas: http://jats.nlm.nih.gov/publishing/tag-library/1.1d1/n-cr42.html; http://jats.nlm.nih.gov/publishing/tag-library/1.1d1/n-ed42.html -->
            <title>Material Suplementar</title>
            <p>......................</p>
        <!-- Em material suplementar há algumas possibilidades: pode ser identificado uma imagem com a tag <fig>, ou uma tabela em imagem, pode ser identificado em um link externo, utilizando a tag <ext-link>, pode ser uma tabela codificada ou apenas um texto -->
        </sec>
        </body>

Back
====
O back é a parte final do texto que compreende referências bibliográficas e demais dados referentes  pesquisa como: nota de autor, nota de rodapé, agradecimentos (com indicação ou não de agência financiadora), referências bibliográficas, link para apêndice/material complementar/anexos e outros dados que o autor considera relevantes mencionar.

ack
----
A seção de agradecimentos (acknowledgment) quando aparece no artigo deve ser marcada em <back>.

É nesta seção que frequentemente os dados financiamento da pesquisa são indicados, como descrito anteriormente em <funding-group> em <front>.

Todo o conteúdo de agradecimentos deverá ser identificado com a tag <ack>, caso haja o título "Agradecimentos" ou "Acknowledgment" identifique-o com a tag <title>. Em <ack> é possível especificar um ou mais parágrafos <p>, dependendo da estrutura do texto.

**Exemplo:**

 
  .. code-block:: xml

    <back>
      <ack>
        <title>Agradecimentos</title>
           <p>Texto de agradecimentos, pode ou não conter dados de financiamento</p> 
      </ack>

(ver tag <funding-group> em <front>)

IMPORTANTE: Não é necessário a identificação da seção de agradecimentos com a tag <sec>, pois a própria tag de <ack> já representa a seção com o título "acknowledgment" ou "Agradecimentos". 
  
ref-list
--------
Existem diversos tipos de referências e normas para apresentá-las num documento textual (ABNT, Vancouver, APA, dentre outras). Independente da norma usada, a representação dos elementos essenciais em xml de uma referência devem ser identificados corretamente para a carga na base de dados bibliométrica.

**IMPORTANTE:** Deve-se levar em consideração que muitas vezes as referências são contruídas de forma incorreta, o que dificulta a marcação de seus elementos, nesse caso não se deve acrescentar dados no texto marcado.

A estrutura geral que abarca a lista de referências deve conter quatro tags principais; a tag da lista geral de referências <ref-list>, a tag da própria referência a ser apresentada <ref> mais seu atributo identificador @id, a tag com a referência no todo sem marcação <mixed-citation> e por fim a tag que irá especificar em seu interior todos os elementos disposto nas referências <element-citation> mais o atributo do tipo de publicação @publication-type. Porém, nem sempre existirá os dados de título <title> e de etiqueta <label>, pois pode se tratar de referências do sistema autor-data (entrada pelo sobrenome no autor no texto) e não pelo sistema numérico que depende de um label/etiqueta para criar um link entre referência no texto e lista de referência <xref>. **Exemplo das tags essenciais para referências:**


  .. code-block:: xml

    <ref-list> 
         <title>References</title>
       <ref id="B00">
            <label>00</label>
             <mixed-citation>Referência no todo conforme aparece no artigo sem marcação</mixed-citation>
            <element-citation publication-type="????"> 
        marcação/tagueamento de todos os elementos da referência na sequência que aparece no documento original    
            </element-citation>
       </ref>
    <ref-list>

- **@publication-type:** indica o tipo de referência citada. As mais comuns são:

  - **journal:** utilizada para referenciar publicações seriadas, editadas em unidades sucessivas, com designações numéricas e/ou cronológicas e destinada a ser continuada indefinidamente.   
  - **book:** utilizada para referenciar monografia/livro. Pode também representar somente uma parte ou capítulo de um livro.
  - **webpage:** utilizada para referencias um relatório técnico,  normalmente de autoria institucional.
  - **thesis:** utilizada para referenciar trabalho de finais de curso para obtenção de um grau acadêmico, tais como livre-docência, doutorado, mestrado, bacharelado, licenciatura, etc.
  - **confproc (evento):** utilizada para referenciar documentos relacionados com eventos científicos: atas, anais, resultados, proceedings, convenção, conferência entre outras denominações.
  - **patent:** utilizada para referenciar patentes. 
  - **software:** utilizada para referenciar um software que pode estar em vários suportes, como CDs, DVDs, em suporte online, dispositivos usb e etc. 
  - **database:** utilizada para referenciar bases de dados.


**IMPORTANTE:**

- Nunca manter uma informação toda com formatação <italic>, <bold> etc, dentro de alguma tag. (mais informação sobre a regra: http://www.ncbi.nlm.nih.gov/pmc/pmcdoc/tagging-guidelines/article/genprac.html#formatting);
- Especificar na marcação os elementos de uma referência na sequência que aparece no documento original;
- Todas as referências devem conter informação de fonte principal <source>;
- Evitar pontuação dentro da marcação em element-citation (ponto final, vírgula etc);
- O uso da tag <comment> só será permitido quando não houver tag coerente para alguma informação.

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
                         <given-names>Nome</given-names>
                  </name>
                  <name>
                         <surname>Sobrenome</surname>
                         <given-names>Nome</given-names>
                  </name>
                </person-group>
               <article-title xml:lang="en">Título do artigo</article-title>
               <source>Nome do Periódico</source>
                   <month>Mês</month>
                   <year>ano</year>
                   <volume>volume</volume>
                  <issue>número</issue>
                   <fpage>página inicial</fpage>
                   <lpage>página final</lpage>        
      <article-id pub-id-type="pmid">somente números</article-id>
      <article-id pub-id-type="pcmid">somente números</article-id>
      <article-id pub-id-type="doi">somente números</article-id>
      <article-id pub-id-type="pii">somente números</article-id>
     <elocation-id>representa um número de página eletrônica</elocation-id>
       </element-citation>
   </ref>

*Para book:*


  .. code-block:: xml

    <ref id="B02">
            <label>2</label>
            <mixed-citation>Referência conforme aparece no artigo</mixed-citation>    
          <element-citation publication-type="book"> 
             <name>
                    <surname>Sobrenome</surname>
                  <given-names>Nome</given-names>
             </name>
              <source>Nome do Livro</source>
              <edition>edição (inserir informação ed. ou th. e etc conforme no pdf)</edition>
              <publisher-loc>Lugar de publicação do livro (cidade, estado, país e etc)</publisher-loc>
              <publisher-name>Nome da editora/Casa publicadora</publisher-name>
             <year>Ano de publicação da obra</year>
        <size units="page">quantidade total de páginas do livro</size>
        </element-citation>
    </ref>

*Para chapter-title (capítulo de livro):*


  .. code-block:: xml

    <ref id="B03">
            <label>3</label>
            <mixed-citation>Referência conforme aparece no artigo</mixed-citation>
    <element-citation publication-type="book"> 
              <name>
                   <surname>Sobrenome</surname>
                    <given-names>Nome</given-names>
              </name>
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

**IMPORTANTE:** A tag <comment> só deverá ser incluída quando na referência completa aparecer o texto: *Disponível em:* ou *Available from:* ou outra  informação similar.

*Para report:*

 
  .. code-block:: xml

    <ref id="B05">
            <label>5</label>
            <mixed-citation>Referência conforme aparece no artigo</mixed-citation>
    <element-citation publication-type="report"> 
    <collab>Nome da instituição organizadora</collab>
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
                   <given-names>nome</given-names>
               </name>
                <name>
                   <surname>sobrenome</surname>
                   <given-names>nome</given-names>
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
              <name>
                    <surname>sobrenome</surname>
                    <given-names>nome</given-names>
              </name>
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
                     <given-names>nome</given-names>
                   </name>
             </person-group>
              <collab>autor institucional (se houver)</collab>
             <article-title>título do documento de patente</article-title>
        <source>identificado o nome do país autorizou a patente. Ex.: United States patent</source>
        <patent country="inserir a informação padronizada do país , ex.:"US" = United States">US Número da Patente</patent>
             <year>ano do documento da patente</year>
              <month>mês (se houver)</month>
            <day>dia (se houver)</day>
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
                        <given-names>nome</given-names>
                     </name>
                    <name>
                             <surname>sobrenome</surname>
                        <given-names>nome</given-names>
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


foot-note
---------
Nota de rodapé (foot note) <fn>, como o nome indica, é uma anotação colocada ao pé de uma página do documento, adicionando comentário de referência, fonte, ou ambos, para parte do texto da matéria na mesma página. Para o xml é possível que uma nota seja somente informativa e não necessariamente tenha alguma referência <xref> no texto (não é muito comum), nesse âmbito também não é necessário utilizar as notas abaixo de sua página já que um documento digital não possui paginação padrão e normalizada como materiais impressos, devendo as notas ficarem sempre ao final do documento.

As notas que devem ser consideradas para entrar como nota de rodapé de <back>, são quaisquer notas que NÃO fazem nenhum tipo de referência aos **autores**, as quais deverão ser identificadas em <author-notes>.

A construção geral das notas de rodapé de back estão sempre representadas por duas tags importantes, a de grupo de notas de rodapé <fn-group> e a tag da própria nota <fn> a qual possuem os atributos @fn-type e @id, esta última deve ser única para cada nota. Dentro da tag <fn> ainda podemos ter uma etiqueta <label> cuja marcação  não é parte obrigatória  (deverá aparecer se no artigo original / pdf aparecer a informação, que pode ser um caracter ou numeral) e depois o(s) parágrafo(s) <p> com o texto referente a descrição da nota. 
**Exemplo:**


  .. code-block:: xml

    <fn-group> 
       <fn fn-type="???" id="fn01">
     <label>*</label>
             <p>Texto...</p>
       </fn>
    </fn-group>


É possível ter quantas notas forem necessárias dentro de uma única tag de grupo de notas <fn-group>.

**Exemplo:**

 
  .. code-block:: xml

    <fn-group> 
       <fn fn-type="???" id="fn01">
     <label>1</label>
             <p>Texto...</p>
       </fn>
       <fn fn-type="???" id="fn02">
     <label>**</label>
             <p>Texto...</p>
       </fn>
    </fn-group>

Também é possível ver notas de rodapé mais simples sem etiqueta <label> ou identificação @id ou ambos.

**Exemplo:**

 
  .. code-block:: xml

    <fn-group> 
       <fn fn-type="???">    
             <p>Texto...</p>
       </fn>
    </fn-group>

Os tipos mais comuns de <fn> são:

- **abbr:** representa abreviaturas de termos e nomes próprios utilizadas ao longo do texto. Caso esteja falando de abreviaturas de nomes dos autores, inserir nota em <author-notes> em <front>.
- **com:** representa nota de algum tipo de comunicado relevante para a realização do artigo.
- **financial-disclosure:** declaração de financiamento ou negação e aceitação de recursos recebidos em apoio à pesquisa em que um artigo é baseado. Normalmente serve para informações de financiamento que possuem um número de contrato ou que só informam se "SIM" ou "N O" houve financiamento.
- **supported-by:** indica que a pesquisa sobre a qual o artigo é baseado foi apoiada por alguma entidade, instituição ou pessoa física. Considerar também informação de financiamento que NÃO possuem números de contrato.
- **presented-at:** indica que o artigo foi apresentado em algum evento científico.
- **supplementary-material:** indica ou descreve o material suplementar do artigo.
- **other:** especifica aquelas notas diferentes das relacionados acim. É possível também ter este tipo de nota em <author-notes> em <front>.

Para mais detalhes sobre as tipologias, consultar link: http://jats.nlm.nih.gov/publishing/tag-library/1.1d1/index.html

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

app
---
Utilizado para indicar a presença de um apêndice ao documento. Para a marcação básica de um apêndice devemos levar em consideração duas tags importantes, a de grupo de apêndice <app-group> e de apêndice propriamente dito <app>; ambas podem possuir o atributo @id, porém não é obrigatório. Também deve ser inserido uma informação de título <title> ou etiqueta <label> ou ambas quando necessário.

**Exemplo de Apêndice com texto:**


  .. code-block:: xml

    <app-group>
    <app>
            <title>Appendix</title> 
        <p>Texto do apêndice...</p>
    </app>
    </app-group>



**Exemplo de Apêndice com imagem (Pode ser imagem de figura, tabela, quadro, equação e etc:**


  .. code-block:: xml

    <app-group>
     <app id="app01">                
         <label>Appendix 1</label>
            <title>Questionnaire for SciELO</title>    
          <graphic xlink:href="xxxx-xxxx-acronimo-vol-nº-pag-app01"/>         
     </app>
    </app-group>

**Exemplo de Apêndice com link externo:**

 
  .. code-block:: xml

    <app-group>
      <app>                
         <title>Appendix 1</title>
           <p>Para mais informações <ext-link ext-link-type="uri" xlink:href="http://www.scielo.org">clique aqui</ext-link> para verificar o pdf.</p>                   
      </app>
    </app-group>

**IMPORTANTE:** Para a criação de link externo o editor do periódico que deve providenciar a inserção de seu material suplementar/apêndice/anexo numa url.

**Exemplo de Apêndice com tabela:**


  .. code-block:: xml

    <app-group>
    <app id="app01">
        <title>Appendix</title>            
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

**Exemplo de Apêndice misto (figura mais tabela) com dois "ids" individuais:**


  .. code-block:: xml

    <app-group>
    <app id="app01">                
         <label>Appendix 1</label>
            <title>Questionnaire for SciELO</title>    
          <graphic xlink:href="xxxx-xxxx-acronimo-vol-nº-app01"/>         
    </app>
    <app id="app02">        
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

**Exemplo de Apêndice misto (texto mais figura) com um "id" de referência ao grupo:**


  .. code-block:: xml

    <app-group id="app01">
      <app>                
            <label>Appendix 1</label>
           <title>Questionnaire for student inclusion</title>    
          <graphic xlink:href="xxxx-xxxx-acronimo-vol-nº-pag-app01"/>
          <p>Texto do apêndice e/ou exmplicativo da imagem</p>         
      </app>
    </app-group>

**Exemplo de Apêndice com vídeo:**
 
  .. code-block:: xml

    <app-group id="S01">
            <caption>
                <title>suplemento eletrônico</title>
            </caption>
            <supplementary-material>
            <media xlink:href="xxxx-xxxx-acronimo-vol-nº-suppl01.avi" mimetype="video" mime-subtype="avi"/>
            </supplementary-material>
    </app-group>

**IMPORTANTE:** Neste caso desconsiderar tag <app> e inserir tag <supplementary-material>, conforme exemplo.

Ainda é possível encontrar o material suplementar inserido em notas (footnote), neste caso também é possível especificá-lo em <back>, dentro da tag <app-group>. Veja o link de estruturas: http://jats.nlm.nih.gov/publishing/tag-library/1.1d1/n-cr42.html


glossary 
--------
Utilizada quando há uma lista de termos e respectivas  definições. O glossário pode ser apresentado como imagem ou como texto com as identificações de <term>, <def-list> e <def>. O glossário pode estar identificado em: app, back, bio, boxed-text, glossary, notes e sec. Frequentemente o glossário aparece em <app> e em <back>.


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
          <graphic xlink:href="nomedoarquivo.tif"/>
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
       <ref-list>
    </back>

**Nota:** regra de atribuição de @id para Afiliações, Notas, Tabelas, Notas de Tabela, Figuras e Equações. 
Para a composição do @id para os elementos que demandam esse atributo, combine uma raiz com uma numeração sequencial, como segue:

- **Afiliações, raiz "aff":** aff01, aff02,....;
- **Equações, raiz "e":** e01, e02, ….;
- **Figuras, raiz "f":** f01,f02, ….;
- **Tabelas, raiz "t"**: t01, t02..;
- **Notas de rodapé de tabelas, raiz "tfn":** tfn01, tfn02, ...;
- **Notas de rodapé do artigo, raiz "fn":** fn01, fn02…;
- **Glossário, raiz "d":** d01, d02, ...;

Referências bibliográficas:
==========================
ASSOCIAÇÃO BRASILEIRA DE NORMAS TÉCNICAS. NBR14724: informação e 
documentação: trabalhos acadêmicos: apresentação. Rio de Janeiro, 2011. 

ASSOCIAÇÃO BRASILEIRA DE NORMAS TÉCNICAS. NBR 6023: informação e 
documentação: referências: elaboração. Rio de Janeiro, 2002. 

JATS standard (ANSI/NISO Z39.96-2012). http://jats.niso.org .
JATS supporting documentation http://jats​.nlm.nih.gov.
http://pt.wikipedia.org/wiki/Patente

http://pt.wikipedia.org/wiki/Notas_de_rodap%C3%A9

http://www.ncbi.nlm.nih.gov/pmc/pmcdoc/tagging-guidelines/article/genprac.html#formatting

http://dtd.nlm.nih.gov/publishing/tag-library/3.0/index.html

http://www.ebah.com.br/content/ABAAAALS0AG/metodologia-trabalho-cientifico?part=21



