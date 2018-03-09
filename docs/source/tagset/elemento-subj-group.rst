.. _elemento-subj-group:

<subj-group>
============

Aparece em:

  :ref:`elemento-article-categories`
  ``<subj-group>``

Atributos obrigatórios:

  1. ``@subj-group-type="heading"``

Ocorre:

  Uma vez


Designa a seção do sumário ao qual pertence o :term:`documento` e também pode ser utilizado para classificar documentos por assunto. É obrigatória a presença de somente uma ocorrência do elemento ``<subj-group>`` com o atributo ``@subj-group-type="heading"``. Em ``<subject>`` atribui-se a seção na qual o artigo encontra-se classificado (devendo-se consultar o sumário para melhor identificá-lo).

Exemplos:

    * :ref:`elemento-subjgroup-exemplo-1`
    * :ref:`elemento-subjgroup-exemplo-2`


Com o elemento ``<subj-group>`` é possível identificar :ref:`subsecao-exemplo-1`



.. _elemento-subjgroup-exemplo-1:

Exemplo de ``<subj-group>`` temática
------------------------------------

.. code-block:: xml

    ...
    <article-categories>
        <subj-group subj-group-type="heading">
            <subject>Biotechnology</subject>
        </subj-group>
    </article-categories>
    ...


.. _elemento-subjgroup-exemplo-2:

Exemplo de ``<subj-group>`` por tipo de documento
-------------------------------------------------

.. code-block:: xml

    ...
    <article-categories>
        <subj-group subj-group-type="heading">
            <subject>Original Article</subject>
        </subj-group>
    </article-categories>
    ...


.. _subsecao-exemplo-1:

Subseções em documento
----------------------

Artigos que apresentam subseções devem ser identificados no :term:`documento` por meio do elemento :ref:`elemento-subj-group`.

Exemplo:

.. code-block:: xml

    ...
    <article-categories>
        <subj-group subj-group-type="heading">
            <subject>Scientific Communication</subject>
            <subj-group>
                <subject>Food Safety</subject>
            </subj-group>
        </subj-group>
    </article-categories>
    ...

.. note:: Apenas a seção de nível mais alto apresenta o atributo ``@subj-group-type`` com o valor ``heading`` e deve aparecer somente uma vez no artigo.


.. {"reviewed_on": "20170828", "by": "carolina.tanigushi@scielo.org"}
