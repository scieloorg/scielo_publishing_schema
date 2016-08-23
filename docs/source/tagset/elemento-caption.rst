.. _elemento-caption:

<caption>
=========

Aparece em:

  :ref:`elemento-boxed-text`
  :ref:`elemento-disp-formula`
  :ref:`elemento-fig`
  :ref:`elemento-media`
  :ref:`elemento-supplementary-material`
  :ref:`elemento-table-wrap`
  

Ocorre:

  Zero ou mais vezes

Descreve uma legenda para vários tipos de objeto. ``<caption>`` envolve o elemento ``<title>`` para conter o texto descritivo de uma tabela, figura, mídia, fórmula ou objeto similar e também o elemento ``<p>`` para identificação de texto adicional.

Exemplo:

.. code-block:: xml

    ...
    <fig id="f03">
        <label>Figura 3</label>
        <caption>
            <title>Percentual de atividade mitocondrial (método MTT) das células dos diferentes grupos experimentais em relação às células do grupo controle</title>
        </caption>
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf03.tif"/>
    </fig>
    ...

Exemplo de Figura com informação adicional:

.. code-block:: xml

  ...
  <fig id="f03">
        <label>Figura 4</label>
        <caption>
            <title>Despesas realizadas pelas IES brasileiras em 2005 como percentuais do PIB</title>
            <p>(Valores em R$ bilhões, a preços de janeiro de 2010, corrigidos pelo IPCA)</p>
        </caption>
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf04.tif"/>
    </fig>
    ...

.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
