.. _elemento-on-behalf-of:

<on-behalf-of>
^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-contrib-group`, 
  :ref:`elemento-contrib`
 
Ocorre
  Zero ou mais vezes


Utiliza-se quando um autor age como representante de um grupo ou 
organização. Ou seja, quando o autor diz ter escrito ou editado um trabalho 
em nome de uma organização. 

 
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
 
