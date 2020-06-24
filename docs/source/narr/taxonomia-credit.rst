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
Para mais informação acesse https://casrai.org/term/contributor-roles/.

+----------------------------+---------------------------------------------------------------------------------------------------------+
| Termo                      | URL                                                                                                     |
+============================+=========================================================================================================+
| Conceptualization          | https://casrai.org/term/contributor-roles-conceptualization/                                            |
+----------------------------+---------------------------------------------------------------------------------------------------------+
| Data curation              | https://casrai.org/term/contributor-roles-data-curation/                                                |
+----------------------------+---------------------------------------------------------------------------------------------------------+
| Formal analysis            | https://casrai.org/term/contributor-roles-formal-analysis/                                              |
+----------------------------+---------------------------------------------------------------------------------------------------------+
| Funding acquisition        | https://casrai.org/term/contributor-roles-funding-acquisition/                                          |
+----------------------------+---------------------------------------------------------------------------------------------------------+
| Investigation              | https://casrai.org/term/contributor-roles-investigation/                                                |
+----------------------------+---------------------------------------------------------------------------------------------------------+
| Methodology                | https://casrai.org/term/contributor-roles-methodology/                                                  |
+----------------------------+---------------------------------------------------------------------------------------------------------+
| Project administration     | https://casrai.org/term/contributor-roles-project-administration/                                       |
+----------------------------+---------------------------------------------------------------------------------------------------------+
| Resources                  | https://casrai.org/term/contributor-roles-resources/                                                    |
+----------------------------+---------------------------------------------------------------------------------------------------------+
| Software                   | https://casrai.org/term/contributor-roles-software/                                                     |
+----------------------------+---------------------------------------------------------------------------------------------------------+
| Supervision                | https://casrai.org/term/contributor-roles-supervision/                                                  |
+----------------------------+---------------------------------------------------------------------------------------------------------+
| Validation                 | https://casrai.org/term/contributor-roles-validation/                                                   |
+----------------------------+---------------------------------------------------------------------------------------------------------+
| Visualization              | https://web.archive.org/web/20180313224017/http://dictionary.casrai.org/Contributor_Roles/Visualization |
+----------------------------+---------------------------------------------------------------------------------------------------------+
| Writing – original draft   | https://casrai.org/term/contributor-roles-writing-original-draft/                                       |
+----------------------------+---------------------------------------------------------------------------------------------------------+
| Writing – review & editing | https://casrai.org/term/contributor-roles-writing-review-editing/                                       |
+----------------------------+---------------------------------------------------------------------------------------------------------+

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
            <role content-type="https://casrai.org/term/contributor-roles-conceptualization/">Conceptualization</role>
            <role content-type="https://casrai.org/term/contributor-roles-data-curation/">Data curation</role>
            <role content-type="https://casrai.org/term/contributor-roles-formal-analysis/">Formal analysis</role>
            <role content-type="https://casrai.org/term/contributor-roles-investigation/">Investigation</role>
            <role content-type="https://casrai.org/term/contributor-roles-writing-original-draft/">Writing - original draft</role>
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
            <role content-type="https://casrai.org/term/contributor-roles-conceptualization/">Conceitualização</role>
            <role>Editor de seção</role>
            <xref ref-type="aff" rid="aff02">2</xref>
        </contrib>
        ...
    </contrib-group>
    ...

Referências

* JATS4R CRediT Taxonomy Guidelines: https://jats4r.org/credit-taxonomy
* NISO JATS 1.1: http://jats.nlm.nih.gov/publishing/tag-library/1.1/
* CASRAI Contributor Roles: https://casrai.org/term/contributor-roles/
* CRediT: Contributor Role Taxonomy - Going beyond authorship: https://docs.google.com/document/d/1aJxrQXYHW5U6By3KEAHrx1Iho6ioeh3ohNsRMwsoGPM
