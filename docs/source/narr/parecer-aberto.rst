.. _parecer-aberto:

Pareceres - Revisão por pares aberta (Open Peer Review)
=======================================================

O termo revisão por pares aberta (em inglês, Open Peer Review - OPR), pode indicar
distintos tipos e níveis de abertura: a) pode significar que as identidades dos
autores e pareceristas são reveladas a ambos; b) que os pareceres são disponibilizados
em seguida aos artigos publicados; c) a utilização de plataformas de interação aberta
com público; d) publicação do nome do editor responsável pelo processo de revisão, 
dentre outras opções ou combinações possíveis.

Para a publicação de pareceres no SciELO deve-se considerar os seguintes aspectos:

* :ref:`elemento-parecer-exemplo-1`
* :ref:`elemento-parecer-exemplo-2`
* :ref:`elemento-parecer-exemplo-3`


.. _elemento-parecer-exemplo-1:

Parecer como ``<article>`` (Recomendado)
----------------------------------------

Publicar parecer como um documento separado, mas relacionado ao artigo por meio
do elemento ``<related-object>``. Para isso considerar:

 * ``@article-type`` com valor ``"referee-report"``; 
 * ``@object-type`` com valor ``"peer-reviewed-material"``;
 * ``@xlink:href`` com número DOI do artigo revisado;
 * ``@ext-link-type`` com valor ``"doi"``;
 * ``@contrib-type`` com valor ``"author"``;
 * ``<role>`` com ``"@specific-use"`` com valores ``"reviewer"`` ou ``"editor"``;
 * ``@date-type`` em ``<history>`` com valor ``"referee-report-received"``;
 * ``<custom-meta-group>`` + ``<custom-meta>`` + ``<meta-name>`` e ``<meta-value>``.


Exemplo:

.. code-block:: xml

    <article xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:mml="http://www.w3.org/1998/Math/MathML" dtd-version="1.1" specific-use="sps-1.10" article-type="referee-report" xml:lang="en">
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
                <contrib contrib-type="author">
                    <name>
                        <surname>Doe</surname>
                        <given-names>Jane X</given-names>
                    </name>
                    <role specific-use="reviewer">Reviewer</role>
                    <xref ref-type="aff" rid="aff1"/>
                </contrib>
                <aff id="aff1">
                ...
                </aff>
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

Parecer como ``<sub-article>``
------------------------------

Publicar parecer junto ao artigo como um :ref:`elemento-sub-article`. SciELO 
publicará um parecer por :ref:`elemento-sub-article`. Para isso considerar:

 * ``@article-type`` com valor ``"referee-report"``;
 * ``@contrib-type`` com valor ``"author"``;
 * ``<role>`` com ``"@specific-use"`` com valores ``"reviewer"`` ou ``"editor"``;
 * ``@date-type`` em ``<history>`` com valor ``"referee-report-received"``;
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
                    <contrib contrib-type="author">
                        <name>
                            <surname>Doe</surname>
                            <given-names>Jane X.</given-names>
                        </name>
                        <role specific-use="reviewer">Reviewer</role>
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
    ...


.. _elemento-parecer-exemplo-3:

Parecer como link externo
-------------------------

O parecer pode estar publicado em outro site e, neste caso, deve-se referenciá-lo 
como link externo. Esta modalidade também pode ocorrer como :ref:`elemento-article` 
(Recomendado) ou :ref:`elemento-sub-article`. Para isso considerar uma das regras 
mencionadas acima, mais:

 * ``@object-type`` com valor ``"referee-report"``;
 * ``@xlink:href`` com a URL do parecer (desde o https://);
 * ``@ext-link-type`` com valor ``"uri"``.


Exemplo:

.. code-block:: xml

    ...
    <body>
        <sec>
            <title>Reviewer</title>
            <p>This report can be read on:<related-object object-type="referee-report" ext-link-type="uri" xlink:href="https://publons.com/publon/000000/#review-2020xxx">Publons</related-object></p>
        </sec>
    </body>
    ...


.. note::
 * Quando o parecer não apresentar autoria explícita utilizar ``<anonymous/>`` 
   + ``<role>`` com atributo ``@specific-use`` com os valores ``reviewer`` ou 
   ``editor``. 
 * É obrigatório o uso de DOI próprio para publicação de parecer. 
 * Fonte: MENDES-DA-SILVA, (2019); SOUZA, (2017) e OLIVEIRA, (2018).

