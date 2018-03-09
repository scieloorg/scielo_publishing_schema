.. _elemento-elocation-id:

<elocation-id>
==============

Aparece em:

  :ref:`elemento-article-meta`
  :ref:`elemento-element-citation`

Ocorre:

  Zero ou uma vez


Identificador eletrônico que substitui paginação sequencial de um documento.

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

.. note:: ``<elocation-id>`` só deve ser utilizado quando não houver informação de :ref:`elemento-fpage`.


.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
