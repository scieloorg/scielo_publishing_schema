.. _elemento-institution:

<institution>
=============

Este elemento possui :ref:`scielo-brasil`


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
| original   | Identifica a afiliação completa conforme consta no texto do artigo |
+------------+--------------------------------------------------------------------+



Exemplo:

.. code-block:: xml

    ...
    <aff id="aff1">
      <institution content-type="orgname">Universidade de São Paulo</institution>
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


Em ``content-type="original"``, deve-se especificar a afiliação completa como aparece no documento original.


Exemplo:

.. code-block:: xml

     <institution content-type="original">Técnica de Cardiopneumologia. Unidade de
     Fisiopatologia Respiratória, Serviço de Pneumologia, Centro Hospitalar Lisboa
     Norte, Lisboa, Portugal. mara@scielo.org</institution>


.. note:: 
 * Divisões abaixo do terceiro nível hierárquico da institução são identificadas somente no elemento ``<institution content-type="original">``.
 * Para mais informações sobre afiliação, verificar item "5.2.9. Afiliação de autores", dos `Critérios SciELO Brasil <http://www.scielo.br/avaliacao/Criterios_SciELO_Brasil_versao_revisada_atualizada_outubro_20171206.pdf>`_ .
