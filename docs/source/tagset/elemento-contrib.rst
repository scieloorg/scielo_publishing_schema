.. _elemento-contrib:

<contrib>
=========

Atributos obrigatórios:

  1. ``@contrib-type``

+-------------------------------+-------------------+
| Aparece em                    | Ocorre            |
+===============================+===================+
| :ref:`elemento-contrib-group` | Uma ou mais vezes |
+-------------------------------+-------------------+



Identifica dados individuais, institucionais ou de grupo, de contribuintes do 
artigo, podendo ser inclusive anônimos. :ref:`elemento-name`, :ref:`elemento-collab`, 
:ref:`elemento-on-behalf-of`, :ref:`elemento-xref`, :ref:`elemento-role` e 
``<anonymous>`` podem ser encontrados neste elemento.

O atributo ``@contrib-type`` define o tipo de contribuição e pode ter os valores:

+--------------------+----------------------------------------------------------------+
| Valor              | Descrição                                                      |
+====================+================================================================+
| author             | Autor do conteúdo.                                             |
+--------------------+----------------------------------------------------------------+
| compiler           | Adaptador - Indivíduo que compilou o conteúdo a partir de      |
|                    | várias fontes.                                                 |
+--------------------+----------------------------------------------------------------+
| editor             | Editor do artigo ou fascículo.                                 |
+--------------------+----------------------------------------------------------------+
| illustrator        | Ilustrador do conteúdo.                                        |
+--------------------+----------------------------------------------------------------+
| translator         | Tradutor do conteúdo.                                          |
+--------------------+----------------------------------------------------------------+
| research-assistant | Assistente de pesquisa do artigo.                              |
+--------------------+----------------------------------------------------------------+

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
            <xref ref-type="aff" rid="aff01">1</xref>
            <role content-type="https://dictionary.casrai.org/Contributor_Roles/Investigation">Pesquisador</role>
        </contrib>
        <contrib contrib-type="editor">
            <name>
                <surname>Santos</surname>
                <given-names>Solange</given-names>
            </name>
        </contrib>
        ...
    </contrib-group>
    ...


.. note::
  * Recomenda-se o uso do registro de :term:`ORCID` e/ou *Currículo Lattes* dos autores para 
    avaliar formas de entrada para nomes.
  * Recomenda-se o uso da taxonomia CRediT para representar a função ou papel de
    cada contribuinte individual. Saiba mais detalhes em :ref:`taxonomia-credit`.

