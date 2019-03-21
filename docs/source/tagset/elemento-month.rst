.. _elemento-month:

<month>
=======

+----------------------------------+-----------------+
| Aparece em                       | Ocorre          |
+==================================+=================+
| :ref:`elemento-date`             | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-element-citation` | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-product`          | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-pub-date`         | Zero ou uma vez |
+----------------------------------+-----------------+


Identifica o mês em referências, podendo representar:

* o mês de publicação de um periódico científico;
* o mês da realização de um relatório;
* o mês de publicação de um artigo (ver :ref:`elemento-pub-date`) ou de um produto (ver :ref:`elemento-product`) quando utilizada em :ref:`elemento-front`.

Os valores possíveis são números inteiros de até 2 dígitos, no intervalo de 1 a 12, sendo aceito zero não significativo à esquerda.

Intervalos de meses, por exemplo, ``Jan-Mar``, devem ser identificados em :ref:`elemento-season`.

Exemplos:

  * :ref:`elemento-month-exemplo-1`
  * :ref:`elemento-month-exemplo-2`
  * :ref:`elemento-month-exemplo-3`



.. _elemento-month-exemplo-1:

Exemplo de ``<month>`` em ``<pub-date>``:
---------------------------------------------------

.. code-block:: xml

   ...
   <pub-date publication-format="electronic" date-type="pub">
       <day>01</day>
       <month>01</month>
       <year>2019</year>
    </pub-date>
   ...

.. _elemento-month-exemplo-2:

Exemplo de ``<month>`` em ``<date>`` de ``<history>``:
--------------------------------------------------------------------------

.. code-block:: xml

   ...
   <date date-type="received">
        <day>20</day>
        <month>10</month>
        <year>2018</year>
   </date>
   ...

.. _elemento-month-exemplo-3:

Exemplo de ``<month>`` em ``<element-citation>``:
-----------------------------------------------------------

.. code-block:: xml

   ...
   <element-citation publication-type="book">
        <person-group person-group-type="author">
             <collab>American Occupational Therapy Association, Ad Hoc Committee on Occupational Therapy Manpower</collab>
        </person-group>
        <source>Occupational therapy manpower: a plan for progress</source>
        <publisher-loc>Rockville (MD)</publisher-loc>
        <publisher-name>The Association</publisher-name>
        <year>1985</year>
        <month>4</month>
        <size units="page">84 p</size>
   </element-citation>
   ...

.. note:: Este elemento é obrigatório em :ref:`elemento-pub-date` com atributo ``@date-type`` com valor "pub" e em em :ref:`elemento-date` com atributo ``@date-type`` com valor "received" e "accepted".