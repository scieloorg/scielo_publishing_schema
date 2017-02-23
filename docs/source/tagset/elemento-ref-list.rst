.. _elemento-ref-list:

<ref-list>
==========

Aparece em:

  :ref:`elemento-back`
  :ref:`ref-list`

Ocorre:

  Zero ou mais vezes

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


.. {"reviewed_on": "20160628", "by": "gandhalf_thewhite@hotmail.com"}
