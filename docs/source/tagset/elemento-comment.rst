.. _elemento-comment:

<comment>
^^^^^^^^^

Aparece em:

  :ref:`elemento-element-citation`

Ocorre:

  Zero ou mais vezes

Identifica informações adicionais, como por exemplo, "Disponível em:", que precede uma URL (ver elemento :ref:`elemento-ext-link`) em uma referência, e que não possuem marcação específica.

Exemplos:

.. code-block:: xml

    ...
    <element-citation>
        <comment>1 CD-ROM: color, 4 3/4 in.</comment>
    </element-citation>
    ...

.. code-block:: xml

    ...
    <element-citation>
        ...
        <comment>Disponível em: <ext-link ext-link-type="uri" xlink:href="http://www.scielo.org/">http://www.scielo.org/</ext-link>.</comment>
        ...
    </element-citation>
    ...


.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
