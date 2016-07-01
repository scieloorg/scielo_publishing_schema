O que há de novo na SciELO PS 1.1
=================================

Este artigo explica as alterações da especificação :term:`SciELO PS` versão 1.1 em 
relação à sua predecessora, a versão 1.0. 


Quebra de compatibilidade
-------------------------

São as alterações na especificação que tornam inválidos os XMLs válidos na
versão anterior.

* O elemento ``//aff/institution[@content-type="orgdiv3"]`` não é mais permitido.
* O atributo ``@xml:lang`` não é mais permitido nos elementos 
  ``article/front/article-meta/article-title`` e ``article/front/article-meta/abstract``. 
  A partir de então, assume-se que o idioma destes elementos é o 
  identificado em ``article/@xml:lang``.
* Licenças de uso do tipo *share alike* não são mais permitidas.
* Referências a arquivos devem conter o nome completo do arquivo, incluindo 
  sua extensão (.tif, .pdf etc).
* Em ``article/front/article-meta/counts``, torna-se obrigatória a presença dos 
  elementos ``<table-count>``, ``<ref-count>``, ``<fig-count>``, 
  ``<equation-count>`` e ``<page-count>``.
* A regra para a formação do valor de ``//table-wrap-foot/fn/@id`` não permite
  mais o sufixo correspondente ao ``<table-wrap>``. i.e.: ``<fn id="TFN01t01">`` 
  passa a ser ``<fn id="TFN01">``.
* O elemento ``//aff/country`` tornou-se obrigatório.
* O atributo ``@xml:lang`` tornou-se obrigatório para o elemento 
  ``article/front/article-meta/kwd-group``.
* O elemento ``<collab>`` passa a ser permitido como descendente de 
  ``article/back/ref-list/ref/element-citation`` apenas quando filho de 
  ``<person-group>``.
* O atributo ``@specific-use="sps-1.1"`` tornou-se obrigatório para o elemento
  ``article``.
* Adicionados os tipos de referência *legal-doc*, *newspaper* e *other*.
* O atributo ``//institution/@content-type="normalized"`` passa a ser permitido.
