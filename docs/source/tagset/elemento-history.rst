.. _elemento-history:

<history>
=========

+------------------------------+-----------------+
| Aparece em                   | Ocorre          |
+==============================+=================+
| :ref:`elemento-article-meta` | Zero ou uma vez |
+------------------------------+-----------------+
| :ref:`elemento-front-stub`   | Zero ou uma vez |
+------------------------------+-----------------+



Agrupa as datas nas quais o artigo foi recebido, aceito e/ou revisado. Contém, obrigatoriamente, elementos do tipo :ref:`elemento-date`.

Exemplo:

.. code-block:: xml

   ...
   <history>
        <date date-type="received">
             <day>20</day>
             <month>10</month>
             <year>2014</year>
        </date>
        <date date-type="rev-recd">
             <day>06</day>
             <month>12</month>
             <year>2014</year>
        </date>
        <date date-type="accepted">
             <day>14</day>
             <month>07</month>
             <year>2015</year>
        </date>
   </history>
   ...


.. {"reviewed_on": "20170720", "by": "aline.cristina@scielo.org"}
