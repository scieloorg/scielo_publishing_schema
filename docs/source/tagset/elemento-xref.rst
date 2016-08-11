.. _elemento-xref:

<xref>
======

Aparece em:

  :ref:`elemento-article-title`,
  :ref:`elemento-trans-title`,
  :ref:`elemento-contrib`,
  :ref:`elemento-p`,
  ``<th>``,
  ``<td>``.
  ``<verse-line>``,
  :ref:`elemento-attrib`.

Atributos obrigatórios:

  1. ``@rid``
  2. ``@ref-type``

Ocorre:

  Zero ou mais vezes


Elemento de referência cruzada usado para relacionar e/ou fazer ligação com alguma informação no texto.

Os atributos obrigatórios para ``xref`` são:

* ``@rid``: contém o identificador do elemento do artigo referenciado, perfazendo assim o link entre a origem (``@rid``) e o destino (``@id``) no texto.
* ``@ref-type``: especifica o tipo de referência cruzada, cujos valores são:


+------------------------+-----------------------------------------+
| Valor                  | Descrição                               |
+========================+=========================================+
| aff                    | afiliação                               |
+------------------------+-----------------------------------------+
| app                    | apêndice                                |
+------------------------+-----------------------------------------+
| author-notes           | notas de autor (ou relacionado a autor) |
+------------------------+-----------------------------------------+
| bibr                   | referência bibliográfica                |
+------------------------+-----------------------------------------+
| boxed-text             | caixa de texto                          |
+------------------------+-----------------------------------------+
| contrib                | contribuinte                            |
+------------------------+-----------------------------------------+
| corresp                | autor correspondente                    |
+------------------------+-----------------------------------------+
| disp-formula           | fórmula                                 |
+------------------------+-----------------------------------------+
| fig                    | figura ou grupo de figuras              |
+------------------------+-----------------------------------------+
| fn                     | nota de rodapé                          |
+------------------------+-----------------------------------------+
| sec                    | seção                                   |
+------------------------+-----------------------------------------+
| supplementary-material | material suplementar                    |
+------------------------+-----------------------------------------+
| table                  | tabela ou grupo de tabelas              |
+------------------------+-----------------------------------------+
| table-fn               | nota de rodapé de tabelas               |
+------------------------+-----------------------------------------+


Exemplos:


.. code-block:: xml

    ...
    <article-meta>
        ...
        <contrib-group>
            <contrib contrib-type="author">
                <name>
                    <surname>Lacerda</surname>
                    <given-names>Marcus VG</given-names>
                </name>
                <xref ref-type="aff" rid="aff1">1</xref>
            </contrib>
            <aff id="aff1">
                <label>1</label>
                <institution content-type="orgname">Universidade do Estado do Amazonas</institution>
                <institution content-type="normalized">Universidade do Estado do Amazonas</institution>
                <addr-line>
                    <named-content content-type="city">Manaus</named-content>
                    <named-content content-type="state">AM</named-content>
                </addr-line>
                <country country="BR">Brasil</country>
                <institution content-type="original">Universidade do Estado do Amazonas, Manaus, AM, Brasil</institution>
            </aff>
            ...
        </contrib-group>
        ...
    </article-meta>
    ...


.. code-block:: xml

     <xref ref-type="bibr" rid="B13">John 2003</xref>


.. code-block:: xml

    <p>Check in <xref ref-type="fig" rid="f01">Figure</xref>:</p>
    <p>
        <fig id="f01">
            <caption>
                <title>Environmental <italic>in situ</italic> conditions during the study period.</title>
            </caption>
            <graphic xlink:href="0074-0276-mioc-0074-0276140068-gf01"/>
        </fig>
    </p>


.. note:: Não envolver a tag ``<xref>`` em ``<sup>``.


Para casos em que não há rótulo (``<label>``) explícito relacionando o autor à afiliação, deve ser inserido em :ref:`elemento-contrib` um elemento ``<xref>`` "fechado".


Exemplo:


.. code-block:: xml

  ...
  <article-meta>
    ...
    <contrib-group>
      <contrib contrib-type="author">
        <name>
            <surname>Broering</surname>
            <given-names>Laurent Wiliam</given-names>
        </name>
        <xref ref-type="aff" rid="aff1"/>
      </contrib>
    </contrib-group>
    <aff id="aff1">
      <institution content-type="normalized">Fundação Getúlio Vargas</institution>
      <institution content-type="orgname">Fundação Getúlio Vargas</institution>
      <institution content-type="orgdiv1">EAESP</institution>
      <addr-line>
        <named-content content-type="city">São Paulo</named-content>
        <named-content content-type="state">SP</named-content>
      </addr-line>
      <country country="BR">Brazil</country>
      <institution content-type="original">Fundação Getúlio Vargas - FGV-EAESP, Av. 9 de Julho, 2029, Bela Vista, 01313-902, São Paulo, SP, Brazil.</institution>
    </aff>
  ...

.. note:: Não inserir rótulo (``<label>``) caso não exista no :term:`documento`.


.. {"reviewed_on": "20160803", "by": "gandhalf_thewhite@hotmail.com"}
