O que há de novo na SciELO PS 1.2
=================================

Este artigo explica as alterações da especificação :term:`SciELO PS` versão 1.2 em 
relação à sua predecessora, a versão 1.1. 


* Mudança na cardinalidade dos elementos de ``//award-group`` [`#52 <https://github.com/scieloorg/scielo_publishing_schema/issues/52>`_].
* Adicionado suporte aos valores ``presented-at`` e ``presented-by`` para o atributo ``//fn/@fn-type`` [`#51 <https://github.com/scieloorg/scielo_publishing_schema/issues/51>`_].
* Adicionado suporte a licença ``CC-BY-NC-ND`` [`#50 <https://github.com/scieloorg/scielo_publishing_schema/issues/50>`_].
* Adicionado suporte a errata, por meio de ``/article/@article-type="correction"`` [`#45 <https://github.com/scieloorg/scielo_publishing_schema/issues/45>`_].
* Revisão das restrições sintáticas dos valores dos atributos ``@id`` [`#15 <https://github.com/scieloorg/scielo_publishing_schema/issues/15>`_].


Quebra de compatibilidade
-------------------------

São as alterações na especificação que tornam inválidos os XMLs válidos na
versão anterior.


* Adicionado suporte e regras para o elemento ``//response`` [`#48 <https://github.com/scieloorg/scielo_publishing_schema/issues/48>`_].
* Removido suporte ao DOCTYPE PMC 3.0 [`#46 <https://github.com/scieloorg/scielo_publishing_schema/issues/46>`_].
* Tornou-se obrigatório o preenchimento do atributo ``//aff/country/@country`` [`#44 <https://github.com/scieloorg/scielo_publishing_schema/issues/44>`_].
* Tornou-se obrigatório o elemento ``//journal-id[@journal-id-type="publisher-id"]`` [`#14 <https://github.com/scieloorg/scielo_publishing_schema/issues/14>`_].


Documentação
------------

São as alterações na documentação que não interferem nas regras da 
especificação.


* Documentação do elemento ``//boxed-text`` [`#53 <https://github.com/scieloorg/scielo_publishing_schema/issues/53>`_].
* Documentação do elemento ``//verse-group`` [`#47 <https://github.com/scieloorg/scielo_publishing_schema/issues/47>`_].
* Documentação do elemento ``//sub-article`` [`#41 <https://github.com/scieloorg/scielo_publishing_schema/issues/41>`_].

