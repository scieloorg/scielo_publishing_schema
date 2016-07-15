.. _elemento-caption:

<caption>
=========

Aparece em:

  :ref:`elemento-disp-formula`
  :ref:`elemento-fig`
  :ref:`elemento-table-wrap`
  :ref:`elemento-media`
  :ref:`elemento-supplementary-material`

Ocorre:

  Zero ou mais vezes

Descreve uma legenda para vários tipos de objeto. ``<caption>`` encerra o elemento ``<title>`` para conter o texto descritivo de uma tabela, figura, mídia, fórmula ou objeto similar.

Exemplo:

.. code-block:: xml

    ...
    <fig id="f03">
        <label>Figura 3</label>
        <caption>
            <title>Percentual de atividade mitocondrial (método MTT) das células dos diferentes grupos experimentais em relação às células do grupo controle</title>
        </caption>
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
    </fig>
    ...


.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
