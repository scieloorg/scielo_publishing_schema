.. _elemento-abbrev-journal-title:

<abbrev-journal-title>
======================

Atributos obrigatórios:

  1. ``@abbrev-type="publisher"``

+-------------------------------------+---------+
| Aparece em                          | Ocorre  |
+=====================================+=========+
| :ref:`elemento-journal-title-group` | Uma vez |
+-------------------------------------+---------+



Define a forma abreviada do título do periódico de acordo com o registro no :term:`ISSN`.

.. note:: 
 * Consulte o :ref:`arquivo de metadados dos periódicos <journal-meta-csv>` como referência na identificação dos elementos.
 * Pode-se também consultar o site do `ISSN <https://portal.issn.org/>`_ .

Exemplo:

.. code-block:: xml

    ...
    <journal-title-group>
        <abbrev-journal-title abbrev-type="publisher">Braz. J. Med. Biol. Res.</abbrev-journal-title>
    </journal-title-group>
    ...

.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
