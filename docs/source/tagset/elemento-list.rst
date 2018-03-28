.. _elemento-list:

<list>
======

Atributos obrigatórios:

  1. ``@list-type``

+----------------------------+--------------------+
| Aparece em                 | Ocorre             |
+============================+====================+
| :ref:`elemento-app`        | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-body`       | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-boxed-text` | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-disp-quote` | Zero ou mais vezes |
+----------------------------+--------------------+
| ``<list-item>``            | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-p`          | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-sec`        | Zero ou mais vezes |
+----------------------------+--------------------+



Elemento utilizado para identificação de uma lista que contem dois ou mais itens. Pode conter, opcionalmente, um elemento ``<title>`` ou um elemento :ref:`elemento-label`, exclusivamente.

O elemento :ref:`elemento-label` deve ser utilizado para identificar a legenda que pode acompanhar a lista. São consideradas legendas: legenda de equação, figura, referência, etc.

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


Exemplos:

  * :ref:`elemento-list-exemplo-1`
  * :ref:`elemento-list-exemplo-2`
  * :ref:`elemento-list-exemplo-3`




.. _elemento-list-exemplo-1:

Exemplo de lista numérica:
--------------------------

Donec rhoncus
 1. Nullam gravida tellus eget condimentum egestas.
 2. Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.
 3. Vestibulum urna elit, auctor ac fringilla ac, sagittis in ex.




Deve ser identificada como:

.. code-block:: xml

  ...
  <list list-type="order">
    <title>Donec rhoncus</title>
      <list-item>
        <p>Nullam gravida tellus eget condimentum egestas.</p>
      </list-item>
      <list-item>
        <p>Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.</p>
      </list-item>
      <list-item>
        <p>Vestibulum urna elit, auctor ac fringilla ac, sagittis in ex.</p>
      </list-item>
  </list>
  ...



.. _elemento-list-exemplo-2:

Exemplo lista numérica com sub-item:
------------------------------------


Vivamus cursus
 1. Nullam gravida tellus eget condimentum egestas.
   1.1. Curabitur luctus lorem ac feugiat pretium.
 2. Donec pulvinar odio ut enim lobortis, eu dignissim elit accumsan.




Deve ser identificada como:


.. code-block:: xml

  ...
  <list list-type="order">
    <title>Vivamus cursus</title>
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



.. _elemento-list-exemplo-3:


Exemplo lista com numeral romano:
---------------------------------

Nam commodo
 I. Morbi luctus elit enim.
 II. Nullam nunc leo.
 III. Proin id dui lorem.
 VI. Nunc finibus risus.



Deve ser identificada como:


.. code-block:: xml

  ...
  <list list-type="roman-lower">
    <title>Nam commodo</title>
      <list-item>
        <p>Morbi luctus elit enim.</p>
      </list-item>
      <list-item>
        <p>Nullam nunc leo.</p>
      </list-item>
      <list-item>
        <p>Proin id dui lorem.</p>
      </list-item>
      <list-item>
        <p>Nunc finibus risus.</p>
      </list-item>
  </list>
  ...











