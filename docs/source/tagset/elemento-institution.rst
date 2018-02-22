.. _elemento-institution:

<institution>
=============

Atributos obrigatórios:

  1. ``@content-type``

+---------------------+--------------------+
| Aparece em          | Ocorre             |
+=====================+====================+
| :ref:`elemento-aff` | Zero ou mais vezes |
+---------------------+--------------------+



Neste elemento identifica-se a instituição de afiliação do autor, a qual pode ser dividida em até três níveis, definidos pelo atributo obrigatório ``@content-type``, cujos valores possíveis são:

+------------+--------------------------------------------------------------------+
| Valor      | Descrição                                                          |
+============+====================================================================+
| orgname    | Representa a instituição de primeiro nível hierárquico mencionado  |
|            | na afiliação.                                                      |
+------------+--------------------------------------------------------------------+
| orgdiv1    | Representa, hierarquicamente, a primeira divisão da instituição    |
|            | mencionada.                                                        |
+------------+--------------------------------------------------------------------+
| orgdiv2    | Representa, hierarquicamente, a segunda divisão da instituição     |
|            | mencionada.                                                        |
+------------+--------------------------------------------------------------------+
| normalized | Nome da instituição na forma normalizada pela SciELO.              |
+------------+--------------------------------------------------------------------+
| original   | Identifica a afiliação completa conforme consta no texto do artigo |
+------------+--------------------------------------------------------------------+


.. note:: Divisões abaixo do terceiro nível hierárquico da institução são identificadas somente no elemento ``<institution content-type="original">``.

Exemplo:

.. code-block:: xml

    ...
    <aff id="aff1">
      <institution content-type="orgname">Universidade de São Paulo</institution>
      <institution content-type="normalized">Universidade de São Paulo</institution>,
      <institution content-type="orgdiv2">Departamento de Fisiologia e Biofísica</institution>
      <institution content-type="orgdiv1">Instituto de Ciências Biomédicas</institution>
      <addr-line>
        <named-content content-type="city">São Paulo</named-content>
        <named-content content-type="state">SP</named-content>
      </addr-line>
      <country country="BR">Brasil</country>
      <institution content-type="original">Departamento de Fisiologia e Biofísica, Instituto de Ciências Biomédicas, Universidade de São Paulo, São Paulo, SP, Brasil</institution>
    </aff>
    ...


Deve-se especificar a afiliação completa como aparece no documento original.

Exemplo:

.. code-block:: xml

     <institution content-type="original">Técnica de Cardiopneumologia. Unidade de
     Fisiopatologia Respiratória, Serviço de Pneumologia, Centro Hospitalar Lisboa
     Norte, Lisboa, Portugal. mara@scielo.org</institution>



.. {"reviewed_on": "20160729", "by": "gandhalf_thewhite@hotmail.com"}
