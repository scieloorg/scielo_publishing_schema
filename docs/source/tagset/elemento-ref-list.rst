.. _elemento-ref-list:

<ref-list>
==========

Aparece em:

  :ref:`elemento-back`

Ocorre:

  Zero ou mais vezes

Representa o conjunto de referências bibliográficas de um artigo e deve conter, obrigatoriamente, três elementos: :ref:`elemento-ref`, :ref:`elemento-mixed-citation` e :ref:`elemento-element-citation`.

Em ``<ref-list>`` deve ser inserido um rótulo sob ``<title>`` identificando aquela seção de texto.

Exemplo:

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
