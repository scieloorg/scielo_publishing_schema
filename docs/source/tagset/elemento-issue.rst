.. _elemento-issue:

<issue>
-------

Aparece em:

  :ref:`elemento-article-meta`
  :ref:`elemento-element-citation`

Ocorre:

  1. Zero ou uma vez em :ref:`elemento-front`
  2. Zero ou mais vezes em :ref:`elemento-back`


Identifica o número de um fascículo (ou suplemento de número), seja este parte de um volume ou de um número especial.

Exemplos:

1. Em caso de suplemento de número em :ref:`elemento-front`, por exemplo, ``v10n5s1``:

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

2. Em caso de número especial em :ref:`elemento-front`, por exemplo, ``v10nspe``:

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


.. {"reviewed_on": "20160626", "by": "gandhalf_thewhite@hotmail.com"}
