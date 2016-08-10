O que há de novo na SciELO PS 1.2
=================================

Este artigo explica as alterações da especificação :term:`SciELO PS` versão 1.2 em 
relação à sua predecessora, a versão 1.1. 


* Mudança na cardinalidade dos elementos de ``//award-group`` 
  [`#52 <https://github.com/scieloorg/scielo_publishing_schema/issues/52>`_].
* Adicionado suporte aos valores ``presented-at`` e ``presented-by`` para o atributo ``//fn/@fn-type`` 
  [`#51 <https://github.com/scieloorg/scielo_publishing_schema/issues/51>`_].
* Adicionado suporte a licença ``CC-BY-NC-ND`` 
  [`#50 <https://github.com/scieloorg/scielo_publishing_schema/issues/50>`_].
* Adicionado suporte a errata, por meio de ``/article/@article-type="correction"`` 
  [`#45 <https://github.com/scieloorg/scielo_publishing_schema/issues/45>`_].
* Revisão das restrições sintáticas dos valores do atributo ``@id`` 
  [`#15 <https://github.com/scieloorg/scielo_publishing_schema/issues/15>`_].
* Títulos de seção deverão ser explicitados por meio do elemento ``title``. Essa
  regra se aplica principalmente aos elementos ``abstract``, ``trans-abstract``,
  ``ref-list`` e ``kwd-group``.

.. versionchanged:: 1.2.1

* Adicionado suporte a licenças ``IGO``.
* A regra de classificar referências como completas ou incompletas, por meio do atributo ``@specific-use="display-only"``, se mostrou equivocada e foi removida.


Quebra de compatibilidade
-------------------------

São as alterações na especificação que tornam inválidos os XMLs válidos na
versão anterior.


* Adicionado suporte e regras para o elemento ``//response`` 
  [`#48 <https://github.com/scieloorg/scielo_publishing_schema/issues/48>`_].
* Removido suporte ao DOCTYPE PMC 3.0 
  [`#46 <https://github.com/scieloorg/scielo_publishing_schema/issues/46>`_].
* Tornou-se obrigatório o preenchimento do atributo ``//aff/country/@country`` 
  [`#44 <https://github.com/scieloorg/scielo_publishing_schema/issues/44>`_].
* Tornou-se obrigatório o elemento ``//journal-id[@journal-id-type="publisher-id"]`` 
  [`#14 <https://github.com/scieloorg/scielo_publishing_schema/issues/14>`_].
* E-mail e país, quando presente no texto original da afiliação, não devem ser 
  identificados utilizando ``//aff//named-content``.
* Elemento ``p`` não deve ser utilizado como filho do elemento ``sig``.

.. versionchanged:: 1.2.1

* Tornou-se obrigatório o preenchimento do atributo ``//media/@mime-type``
  [`#62 <https://github.com/scieloorg/scielo_publishing_schema/issues/62>`_].


Documentação
------------

São as alterações na documentação que não interferem nas regras da 
especificação.


* Documentação do elemento ``//boxed-text`` 
  [`#53 <https://github.com/scieloorg/scielo_publishing_schema/issues/53>`_].
* Documentação do elemento ``//verse-group`` 
  [`#47 <https://github.com/scieloorg/scielo_publishing_schema/issues/47>`_].
* Documentação do elemento ``//sub-article`` 
  [`#41 <https://github.com/scieloorg/scielo_publishing_schema/issues/41>`_].
* Adicionado exemplo de ``ref/element-citation[@publication-type="confproc"]`` e 
  ``ref/element-citation[@publication-type="other"]``.
* Documentação do elemento ``//attrib``.
* Documentação do elemento ``//front-stub``.
* Adicionado exemplo de título de seção contendo marcador de numeração.
* Diversas correções nos exemplos.
* Adicionada seção para documentação narrativa, onde serão disponibilizadas 
  recomendações específicas ao processo de produção dos documentos e outras 
  práticas.

.. versionchanged:: 1.2.1

* Diversas melhorias e correções nos tópicos e exemplos 
  [`#105 <https://github.com/scieloorg/scielo_publishing_schema/issues/105>`_],
  [`#108 <https://github.com/scieloorg/scielo_publishing_schema/issues/108>`_],
  [`#95 <https://github.com/scieloorg/scielo_publishing_schema/issues/95>`_],
  [`#63 <https://github.com/scieloorg/scielo_publishing_schema/issues/63>`_],
  [`#100 <https://github.com/scieloorg/scielo_publishing_schema/issues/100>`_].

.. {"reviewed_on": "20160809", "by": "gandhalf_thewhite@hotmail.com"}