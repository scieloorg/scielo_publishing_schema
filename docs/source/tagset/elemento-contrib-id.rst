.. _elemento-contrib-id:
 
<contrib-id>
^^^^^^^^^^^^

Aparece em
  :ref:`elemento-contrib`
 
Atributos obrigatórios
  contrib-id-type
 
Ocorre
  Zero ou mais vezes

Representa um identificador digital atribuído a um pesquisador. 

O atributo ``@contrib-id-type`` pode possuir os valores:

+------------+-------------------------------------------------------+
|  Valor     | Descrição                                             |
+============+=======================================================+
|  lattes    | identificador digital do Currículo Lattes             |
+------------+-------------------------------------------------------+
|  orcid     | identificador digital da ORCID Organization           |
+------------+-------------------------------------------------------+
| researchid | identificador digital da Thomson Reuters              |
+------------+-------------------------------------------------------+
|  scopus    | identificador digital do Scopus                       |
+------------+-------------------------------------------------------+


Exemplo:

.. code-block:: xml

    ...
    <contrib-group>
        <contrib>
            <contrib-id contrib-id-type="orcid">0000-0001-8528-2091</contrib-id>
            <contrib-id contrib-id-type="scopus">24771926600</contrib-id>            
            <name>
                <surname>Einstein</surname>
                <given-names>Albert</given-names>
            </name>
            ...
        </contrib>
        <contrib>
            <contrib-id contrib-id-type="lattes">4760273612238540</contrib-id>
            <name>
                <surname>Meneghini</surname>
                <given-names>Rogerio</given-names>
            </name>
            ...
        </contrib>
        ...
    </contrib-group>
    ...

.. note:: Não considerar URL para inserção em ``@contrib-id-type``. Exemplos **não** aceitos: 
          
          * ``<contrib-id contrib-id-type="lattes">http://lattes.cnpq.br/4760273612238540</contrib-id>``
          * ``<contrib-id contrib-id-type="orcid">http://orcid.org/0000-0001-8528-2091</contrib-id>``
