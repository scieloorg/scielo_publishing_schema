.. _elemento-elocation-id:

<elocation-id>
--------------

Aparece em
  :ref:`elemento-article-meta`,
  :ref:`elemento-element-citation`
 
Ocorre
  Zero ou uma vez 
 

Esta tag irá identificar uma paginação eletrônica, pode ser encontrada também 
em :ref:`elemento-element-citation`. Ela só deverá ser usada quando só houver 
um único número de paginação eletrônica, caso haja o intervalo de páginas 
deve-se optar pelo uso de :ref:`elemento-fpage` e :ref:`elemento-lpage`.
 
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


.. note:: ``elocation-id`` só deve ser identificado quando não houver informação de 
          :ref:`elemento-fpage`.
 
