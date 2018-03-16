.. _elemento-institution-id:

<institution-id>
================

+-------------------------+--------------------+
| Aparece em              | Ocorre             |
+=========================+====================+
| ``<institution-wrap>``  | Zero ou mais vezes |
+-------------------------+--------------------+


Elemento que designa em afiliação um identificador padronizado para instituição.


Exemplo:

.. code-block:: xml

    ...
    <aff id="aff2">
      <label>2</label>
        <institution content-type="original">Universidade de São Paulo (USP), São Paulo, SP, Brasil. 0000 0004 1937 0722</institution>
        <institution content-type="normalized">Universidade de São Paulo</institution>
        <institution content-type="orgname">Universidade de São Paulo (USP)</institution>
        <institution-wrap>
            <institution-id institution-id-type="insi">0000 0004 1937 0722</institution-id>
        <institution-wrap>
    </aff>
