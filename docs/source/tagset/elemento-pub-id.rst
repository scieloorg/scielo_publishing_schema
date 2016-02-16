.. _elemento-pub-id:

<pub-id>
^^^^^^^^

Aparece em
  :ref:`elemento-element-citation`
  

Atributos obrigatórios 
  ``@pub-id-type``

Ocorre 
  Zero ou mais vezes

Identifica o tipo de identificador (id) de um :term:`documento` em uma referência.
Deve possuir o atributo ``@pub-id-type`` com os seguintes possíveis valores:

+--------+----------------------------------------+
| Valor  | Descrição                              |
+========+========================================+
| pmid   | :term:`PubMed` ID                      |
+--------+----------------------------------------+
| pcmid  | :term:`PubMed` Central ID              |
+--------+----------------------------------------+
| doi    | Número DOI registrado no Crossref      |
+--------+----------------------------------------+
| pii    | Identificador do editor                |
+--------+----------------------------------------+
| other  | qualquer outro identificador           |
+--------+----------------------------------------+

Exemplo:

.. code-block:: xml

    ...
    <element-citation>
        <pub-id pub-id-type="pmid">15867408</pub-id>
    </element-citation>
    ...

