Guia de uso de elementos e atributos XML para documentos que seguem a implementação SciELO Publishing Schema.
=============================================================================================================

Versão |version| - setembro de 2016.


Versões anteriores:

* `Versão 1.4 <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/1.4-branch/>`_ (suportada).
* `Versão 1.3 <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/1.3-branch/>`_.
* `Versão 1.2 <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/1.2-branch/>`_.
* `Versão 1.1 <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/1.1-branch/>`_.
* `Versão 1.0 <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/1.0-branch/>`_.


Introdução
----------

Este guia descreve o uso do estilo de marcação adotado pela *SciELO* para submissão de documentos em formato :term:`XML`.

A :term:`SciELO Publishing Schema` (:term:`SciELO PS`) é composta pelas especificações:

* :term:`NISO JATS Journal Publishing DTD` (`JATS versão 1.0 <http://jats.nlm.nih.gov/publishing/1.0/>`_);
* :term:`Estilo SciELO PS` com regras especializadas da :term:`Metodologia SciELO`.

Os usuários deste guia devem possuir conhecimentos prévios de :term:`XML` e :term:`DTD`.

Dúvidas e/ou comentários acerca da especificação :term:`SciELO PS`, deste guia de uso ou das ferramentas disponibilizadas pela *SciELO* como apoio à marcação em :term:`XML` devem ser tratadas por meio de lista de discussão `scielo-xml <http://groups.google.com/group/scielo-xml/>`_.


Notas da versão
---------------

As versões são disponibilizadas a cada seis meses em calendário fixo. Versões de correção são disponibilizadas por demanda, sendo identificadas no terceiro dígito da versão. Ex.: versão *1.1.1*.

Duas versões são suportadas simultaneamente, a atual e a imediatamente anterior. Essa medida garante um ciclo de vida de 1 (um) ano para cada versão.

.. toctree::
   :maxdepth: 1

   whatsnew-1.5
   whatsnew-1.4
   whatsnew-1.3
   whatsnew-1.2
   whatsnew-1.1


Ferramentas de apoio
--------------------

Algumas ferramentas são disponibilizadas e mantidas pela *SciELO* seguindo o modelo :term:`open source`, para apoiar o processo de marcação de documentos em formato *XML*.

 `Markup <http://docs.scielo.org/projects/scielo-pc-programs/en/latest/markup.html>`_:
     Coleção de macros para :term:`Microsoft Word` para marcação de documentos conforme a :term:`SciELO PS`.


 `Stylechecker <http://manager.scielo.org/tools/validators/stylechecker/>`_:
     Ferramenta online para verificar se determinado *XML* está em conformidade com a especificação :term:`SciELO PS`. Disponível a partir do :term:`SciELO  Manager`.


 `Packtools <https://github.com/scieloorg/packtools/>`_:
     Biblioteca escrita em :term:`Python` com funcionalidades e utilitários para manipulação de pacotes e XMLs da :term:`SciELO PS`.


 `Package Maker <http://docs.scielo.org/projects/scielo-pc-programs/en/latest/xml_package_maker.html>`_:
     Ferramenta para geração de :term:`Pacotes SciELO PS` e :term:`PMC`. Adicionalmente, fornece relatórios detalhados sobre a estrutura e a validade de alguns metadados de documentos *XML* como subproduto do processo de geração.

.. _journal-meta-csv:

Metadados de periódicos
^^^^^^^^^^^^^^^^^^^^^^^

Complementarmente, encontra-se disponível em formato :term:`csv` uma lista de metadados de periódicos necessários para identificação de elementos em ``<journal-meta>``. O documento pode ser baixado a partir deste `link <http://static.scielo.org/sps/titles-tab-v2-utf-8.csv>`_ e sua atualização é semanal, sempre às quartas-feiras.


Convenções utilizadas neste guia
--------------------------------

Para facilitar a compreensão deste guia, foram utilizadas algumas convenções de estilo e formatação.

Formatação
^^^^^^^^^^

.. note:: Estas caixas apresentam informação importante e diretamente relacionada ao contexto em que estão inseridas.

*Itálico*

  Utilizado sempre para:

  * palavras e/ou termos estrangeiros;
  * nomes de publicações, empresas, instituições, projetos, técnicas, tecnologias, marcas etc;
  * nomes de arquivos, normas e referências.

**Negrito**

  Identifica palavras ou termos que devem ser substituídos por conteúdo adequado fornecido pelo usuário.

``Fonte monoespaçada``

  Usado para exemplos, trechos de código e referências estáticas a elementos   e atributos do *XML*.

Será utilizada a linguagem de marcação :term:`RST` (*reStructuredText*) para formatar e habilitar recursos de hipertexto aos documentos.

Estruturação
^^^^^^^^^^^^

Na descrição dos elementos, devem obrigatoriamente aparecer os seguintes itens, salvo quando especificado em contrário:

1. Nome do elemento em formato de *tag*.

   Ex. ``<article-meta>``

2. Aparece em: apresenta o contexto (:term:`elemento-pai`) onde o elemento ocorre, podendo ser uma lista.

   Ex. ``<journal-meta>``

3. Atributos obrigatórios: lista somente os atributos obrigatórios ao elemento descrito. Pode vir acompanhado de valores predefinidos e/ou obrigatórios. Item opcional.

   Ex. ``@journal-id-type``

4. Ocorre: especifica a quantidade de ocorrências.

   Ex. Uma vez

5. Descrição do elemento.

6. Exemplo(s).

7. Nota(s). (se necessário)

.. note:: A especificação :term:`NISO JATS Journal Publishing DTD` deve ser consultada sempre que houver dúvida em relação a contextualização de elementos.

Documentação narrativa
----------------------

.. toctree::
   :maxdepth: 2

   narr/caracteres
   narr/regra-nomeacao
   narr/tipos-especiais-documentos
   narr/scielo-brasil

   faq
   glossary
   reference

Lista de elementos
------------------

Esta lista compreende apenas os elementos *XML* do :term:`Estilo SciELO PS`. A lista completa dos elementos *XML* que compõem o :term:`tag set` da `JATS versão 1.0 <http://jats.nlm.nih.gov/publishing/1.0/>`_ deve ser consultada se necessário.

.. toctree::
   :maxdepth: 1

   tagset/xml-encoding
   tagset/xml-doctype
   tagset/sugestao-atribuicao-id


.. toctree::
   :maxdepth: 1
   :glob:

   tagset/elemento-*


Índices e tabelas
=================

* :ref:`genindex`
* :ref:`search`

.. {"reviewed_on": "20160729", "by": "gandhalf_thewhite@hotmail.com"}
