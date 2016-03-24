.. _elemento-issue:

<issue>
-------
 
Aparece em
  :ref:`elemento-article-meta`, :ref:`elemento-element-citation`
 
Ocorre
  1. Zero ou uma vez em :ref:`elemento-front`
  2. Zero ou mais vezes em :ref:`elemento-back`

 
Em caso de suplemento de número em :ref:`elemento-front`, exemplo: ``v10n5s1``:
 
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

Em caso de número especial em :ref:`elemento-front`, exemplo: ``v10nspe``:
 
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
 
