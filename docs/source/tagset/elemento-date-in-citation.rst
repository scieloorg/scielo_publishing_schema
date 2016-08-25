.. _elemento-date-in-citation:

<date-in-citation>
==================

Aparece em:

  :ref:`elemento-element-citation`

Atributos obrigatórios:

  1. ``@content-type``

Ocorre:

  Zero ou mais vezes

Indica a data de citação em uma referência. O atributo ``@content-type`` é obrigatório e deve conter um valor que qualifica a data de acesso ou a data de atualização do :term:`documento`, cujos valores possíveis são:

* ``update``;
* ``access-date``.


Exemplos:

  * :ref:`elemento-datcitation-exemplo-1`
  * :ref:`elemento-datcitation-exemplo-2`


.. _elemento-datcitation-exemplo-1:

Exemplo de ``<date-in-citation>`` do tipo data de acesso:
---------------------------------------------------------

.. code-block:: xml

    ...
    <element-citation>
        <date-in-citation content-type="access-date">cited 2007 Feb 21</date-in-citation>
    </element-citation>
    ...


.. _elemento-datcitation-exemplo-2:

Exemplo ``<date-in-citation>`` do tipo data de atualização:
-----------------------------------------------------------

.. code-block:: xml

    ...
    <element-citation>
        <date-in-citation content-type="updated">2006 Jul 20</date-in-citation>
    </element-citation>
    ...


.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
