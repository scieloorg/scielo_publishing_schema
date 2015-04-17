SciELO Publishing Schema - Guia de uso dos elementos e atributos para documentos em XML
=======================================================================================
 
Versão |version| - março de 2015 (previsão).

.. warning:: Esta é uma versão em desenvolvimento e não deve ser utilizada como 
             referência para a produção de documentos em XML. 


Versões anteriores:

* `Versão 1.1 <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/1.1-branch/>`_.
* `Versão 1.0 <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/1.0-branch/>`_.


Introdução
----------

Este guia de uso descreve o estilo de marcação adotado pelo projeto SciELO para
a submissão de documentos no formato XML. 

A especificação :term:`SciELO Publishing Schema` — também chamada :term:`SciELO PS` — é composta 
pela especificação `NISO JATS Journal Publishing DTD <http://jats.nlm.nih.gov/publishing/>`_ 
na versão 1.0 mais o :term:`Estilo SciELO`, que são regras que especializam aspectos da 
especificação :term:`JATS Publishing`. Os usuários deste guia devem possuir conhecimentos 
prévios sobre :term:`XML` e familiaridade com :term:`DTD`.

Por motivos de compatibilidade com a última versão das recomendações disponibilizadas 
pelo SciELO, a especificação `NLM Journal Publishing DTD <http://dtd.nlm.nih.gov/publishing/>`_ 
na versão 3.0 ainda será suportada nesta versão do guia de uso, assim como pelas 
ferramentas disponibilizadas.

As dúvidas e comentários sobre a especificação :term:`SciELO PS`, sobre este guia 
de uso ou sobre as ferramentas disponibilizadas pelo SciELO para apoiar a marcação 
em :term:`XML` são tratadas na lista de discussão 
`scielo-xml <http://groups.google.com/group/scielo-xml/>`_.


Notas da versão
---------------

Novas versões serão disponibilizadas em um calendário fixo, a cada seis meses. 
Versões de correção serão disponibilizadas sob demanda, e serão identificadas 
no terceiro dígito identificador da versão. e.g.: versão *1.1.1*.

Duas versões são suportadas simultaneamente, a mais recente e a imediatamente
anterior. Essa medida garante um ciclo de vida de 1 ano para cada versão. Por
**suportar** entenda manter a documentação, ferramentas de apoio, ingresso no 
processo de submissão e comunidade de usuários.


.. toctree::
   :maxdepth: 1

   whatsnew-1.1


Ferramentas de apoio
--------------------

Algumas ferramentas são disponibilizadas e mantidas pelo SciELO, seguindo o modelo 
:term:`open-source`, para apoiar o processo de marcação dos documentos no 
formato XML. 

* `Markup <http://docs.scielo.org/projects/scielo-pc-programs/en/latest/markup.html>`_: 
  Macro para Microsoft Word que apoia o processo de marcação de documentos, 
  de acordo com a `DTD PMC <http://dtd.nlm.nih.gov/publishing/3.0/>`_.
* `Stylechecker <http://manager.scielo.org/tools/validators/stylechecker/>`_: 
  Ferramenta baseada na web que apresenta relatório detalhado sobre a 
  conformidade de um dado XML em relação à especificação :term:`SciELO PS`.
* `Packtools <https://github.com/scieloorg/packtools/>`_: Biblioteca 
  :term:`Python` que agrega funcionalidades e utilitários para a manipulação 
  de :term:`pacotes SciELO PS` e XMLs :term:`SciELO PS`.

.. _journal-meta-csv:

Metadados dos periódicos
^^^^^^^^^^^^^^^^^^^^^^^^

Adicionalmente, diversos metadados dos periódicos necessários para a identificação de 
elementos em ``<journal-meta>`` estão disponíveis em uma listagem no formato :term:`csv`, 
que pode ser baixada `aqui <http://static.scielo.org/sps/titles-tab-utf-8.csv>`_. 
Esta listagem é atualizada semanalmente, às terças-feiras.


Convenções utilizadas neste guia
--------------------------------

A fim de facilitar a compreensão deste guia, foram utilizadas algumas
convenções de estilo e formatação.

.. note:: Estas caixas apresentam informação importante e diretamente relacionada ao contexto
          em que estão inseridas.


*Itálico*
  Utilizado para nomes de arquivos, normas, URLs, referências ativas a elementos do XML 
  (hiperlinks) ou para introduzir novos termos.

**Negrito**
  Utilizado para identificar textos que devem ser substituídos por valores fornecidos
  pelo usuário.

``Largura fixa``
  Utilizado para exemplos, trechos ou referências estáticas a elementos ou atributos
  do XML.


Para cada elemento descrito, há uma lista de definições no formato::

  Aparece em
    <journal-meta>

  Atributos obrigatórios
    @journal-id-type

  Ocorre
    Uma vez


Onde:

* **Aparece em**: Apresenta o contexto (elemento-pai) onde o elemento em foco é comumente 
  identificado. O fato de um determinado contexto não constar nesta lista não 
  o exclui automaticamente, e a especificação JATS Publishing deve ser consultada.
* **Atributos obrigatórios**: Apresenta apenas os atributos onde, no caso da 
  presença do elemento, devem ser marcados obrigatoriamente. Esta definição pode vir 
  acompanhada de seus valores, também obrigatórios. Caso não existam atributos 
  obrigatórios, este item é omitido.
* **Ocorre**: O número de vezes que o elemento pode ocorrer em um contexto.


Lista de elementos
------------------

A seguir os elementos do XML que apresentam regras de estilo na 
especificação :term:`SciELO PS`. Note que esta não é a lista completa dos elementos 
XML que compõem o :term:`tag set` JATS Publishing versão 1.0 ou PMC versão 3.0, e 
não elimina a necessidade de consultar suas respectivas documentações.


.. toctree::
   :maxdepth: 3

   tagset
   glossary


Documentação narrativa
----------------------

.. toctree::
   :maxdepth: 2

   narr/pressrelease
   narr/errata
   narr/aheadofprint


Indices and tables
==================

* :ref:`genindex`
* :ref:`modindex`
* :ref:`search`

