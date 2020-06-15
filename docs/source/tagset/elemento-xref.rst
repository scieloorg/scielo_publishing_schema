.. _elemento-xref:

<xref>
======

Este elemento possui :ref:`scielo-brasil`


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
                     <city>Manaus</city>
                     <state>AM</state>
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


.. note:: 
 * Não envolver a tag ``<xref>`` em ``<sup>``.
 * Não inserir ``<label>`` caso não exista no :term:`documento`.
 * Recomenda-se ver sugestão de atribuição de `@id <https://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/tagset/sugestao-atribuicao-id.html>`_ .



