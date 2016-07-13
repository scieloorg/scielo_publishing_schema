O que há de novo na SciELO PS 1.4
=================================


Este artigo explica as alterações da especificação :term:`SciELO PS` versão 1.4 em 
relação à sua predecessora, a versão 1.3. 

* Flexibilização das restrições relativas ao *scheme* da URI, parte do valor do 
  atributo ``//ext-link/@xlink:href``
  [`#185 <https://github.com/scieloorg/scielo_publishing_schema/issues/185>`_].
* Licenciamento de objetos no corpo do texto
  [`#181 <https://github.com/scieloorg/scielo_publishing_schema/issues/181>`_].


Quebra de compatibilidade
-------------------------

São as alterações na especificação que tornam inválidos os XMLs válidos na
versão anterior.

* Elementos ``//permission/license`` passou a ocorrer 1 ou mais vezes e é 
  obrigatória a indicação de língua, sendo que o conteúdo de ``license-p`` deve 
  ser obrigatoriamente em inglês ou no língua principal do artigo
  [`#71 <https://github.com/scieloorg/scielo_publishing_schema/issues/71>`_].
* Identificadores de contribuidor
  [`#174 <https://github.com/scieloorg/scielo_publishing_schema/issues/174>`_].
* Elemento ``title`` zero ou uma vez em ``//fn-group``
  [`#128 <https://github.com/scieloorg/scielo_publishing_schema/issues/128>`_].


Documentação
------------

São as alterações na documentação que não interferem nas regras da 
especificação.


* Documentação de resenha de produto 
  [`#200 <https://github.com/scieloorg/scielo_publishing_schema/issues/200>`_].
* Documentação do elemento ``//permissions/copyright-holder``
  [`#180 <https://github.com/scieloorg/scielo_publishing_schema/issues/180>`_].
* Correção no guia para produção de errata 
  [`#146 <https://github.com/scieloorg/scielo_publishing_schema/issues/146>`_],
  [`#176 <https://github.com/scieloorg/scielo_publishing_schema/issues/176>`_].
* Diversas melhorias e correções nos tópicos e exemplos
  [`#182 <https://github.com/scieloorg/scielo_publishing_schema/issues/182>`_],
  [`#173 <https://github.com/scieloorg/scielo_publishing_schema/issues/173>`_],
  [`#170 <https://github.com/scieloorg/scielo_publishing_schema/issues/170>`_],
  [`#169 <https://github.com/scieloorg/scielo_publishing_schema/issues/169>`_],
  [`#168 <https://github.com/scieloorg/scielo_publishing_schema/issues/168>`_],
  [`#119 <https://github.com/scieloorg/scielo_publishing_schema/issues/119>`_],
  [`#85 <https://github.com/scieloorg/scielo_publishing_schema/issues/85>`_],
  [`#66 <https://github.com/scieloorg/scielo_publishing_schema/issues/66>`_].

