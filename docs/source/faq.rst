.. _faq:

Perguntas frequentes
====================

Como identificar uma menção a um Ensaio Clínico?
------------------------------------------------

O Ensaio Clínico é um estudo em voluntários humanos com o objetivo de responder a questões específicas de saúde, cujo registro deve ser identificado pelo elemento :ref:`elemento-ext-link`.

Exemplo:

.. code-block:: xml

   ...
   <p>Número de registro clínico:<ext-link ext-link-type="ClinicalTrial" xlink:href="https://clinicaltrials.gov/ct2/show/NCT00981734">NCT00981734</ext-link></p>
   ...


Para identificação de um Ensaio Clínico, o elemento :ref:`elemento-ext-link` deve apresentar o valor ``ClinicalTrial`` no atributo ``@ext-link-type`` e ter preenchida a URL do registro de Ensaio Clínico no atributo ``@xlink:href``.

Informações adicionais encontram-se disponíveis nos sites abaixo identificados:

* `Registro Brasileiro de Ensaios Clínicos <http://www.ensaiosclinicos.gov.br/>`_;
* `Sociedade Brasileira de Profissionais em Pesquisa Clínica <http://www.sbppc.org.br/portal/index.php>`_;
* `Clinical Trials.Gov <https://clinicaltrials.gov/>`_;
* `NLM's MedlinePlus - Clinical Trials information <https://www.nlm.nih.gov/medlineplus/clinicaltrials.html>`_.


Como identificar as subseções de um documento?
----------------------------------------------

Artigos que apresentam subseções devem ser identificados no :term:`documento` por meio do elemento :ref:`elemento-subj-group`.

Exemplo:

.. code-block:: xml

	...
	<article-categories>
		<subj-group subj-group-type="heading">
			<subject>Scientific Communication</subject>
			<subj-group>
				<subject>Food Safety</subject>
			</subj-group>
		</subj-group>
	</article-categories>
	...

.. note:: Apenas a seção de nível mais alto apresenta o atributo ``@subj-group-type`` com o valor ``heading`` e que deve aparecer somente uma vez no documento *XML*.


.. {"reviewed_on": "20160719", "by": "gandhalf_thewhite@hotmail.com"}
