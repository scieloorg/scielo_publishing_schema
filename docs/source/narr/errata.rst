.. _errata:

Errata
======

Arquivos do tipo errata devem apresentar no atributo ``@article-type`` o valor ``correction`` . A seção em ``<subject>`` deve conter a informação apresentada no PDF da errata. O elemento :ref:`elemento-article-title` para publicações regulares e contínua em números, deve replicar a informação da seção, usualmente encontra-se: Errata, Erratum, Correção, Correction, etc, para arquivos em *Ahead of Print* ou publicação contínua em um único volume, além de replicar o título da seção, deve-se inserir dois pontos mais o título do artigo a ser corrigido.

O elemento :ref:`elemento-related-article` pode ser usado uma ou mais vezes e é utilizado para referenciar o artigo que se deseja corrigir e deve conter obrigatoriamente os atributos:


 * ``@related-article-type`` com valor ``"corrected-article"``
 * ``@id``
 * ``@xLink:href`` com número DOI do artigo que está sendo corrigido
 * ``@ext-link-type`` com valor "doi"


Exemplo:

.. code-block:: xml


    ...
    <article xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:mml="http://www.w3.org/1998/Math/MathML" dtd-version="1.0" specific-use="sps-1.8" article-type="correction" xml:lang="pt">`
    ...
        <front>
            <article-meta>
                <article-id pub-id-type="doi">10.1590/123456720182998e</article-id>
                <article-categories>
                    <subj-group subj-group-type="heading">
                        <subject>Errata</subject>
                    </subj-group>
                    ...
                </article-categories>
                <title-group>
                    <article-title>Errata</article-title>
                </title-group>
                ...
                <permissions>
                    ...
                </permissions>
                <related-article related-article-type="corrected-article" id="r01" xlink:href="10.1590/abd1806-4841.20142998" ext-link-type="doi"/>
                <counts>
                    ...
                </counts>
                ...
            </article-meta>
            ...
        </front>
        ...
    </article>



No artigo que esta sendo corrigido, deve-se inserir uma nota geral em :ref:`elemento-back` com atributo ``fn-type`` com valor ``other`` contendo o :ref:`elemento-label` igual ao título do arquivo da errata e os parágrafos considerando exatamente o mesmo texto publicado na errata.


Exemplo:

.. code-block:: xml

    ...
    <back>
        ...
        <fn-group>
          <fn fn-type="other">
            <label>Errata</label>
              <p>Texto da errata</p>
              <p>Texto da errata</p>
            </fn>
        </fn-group>
        ...
    </back>
    ...



.. note::
 * :ref:`elemento-related-article` deve ser inserido abaixo das informações de :ref:`elemento-permissions` ou acima de :ref:`elemento-counts`.
 * Mais informações podem ser obtidas no `Guia para o registro e publicação de Errata <http://www.scielo.org/local/File/Guia_para_o_registro_e_publicacao_de_Errata.pdf>`_.


