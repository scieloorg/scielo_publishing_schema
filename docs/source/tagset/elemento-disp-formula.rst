.. _elemento-disp-formula:

<disp-formula>
==============

Este elemento possui :ref:`scielo-brasil`


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



Identifica equações e fórmulas exibidas em bloco, fora de um parágrafo. A codificação pode ser escrita de acordo com :term:`W3C` em linguagem :term:`MathML` (http://www.w3.org/TR/MathML3/), sendo o elemento base ``<mml:math>`` ou com codificação TeX ou LaTeX.
 

Exemplos:

  * :ref:`elemento-dispmath-exemplo-1`
  * :ref:`elemento-displatex-exemplo-2`

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



.. note:: Equações que não estejam identificadas sob ``<app-group>`` devem ser inseridas obrigatoriamente após a primeira chamada no texto.

