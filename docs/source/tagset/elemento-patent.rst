.. _elemento-patent:

<patent>
^^^^^^^^

Aparece em
  :ref:`elemento-element-citation`
  
Atributos obrigatórios 
  ``@country``

Ocorre 
  Zero ou uma vez

Tag utilizada para identificar um número de patente. Deve possuir o atributo 
``@country`` e nele deve ser atribuído o código do país de acordo com a 
Norma ISO 3166, com dois caracteres alfabéticos.

Para consultar ao código do país consulte o link da norma ISO: https://www.iso.org/obp/ui/#iso:pub:PUB500001:en

Exemplo de patente americana:

.. code-block:: xml

    ...
    <element-citation>
        <patent country="US">US 6,980,855</patent>
    </element-citation>
    ...


