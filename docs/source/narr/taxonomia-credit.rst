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
Para mais informação acesse http://credit.niso.org/.

+----------------------------+------------------------------------------------------------------+
| Termo                      | URL                                                              |
+============================+==================================================================+
| Conceptualization          | http://credit.niso.org/contributor-roles/conceptualization/      |
+----------------------------+------------------------------------------------------------------+
| Data curation              | http://credit.niso.org/contributor-roles/data-curation/          |
+----------------------------+------------------------------------------------------------------+
| Formal analysis            | http://credit.niso.org/contributor-roles/formal-analysis/        |
+----------------------------+------------------------------------------------------------------+
| Funding acquisition        | http://credit.niso.org/contributor-roles/funding-acquisition/    |
+----------------------------+------------------------------------------------------------------+
| Investigation              | http://credit.niso.org/contributor-roles/investigation/          |
+----------------------------+------------------------------------------------------------------+
| Methodology                | http://credit.niso.org/contributor-roles/methodology/            |
+----------------------------+------------------------------------------------------------------+
| Project administration     | http://credit.niso.org/contributor-roles/project-administration/ |
+----------------------------+------------------------------------------------------------------+
| Resources                  | http://credit.niso.org/contributor-roles/resources/              |
+----------------------------+------------------------------------------------------------------+
| Software                   | http://credit.niso.org/contributor-roles/software/               |
+----------------------------+------------------------------------------------------------------+
| Supervision                | http://credit.niso.org/contributor-roles/supervision/            |
+----------------------------+------------------------------------------------------------------+
| Validation                 | http://credit.niso.org/contributor-roles/validation/             |
+----------------------------+------------------------------------------------------------------+
| Visualization              | http://credit.niso.org/contributor-roles/visualization/          |
+----------------------------+------------------------------------------------------------------+
| Writing – original draft   | http://credit.niso.org/contributor-roles/writing-original-draft/ |
+----------------------------+------------------------------------------------------------------+
| Writing – review & editing | http://credit.niso.org/contributor-roles/writing-review-editing/ |
+----------------------------+------------------------------------------------------------------+

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
            <role content-type="http://credit.niso.org/contributor-roles/conceptualization/">Conceptualization</role>
            <role content-type="http://credit.niso.org/contributor-roles/data-curation/">Data curation</role>
            <role content-type="http://credit.niso.org/contributor-roles/formal-analysis/">Formal analysis</role>
            <role content-type="http://credit.niso.org/contributor-roles/investigation/">Investigation</role>
            <role content-type="http://credit.niso.org/contributor-roles/writing-original-draft/">Writing - original draft</role>
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
            <role content-type="http://credit.niso.org/contributor-roles/conceptualization/">Conceitualização</role>
            <role>Editor de seção</role>
            <xref ref-type="aff" rid="aff02">2</xref>
        </contrib>
        ...
    </contrib-group>
    ...

Referências

* JATS4R CRediT Taxonomy Guidelines: https://jats4r.org/credit-taxonomy
* NISO JATS 1.1: http://jats.nlm.nih.gov/publishing/tag-library/1.1/
* NISO Contributor Roles: http://credit.niso.org/
* Implementing CRediT: http://credit.niso.org/implementing-credit/
