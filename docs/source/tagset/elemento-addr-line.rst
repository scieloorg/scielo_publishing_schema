.. _elemento-addr-line:

<addr-line>
===========

+---------------------+--------------------+
| Aparece em          | Ocorre             |
+=====================+====================+
| :ref:`elemento-aff` | Zero ou mais vezes |
+---------------------+--------------------+


Identifica a cidade e o estado da instituição vinculada ao autor, caso exista.

Exemplo:

.. code-block:: xml

    ...
    <addr-line>
        <named-content content-type="city">São Paulo</named-content>
        <named-content content-type="state">SP</named-content>
    </addr-line>
    ...


.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
