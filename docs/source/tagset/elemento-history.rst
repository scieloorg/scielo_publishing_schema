.. _elemento-history:

<history>
=========

Aparece em:

  :ref:`elemento-article-meta`

Ocorre:

  Zero ou uma vez


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
             <month>11</month>
             <year>2013</year>
        </date>
        <date date-type="accepted">
             <day>14</day>
             <month>07</month>
             <year>2015</year>
        </date>
   </history>
   ...


.. {"reviewed_on": "20160626", "by": "gandhalf_thewhite@hotmail.com"}
