.. _elemento-named-content:
 
<named-content>
^^^^^^^^^^^^^^^
 
Aparece em
  :ref:`elemento-addr-line`
 
Atributos obrigatórios
  1. content-type
 
Ocorre
  Zero ou mais vezes


Esta tag representa as informações de endereço que aparecem em afiliação e 
portanto irá dentro da tag de :ref:`elemento-addr-line` e obrigatoriamente 
terá o atributo ``@content-type``, podendo possuir os seguintes valores: 


+---------+------------+ 
| Valor   | Descrição  |
+=========+============+
| city    | Cidade     |
+---------+------------+
| state   | Estado     |
+---------+------------+
 

.. code-block:: xml
    
    ...
    <addr-line>
        <named-content content-type="city">
            São José do Rio Preto
        </named-content>
        <named-content content-type="state">
            São Paulo
        </named-content>
        ...
    </addr-line>
    ...
 
