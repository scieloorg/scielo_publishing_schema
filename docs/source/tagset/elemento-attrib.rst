.. _elemento-attrib:

<attrib>
--------

Aparece em:

  :ref:`elemento-boxed-text`
  :ref:`elemento-fig`
  ``<graphic>``
  :ref:`elemento-media`
  :ref:`elemento-supplementary-material`
  :ref:`elemento-table-wrap`
  :ref:`elemento-verse-group`

Ocorre:

  Zero ou mais vezes

Utilizado para creditar o autor ou o licenciador de ativos ou conteúdos que requerem tal atribuição.

Exemplo em figura:

.. code-block:: xml

    ...
    <fig id="f02" fig-type="other">
      <label>Figure 2</label>
        <caption>
          <title>Produtividade das variantes lexicais para a questão 132 do QSL segundo a região administrativa</title>
        </caption>
        <graphic xlink:href="0103-507X-rbti-26-02-0130-g02.tif"/>
        <attrib>Fonte: Banco de dados do ALiB (2013).</attrib>
    </fig>

.. note:: em figuras o elemento :ref:`elemento-attrib` deve ser inserido abaixo de ``<graphic>``.


Exemplo em versos:

.. code-block:: xml

    ...
    <verse-group>
        <verse-line>Porque quando te não vejo, deixastes de existir.</verse-line>
        <verse-line>E se se tem saudades do que não existe,</verse-line>
        <verse-line>Sinto-a em relação a cousa nenhuma;</verse-line>
        <verse-line>Não é do navio, é de nós, que sentimos saudade.</verse-line>
        <attrib>(Alberto Caeiro, O guardador de rebanhos e outros poemas).</attrib>
    </verse-group>
    ...


.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
