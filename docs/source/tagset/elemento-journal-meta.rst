.. _elemento-journal-meta:

<journal-meta>
==============

+-----------------------+---------+
| Aparece em            | Ocorre  |
+=======================+=========+
| :ref:`elemento-front` | Uma vez |
+-----------------------+---------+



Em ``<journal-meta>`` são identificados os metadados do periódico.

.. note:: Sugere-se consultar o :ref:`arquivo de metadados dos periódicos <journal-meta-csv>` como referência na identificação dos elementos.

Exemplo:

.. code-block:: xml

   ...
   <journal-meta>
        <journal-id journal-id-type="nlm-ta">Braz J Med Biol Res</journal-id>
        <journal-id journal-id-type="publisher-id">bjmbr</journal-id>
        <journal-title-group>
             <journal-title>Brazilian Journal of Medical and Biological Research</journal-title>
             <abbrev-journal-title abbrev-type="publisher">Braz. J. Med. Biol. Res.</abbrev-journal-title>
        </journal-title-group>
        <issn pub-type="epub">1414-431X</issn>
        <issn pub-type="ppub">0100-879X</issn>
        <publisher>
             <publisher-name>Associação Brasileira de Divulgação Científica</publisher-name>
        </publisher>
   </journal-meta>
   ...


.. {"reviewed_on": "20160626", "by": "gandhalf_thewhite@hotmail.com"}
