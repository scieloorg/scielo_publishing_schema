.. _elemento-on-behalf-of:

<on-behalf-of>
^^^^^^^^^^^^^^

Aparece em:

  :ref:`elemento-contrib-group`
  :ref:`elemento-contrib`

Ocorre:

  Zero ou mais vezes

Utiliza-se quando um autor age como representante de um grupo ou organização na autoria ou edição de um artigo.


Exemplo:

.. code-block:: xml

    ...
    <contrib-group>
        ...
        <contrib>
            <name>
                <surname>Proietti</surname>
                <given-names>Fernando Augusto</given-names>
            </name>
            <xref ref-type="aff" rid="aff02">II</xref>
            <on-behalf-of>Interdisciplinary HTLV Research Group</on-behalf-of>
        </contrib>
        ...
    </contrib-group>
    ...


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
