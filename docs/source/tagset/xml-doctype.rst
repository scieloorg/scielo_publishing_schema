.. _xml-doctype:

<!DOCTYPE>
==========

A declaração ``<!DOCTYPE>`` indica a :term:`DTD` à qual o XML encontra-se associado, ou seja, define as regras estruturais do :term:`documento`. O :term:`SciELO Publishing Schema` utiliza como base o padrão JATS na versão `1.1 <https://jats.nlm.nih.gov/publishing/1.1/>`_.

Exemplo *JATS versão 1.1*:

.. code-block:: xml

    <!DOCTYPE article PUBLIC "-//NLM//DTD JATS (Z39.96) Journal Publishing DTD v1.1 20151215//EN" "https://jats.nlm.nih.gov/publishing/1.1/JATS-journalpublishing1.dtd">


Elementos Flutuantes
====================

Os elementos flutuantes podem aparecer em todo o :term:`documento`, seja em :ref:`elemento-article` :ref:`elemento-sub-article` ou em :ref:`elemento-response` nos blocos: :ref:`elemento-article-meta` ou :ref:`elemento-front-stub`, :ref:`elemento-body` e :ref:`elemento-back`.


Exemplos:

  * :ref:`elemento-xrefflut-exemplo-1`
  * :ref:`elemento-xrefflut-exemplo-2`
  * :ref:`elemento-xrefflut-exemplo-3`


.. _elemento-xrefflut-exemplo-1:

Exemplo de elemento flutuante ``<xref>`` em ``<article-meta>``:
---------------------------------------------------------------

.. code-block:: xml

	...
	<article-meta>
    	...
    	<contrib contrib-type="author">
        	<name>
            	<surname>
            	<given-names>
        	</name>
        	<xref ref-type="aff" rid="aff01">1</xref>
    	</contrib>
    ...
	</article-meta>
	...


.. _elemento-xrefflut-exemplo-2:

Exemplo de elemento flutuante ``<xref>`` em ``<p>``:
----------------------------------------------------

.. code-block:: xml

	...
	<body>
    	<p>text text text text text text text (<xref ref-type="bibr" rid="B42">Da Silva, 1976</xref>). text text text</p>
	...
	</body>
	...


.. _elemento-xrefflut-exemplo-3:

Exemplo de elemento flutuante ``<xref>`` em elementos de ``<back>``:
--------------------------------------------------------------------

.. code-block:: xml

	...
	<fn fn-type="other" id="fn2">
    	<label>1</label>
        	<p>Compreende-se por habilidades "comportamentos ou conjuntos de comportamentos que caracterizam determinado desempenho do indivíduo" (<xref ref-type="bibr" rid="B22">Santos, Kienen, Viecili, Botomé, &amp; Kubo, 2009</xref>, p. 133-134).</p>
	</fn>
	...




.. {"reviewed_on": "20160629", "by": "gandhalf_thewhite@hotmail.com"}
