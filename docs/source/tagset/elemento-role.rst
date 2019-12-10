.. _elemento-role:

<role>
======

+----------------------------------+--------------------+
| Aparece em                       | Ocorre             |
+==================================+====================+
| :ref:`elemento-collab`           | Zero ou mais vezes |
+----------------------------------+--------------------+
| :ref:`elemento-contrib`          | Zero ou mais vezes |
+----------------------------------+--------------------+
| :ref:`elemento-contrib-group`    | Zero ou mais vezes |
+----------------------------------+--------------------+
| :ref:`elemento-element-citation` | Zero ou mais vezes |
+----------------------------------+--------------------+
| :ref:`elemento-person-group`     | Zero ou mais vezes |
+----------------------------------+--------------------+
| :ref:`elemento-product`          | Zero ou mais vezes |
+----------------------------------+--------------------+



``<role>`` (função ou papel) é usado para especificar o tipo de responsabilidade 
(ou função) do contribuinte do :term:`artigo`. Recomenda-se o uso da taxonomia 
CRediT para representar esta informação de maneira a prover maior transparência 
em relação às contribuições dos autores aos trabalhos científicos. Saiba mais 
detalhes em :ref:`taxonomia-credit`.

Exemplos:

    * :ref:`elemento-role-exemplo-1`
    * :ref:`elemento-role-exemplo-2`



.. _elemento-role-exemplo-1:

Exemplo de ``<role>`` em ``<contrib>``:
---------------------------------------

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
        <role content-type="https://dictionary.casrai.org/Contributor_Roles/Investigation">Pesquisador</role>
        ...
    </contrib>
    ...

.. _elemento-role-exemplo-2:

Exemplo de ``<role>`` em ``<element-citation>``:
------------------------------------------------

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

.. {"reviewed_on": "20160628", "by": "gandhalf_thewhite@hotmail.com"}
