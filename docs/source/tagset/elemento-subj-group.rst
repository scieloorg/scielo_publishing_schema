.. _elemento-subj-group:

<subj-group>
^^^^^^^^^^^^

Aparece em:

  :ref:`elemento-article-categories`

Atributos obrigatórios:

  1. ``@subj-group-type="heading"``

Ocorre:

  Uma vez


Designa a seção do :term:`documento` e é utilizado para agrupar documentos por assunto. É obrigatória a presença de somente uma ocorrência do elemento ``<subj-group>`` com o atributo ``@subj-group-type="heading"``. Em ``<subject>`` atribui-se a seção na qual o artigo encontra-se classificado (devendo-se consultar o sumário para melhor identificá-lo). Para :term:`ahead-of-print` deve ser adotada sempre a seção ``Articles`` conforme exemplo em :ref:`ahead-of-print`.


Exemplos:

1. Seção temática:

.. code-block:: xml

    ...
    <article-categories>
        <subj-group subj-group-type="heading">
            <subject>Biotechnology</subject>
        </subj-group>
    </article-categories>
    ...


2. Seção por tipo de documento:

.. code-block:: xml

    ...
    <article-categories>
        <subj-group subj-group-type="heading">
            <subject>Original Article</subject>
        </subj-group>
    </article-categories>
    ...

3. Para ``<ahead-of-print>``:

.. code-block:: xml

    ...
    <article-categories>
        <subj-group subj-group-type="heading">
            <subject>Articles</subject>
        </subj-group>
    </article-categories>
    ...


.. note:: Para documentos como editoriais, erratas, cartas ao editor etc., que não apresentam título, apenas a seção, é necessário repetir o título da seção no ``<front>`` e marcá-lo com os elementos de título.


.. {"reviewed_on": "20160629", "by": "gandhalf_thewhite@hotmail.com"}
