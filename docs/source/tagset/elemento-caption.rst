.. _elemento-caption:

<caption>
=========


+----------------------------------------+--------------------+
| Aparece em                             | Ocorre             |
+========================================+====================+
| :ref:`elemento-boxed-text`             | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-disp-formula`           | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-fig`                    | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-media`                  | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-supplementary-material` | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-table-wrap`             | Zero ou mais vezes |
+----------------------------------------+--------------------+


Descreve uma legenda para vários tipos de objeto. ``<caption>`` envolve o elemento ``<title>`` para conter o texto descritivo de uma tabela, figura, mídia, fórmula ou objeto similar e também o elemento ``<p>`` para identificação de texto adicional.


Exemplos:

  * :ref:`elemento-caption-exemplo-1`
  * :ref:`elemento-caption-exemplo-2`


.. _elemento-caption-exemplo-1:

Exemplo de ``<fig>`` com ``<caption>`` simples:
-----------------------------------------------

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


.. _elemento-caption-exemplo-2:

Exemplo de ``<fig>`` com ``<caption>`` com informação adicional:
----------------------------------------------------------------

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
