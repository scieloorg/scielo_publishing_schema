.. _elemento-month:

<month>
=======

Aparece em:

  :ref:`elemento-pub-date`
  :ref:`elemento-product`
  :ref:`elemento-element-citation`
  :ref:`elemento-date`

Ocorre :

  1. Zero ou uma vez em :ref:`elemento-front`
  2. Zero ou mais vezes em :ref:`elemento-back`

Identifica o mês em referências, podendo representar:

* o mês de publicação de um periódico científico;
* o mês da realização de um relatório;
* o mês de publicação de um artigo (ver :ref:`elemento-pub-date`) ou de um produto (ver :ref:`elemento-product`) quando utilizada em :ref:`elemento-front`.

Os valores possíveis são números inteiros de até 2 dígitos, no intervalo de 1 a 12, sendo aceito zero não significativo à esquerda.

Intervalos de meses, por exemplo, ``Jan-Mar``, devem ser identificados em :ref:`elemento-season`.

Exemplos:

1. em ``<pub-date>``:

.. code-block:: xml

   ...
   <pub-date pub-type="epub-ppub">
        <day>01</day>
        <month>06</month>
        <year>2016</year>
   </pub-date>
   ...

2. em ``<date>`` de ``<history>``:

.. code-block:: xml

   ...
   <date date-type="received">
        <day>20</day>
        <month>10</month>
        <year>2014</year>
   </date>
   ...

3. em ``<element-citation>``:

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


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
