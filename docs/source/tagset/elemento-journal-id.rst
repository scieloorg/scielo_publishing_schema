.. _elemento-journal-id:
 
<journal-id>
^^^^^^^^^^^^

Aparece em
  :ref:`elemento-journal-meta`
 
Atributos obrigatórios
  1. journal-id-type='publisher-id'
 
Ocorre
  Uma ou mais vezes


Especifica o título padronizado do periódico.

Os valores permitidos para o atributo ``@journal-id-type`` são:

+---------------+-----------------------------------------+
| Valor         | Descrição                               |
+===============+=========================================+
| publisher-id  | Acrônimo do periódoco na coleção SciELO |
+---------------+-----------------------------------------+
| nlm-ta        | Título abreviado no :term:`PubMed`      |
+---------------+-----------------------------------------+
 
Artigos de periódicos indexados no :term:`PubMed`, devem apresentar adicionalmente 
o título abreviado do periódico no :term:`PubMed` por meio do elemento 
``<journal-id @journal-id-type="nlm-ta">``, conforme o exemplo:
 

.. code-block:: xml
   
    ...
    <journal-meta>
        ...
        <journal-id journal-id-type="publisher-id">mioc</journal-id>
        <journal-id journal-id-type="nlm-ta">Mem Inst Oswaldo Cruz</journal-id>
        ...
    </journal-meta>
    ...

Para verificar se o periódico está indexado no :term:`PubMed` consulte o link 
http://www.ncbi.nlm.nih.gov/pubmed/advanced


.. note:: Consulte o :ref:`arquivo de metadados dos periódicos <journal-meta-csv>` 
          como referência na identificação dos elementos.

