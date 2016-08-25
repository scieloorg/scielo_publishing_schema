.. _elemento-ref-list:

<ref-list>
==========

Aparece em:

  :ref:`elemento-back`

Ocorre:

  Zero ou mais vezes

Representa o conjunto de referências bibliográficas de um artigo e deve conter, obrigatoriamente, o elemento :ref:`elemento-ref`, que por sua vez contém :ref:`elemento-mixed-citation` e :ref:`elemento-element-citation`.

Em ``<ref-list>`` deve ser inserido um rótulo sob ``<title>`` identificando aquela seção de texto. O elemento ``<ref-list>`` permite também o elemento ``<label>`` para identificação de texto adicional ou subtítulo.


Exemplos:

* :ref:`elemento-ref-list-exemplo-1`
* :ref:`elemento-ref-list-exemplo-2`


.. _elemento-ref-list-exemplo-1:

Exemplo de ``<ref-list>`` simples:

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


.. _elemento-ref-list-exemplo-2:

Exemplo de ``<ref-list>`` com 2 títulos:
----------------------------------------

.. code-bloc:: xml

    ...
    <ref-list>
        <title>Referências Bibliográficas</title>
        <label>Fontes primárias</label>
        <ref id="B1">
            ...
        </ref>
        ...
    </ref-list>
    ...


.. note:: A ordem dos elementos é importante. O elemento ``<title>`` deve ser inserido antes do elemento ``<label>``.



.. {"reviewed_on": "20160628", "by": "gandhalf_thewhite@hotmail.com"}
