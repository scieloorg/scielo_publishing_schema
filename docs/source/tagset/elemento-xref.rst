.. _elemento-xref:

<xref>
======

Atributos obrigatórios:

  1. ``@rid``
  2. ``@ref-type``

+--------------------------------+--------------------+
| Aparece em                     | Ocorre             |
+================================+====================+
| :ref:`elemento-article-title`  | Zero ou mais vezes |
+--------------------------------+--------------------+
| :ref:`elemento-attrib`         | Zero ou mais vezes |
+--------------------------------+--------------------+
| :ref:`elemento-contrib`        | Zero ou mais vezes |
+--------------------------------+--------------------+
| :ref:`elemento-p`              | Zero ou mais vezes |
+--------------------------------+--------------------+
| ``<td>``                       | Zero ou mais vezes |
+--------------------------------+--------------------+
| ``<th>``                       | Zero ou mais vezes |
+--------------------------------+--------------------+
| :ref:`elemento-trans-title`    | Zero ou mais vezes |
+--------------------------------+--------------------+
| :ref:`elemento-sec`            | Zero ou mais vezes |
+--------------------------------+--------------------+
| ``<verse-line>``               | Zero ou mais vezes |
+--------------------------------+--------------------+



Elemento de referência cruzada usado para relacionar alguma informação no texto.

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

  * :ref:`elemento-xref-exemplo-1`
  * :ref:`elemento-xref-exemplo-2`
  * :ref:`elemento-xref-exemplo-3`
  * :ref:`elemento-xref-exemplo-4`


.. _elemento-xref-exemplo-1:

Exemplo de ``<xref>`` em ``<article-meta>``:
--------------------------------------------

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


.. _elemento-xref-exemplo-2:

Exemplo de ``<xref>`` em ``<p>``:
---------------------------------

.. code-block:: xml

  ...
  <p>
    ...
     <xref ref-type="bibr" rid="B13">John 2003</xref>
     ...
  </p>
  ...


.. _elemento-xref-exemplo-3:

Exemplo de ``<xref>`` relacionado a objeto no texto:
----------------------------------------------------

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



.. _elemento-xref-exemplo-4:

Exemplo de ``<xref>`` "fechado":
--------------------------------

Para casos em que não há rótulo (``<label>``) explícito relacionando o autor à afiliação, deve ser inserido em :ref:`elemento-contrib` um elemento ``<xref>`` "fechado".


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


.. note:: 
 * Não envolver a tag ``<xref>`` em ``<sup>``.
 * Não inserir ``<label>`` caso não exista no :term:`documento`.
 * Recomenda-se ver sugestão de atribuição de `@id <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/tagset/sugestao-atribuicao-id.html>`_ .



