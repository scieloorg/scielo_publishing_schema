.. _elemento-ref-list:

<ref-list>
----------

Aparece em
  :ref:`elemento-back`

Ocorre
  Zero ou mais vezes

  O conjunto de referências biliográficas de um artigo é representado pela tag
  ``<ref-list>``. Esse elemento deve conter, obrigatoriamente, três tags: 
  :ref:`elemento-ref`, :ref:`elemento-mixed-citation` e
  :ref:`elemento-element-citation`.

Em ``<ref-list>`` deve ser inserida uma informação de etiqueta ``title``.

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

