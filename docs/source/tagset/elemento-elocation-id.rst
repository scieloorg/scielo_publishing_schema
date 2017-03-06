.. _elemento-elocation-id:

<elocation-id>
==============

Aparece em:

  :ref:`elemento-article-meta`
  :ref:`elemento-element-citation`

Ocorre:

  Zero ou uma vez


Identificar bibliográfico de um documento que não possui numeração sequencial de páginas tradicionalmente usada em publicações impressas. Pode ocorrer também em :ref:`elemento-element-citation`. Para um intervalo de páginas, deve-se optar pelo uso de :ref:`elemento-fpage` e :ref:`elemento-lpage`.

Exemplo em :ref:`elemento-article-meta`:

.. code-block:: xml

    ...
    <article-meta>
        ...
        <volume>10</volume>
        <issue>2</issue>
        <elocation-id>0102961</elocation-id>
        ...
    </article-meta>
    ...

.. note:: ``<elocation-id>`` só deve ser utilizado quando não houver informação de :ref:`elemento-fpage`.


Exemplo em :ref:`elemento-element-citation`:

.. code-block:: xml

    ...
    <element-citation publication-type="journal">
        ...
        <source>PLoS ONE</source>
        <volume>6</volume>
        <elocation-id>e27721</elocation-id>
    </element-citation>
    ...


.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
