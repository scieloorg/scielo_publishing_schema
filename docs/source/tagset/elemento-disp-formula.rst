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


Identifica equações, expressões ou fórmulas matemáticas exibidas como um bloco dentro de um fluxo narrativo. Pode ser codificada usando MathML, TeX ou LaTeX.

Exemplos:

  * :ref:`elemento-dispmath-exemplo-1`
  * :ref:`elemento-displatex-exemplo-2`

.. _elemento-dispmath-exemplo-1:


Equação codificada em MathML:
-----------------------------

.. code-block:: xml

    <!-- codificar: σˆ2 -->

    ...
    <xref ref-type="disp-formula" rid="e03">Equation 3</xref>
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

.. _elemento-displatex-exemplo-2:


Equação codificada em LaTeX:
----------------------------

.. code-block:: xml

    ...
        <disp-formula id="e10">
            <label>(1)</label>
              <alternatives>
                 <tex-math id="tx1">
                  \documentclass {article}
                  \usepackage{wasysym}
                  \usepackage[substack]{amsmath}
                  \usepackage{amsfonts}
                  \usepackage{amssymb}
                  \usepackage{amsbsy}
                  \usepackage[mathscr]{eucal}
                  \usepackage{mathrsfs}                           
                  \usepackage{pmc}
                  \usepackage[Euler]{upgreek}
                  \pagestyle{empty}
                   \oddsidemargin -1.0in
                   \begin{document}
                   \[E_it=α_i+Z_it γ+W_it δ+C_it θ+∑_i^n EFind_i+∑_t^n EFtemp_t+ ε_it                                 \]
                   \end{document}
                 </tex-math>
                 <graphic xlink:href="0103-507X-rbti-26-02-0089-ee10.svg"/>
                </alternatives>
         </disp-formula>
    ...

.. note:: Equações que não estejam identificadas sob ``<app-group>`` devem ser inseridas obrigatoriamente após a primeira chamada no texto. Para material suplementar, analisar e identificar caso a caso.

.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
