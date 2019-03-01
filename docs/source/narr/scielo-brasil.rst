.. _scielo-brasil:

Regras Específicas para SciELO Brasil
=====================================

Para atender aos "`Critérios, política e procedimentos para a admissão e a 
permanência de periódicos científicos na Coleção SciELO Brasil <http://www.scielo.br/avaliacao/Criterios_SciELO_Brasil_versao_revisada_atualizada_outubro_20171206.pdf>`_" alguns 
elementos apresentam regras específicas de uso:


  * :ref:`elemento-scibrasil-article-id`
  * :ref:`elemento-scibrasil-disp`
  * :ref:`elemento-scibrasil-history`
  * :ref:`elemento-scibrasil-article`
  * :ref:`elemento-scibrasil-contrib-group`
  * :ref:`elemento-scibrasil-institution`
  * :ref:`elemento-scibrasil-article-title`
  * :ref:`elemento-scibrasil-xref`
  * :ref:`elemento-scibrasil-ref-list`
  * :ref:`elemento-scibrasil-country`
  * :ref:`elemento-scibrasil-product`
  * :ref:`elemento-scibrasil-license`
  * :ref:`elemento-scibrasil-pub-date`


.. _elemento-scibrasil-article-id:

<article-id>
^^^^^^^^^^^^

Em :ref:`elemento-article-id` o atributo ``@pub-id-type`` deve, 
obrigatoriamente, apresentar o valor "doi". Exemplo:

.. code-block:: xml

	...
	<article-id pub-id-type="doi">10.1590/0100-29452016221</article-id>
	...
	
.. note:: 
 Quando existir no PDF um número DOI diferente para o artigo traduzido, obrigatoriamente deve ser identificado em :ref:`elemento-front-stub`.

.. _elemento-scibrasil-disp:

Tabelas e equações codificadas
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Conforme `comunicado <http://us4.campaign-archive2.com/?u=f26dcf71797dd37381acb4aa5&id=0211ed957f&e=[UNIQID>`_ enviado aos editores em 09/12/2016, a partir de Outubro de 2017, equações, fórmulas e tabelas devem ser codificadas. Adicionalmente, as versões em imagem em formato .svg podem ser enviadas dentro do elemento :ref:`elemento-alternatives`.

.. _elemento-scibrasil-history:

<history>
^^^^^^^^^

O histórico do processo de arbitragem do artigo, compreendendo as datas de recebimento, 
de aprovação e de revisão, quando presente, deve conter :ref:`elemento-day`, :ref:`elemento-month` e :ref:`elemento-year`. Para acessar o comunicado `clique aqui <http://us4.campaign-archive2.com/?u=f26dcf71797dd37381acb4aa5&id=2a6634a845>`_


.. _elemento-scibrasil-article:

Tipos de documentos
^^^^^^^^^^^^^^^^^^^

Em :ref:`elemento-article` o atributo ``@article-type`` não permite os tipos de documento:

* announcement
* calendar
* in-brief
* book-received
* news
* reprint
* meeting-report
* abstract
* product-review
* dissertation
* translation

.. _elemento-scibrasil-contrib-group:

<contrib-group>
^^^^^^^^^^^^^^^

Este elemento em :ref:`elemento-article-meta` é obrigatório para SciELO Brasil e deve ocorrer uma ou mais vezes.

.. note::
 Uso não é obrigatório para `Errata <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/errata.html>`_ e `Retratação <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/retratacao.html>`_


.. _elemento-scibrasil-institution:

<institution>
^^^^^^^^^^^^^

Este elemento é obrigatório para SciELO Brasil e deve ocorrer uma ou mais vezes.

.. note::
 Uso não é obrigatório para `Errata <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/errata.html>`_ e `Retratação <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/retratacao.html>`_


.. _elemento-scibrasil-article-title:

<article-title>
^^^^^^^^^^^^^^^

Este elemento em :ref:`elemento-title-group` é obrigatório para SciELO Brasil e deve ocorrer uma vez.


.. _elemento-scibrasil-xref:

<xref>
^^^^^^

É obrigatório este elemento para SciELO Brasil na referência cruzada com atributo ``@ref-type`` do tipo "bibr" e deve ocorrer uma ou mais vezes.

.. note::
 Uso não é obrigatório para `Errata <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/errata.html>`_ , `Retratação <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/retratacao.html>`_ e Editorial.


.. _elemento-scibrasil-ref-list:

<ref-list>
^^^^^^^^^^

Este elemento em :ref:`elemento-back` é obrigatório para SciELO Brasil e deve ocorrer uma ou mais vezes.

.. note::
 Uso não é obrigatório para `Errata <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/errata.html>`_ , `Retratação <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/retratacao.html>`_ e Editorial.


.. _elemento-scibrasil-country:

<country>
^^^^^^^^^

Este elemento em :ref:`elemento-aff` é obrigatório para SciELO Brasil e deve ocorrer uma vez.

.. note::
 Uso não é obrigatório para `Errata <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/errata.html>`_ e `Retratação <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/retratacao.html>`_


.. _elemento-scibrasil-product:

<product>
^^^^^^^^^

:ref:`elemento-product` contém informações de produto resenhado, mas somente deverá ser utilizado quando :ref:`elemento-article` possuir o atributo ``@article-type="book-review"``.


.. _elemento-scibrasil-license:

<license>
^^^^^^^^^

Em ``license-p`` é obrigatório o uso da seguinte frase:
 * Inglês: This is an article published in open access under a Creative Commons license.
 * Português: Este é um artigo publicado em acesso aberto sob uma licença Creative Commons.
 * Espanhol: Este es un artículo publicado en acceso abierto bajo una licencia Creative Commons.


.. _elemento-scibrasil-pub-date:

<pub-date>
^^^^^^^^^^

``<pub-date>`` deve estar acompanhada do atributo ``@pub-type``, do tipo ``scielo`` e ``collection`` quando necessário, sendo: 


+---------------+---------------------------------------------+------------------------------------+
| ``@pub-type`` | Descrição                                   | Tipos de Datas                     |
+===============+=============================================+====================================+
|    scielo     | Data efetiva de publicação em SciELO.       | dia + mês + ano                    |
+---------------+---------------------------------------------+------------------------------------+
|  collection   | Data do fascículo ao qual pertence o artigo.| ano OU; mês + ano OU; season + ano.|
+---------------+---------------------------------------------+------------------------------------+

Exemplos:

    * :ref:`elemento-pubdate-exemplo-1`
    * :ref:`elemento-pubdate-exemplo-2`
    * :ref:`elemento-pubdate-exemplo-3`
    * :ref:`elemento-pubdate-exemplo-4`

    
.. _elemento-pubdate-exemplo-1: 

Exemplo de ``<pub-date>`` em publicação regular 1:
--------------------------------------------------

.. code-block:: xml

    <pub-date pub-type="scielo">
       <day>01</day>
       <month>01</month>
       <year>2018</year>
    </pub-date>
     <pub-date pub-type="collection">
       <season>Jan-Feb</season>
       <year>2018</year>
    </pub-date>


.. _elemento-pubdate-exemplo-2: 

Exemplo de ``<pub-date>`` em publicação regular 2:
--------------------------------------------------

.. code-block:: xml

    <pub-date pub-type="scielo">
       <day>01</day>
       <month>01</month>
       <year>2018</year>
    </pub-date>
     <pub-date pub-type="collection">
       <month>01</month>
       <year>2018</year>
    </pub-date>


.. _elemento-pubdate-exemplo-3: 

Exemplo de ``<pub-date>`` em modalidade de `publicação contínua (PC) <http://www.scielo.org/local/Image/guiarpass.pdf>`_
-------------------------------------------------------------------------------------------------------------------------

.. code-block:: xml

    <pub-date pub-type="scielo">
       <day>01</day>
       <month>12</month>
       <year>2018</year>
    </pub-date>
     <pub-date pub-type="collection">      
       <year>2019</year>
    </pub-date>


.. _elemento-pubdate-exemplo-4:

Exemplo de ``<pub-date>`` em modalidade `ahead of print (AOP) <http://www.scielo.org/local/File/Guia_AOP.pdf>`_
----------------------------------------------------------------------------------------------------------------

.. code-block:: xml

    <pub-date pub-type="scielo">
       <day>17</day>
       <month>02</month>
       <year>2019</year>
    </pub-date>


.. note::
 * Para datas do tipo scielo, criar as tags :ref:`elemento-day` e :ref:`elemento-month` com informação 00 para que seja alterada posteriormente com a data efetiva da publicação pela unidade de produção.
 * Para datas do tipo collection, sempre preencher a data ao qual o fascículo pertence, seguindo sua periodicidade.
 * Para revistas que adotam `publicação contínua (PC) <http://www.scielo.org/local/Image/guiarpass.pdf>`_, só considerar o ano ao qual o fascículo pertence para data do tipo collection.




