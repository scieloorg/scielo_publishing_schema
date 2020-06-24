.. _elemento-date:

<date>
======

Atributos obrigatórios:

  1. ``@date-type``

+-------------------------+-------------------+
| Aparece em              | Ocorre            |
+=========================+===================+
| :ref:`elemento-history` | Uma ou mais vezes |
+-------------------------+-------------------+


 Usa-se o atributo ``@date-type`` para especificar o tipo da ação envolvida.


 Os valores possíveis para o atributo ``@date-type`` são:

+-------------+------------------------------------------------+
| Valor       | Descrição                                      |
+=============+================================================+
| accepted    | Data em que um manuscrito foi aceito           |
+-------------+------------------------------------------------+
| corrected   | Data em que um artigo foi corrigido            |
+-------------+------------------------------------------------+
| pub         | Data de publicação (eletrônica ou impressa)    |
+-------------+------------------------------------------------+
| preprint    | Data de divulgação de preprint                 |
+-------------+------------------------------------------------+
| retracted   | Data em que um artigo foi retratado            |
+-------------+------------------------------------------------+
| received    | Data em que um manuscrito foi recebido         |
+-------------+------------------------------------------------+
| rev-recd    | Data em que um documento revisado foi recebido |
+-------------+------------------------------------------------+
| rev-request | Data de solicitação das revisões               |
+-------------+------------------------------------------------+
| referee-    |                                                |
| report-     | Data da revisão por pares / parecer            |
| received    |                                                |
+-------------+------------------------------------------------+

Exemplo:

.. code-block:: xml

    ...
    <article-meta>
        ...
        <history>
            <date date-type="received">
                <day>15</day>
                <month>03</month>
                <year>2013</year>
            </date>
            <date date-type="rev-recd">
                <day>06</day>
                <month>11</month>
                <year>2013</year>
            </date>
            <date date-type="accepted">
                <day>12</day>
                <month>05</month>
                <year>2014</year>
            </date>
            <date date-type="preprint">
                <day>21</day>
                <month>09</month>
                <year>2012</year>
            </date>
        </history>
        ...
    </article-meta>
    ...


.. note:: 
 * ``<date>`` deve conter obrigatoriamente o elemento :ref:`elemento-year`.
 * ``@date-type`` com os valores "received" e "accepted" obrigatoriamente devem ter suas datas completas considerando :ref:`elemento-day`, :ref:`elemento-month` e :ref:`elemento-year`. Para mais informações consultar `Comunicado SciELO <https://us4.campaign-archive.com/?u=f26dcf71797dd37381acb4aa5&id=2a6634a845>`_ e `Critérios, política e procedimentos para a admissão e a permanência de periódicos científicos na Coleção SciELO Brasil <https://www.scielo.br/avaliacao/20200500%20Criterios%20SciELO%20Brasil.pdf>`_  



.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
