.. _elemento-role:

<role>
^^^^^^

Aparece em
  :ref:`elemento-collab`, 
  :ref:`elemento-contrib`, 
  :ref:`elemento-contrib-group`, 
  :ref:`elemento-element-citation`, 
  :ref:`elemento-person-group`, 
  :ref:`elemento-product`
 
Ocorre
  Zero ou mais vezes


A tag ``<role>`` (função ou papel) é usada para especificar o cargo 
(ou função) do contribuinte do documento.  

Exemplos:
 
.. code-block:: xml
 
    ...
    <contrib contrib-type="author">
        ...
        <name>
            <surname>Meader</surname>
            <given-names>CR</given-names>
            <prefix>Dr.</prefix>
            <suffix>Junior</suffix>
        </name>
        <xref ref-type="aff" rid="aff02">2</xref>
        <role>Pesquisador</role>
        ...
    </contrib>
    ...
 
 
.. code-block:: xml
 
    ...
    <element-citation publication-type="journal">
        ...
        <person-group person-group-type="author">
            <name>
                <surname>Petitti</surname>
                <given-names>DB</given-names>
                ...
            </name>
            <name>
                <surname>Crooks</surname>
                <given-names>VC</given-names>
                ...
            </name>
            <role>pesquisador</role>
            ...
        </person-group>
        ...
    </element-citation>
    ...
      
