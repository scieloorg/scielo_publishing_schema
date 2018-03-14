.. _elemento-issue:

<issue>
=======

+----------------------------------+--------------------+
| Aparece em                       | Ocorre             |
+==================================+====================+
| :ref:`elemento-article-meta`     | 1. Zero ou uma vez |
+----------------------------------+--------------------+
| :ref:`elemento-element-citation` | 1. Zero ou uma vez |
+----------------------------------+--------------------+



Identifica o fascículo (ou suplemento deste), seja como parte de um volume ou de fascículo especial.

Exemplos:

  * :ref:`elemento-issue-exemplo-1`
  * :ref:`elemento-issue-exemplo-2`
  * :ref:`elemento-issue-exemplo-3`
  * :ref:`elemento-issue-exemplo-4`



.. _elemento-issue-exemplo-1:

Exemplo de Suplemento de Fascículo em ``<front>``:
--------------------------------------------------

.. code-block:: xml

    ...
    <front>
        ...
        <article-meta>
            ...
            <volume>10</volume>
            <issue>5 suppl 1</issue>
            ...
        </article-meta>
        ...
    </front>
    ...



.. _elemento-issue-exemplo-2:

Exemplo de Fascículo Especial em ``<front>``:
---------------------------------------------

.. code-block:: xml

    ...
    <front>
        ...
        <article-meta>
            ...
            <volume>10</volume>
            <issue>spe</issue>
            ...
        </article-meta>
        ...
    </front>
    ...



.. _elemento-issue-exemplo-3:

Exemplo de Fascículo Especial com Numeração em ``<front>``:
-----------------------------------------------------------

.. code-block:: xml

    ...
    <front>
        ...
        <article-meta>
            ...
            <volume>59</volume>
            <issue>spe2</issue>
            ...
        </article-meta>
        ...
    </front>
    ...



.. _elemento-issue-exemplo-4:

Exemplo de ``<issue>`` em ``<element-citation>``:
-------------------------------------------------

.. code-block:: xml

    ...
    <ref id="B01">
        ...
        <source>text text text</source>
        <volume>10</volume>
        <issue>5</issue>
        ...
    </ref>
    ...


.. {"reviewed_on": "20170921", "by": "carolina.tanigushi@scielo.org"}
