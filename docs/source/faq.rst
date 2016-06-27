.. _faq:

Perguntas frequentes
====================

Como identificar menção a um Ensaio Clínico?
--------------------------------------------

O Ensaio Clínico é um estudo em voluntários humanos com o objetivo de responder 
a questões específicas de saúde. O registro de ensaio clínico deve ser 
identificado pelo elemento :ref:`elemento-ext-link`. Veja:

.. code-block:: xml

   ...
   <p>Número de registro clínico:<ext-link ext-link-type="ClinicalTrial" xlink:href="https://clinicaltrials.gov/ct2/show/NCT00981734">NCT00981734</ext-link></p>
   ...


Para identificação de Ensaio Clínico o elemento :ref:`elemento-ext-link` deve 
apresentar o valor "ClinicalTrial" no atributo @ext-link-type e no atributo 
@xlink:href="" inserir a URL do registro de Ensaio Clínico.


Para saber mais sobre Ensaio Clínico, clique no link abaixo:
O que é Ensaio Clínico?


Como identificar as subseções de um documento?
----------------------------------------------

Artigos que apresentam subseções, devem ser identificados no documento pelo 
elemento :ref:`elemento-subj-group`. Veja:

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

.. note:: Apenas a seção maior apresenta o atributo @subj-group-type com o valor 
          "heading". Esse valor deve aparecer 1 vez no documento .xml.


