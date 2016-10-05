.. _elemento-issue:

<issue>
=======

Aparece em:

  :ref:`elemento-article-meta`
  :ref:`elemento-element-citation`

Ocorre:

  1. Zero ou uma vez


Identifica o fascículo (ou suplemento deste), seja como parte de um volume ou de fascículo especial.

Exemplos:

  * :ref:`elemento-issue-exemplo-1`
  * :ref:`elemento-issue-exemplo-2`
  * :ref:`elemento-issue-exemplo-3`



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


.. {"reviewed_on": "20160626", "by": "gandhalf_thewhite@hotmail.com"}
