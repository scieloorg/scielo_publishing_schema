.. _elemento-ref-list:

<ref-list>
==========

Este elemento possui :ref:`scielo-brasil`


+--------------------------+--------------------+
| Aparece em               | Ocorre             |
+==========================+====================+
| :ref:`elemento-back`     | Zero ou mais vezes |
+--------------------------+--------------------+
| :ref:`elemento-ref-list` | Zero ou mais vezes |
+--------------------------+--------------------+


Representa o conjunto de referências bibliográficas de um artigo e deve conter, obrigatoriamente, o elemento :ref:`elemento-ref`, que por sua vez contém :ref:`elemento-mixed-citation` e :ref:`elemento-element-citation`.

Em ``<ref-list>`` deve ser inserido um rótulo sob ``<title>`` identificando aquela seção de texto.

.. _elemento-ref-list-exemplo-1:

Exemplo de ``<ref-list>`` simples:
----------------------------------

.. code-block:: xml

    ...
    <ref-list>
        <title>Referência Bibliográfica</title>
        <ref id="B1">
            ...
        </ref>
        ...
    </ref-list>
    ...


