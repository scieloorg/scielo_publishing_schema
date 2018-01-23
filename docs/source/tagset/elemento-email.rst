.. _elemento-email:

<email>
=======

+-------------------------+--------------------+
| Aparece em              | Ocorre             |
+=========================+====================+
| :ref:`elemento-aff`     | Zero ou mais vezes |
+-------------------------+--------------------+
| :ref:`elemento-corresp` | Zero ou mais vezes |
+-------------------------+--------------------+



Identifica endereços de email.

Exemplos:

    * :ref:`elemento-email-exemplo-1`
    * :ref:`elemento-email-exemplo-2`

.. _elemento-email-exemplo-1:

Exemplo de ``<email>`` em ``<aff>``:
------------------------------------

.. code-block:: xml

    ...
    <aff id="aff01">
        ...
        <email>ciaocomestai@foo.com</email>
        ...
    </aff>
    ...


.. _elemento-email-exemplo-2:

Exemplo de ``<email>`` em ``<corresp>``:
----------------------------------------

.. code-block:: xml

    ...
    <corresp id="c01">
        <label>*</label>
        <italic>E-mail:</italic>
        <email>allorafaciamocosi@foo.com</email>
    </corresp>
    ...


.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
