.. _elemento-collab:

<collab>
========

+------------------------------+--------------------+
| Aparece em                   | Ocorre             |
+==============================+====================+
| :ref:`elemento-contrib`      | Zero ou mais vezes |
+------------------------------+--------------------+
| :ref:`elemento-person-group` | Zero ou mais vezes |
+------------------------------+--------------------+


Identifica uma autoria institucional individual ou em grupo. Quando descrito nomes dos colaboradores identifica-los em :ref:`elemento-contrib-group` com ``@content-type="collab-list"``, para estes casos o tipo de contribuição deve ser ``@contrib-type="non-byline-author"``.


Exemplos:

  * :ref:`elemento-collab-exemplo-1`
  * :ref:`elemento-collab-exemplo-2`
  * :ref:`elemento-collab-exemplo-3`
  * :ref:`elemento-collab-exemplo-4`
  * :ref:`elemento-collab-exemplo-5`

.. _elemento-collab-exemplo-1:

Exemplo de ``<collab>`` em ``<front>`` com uma autoria institucional:
----------------------------------------------------------------------

.. code-block:: xml

   ...
   <contrib-group>
        <contrib contrib-type="author">
             <collab>The Brazil Flora Group</collab>
        </contrib>        
   </contrib-group>
   ...


.. _elemento-collab-exemplo-2:

Exemplo de ``<collab>`` em ``<front>`` com uma autoria institucional e nomes dos colaboradores pertencentes a instituição:
---------------------------------------------------------------------------------------------------------------------------

.. code-block:: xml

   ...
   <contrib-group>
      <contrib contrib-type="author" id="collab">
          <collab>The MARS Group</collab>
          <xref ref-type="author-notes" rid="fn1">1</xref>
      </contrib>
   </contrib-group>
   <contrib-group content-type="collab-list">
      <contrib contrib-type="non-byline-author" rid="collab">
         <name>
              <surname>Wright</surname>
              <given-names>Rick W.</given-names>
         </name>    
      </contrib>
      <contrib contrib-type="non-byline-author" rid="collab">
         <name>
              <surname>Huston</surname>
              <given-names>Laura J.</given-names>
         </name>     
      </contrib>
      <contrib contrib-type="non-byline-author" rid="collab">
         <name>
              <surname>Spindler</surname>
              <given-names>Kurt P.</given-names>
         </name>     
      </contrib>
   </contrib-group>
   <author-notes>
     <fn fn-type="study-group-members" id="fn1">
        <label>1</label>
      <p>The writing committee for this article consisted of Rick W. Wright, MD; Laura J. Huston, MS; Kurt P. Spindler, MD; Warren R. Dunn, MD, MPH; Amanda K. Haas, MA. Members of the MARS Group</p>
     </fn>
  </author-notes>


.. _elemento-collab-exemplo-3:

Exemplo de ``<collab>`` em ``<front>`` com duas autorias institucionais:
-------------------------------------------------------------------------

.. code-block:: xml

   ...
   <contrib-group>
     <contrib contrib-type="author">
          <collab>The Brazil Flora Group</collab>
     </contrib>
     <contrib contrib-type="author">
          <collab>The MARS Group</collab>
     </contrib>
   </contrib-group>


.. _elemento-collab-exemplo-4:

Exemplo de ``<collab>`` em ``<front>`` com uma autoria institucional e nomes dos colaboradores pertencentes a instituição mais nomes de autores pessoa física, não pertencentes a instituição (autoria mista):
--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

.. code-block:: xml

   ...
   <contrib-group>
      <contrib contrib-type="author" id="collab">
        <collab>The MARS Group</collab>
        <xref ref-type="author-notes" rid="fn1">1</xref>
      </contrib>
      <contrib contrib-type="author">  
      <contrib-id contrib-id-type="orcid">0000-0001-8528-2091</contrib-id>      
        <name>
            <surname>Einstein</surname>
            <given-names>Albert</given-names>
        </name>
      </contrib> 
   </contrib-group>
   <contrib-group content-type="collab-list">
       <contrib contrib-type="non-byline-author" rid="collab">
         <name>
              <surname>Wright</surname>
              <given-names>Rick W.</given-names>
         </name>    
       </contrib>
       <contrib contrib-type="non-byline-author" rid="collab">
         <name>
              <surname>Huston</surname>
              <given-names>Laura J.</given-names>
         </name>     
       </contrib>
       <contrib contrib-type="non-byline-author" rid="collab">
         <name>
              <surname>Spindler</surname>
              <given-names>Kurt P.</given-names>
         </name>     
       </contrib>
   </contrib-group>



.. _elemento-collab-exemplo-5:

Exemplo de ``<collab>`` em ``<back>``:
--------------------------------------

.. code-block:: xml

   ...
   <element-citation publication-type="book">
        <person-group person-group-type="author">
             <collab>World Health Organization</collab>
        </person-group>
        <source>The top 10 causes of death. Fact sheet nº 310</source>
        <date-in-citation content-type="updated">Updated May 2014</date-in-citation>
        <date-in-citation content-type="access-date">citado 2012 Out 10</date-in-citation>
        <comment>Disponível em: <ext-link ext-link-type="uri" xlink:href="http://www.who.int/mediacentre/factsheets/fs310/en/index2.html">http://www.who.int/mediacentre/factsheets/fs310/en/index2.html</ext-link>
        </comment>
   </element-citation>
   ...

.. note:: 
 * Independente dos autores pessoa física fazerem parte da autoria institucional ``<collab>``, cada um deles devem possuir afiliação completa. Para mais informações acessar item 5.2.9. Afiliação de autores dos `Critérios, política e procedimentos para a admissão e a permanência de periódicos científicos na Coleção SciELO Brasil <http://www.scielo.br/avaliacao/Criterios_SciELO_Brasil_versao_revisada_atualizada_outubro_20171206.pdf>`_ 

.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
