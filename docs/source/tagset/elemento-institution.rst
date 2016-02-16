.. _elemento-institution:

<institution>
^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-aff`
 
Atributos obrigatórios
  1. content-type
 
Ocorre
  Zero ou mais vezes


Nesta tag especifica-se a instituição do autor, a qual pode ser dividida 
em até três níveis. Estes níveis serão definidos pelo atributo obrigatório 
``@content-type``, podendo possuir os seguintes valores:

+------------+--------------------------------------------------------------------+ 
| Valor      | Descrição                                                          |
+============+====================================================================+
| orgname    | Representando a instituição de nível hierárquico maior mencionado  |
|            | na afiliação.                                                      |
+------------+--------------------------------------------------------------------+ 
| orgdiv1    | Representando a primeira divisão da instituição mencionada em      |
|            | orgname.                                                           |
+------------+--------------------------------------------------------------------+ 
| orgdiv2    | Representando a segunda divisão da instituição mencionada em       |
|            | orgname.                                                           |
+------------+--------------------------------------------------------------------+ 
| normalized | Nome da instituição na forma normalizada pela SciELO.              |     
+------------+--------------------------------------------------------------------+
| original   | Utilizado para identificar a afiliação completa, conforme consta   |
|            | no PDF                                                             |
+------------+--------------------------------------------------------------------+ 
 

.. note:: No caso de mais divisões mencionadas em afiliações no PDF, 
          identifica-las somente na tag ``<institution content-type="original">``.
 

.. code-block:: xml
 
    ...
    <aff id="aff01">
        <institution content-type="orgname">
            Universidade de São Paulo
        </institution>
        <institution content-type="orgdiv1">
            Faculdade de Filosofia, Letras e Ciências Humanas
        </institution>
        <institution content-type="orgdiv2">
            Departamento de Vernáculos
        </institution>
        ...
    </aff>
    ...
 

Deve-se especificar a afiliação completa como aparece no documento 
original. 


.. code-block:: xml
 
     <institution content-type="original">Técnica de Cardiopneumologia. Unidade de
     Fisiopatologia Respiratória, Serviço de Pneumologia, Centro Hospitalar Lisboa
     Norte, Lisboa, Portugal. mara@scielo.org</institution>

