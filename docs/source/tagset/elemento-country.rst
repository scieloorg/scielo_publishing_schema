.. _elemento-country:

<country>
=========

Atributos obrigatórios:

  1. ``@country``

+-------------------------+---------+
| Aparece em              | Ocorre  |
+=========================+=========+
| :ref:`elemento-aff`     | Uma vez |
+-------------------------+---------+
| :ref:`elemento-corresp` | Uma vez |
+-------------------------+---------+



Identifica o país em um endereço. Em afiliação de autor é elemento obrigatório.

O atributo ``@country`` é mandatório e deve ser preenchido de acordo com a Norma *ISO 3166*, cujos códigos tem dois caracteres alfabéticos em caixa alta.

Os códigos de país podem ser consultados através deste `link <http://www.iso.org/iso/country_codes>`_.


Exemplo:


.. code-block:: xml

    ...
    <aff id="aff01">
        ...
        <country country="BR">Brasil</country>
        ...
    </aff>
    ...

.. note:: Artigos do tipo "translation" não devem apresentar o elemento ``<country>`` em ``<aff>``. No caso de tradução, o detalhamento da afiliação é feito apenas uma vez e no arquivo de idioma principal.


.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
