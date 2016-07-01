.. _elemento-named-content:

<named-content>
^^^^^^^^^^^^^^^

Aparece em:

  :ref:`elemento-addr-line`

Atributos obrigatórios:

  1. ``@content-type``

Ocorre:

  Zero ou mais vezes


Representa as informações de endereço na afiliação, sendo portanto, parte de :ref:`elemento-addr-line`. Tem, obrigatoriamente, o atributo ``@content-type`` cujos valores possíveis são:

+---------+------------+
| Valor   | Descrição  |
+=========+============+
| city    | Cidade     |
+---------+------------+
| state   | Estado     |
+---------+------------+

Exemplo:

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


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
