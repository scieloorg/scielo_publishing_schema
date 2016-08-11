.. _elemento-collab:

<collab>
========

Aparece em:

  :ref:`elemento-contrib`
  :ref:`elemento-person-group`

Ocorre:

  Zero ou mais vezes

Identifica uma autoria institucional individual ou em grupo.

Exemplos:

1. Em Front:

.. code-block:: xml

   ...
   <contrib-group>
        <contrib contrib-type="author">
             <collab>BFG - The Brazil Flora Group</collab>
        </contrib>
        <contrib contrib-type="author">
             <name>
                  <surname>Zappi</surname>
                  <given-names>Daniela C.</given-names>
             </name>
             <xref ref-type="corresp" rid="c1">1</xref>
        </contrib>
   </contrib-group>
   ...


2. Em back:

.. code-block:: xml

   ...
   <element-citation publication-type="book">
        <person-group person-group-type="author">
             <collab>World Health Organization (WHO)</collab>
        </person-group>
        <source>The top 10 causes of death. Fact sheet nº 310</source>
        <date-in-citation content-type="updated">Updated May 2014</date-in-citation>
        <date-in-citation content-type="access-date">citado 2012 Out 10</date-in-citation>
        <comment>Disponível em: <ext-link ext-link-type="uri" xlink:href="http://www.who.int/mediacentre/factsheets/fs310/en/index2.html">http://www.who.int/mediacentre/factsheets/fs310/en/index2.html</ext-link>
        </comment>
   </element-citation>
   ...



.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
