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



``<date>`` deve conter obrigatoriamente o elemento :ref:`elemento-year`. Usa-se o atributo ``@date-type`` para especificar o tipo da ação envolvida.

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
        </history>
        ...
    </article-meta>
    ...


.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
