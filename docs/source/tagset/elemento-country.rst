.. _elemento-country:

<country>
^^^^^^^^^

Aparece em
  :ref:`elemento-aff`

Atributos obrigatórios
  1. country
 
Ocorre
  Uma vez


Identifica o país da afiliação.
 
A tag deve possuir o atributo ``@country`` e nele deve ser atribuído o código 
do país de acordo com a Norma *ISO 3166*, de dois caracteres alfabéticos.

Para consultar o código do país consulte o link: 
https://www.iso.org/obp/ui/#iso:pub:PUB500001:en


Exemplo:


.. code-block:: xml

    ...
    <aff id="aff01">
        ...
        <country country="BR">Brasil</country>
        ...
    </aff>
    ...

.. note:: Artigos do tipo "translation" não devem apresentar o elemento ``<country>`` em ``<aff>``.
O detalhamento da afiliação, no caso de tradução, é feito apenas 1 vez no arquivo de idioma principal.

