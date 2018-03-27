.. _elemento-volume:

<volume>
========

+----------------------------------+-----------------+
| Aparece em                       | Ocorre          |
+==================================+=================+
| :ref:`elemento-article-meta`     | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-element-citation` | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-product`          | Zero ou uma vez |
+----------------------------------+-----------------+


Identifica o volume de um fascículo. Caso haja suplemento de volume, este deve ser identificado em :ref:`elemento-issue`.


Exemplos:

 * :ref:`elemento-volume-exemplo-1`
 * :ref:`elemento-volume-exemplo-2`


.. _elemento-volume-exemplo-1:


Exemplo de ``<volume>`` em um fascículo:
--------------------------------------------------

 * Refere-se ao fascículo: volume 32, número 12 (``v32n12``):


.. code-block:: xml

    ...
    <front>
        ...
        <article-meta>
            ...
            <volume>32</volume>
            <issue>12</issue>
            ...
        </article-meta>
        ...
    </front>
    ...


.. _elemento-volume-exemplo-2:

Exemplo de ``<volume>`` em ``<element-citation>``:
--------------------------------------------------

 * Refere-se a um volume em uma referência


.. code-block:: xml

    ...
    <ref id="B01">
        ...
        <source>SciELO Journal</source>
        <volume>32</volume>
        <issue>12</issue>
        ...
    </ref>
    ...

