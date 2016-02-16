.. _elemento-front-stub:

<front-stub>
------------

Aparece em
    :ref:`elemento-sub-article`,
    :ref:`elemento-response`.


Tags obrigatórias
    ``<subject>``
    :ref:`elemento-article-title`


Ocorre
    Uma vez


Tag utilizada em :ref:`elemento-sub-article` a qual herda os metadados do xml principal, 
portanto não inserir as tags :ref:`elemento-journal-meta` e :ref:`elemento-article-meta`. 
Nessa tag deve ser inserido apenas as informações que são diferentes das que 
constam no artigo principal, ou seja, não é necessário inserir informações como 
:ref:`elemento-volume`, :ref:`elemento-issue`, :ref:`elemento-pub-date`, 
:ref:`elemento-funding-group` e :ref:`elemento-history`.


Versões em outros idiomas podem apresentar elementos de numeração de página diferentes do documento no idioma original. Nesses casos os elementos :ref:`elemento-fpage` :ref:`elemento-lpage` e :ref:`elemento-elocation-id` devem ser identificados em :ref:`elemento-front-stub`.


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


.. note:: Para :ref:`elemento-sub-article` do tipo ``@translation``, inserir em ``<front-stub>`` 
          apenas os dados traduzidos. Para afiliação, manter os dados apenas em ``<institution content-type="original">``.
          
