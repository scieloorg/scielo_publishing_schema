.. _scielo-brasil:

Regras Específicas para SciELO Brasil
=====================================

Para atender aos "`Critérios, política e procedimentos para a admissão e a 
permanência de periódicos científicos na Coleção SciELO Brasil <http://www.scielo.br/avaliacao/Criterios_SciELO_Brasil_versao_revisada_atualizada_outubro_20171206.pdf>`_" alguns 
elementos apresentam regras específicas de uso:


  * :ref:`elemento-scibrasil-article-id`
  * :ref:`elemento-scibrasil-license`
  * :ref:`elemento-scibrasil-disp`
  * :ref:`elemento-scibrasil-history`
  * :ref:`elemento-scibrasil-article`
  * :ref:`elemento-scibrasil-contrib-group`
  * :ref:`elemento-scibrasil-institution`
  * :ref:`elemento-scibrasil-article-title`
  * :ref:`elemento-scibrasil-xref`
  * :ref:`elemento-scibrasil-ref-list`


.. _elemento-scibrasil-article-id:

<article-id>
^^^^^^^^^^^^

Em :ref:`elemento-article-id` o atributo ``@pub-id-type`` deve, 
obrigatoriamente, apresentar o valor "doi". Exemplo:

.. code-block:: xml

	...
	<article-id pub-id-type="doi">10.1590/0100-29452016221</article-id>
	...
	
.. _elemento-scibrasil-license:

<license>
^^^^^^^^^

De acordo com a política de acesso aberto adotada por SciELO Brasil, serão 
aceitas quaisquer licenças `Creative Commons <http://creativecommons.org/>`_

A URL da licença deve ser inserida como valor do atributo ``@xlink:href`` de 
:ref:`elemento-license`. Exemplo:


.. code-block:: xml

	...
    <article-meta>
        ...
        <permissions>
            ...
            <license license-type="open-access"
                     xlink:href="http://creativecommons.org/licenses/by/4.0/"
                     xml:lang="en">
                <license-p>This is an open-access article distributed under the terms of the Creative Commons Attribution License, which permits unrestricted use, distribution, and reproduction in any medium, provided the original work is properly cited.</license-p>
            </license>
        </permissions>
      	...
    </article-meta>
    ...



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

Este elemento é obrigatório para SciELO Brasil e deve ocorrer uma ou mais vezes.

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
 Uso não é obrigatório para `Errata <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/errata.html>`_ e `Retratação <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/retratacao.html>`_


.. _elemento-scibrasil-ref-list:

<ref-list>
^^^^^^^^^^

Este elemento é obrigatório para SciELO Brasil e deve ocorrer uma ou mais vezes.

.. note::
 Uso não é obrigatório para `Errata <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/errata.html>`_ e `Retratação <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/retratacao.html>`_

