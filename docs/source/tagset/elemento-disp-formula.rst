.. _elemento-disp-formula:

<disp-formula>
==============

Aparece em:

  :ref:`elemento-body`
  :ref:`elemento-p`
  ``<th>``
  ``<td>``
  :ref:`elemento-app`
  :ref:`elemento-supplementary-material`

Atributos obrigatórios:

  1. ``@id`` (ver :ref:`sugestao-atribuicao-id`)

Ocorre:

  Zero ou mais vezes


Identifica equações em parágrafos do texto, preferencialmente codificadas. Podem, excepcionalmente, ser apresentadas como imagem, devendo incluir o nome do arquivo de imagem no elemento ``<graphic>``. O atributo ``@id`` é mandatório.


Exemplos:

1. codificada:

.. code-block:: xml

    <!-- codificar: σˆ2 -->

    ...
    <xref ref-type="disp-formula" rid="e07">Equation 3</xref>
    <disp-formula>
        <mml:math id="e03">
            <mml:mrow>
                <mml:msup>
                    <mml:mover accent="true">
                        <mml:mi>σ</mml:mi>
                        <mml:mo>ˆ</mml:mo>
                    </mml:mover>
                    <mml:mn>2</mml:mn>
                </mml:msup>
            </mml:mrow>
        </mml:math>
    </disp-formula>
    ...

2. em imagem:

.. code-block:: xml

    ...
    <p>The Eh measurements were recalculated to the standard hydrogen potential (Standard Hydrogen Electrode - SHE), using the following <xref ref-type="disp-formula" rid="e01">equation 1</xref>(in mV):</p>
    <disp-formula id="e01">
        <graphic xlink:href="1234-5678-rctb-45-05-0110-e01.tif"/>
    </disp-formula>
    ...



.. note:: Equações que não estejam identificadas sob ``<app-group>`` devem ser inseridas obrigatoriamente após a primeira chamada no texto. Para material suplementar, analisar e identificar caso a caso.

.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
