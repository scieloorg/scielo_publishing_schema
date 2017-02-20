.. _scielo-brasil:

Regras Específicas para SciELO Brasil
=====================================

Para atender aos "Critérios, política e procedimentos para a admissão e a permanência de periódicos científicos na Coleção SciELO Brasil" alguns elementos apresentam restrições:


  * :ref:`elemento-scibrasil-article-id`
  * :ref:`elemento-scibrasil-license`



`Critérios SciELO Brasil <http://www.scielo.br/avaliacao/20141003NovosCriterios_SciELO_Brasil.pdf>`_


.. _elemento-scibrasil-article-id:

<article-id>
^^^^^^^^^^^^

Em :ref:`elemento-article-id` o atributo ``@pub-id-type`` deve, obrigatoriamente, apresentar o valor "doi".
Exemplo:

.. code-block:: xml

	...
	<article-id pub-id-type="doi">10.1590/0100-29452016221</article-id>
	...
	
