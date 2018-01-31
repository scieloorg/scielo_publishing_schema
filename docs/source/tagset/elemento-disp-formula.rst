.. _elemento-disp-formula:

<disp-formula>
==============

Atributos obrigatórios:

  1. ``@id`` (ver :ref:`sugestao-atribuicao-id`)

+----------------------------------------+--------------------+
| Aparece em                             | Ocorre             |
+========================================+====================+
| :ref:`elemento-body`                   | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-p`                      | Zero ou mais vezes |
+----------------------------------------+--------------------+
| ``<th>``                               | Zero ou mais vezes |
+----------------------------------------+--------------------+
| ``<td>``                               | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-app`                    | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-supplementary-material` | Zero ou mais vezes |
+----------------------------------------+--------------------+



Identifica equações, expressões ou fórmulas matemáticas exibidas como um bloco dentro de um fluxo narrativo. Pode ser codificada usando MathML, TeX ou LaTeX.

Exemplos:

  * :ref:`elemento-dispmath-exemplo-1`
  * :ref:`elemento-displatex-exemplo-2`
  * :ref:`elemento-dispimg-exemplo-3`

.. _elemento-dispmath-exemplo-1:


Equação codificada em MathML:
-----------------------------

.. code-block:: xml

    <!-- codificar: σˆ2 -->

    ...
    <xref ref-type="disp-formula" rid="e3">Equation 3</xref>
    ...
    <disp-formula id="e3">
      <mml:math id="m1" display="block">
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
    </disp-formula>
    ...

.. _elemento-dispimg-exemplo-3:

Equação em imagem:
------------------

.. code-block:: xml

    ...
    <p>The Eh measurements were recalculated to the standard hydrogen potential (Standard Hydrogen Electrode - SHE), using the following <xref ref-type="disp-formula" rid="e1">equation 1</xref>(in mV):</p>
    <disp-formula id="e1">
        <graphic xlink:href="1234-5678-rctb-45-05-0110-e01.tif"/>
    </disp-formula>
    ...


Para *SciELO* Brasil consulte:

:ref:`scielo-brasil`

.. note:: Equações que não estejam identificadas sob ``<app-group>`` devem ser inseridas obrigatoriamente após a primeira chamada no texto. Para material suplementar, analisar e identificar caso a caso.

.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}