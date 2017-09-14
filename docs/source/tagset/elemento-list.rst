.. _elemento-list:

<list>
======

Aparece em:

  :ref:`elemento-app`
  :ref:`elemento-body`
  :ref:`elemento-boxed-text`
  :ref:`elemento-disp-quote`
  ``<list-item>``
  :ref:`elemento-p`
  :ref:`elemento-sec`
      
Atributos obrigatórios:

  1. ``@list-type``

Ocorre:

  Zero ou mais vezes


Lista contendo dois ou mais itens. Pode conter, opcionalmente, um elemento ``<title>`` ou um elemento ``<label>``, exclusivamente.

O elemento ``<label>`` deve ser utilizado para identificar a legenda que pode acompanhar a lista. São consideradas legendas: legenda de equação, figura, referência, etc.

O atributo ``@list-type`` especifica o prefixo a ser utilizado no marcador da lista, cujos valores possíveis são:

+----------------+-------------------------------------------------------------------+
| Valor          | Descrição                                                         |
+================+===================================================================+
| order          | Lista ordenada, cujo prefixo é um número ou letra, dependendo     |
|                | do estilo utilizado.                                              |
+----------------+-------------------------------------------------------------------+
| bullet         | Lista desordenada, cujo prefixo utilizado é um ponto, barra ou    |
|                | outro símbolo.                                                    |
+----------------+-------------------------------------------------------------------+
| alpha-lower    | Lista ordenada, cujo prefixo é um caractere alfabético minúsculo. |
+----------------+-------------------------------------------------------------------+
| alpha-upper    | Lista ordenada, cujo prefixo é um caractere alfabético maiúsculo. |
+----------------+-------------------------------------------------------------------+
| roman-lower    | Lista ordenada, cujo prefixo é um numeral romano minúsculo.       |
+----------------+-------------------------------------------------------------------+
| roman-upper    | Lista ordenada, cujo prefixo é um numeral romano maiúsculo.       |
+----------------+-------------------------------------------------------------------+
| simple         | Lista simples, sem prefixo nos itens.                             |
+----------------+-------------------------------------------------------------------+


Exemplo:


  Lista Numérica:

  1. Nullam gravida tellus eget condimentum egestas.

     1.1. Curabitur luctus lorem ac feugiat pretium.

  2. Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.


Deve ser identificada como:

.. code-block:: xml

    ...
    <list list-type="order">
        <title>Lista Númerica</title>
        <list-item>
            <p>Nullam gravida tellus eget condimentum egestas.</p>
            	<list list-type="order">
                	<list-item>
                    	<p>Curabitur luctus lorem ac feugiat pretium.</p>
                	</list-item>
            	</list>
        </list-item>
        <list-item>
            <p>Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.</p>
        </list-item>
    </list>
    ...

.. note:: Note que o marcador não deve ser identificado como parte do texto no elemento ``<list-item>``.


.. {"reviewed_on": "20170912", "by": "carolina.tanigushi@scielo.org"}
