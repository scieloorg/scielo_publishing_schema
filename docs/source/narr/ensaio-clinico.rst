.. _ensaio-clinico:

Ensaio Clínico
--------------


O Ensaio Clínico é um estudo em voluntários com o objetivo de responder a questões específicas de saúde, cujo registro deve ser identificado pelo elemento :ref:`elemento-ext-link`.


Exemplo:

.. code-block:: xml

   ...
   <p>Número de registro clínico:<ext-link ext-link-type="clinical-trial" xlink:href="https://clinicaltrials.gov/ct2/show/NCT00981734">NCT00981734</ext-link></p>
   ...


Para identificação de um Ensaio Clínico, o elemento :ref:`elemento-ext-link` deve apresentar o valor ``clinical-trial`` no atributo ``@ext-link-type`` e ter preenchida a URL do registro de Ensaio Clínico no atributo ``@xlink:href``.


Informações adicionais encontram-se disponíveis nos sites abaixo identificados:

* `Sociedade Brasileira de Profissionais em Pesquisa Clínica <https://www.sbppc.org.br/home>`_;
* `Clinical Trials.Gov <https://clinicaltrials.gov/>`_;
* `NLM's MedlinePlus - Clinical Trials information <https://www.nlm.nih.gov/medlineplus/clinicaltrials.html>`_.
