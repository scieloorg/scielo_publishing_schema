.. _elemento-publisher:

<publisher>
===========

+------------------------------+---------+
| Aparece em                   | Ocorre  |
+==============================+=========+
| :ref:`elemento-journal-meta` | Uma vez |
+------------------------------+---------+



Contém o nome do publicador ou editora do periódico conforme registro no :term:`ISSN`.

.. note::
 * O :ref:`arquivo de metadados dos periódicos <journal-meta-csv>` deve ser consultado como referência na identificação dos elementos.
 * Pode-se também consultar o site do `ISSN <https://portal.issn.org/>`_ .


Exemplo:

.. code-block:: xml

    ...
    <journal-meta>
        ...
        <publisher>
            <publisher-name>Instituto Oswaldo Cruz, Ministério da Saúde</publisher-name>
        </publisher>
        ...
    </journal-meta>
    ...


.. {"reviewed_on": "20160628", "by": "gandhalf_thewhite@hotmail.com"}
