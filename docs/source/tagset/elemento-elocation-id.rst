.. _elemento-elocation-id:

<elocation-id>
--------------

Aparece em:

  :ref:`elemento-article-meta`
  :ref:`elemento-element-citation`

Ocorre:

  Zero ou uma vez


Identifica uma paginação eletrônica. Pode ocorrer também em :ref:`elemento-element-citation`. Entretanto, só deverá ser utilizado quando houver um único número de paginação eletrônica. Para um intervalo de páginas, deve-se optar pelo uso de :ref:`elemento-fpage` e :ref:`elemento-lpage`.

Exemplo:

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


.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
