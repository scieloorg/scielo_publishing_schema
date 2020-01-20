.. _parecer-aberto:

Revisão por pares aberta (Open Peer Review)
============================================

É o processo pelo qual passa um artigo científico submetido a uma revista científica feita por pessoas da área – os pares –, de forma aberta, onde os autores sabem quem são os revisores e vice-versa. A revisão por pares aberta (em inglês, Open Peer Review ou OPR) coincide com o advento da Ciência Aberta, a partir do surgimento de periódicos de acesso aberto e de abordagens a respeito da forma com que a pesquisa é conduzida, disseminada e publicada. É também caracterizada como um movimento no sentido de maior transparência, participação e exploração de novas formas de colaboração, comunicação e difusão do conhecimento.

Para a publicação de OPR em SciELO deve-se considerar os seguintes aspectos:

* :ref:`elemento-parecer-exemplo-1`
* :ref:`elemento-parecer-exemplo-2`
* :ref:`elemento-parecer-exemplo-3`


.. _elemento-parecer-exemplo-1:

OPR como ``<article>`` (Recomendado)
------------------------------------

Publicar OPR como um documento separado :ref:`elemento-article`, mas relacionado ``<related-object>`` ao artigo. SciELO só publicará um parecer por documento. Para isso considerar:

 * ``@article-type`` com valor ``"aggregated-review-documents"``;
 * ``@object-type`` com valor ``"peer-reviewed-material"``;
 * ``@xlink:href`` com número DOI do artigo revisado;
 * ``@ext-link-type`` com valor ``"doi"``;
 * ``@contrib-type`` com valor ``"reviewer"``;
 * ``@date-type`` com valor ``"referee-report-received"``;
 * ``<custom-meta-group>`` + ``<custom-meta>`` + ``<meta-name>`` e ``<meta-value>``.


Exemplo:

.. code-block:: xml


    ...
    <article xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:mml="http://www.w3.org/1998/Math/MathML" dtd-version="1.1" specific-use="sps-1.10" article-type="aggregated-review-documents" xml:lang="en">
    ...
        <front>
            <article-meta>
                <article-id pub-id-type="doi">10.1590/123456720182998OPR</article-id>
                <article-categories>
                    <subj-group subj-group-type="heading">
                        <subject>Peer-Review</subject>
                    </subj-group>
                    ...
                </article-categories>
                <title-group>
                    <article-title>Open Peer Review: article X</article-title>
                </title-group>
                <contrib-group>
                <contrib contrib-type="reviewer">
                    <name>
                        <surname>Doe</surname>
                        <given-names>Jane X</given-names>
                    </name>
                    <xref ref-type="aff" rid="aff1"/>
                </contrib>
                <aff id="aff1">
                ...
                <permissions>
                ...
                </permissions>
                <related-object object-type="peer-reviewed-material" id="r01" xlink:href="10.1590/abd1806-4841.20142998" ext-link-type="doi"/>
                <history>
                    <date date-type="referee-report-received">
                       <day>10</day>
                       <month>01</month>
                        <year>2020</year>
                    </date>
                </history>
                <custom-meta-group>
                   <custom-meta>
                     <meta-name>peer-review-recommendation</meta-name>
                     <meta-value>accept</meta-value>
                   </custom-meta>
                </custom-meta-group>
                ...
            </article-meta>
        </front>
        <body>
        <sec>
            <title>Reviewer</title>
            <p>Vivamus elementum sapien tellus, a suscipit elit auctor in. Cras est nisl, egestas non ultrices ut, fringilla eu magna. Morbi ullamcorper et diam a elementum. Phasellus vitae diam eget arcu dignissim ultrices. Mauris tempor orci metus, a finibus augue viverra id. Phasellus vitae metus quis metus ultrices venenatis. Integer risus massa, sodales in luctus eget, facilisis at ante. Aliquam pulvinar elit venenatis libero auctor vestibulum.</p>
            <p>Sed in laoreet sem. Morbi vel imperdiet magna. Curabitur a velit maximus, volutpat metus in, posuere sem. Etiam eget lacus lorem. Nulla facilisi. Phasellus in mi urna. Donec finibus, erat non pharetra dignissim, arcu neque vestibulum enim, vel mollis orci nisl sit amet mauris. Nullam ac iaculis leo. Morbi lobortis arcu velit, at aliquet metus faucibus id.</p>
        </sec>
    </body>
        ...
    </article>

.. _elemento-parecer-exemplo-2:

OPR como ``<sub-article>``
---------------------------

Publicar OPR junto ao artigo como um :ref:`elemento-sub-article`. SciELO só publicará um parecer por :ref:`elemento-sub-article`. Para isso considerar:

 * ``@article-type`` com valor ``"referee-report"``;
 * ``@contrib-type`` com valor ``"reviewer"``;
 * ``@date-type`` com valor ``"referee-report-received"``;
 * ``<custom-meta-group>`` + ``<custom-meta>`` + ``<meta-name>`` e ``<meta-value>``.


Exemplo:

.. code-block:: xml


    ...
    <sub-article article-type="referee-report" id="s1" xml:lang="en">
    ...
        <front-stub>
            <article-meta>
                <article-id pub-id-type="doi">10.1590/123456720182998OPR</article-id>
                <article-categories>
                    <subj-group subj-group-type="heading">
                        <subject>Peer-Review</subject>
                    </subj-group>
                    ...
                </article-categories>
                <title-group>
                    <article-title>Open Peer Review: article X</article-title>
                </title-group>
                <contrib-group>
                <contrib contrib-type="reviewer">
                    <name>
                        <surname>Doe</surname>
                        <given-names>Jane X.</given-names>
                    </name>
                    <xref ref-type="aff" rid="aff1"/>
                </contrib>
                </contrib-group>
                <aff id="aff1">
                  ...
                </aff>
                <permissions>
                ...
                </permissions>
                <history>
                    <date date-type="referee-report-received">
                       <day>10</day>
                       <month>01</month>
                        <year>2020</year>
                    </date>
                </history>
                <custom-meta-group>
                   <custom-meta>
                     <meta-name>peer-review-recommendation</meta-name>
                     <meta-value>accept</meta-value>
                   </custom-meta>
                </custom-meta-group>
                ...
            </article-meta>
        </front-stub>
        <body>
        <sec>
            <title>Reviewer</title>
            <p>Vivamus elementum sapien tellus, a suscipit elit auctor in. Cras est nisl, egestas non ultrices ut, fringilla eu magna. Morbi ullamcorper et diam a elementum. Phasellus vitae diam eget arcu dignissim ultrices. Mauris tempor orci metus, a finibus augue viverra id. Phasellus vitae metus quis metus ultrices venenatis. Integer risus massa, sodales in luctus eget, facilisis at ante. Aliquam pulvinar elit venenatis libero auctor vestibulum.</p>
            <p>Sed in laoreet sem. Morbi vel imperdiet magna. Curabitur a velit maximus, volutpat metus in, posuere sem. Etiam eget lacus lorem. Nulla facilisi. Phasellus in mi urna. Donec finibus, erat non pharetra dignissim, arcu neque vestibulum enim, vel mollis orci nisl sit amet mauris. Nullam ac iaculis leo. Morbi lobortis arcu velit, at aliquet metus faucibus id.</p>
        </sec>
    </body>
        ...
    </sub-article>


.. _elemento-parecer-exemplo-3:

OPR como link externo
----------------------

O OPR pode estar publicado em outro site; neste caso, deve-se usar a publicação do parecer como link externo. Esta modalidade também pode ocorrer como :ref:`elemento-article` (Recomendado) ou :ref:`elemento-sub-article`. Para isso considerar uma das regras mencionadas acima, mais:


 * ``@object-type`` com valor ``"referee-report"``;
 * ``@xlink:href`` com a URL do parecer (desde o https://);
 * ``@ext-link-type`` com valor ``"uri"``.

Exemplo:

.. code-block:: xml


    ...
    <body>
        <sec>
            <title>Reviewer</title>
            <p>This report can be read on:<related-object object-type="referee-report" ext-link-type="uri" xlink:href="https://publons.com/publon/000000/#review-2020xxx">Publons</related-object>
            </p>
        </sec>
    </body>
     ...


.. note::
 * É obrigatório o uso de DOI próprio para publicação de parecer.
 * Fonte: MENDES-DA-SILVA, (2019); SOUZA, (2017) e OLIVEIRA, (2018).
 