O que há de novo na SciELO PS 1.5
=================================


Este artigo explica as alterações da especificação :term:`SciELO PS` versão 1.5 em 
relação à sua predecessora, a versão 1.4. 


* Adicionado suporte ao valor “partial-retraction” para o atributo article/@article-type 
  [`#459 <https://github.com/scieloorg/scielo_publishing_schema/issues/459>`_].
* Adicionada seção SciELO Brasil destacando as restrições da coleção 
  [`#373 <https://github.com/scieloorg/scielo_publishing_schema/issues/373>`_].
* Aceitar <title> e <label> ao mesmo tempo dentro de <ref-list> 
  [`#372 <https://github.com/scieloorg/scielo_publishing_schema/issues/372>`_].
* Cardinalidade do elemento ``<year>``
  [`#370 <https://github.com/scieloorg/scielo_publishing_schema/issues/370>`_].
* Incluído exemplo de Regra de Nomeação de outras modalidades
  [`#317 <https://github.com/scieloorg/scielo_publishing_schema/issues/317>`_],
  [`#210 <https://github.com/scieloorg/scielo_publishing_schema/issues/210>`_].
* Adicionado suporte ao valor ``ext-link/@ext-link-type="ClinicalTrial"``
  [`#242 <https://github.com/scieloorg/scielo_publishing_schema/issues/242>`_].
* Adicionados novos valores possíveis para ``related-article/@related-article-type``
  [`#232 <https://github.com/scieloorg/scielo_publishing_schema/issues/232>`_],
  [`#255 <https://github.com/scieloorg/scielo_publishing_schema/issues/255>`_].
* Adicionado valor "letter" para o elemento related-article/@related-article-type
  [`#228 <https://github.com/scieloorg/scielo_publishing_schema/issues/228>`_].

 


Quebra de compatibilidade
-------------------------

São as alterações na especificação que tornam inválidos os XMLs válidos na
versão anterior.


* Alterada a cardinalidade dos elementos: ``<surname>``,  ``<suffix>``, ``<volume>``, ``<source>``, ``<size>``, ``<month>``, ``<issue>``,  ``<given-names>``, ``<element-citation>``, ``<chapter-title>``
  [`#360 <https://github.com/scieloorg/scielo_publishing_schema/issues/360>`_],
  [`#358 <https://github.com/scieloorg/scielo_publishing_schema/issues/358>`_],
  [`#357 <https://github.com/scieloorg/scielo_publishing_schema/issues/357>`_],
  [`#354 <https://github.com/scieloorg/scielo_publishing_schema/issues/354>`_],
  [`#353 <https://github.com/scieloorg/scielo_publishing_schema/issues/353>`_],
  [`#345 <https://github.com/scieloorg/scielo_publishing_schema/issues/345>`_],
  [`#341 <https://github.com/scieloorg/scielo_publishing_schema/issues/341>`_],
  [`#337 <https://github.com/scieloorg/scielo_publishing_schema/issues/337>`_],
  [`#330 <https://github.com/scieloorg/scielo_publishing_schema/issues/330>`_],
  [`#329 <https://github.com/scieloorg/scielo_publishing_schema/issues/329>`_].


* A formatação do texto do item resenhado, em ``<product>``, é preservada
  [`#257 <https://github.com/scieloorg/scielo_publishing_schema/issues/257>`_].



Documentação
------------

São as alterações na documentação que não interferem nas regras da 
especificação.


* Toda a documentação passou por revisão ortográfica, de estilo editorial e exemplos de uso
  [`#371 <https://github.com/scieloorg/scielo_publishing_schema/issues/371>`_],
  [`#368 <https://github.com/scieloorg/scielo_publishing_schema/issues/368>`_],
  [`#367 <https://github.com/scieloorg/scielo_publishing_schema/issues/367>`_],
  [`#366 <https://github.com/scieloorg/scielo_publishing_schema/issues/366>`_],
  [`#364 <https://github.com/scieloorg/scielo_publishing_schema/issues/364>`_],
  [`#365 <https://github.com/scieloorg/scielo_publishing_schema/issues/365>`_],
  [`#363 <https://github.com/scieloorg/scielo_publishing_schema/issues/363>`_],
  [`#362 <https://github.com/scieloorg/scielo_publishing_schema/issues/362>`_],
  [`#359 <https://github.com/scieloorg/scielo_publishing_schema/issues/359>`_],
  [`#356 <https://github.com/scieloorg/scielo_publishing_schema/issues/356>`_],
  [`#355 <https://github.com/scieloorg/scielo_publishing_schema/issues/355>`_],
  [`#352 <https://github.com/scieloorg/scielo_publishing_schema/issues/352>`_],
  [`#351 <https://github.com/scieloorg/scielo_publishing_schema/issues/351>`_],
  [`#350 <https://github.com/scieloorg/scielo_publishing_schema/issues/350>`_],
  [`#349 <https://github.com/scieloorg/scielo_publishing_schema/issues/349>`_],
  [`#347 <https://github.com/scieloorg/scielo_publishing_schema/issues/347>`_],
  [`#346 <https://github.com/scieloorg/scielo_publishing_schema/issues/346>`_],
  [`#344 <https://github.com/scieloorg/scielo_publishing_schema/issues/344>`_], 
  [`#343 <https://github.com/scieloorg/scielo_publishing_schema/issues/343>`_],
  [`#342 <https://github.com/scieloorg/scielo_publishing_schema/issues/342>`_],
  [`#340 <https://github.com/scieloorg/scielo_publishing_schema/issues/340>`_],
  [`#339 <https://github.com/scieloorg/scielo_publishing_schema/issues/339>`_],
  [`#336 <https://github.com/scieloorg/scielo_publishing_schema/issues/336>`_],
  [`#335 <https://github.com/scieloorg/scielo_publishing_schema/issues/335>`_],
  [`#334 <https://github.com/scieloorg/scielo_publishing_schema/issues/334>`_],
  [`#333 <https://github.com/scieloorg/scielo_publishing_schema/issues/333>`_],
  [`#331 <https://github.com/scieloorg/scielo_publishing_schema/issues/331>`_],
  [`#328 <https://github.com/scieloorg/scielo_publishing_schema/issues/328>`_],
  [`#327 <https://github.com/scieloorg/scielo_publishing_schema/issues/327>`_],
  [`#325 <https://github.com/scieloorg/scielo_publishing_schema/issues/325>`_],
  [`#320 <https://github.com/scieloorg/scielo_publishing_schema/issues/320>`_],
  [`#319 <https://github.com/scieloorg/scielo_publishing_schema/issues/319>`_],
  [`#318 <https://github.com/scieloorg/scielo_publishing_schema/issues/318>`_],
  [`#315 <https://github.com/scieloorg/scielo_publishing_schema/issues/315>`_],
  [`#259 <https://github.com/scieloorg/scielo_publishing_schema/issues/259>`_],
  [`#256 <https://github.com/scieloorg/scielo_publishing_schema/issues/256>`_],
  [`#222 <https://github.com/scieloorg/scielo_publishing_schema/issues/222>`_].