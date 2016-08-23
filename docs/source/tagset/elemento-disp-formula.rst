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

1. Equação codificada:

.. code-block:: xml

    <!-- codificar: σˆ2 -->

    ...
    <xref ref-type="disp-formula" rid="e07">Equation 3</xref>
    <disp-formula id="e03">
     <mml:math display="block">
          <mml:mrow>
               <mml:msub>
                    <mml:mi>q</mml:mi>
                    <mml:mi>c</mml:mi>
               </mml:msub>
               <mml:mo>=</mml:mo>
               <mml:mi>h</mml:mi>
               <mml:mrow>
                    <mml:mo>(</mml:mo>
                    <mml:mrow>
                         <mml:mi>T</mml:mi>
                         <mml:mo>−</mml:mo>
                         <mml:msub>
                              <mml:mi>T</mml:mi>
                              <mml:mn>0</mml:mn>
                         </mml:msub>
                    </mml:mrow>
                    <mml:mo>)</mml:mo>
               </mml:mrow>
          </mml:mrow>
     </mml:math>
     <label>(3)</label>
</disp-formula>
    ...

2. Equação em imagem:

.. code-block:: xml

    ...
    <p>The Eh measurements were recalculated to the standard hydrogen potential (Standard Hydrogen Electrode - SHE), using the following <xref ref-type="disp-formula" rid="e01">equation 1</xref>(in mV):</p>
    <disp-formula id="e01">
        <graphic xlink:href="1234-5678-rctb-45-05-0110-e01.tif"/>
    </disp-formula>
    ...



.. note:: Equações que não estejam identificadas sob ``<app-group>`` devem ser inseridas obrigatoriamente após a primeira chamada no texto. Para material suplementar, analisar e identificar caso a caso.

.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
