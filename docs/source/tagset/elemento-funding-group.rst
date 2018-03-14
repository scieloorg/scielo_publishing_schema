.. _elemento-funding-group:

<funding-group>
===============

+------------------------------+-----------------+
| Aparece em                   | Ocorre          |
+==============================+=================+
| :ref:`elemento-article-meta` | Zero ou uma vez |
+------------------------------+-----------------+



Usado somente quando há um número de contrato explicitado no artigo. As informações de  financiamento podem aparecer nas tags :ref:`elemento-fn` ou :ref:`elemento-ack`.


Exemplo:

.. code-block:: xml

   ...
	<funding-group>
		<award-group>
			<funding-source>CNPQ</funding-source>
			<award-id>12345</award-id>
		</award-group>
	</funding-group>
	...


.. note:: ``<funding-group>`` deve ser inserido antes de :ref:`elemento-counts` ou depois de :ref:`elemento-kwd-group`.


.. {"reviewed_on": "20160625", "by": "gandhalf_thewhite@hotmail.com"}
