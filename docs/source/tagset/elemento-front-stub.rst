.. _elemento-front-stub:

<front-stub>
============

Aparece em:

    :ref:`elemento-sub-article`
    :ref:`elemento-response`


Tags obrigatórias:

    ``<subject>``
    :ref:`elemento-article-title`


Ocorre:

    Uma vez


Utilizado em :ref:`elemento-sub-article` o qual herda os metadados do xml principal. Por este motivo não devem ser inseridos os elementos :ref:`elemento-journal-meta` e :ref:`elemento-article-meta`.

Nesse elemento devem ser inseridas apenas informações diferentes das que constam no artigo principal, ou seja, não é necessário incluir :ref:`elemento-volume`, :ref:`elemento-issue`, :ref:`elemento-pub-date`,  :ref:`elemento-funding-group` e :ref:`elemento-history` uma vez que estes tenham seus conteúdos definidos no artigo principal.

.. note:: Caso ocorra *tradução de afiliação* e/ou *notas de autor*, os dados destes autores devem ser duplicados para permitir uma referência cruzada entre os elementos no artigo traduzido.


Exemplo da tag completa:

.. code-block:: xml

    ...
    <front-stub>
        <article-categories>
            <subj-group subj-group-type="heading">
                <subject>Editorial</subject>
            </subj-group>
        </article-categories>
        <title-group>
            <article-title>Economia Clínica e Enfermagem</article-title>
        </title-group>
        <contrib-group>
            <contrib contrib-type="author">
                <name>
                    <surname>Porzsolt</surname>
                    <given-names>Franz</given-names>
                </name>
                <xref ref-type="aff" rid="aff4">1</xref>
            </contrib>
            <aff id="aff4">
                <label>1</label>
                <institution content-type="original">Health Care Research, General and Visceral Surgery, University Hospital Ulm, 89070 Ulm, Alemanha. Institute of Clinical Economics (ICE) e. V., 89081 Ulm, Alemanha. E-mail: pesquisador@pesquisador.org</institution>
            </aff>
        </contrib-group>
    </front-stub>
    ...


.. note:: Para :ref:`elemento-sub-article` do tipo ``@translation``, inserir em ``<front-stub>`` somente os dados traduzidos. Para afiliação, manter os dados apenas em ``<institution content-type="original">``.


.. {"reviewed_on": "20160803", "by": "gandhalf_thewhite@hotmail.com"}
