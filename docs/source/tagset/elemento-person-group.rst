.. _elemento-person-group:

<person-group>
==============

Aparece em:

  :ref:`elemento-element-citation`
  :ref:`elemento-product`

Atributos obrigatórios:

  1. ``@person-group-type``

Ocorre:

  Zero ou mais vezes

Identifica grupo ou indivíduo criador/elaborador do :term:`documento`. Caso existam, os elementos :ref:`elemento-collab`, :ref:`elemento-role`, :ref:`elemento-name` e :ref:`elemento-etal`, somente devem ser identificados em ``<person-group>``.

Os valores possíveis para ``@person-group-type`` são:

+-----------+---------------+
| Valor     | Descrição     |
+===========+===============+
| author    | valor padrão  |
+-----------+---------------+
| compiler  | compilador    |
+-----------+---------------+
| editor    | editor        |
+-----------+---------------+
| translator| tradutor      |
+-----------+---------------+

Exemplo:

.. code-block:: xml

    ...
    <ref>
        <element-citation publication-type="book">
            <person-group person-group-type="author">
                <name>
                    <surname>Silva</surname>
                    <given-names>Jaqueline Figueiredo da</given-names>
                </name>
                <collab>Instituto Brasil Leitor</collab>
                ...
            </person-group>
            ...
        </element-citation>
        ...
    </ref>
    ...

.. note:: Em ``person-group`` o elemento :ref:`elemento-name` ocorre zero ou mais vezes.


.. {"reviewed_on": "20160729", "by": "gandhalf_thewhite@hotmail.com"}
