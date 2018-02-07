.. _elemento-label:

<label>
=======


+----------------------------------------+-----------------+
| Aparece em                             | Ocorre          |
+========================================+=================+
| :ref:`elemento-aff`                    | Zero ou uma vez |
+----------------------------------------+-----------------+
| :ref:`elemento-app`                    | Zero ou uma vez |
+----------------------------------------+-----------------+
| :ref:`elemento-boxed-text`             | Zero ou uma vez |
+----------------------------------------+-----------------+
| :ref:`elemento-corresp`                | Zero ou uma vez |
+----------------------------------------+-----------------+
| :ref:`elemento-def-list`               | Zero ou uma vez |
+----------------------------------------+-----------------+
| :ref:`elemento-disp-formula`           | Zero ou uma vez |
+----------------------------------------+-----------------+
| :ref:`elemento-fig`                    | Zero ou uma vez |
+----------------------------------------+-----------------+
| :ref:`elemento-fn`                     | Zero ou uma vez |
+----------------------------------------+-----------------+
| ``glossary``                           | Zero ou uma vez |
+----------------------------------------+-----------------+
| :ref:`elemento-list`                   | Zero ou uma vez |
+----------------------------------------+-----------------+
| ``list-item``                          | Zero ou uma vez |
+----------------------------------------+-----------------+
| :ref:`elemento-media`                  | Zero ou uma vez |
+----------------------------------------+-----------------+
| :ref:`elemento-ref`                    | Zero ou uma vez |
+----------------------------------------+-----------------+
| :ref:`elemento-supplementary-material` | Zero ou uma vez |
+----------------------------------------+-----------------+
| :ref:`elemento-table-wrap`             | Zero ou uma vez |
+----------------------------------------+-----------------+
| :ref:`elemento-verse-group`            | Zero ou uma vez |
+----------------------------------------+-----------------+



``<label>`` tem como função identificar, numérica e/ou alfabéticamente, um grupo de elementos de tipo específico.

Exemplos:

 * :ref:`elemento-label-exemplo-1`
 * :ref:`elemento-label-exemplo-2`
 * :ref:`elemento-label-exemplo-3`
 * :ref:`elemento-label-exemplo-4`
 * :ref:`elemento-label-exemplo-5`
 * :ref:`elemento-label-exemplo-6`


.. _elemento-label-exemplo-1:

Exemplo em ``<aff>``:
---------------------


.. code-block:: xml

    <aff id="aff01">
        <label>a</label>
        ...
    </aff>



.. _elemento-label-exemplo-2:

Exemplo em ``<corresp>``:
-------------------------

.. code-block:: xml

    <corresp id="c01">
       <label>*</label>
       ...
    </corresp>


.. _elemento-label-exemplo-3:

Exemplo em ``<fig>``:
---------------------

.. code-block:: xml

    <fig id="f01">
        <label>Figure 1</label>
        ...
    </fig>


.. _elemento-label-exemplo-4:

Exemplo em ``<table-wrap>``:
----------------------------

.. code-block:: xml

    <table-wrap id="t01">
        <label>Table 1</label>
        ...
    </table-wrap>


.. _elemento-label-exemplo-5:

Exemplo em ``<ref>``:
---------------------

.. code-block:: xml

    <ref id="B01">1</ref>
        <label>1</label>
        ...
    </ref>


.. _elemento-label-exemplo-6:

Exemplo em ``<app>``:
---------------------

.. code-block:: xml

    <app id="app01">
        <label>Apêndice</label>
        ...
    </app>


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
