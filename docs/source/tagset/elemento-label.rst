.. _elemento-label:
 
<label>
-------

Aparece em
  :ref:`elemento-aff`,
  :ref:`elemento-corresp`, 
  :ref:`elemento-fn`,
  :ref:`elemento-fig`,
  :ref:`elemento-table-wrap`,
  :ref:`elemento-disp-formula`,
  :ref:`elemento-media`,
  :ref:`elemento-supplementary-material`,
  :ref:`elemento-list`,
  ``list-item``,
  :ref:`elemento-ref`,
  ``glossary``,
  :ref:`elemento-app`,
  :ref:`elemento-def-list`
  :ref:`elemento-verse-group`
  :ref:`elemento-boxed-text`

Ocorre
  Zero ou mais vezes


A tag ``<label>`` é responsável pela identificação numérica ou alfabética 
que faz a ligação entre etiquetas.

Exemplos:
 
.. code-block:: xml
 
    <aff id="aff01">
        <label>a</label>
        ...
    </aff>


.. code-block:: xml

    <corresp id="c01">
       <label>*</label>
       ...
    </corresp>


.. code-block:: xml

    <fig id="f01">
        <label>Figure 1</label>
        ...
    </fig>
    

.. code-block:: xml

    <table-wrap id="t01">
        <label>Table 1</label>
        ...
    </table-wrap>
 

.. code-block:: xml

    <ref id="B01">1</ref>
        <label>1</label>
        ...
    </ref>
 

.. code-block:: xml

    <app id="app01">
        <label>Apêndice</label>
        ...
    </app>
 
