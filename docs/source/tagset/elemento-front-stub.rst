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


Exemplo da tag completa:

.. code-block:: xml

    ...
    <sub-article article-type="translation" xml:lang="en" id="S1">
        <front-stub>
            <subj-group subj-group-type="heading">
                <subject>Letter to the Editor</subject>
            </subj-group>
        </front-stub>
        ...
    </sub-article>
    ...


.. note:: Para :ref:`elemento-sub-article` do tipo ``@translation``, inserir em ``<front-stub>`` somente os dados traduzidos. Para afiliação, manter os dados apenas em ``<institution content-type="original">``.


.. {"reviewed_on": "20160625", "by": "gandhalf_thewhite@hotmail.com"}
