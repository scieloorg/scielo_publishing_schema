.. _elemento-journal-id:

<journal-id>
============

Aparece em:

  :ref:`elemento-journal-meta`

Atributos obrigatórios:

  1. ``@journal-id-type``

Ocorre:

  Uma ou mais vezes


Contém o identificador único do periódico indexado em uma base de dados ou instituição publicadora. Minimamente, o acrônimo do periódico deve ser identificado por meio do valor ``publisher-id``.

É obrigatório ter ao menos uma ocorrência de ``<journal-id>`` com o valor ``publisher-id`` no atributo ``@journal-id-type``. Nesta ocorrência deve ser identificado o acrônimo do periódico.

Os valores permitidos para ``@journal-id-type`` são:

+---------------+-----------------------------------------+
| Valor         | Descrição                               |
+===============+=========================================+
| publisher-id  | Acrônimo do periódoco na coleção SciELO |
+---------------+-----------------------------------------+
| nlm-ta        | Título abreviado no :term:`PubMed`      |
+---------------+-----------------------------------------+

Artigos de periódico indexados no :term:`PubMed` devem apresentar, adicionalmente, o título abreviado do periódico naquele índice por meio do elemento ``<journal-id @journal-id-type="nlm-ta">``.

Exemplo:

.. code-block:: xml

    ...
    <journal-meta>
        ...
        <journal-id journal-id-type="publisher-id">mioc</journal-id>
        <journal-id journal-id-type="nlm-ta">Mem Inst Oswaldo Cruz</journal-id>
        ...
    </journal-meta>
    ...

Pode-se consultar o `PubMed <http://www.ncbi.nlm.nih.gov/pubmed/advanced>`_ para verificar se o periódico encontra-se indexado.


.. note:: Sugere-se consultar o :ref:`arquivo de metadados dos periódicos <journal-meta-csv>` como referência na identificação dos elementos.


.. {"reviewed_on": "20160803", "by": "gandhalf_thewhite@hotmail.com"}
