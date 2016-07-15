.. _elemento-email:

<email>
=======

Aparece em:

  :ref:`elemento-aff`
  :ref:`elemento-corresp`

Ocorre:

  Zero ou mais vezes


Identifica endereços de email.


Exemplos:

1. em ``<aff>``:

.. code-block:: xml

    ...
    <aff id="aff01">
        ...
        <email>ciaocomestai@foo.com</email>
        ...
    </aff>
    ...

2. em ``<corresp>``:

.. code-block:: xml

    ...
    <corresp id="c01">
        <label>*</label>
        <italic>E-mail:</italic>
        <email>allorafaciamocosi@foo.com</email>
    </corresp>
    ...


.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
