.. _elemento-subj-group:

<subj-group>
^^^^^^^^^^^^

Aparece em
  :ref:`elemento-article-categories`
 
Atributos obrigatórios
  1. subj-group-type="heading"
 
Ocorre
  Uma vez
 

Designa a seção do :term:`documento` e serve para organizar documentos em grupos 
por assunto. É obrigatória a presença de uma e somente uma ocorrência do
elemento ``<subj-group>`` com o atributo ``@subj-group-type="heading"``. 
Em ``<subject>`` atribui-se a seção em que o artigo foi classificado 
(consultar o sumário para melhor identificação) e para :term:`ahead-of-print` 
deve ser adotado sempre a seção ``Articles``. Ver exemplo de :ref:`ahead-of-print`
 
 
Exemplos:
 
Seção temática:
 
.. code-block:: xml
 
    ...
    <article-categories>
        <subj-group subj-group-type="heading">
            <subject>Biotechnology</subject>
        </subj-group>
    </article-categories>
    ...


Seção por tipo de documento:
 
.. code-block:: xml
 
    ...
    <article-categories>
        <subj-group subj-group-type="heading">
            <subject>Original Article</subject>
        </subj-group>
    </article-categories>
    ...
 
Para ahead-of-print:
 
.. code-block:: xml
 
    ...
    <article-categories>
        <subj-group subj-group-type="heading">
            <subject>Articles</subject>
        </subj-group>
    </article-categories>
    ...
 

.. note:: Para documentos como editoriais, erratas, cartas ao editor etc que não 
          apresentam título, mas apenas a seção, é preciso repetir o título da 
          seção no front e marcá-lo com as tags de título.

