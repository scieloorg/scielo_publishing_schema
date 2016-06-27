.. _elemento-label:

<label>
-------

Aparece em:

  :ref:`elemento-aff`
  :ref:`elemento-corresp`
  :ref:`elemento-fn`
  :ref:`elemento-fig`
  :ref:`elemento-table-wrap`
  :ref:`elemento-disp-formula`
  :ref:`elemento-media`
  :ref:`elemento-supplementary-material`
  :ref:`elemento-list`
  ``list-item``
  :ref:`elemento-ref`
  ``glossary``
  :ref:`elemento-app`
  :ref:`elemento-def-list`
  :ref:`elemento-verse-group`
  :ref:`elemento-boxed-text`

Ocorre:

  Zero ou mais vezes


``<label`` tem como função identificar, numérica e/ou alfabéticamente, um grupo de elementos de tipo específico.

Exemplos:

1. em ``<aff>``:

.. code-block:: xml

    <aff id="aff01">
        <label>a</label>
        ...
    </aff>

2. em ``<corresp>``:

.. code-block:: xml

    <corresp id="c01">
       <label>*</label>
       ...
    </corresp>

3. em ``<fig>``:

.. code-block:: xml

    <fig id="f01">
        <label>Figure 1</label>
        ...
    </fig>

4. em ``<table-wrap>``:

.. code-block:: xml

    <table-wrap id="t01">
        <label>Table 1</label>
        ...
    </table-wrap>

5. em ``<ref>``:

.. code-block:: xml

    <ref id="B01">1</ref>
        <label>1</label>
        ...
    </ref>

6. em ``<app>``:

.. code-block:: xml

    <app id="app01">
        <label>Apêndice</label>
        ...
    </app>


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
