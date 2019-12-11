.. _taxonomia-credit:

Contribuição dos autores (taxonomia CRediT)
===========================================

A taxonomia CRediT proporciona uma maneira de representar informação sobre a 
contribuição individual dos autores em documentos XML que seguem a especificação 
SciELO PS. O propósito da taxonomia CRediT é prover transparência em relação às 
contribuições dos autores em trabalhos científicos, possibilitando melhorias nos 
sistemas de atribuição, crédito e prestação de contas.

A tabela a seguir apresenta os termos definidos pela taxonomia CRediT. É 
importante notar que múltiplos termos podem ser atribuídos a um único contribuidor. 
Para mais informação acesse https://dictionary.casrai.org/Contributor_Roles.

+----------------------------+------------------------------------------------------------------------+
| Termo                      | URL                                                                    |
+============================+========================================================================+
| Conceptualization          | https://dictionary.casrai.org/Contributor_Roles/Conceptualization      |
+----------------------------+------------------------------------------------------------------------+
| Data curation              | https://dictionary.casrai.org/Contributor_Roles/Data_curation          |
+----------------------------+------------------------------------------------------------------------+
| Formal analysis            | https://dictionary.casrai.org/Contributor_Roles/Formal_analysis        |
+----------------------------+------------------------------------------------------------------------+
| Funding acquisition        | https://dictionary.casrai.org/Contributor_Roles/Funding_acquisition    |
+----------------------------+------------------------------------------------------------------------+
| Investigation              | https://dictionary.casrai.org/Contributor_Roles/Investigation          |
+----------------------------+------------------------------------------------------------------------+
| Methodology                | https://dictionary.casrai.org/Contributor_Roles/Methodology            |
+----------------------------+------------------------------------------------------------------------+
| Project administration     | https://dictionary.casrai.org/Contributor_Roles/Project_administration |
+----------------------------+------------------------------------------------------------------------+
| Resources                  | https://dictionary.casrai.org/Contributor_Roles/Resources              |
+----------------------------+------------------------------------------------------------------------+
| Software                   | https://dictionary.casrai.org/Contributor_Roles/Software               |
+----------------------------+------------------------------------------------------------------------+
| Supervision                | https://dictionary.casrai.org/Contributor_Roles/Supervision            |
+----------------------------+------------------------------------------------------------------------+
| Validation                 | https://dictionary.casrai.org/Contributor_Roles/Validation             |
+----------------------------+------------------------------------------------------------------------+
| Visualization              | https://dictionary.casrai.org/Contributor_Roles/Visualization          |
+----------------------------+------------------------------------------------------------------------+
| Writing – original draft   | https://dictionary.casrai.org/Contributor_Roles/Writing_original_draft |
+----------------------------+------------------------------------------------------------------------+
| Writing – review & editing | https://dictionary.casrai.org/Contributor_Roles/Writing_review_editing |
+----------------------------+------------------------------------------------------------------------+

O papel do autor em relação ao artigo deve ser expresso por um termo no elemento 
`<role>` do XML. Este termo pode ou não ser idêntico aos da tabela acima, desde 
que a URL correspondente definida pela taxonomia CRediT seja informada no 
atributo `@content-type`.

Exemplo:

.. code-block:: xml

    ...
    <contrib-group>
        <contrib contrib-type="author">
            <name>
                <surname>Freitas</surname>
                <given-names>Ismael Forte</given-names>
                <suffix>Júnior</suffix>
            </name>
            <role content-type="https://dictionary.casrai.org/Contributor_Roles/Conceptualization">Conceptualization</role>
            <role content-type="https://dictionary.casrai.org/Contributor_Roles/Data_curation">Data curation</role>
            <role content-type="https://dictionary.casrai.org/Contributor_Roles/Formal_analysis">Formal analysis</role>
            <role content-type="https://dictionary.casrai.org/Contributor_Roles/Investigation">Investigation</role>
            <role content-type=" https://dictionary.casrai.org/Contributor_Roles/Writing_original_draft">Writing - original draft</role>
            <xref ref-type="aff" rid="aff01">1</xref>
        </contrib>
        ...
    </contrib-group>
    ...

É importante notar que o elemento `<role>` também pode ser utilizado para 
representar informação não relacionada com a taxonomia CRediT, e nestes casos a 
decisão sobre como e qual informação incluir é de responsabilidade de cada 
organização e não há a necessidade de utilizar o atributo `@content-type`.

Exemplo:

.. code-block:: xml

    ...
    <contrib-group>
        <contrib contrib-type="author">
            <name>
                <surname>Silva</surname>
                <given-names>Rosângela</given-names>
            </name>
            <role content-type="https://dictionary.casrai.org/Contributor_Roles/Conceptualization">Conceitualização</role>
            <role>Editor de seção</role>
            <xref ref-type="aff" rid="aff02">2</xref>
        </contrib>
        ...
    </contrib-group>
    ...

Referências

* JATS4R CRediT Taxonomy Guidelines: https://jats4r.org/credit-taxonomy
* NISO JATS 1.1: http://jats.nlm.nih.gov/publishing/tag-library/1.1/
* CASRAI Contributor Roles: https://dictionary.casrai.org/Contributor_Roles
* CRediT: Contributor Role Taxonomy - Going beyond authorship: https://docs.google.com/document/d/1aJxrQXYHW5U6By3KEAHrx1Iho6ioeh3ohNsRMwsoGPM
