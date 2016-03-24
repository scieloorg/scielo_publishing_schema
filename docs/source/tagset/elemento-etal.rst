.. _elemento-etal:

<etal>
^^^^^^

Aparece em
  :ref:`elemento-person-group`
  :ref:`elemento-product`

Ocorre 
  Zero ou uma vez


Esta deve deve aparecer apenas em :ref:`elemento-person-group` e é usada 
quando existirem mais de três autores, onde indica-se apenas o primeiro, 
acrescentando-se a expressão et al. que significa "entre outros". 

Esta informação aparece primordialmente em referências. 

.. note:: Quando a informação aparecer no texto da referência, não é 
          necessário envolver o texto "et al." com a tag <etal></etal>, 
          basta inserir a tag na forma ``<etal/>``.


Exemplo:

.. code-block:: xml

    ...
    <ref>
        <element-citation publication-type="book">
            <person-group person-group-type="author">
                <name>
                    <surname>Borba</surname>
                    <given-names>Quincas</given-names>
                </name>
                <etal/>
                ...
            </person-group>
            ...
        </element-citation>
        ...
    </ref>
    ...

