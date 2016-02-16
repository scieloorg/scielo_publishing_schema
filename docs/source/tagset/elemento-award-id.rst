.. _elemento-award-id:
 
<award-id>
^^^^^^^^^^

Aparece em
  :ref:`elemento-award-group`
 
Ocorre
  Uma ou mais vezes


Esta tag deve ficar dentro de :ref:`elemento-award-group` e nela será 
especificado o número de contrato estipulado pela instituição financiadora.
 
Exemplo:

.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <funding-group>           
            <award-group>
                <funding-source>CNPq</funding-source>
                <award-id>00001</award-id>
                <award-id>00002</award-id>
            </award-group>
            <award-group>
                <funding-source>FAPESP</funding-source>
                <award-id>0000X</award-id>
            </award-group>
        </funding-group>
        ...
    </article-meta>
    ...
     
 
