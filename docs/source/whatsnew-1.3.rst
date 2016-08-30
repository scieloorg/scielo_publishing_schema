O que há de novo na SciELO PS 1.3
=================================

Este artigo explica as alterações da especificação :term:`SciELO PS` versão 1.3 em 
relação à sua predecessora, a versão 1.2. 


* Elementos ``//article-meta/volume`` e ``//article-meta/issue`` deixaram de ser
  obrigatórios
  [`#132 <https://github.com/scieloorg/scielo_publishing_schema/issues/132>`_].
* Elemento ``//article-meta/abstract`` deixou de ser obrigatório
  [`#127 <https://github.com/scieloorg/scielo_publishing_schema/issues/127>`_].
* Adicionado suporte ao valor ``boxed-text`` em ``//xref/@ref-type``
  [`#123 <https://github.com/scieloorg/scielo_publishing_schema/issues/123>`_].
* Regra para o referenciamento de Ensaios Clínicos 
  [`#111 <https://github.com/scieloorg/scielo_publishing_schema/issues/111>`_].
* Elemento ``//article-meta/counts`` deixou de ser obrigatório
  [`#104 <https://github.com/scieloorg/scielo_publishing_schema/issues/104>`_].
* Definição de regra para a identificação de rótulos multilíngues em tabelas e 
  figuras.



Quebra de compatibilidade
-------------------------

São as alterações na especificação que tornam inválidos os XMLs válidos na
versão anterior.


* Valores ``announcement`` e ``abstract`` deixaram de ser suportados em 
  ``article/@article-type``
  [`#124 <https://github.com/scieloorg/scielo_publishing_schema/issues/124>`_].



Documentação
------------

São as alterações na documentação que não interferem nas regras da 
especificação.


* Cardinalidade do elemento ``//contrib/name``
  [`#138 <https://github.com/scieloorg/scielo_publishing_schema/issues/138>`_].
* Cardinalidade do elemento ``//funding-group/award-group``
  [`#135 <https://github.com/scieloorg/scielo_publishing_schema/issues/135>`_].
* Documentação do valor ``original`` no atributo ``//institution/@content-type``
  [`#126 <https://github.com/scieloorg/scielo_publishing_schema/issues/126>`_].
* Documentação do atributo ``//fpage/@seq`` para documentos, de um mesmo número,
  que compartilham o valor de ``//fpage``
  [`#114 <https://github.com/scieloorg/scielo_publishing_schema/issues/114>`_].
* Documentação do uso de subseções
  [`#99 <https://github.com/scieloorg/scielo_publishing_schema/issues/99>`_].
* Documentação do elemento ``email``
  [`#83 <https://github.com/scieloorg/scielo_publishing_schema/issues/83>`_].
* Diversas melhorias e correções nos tópicos e exemplos 
  [`#137 <https://github.com/scieloorg/scielo_publishing_schema/issues/137>`_],
  [`#136 <https://github.com/scieloorg/scielo_publishing_schema/issues/136>`_],
  [`#134 <https://github.com/scieloorg/scielo_publishing_schema/issues/134>`_],
  [`#133 <https://github.com/scieloorg/scielo_publishing_schema/issues/133>`_],
  [`#131 <https://github.com/scieloorg/scielo_publishing_schema/issues/131>`_],
  [`#130 <https://github.com/scieloorg/scielo_publishing_schema/issues/130>`_],
  [`#125 <https://github.com/scieloorg/scielo_publishing_schema/issues/125>`_],
  [`#122 <https://github.com/scieloorg/scielo_publishing_schema/issues/122>`_],
  [`#121 <https://github.com/scieloorg/scielo_publishing_schema/issues/121>`_],
  [`#103 <https://github.com/scieloorg/scielo_publishing_schema/issues/103>`_],
  [`#102 <https://github.com/scieloorg/scielo_publishing_schema/issues/102>`_].


.. {"reviewed_on": "20160809", "by": "gandhalf_thewhite@hotmail.com"}