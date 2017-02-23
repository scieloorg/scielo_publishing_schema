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

<p>... Selected as described for Acc-29
<disp-formula>
<tex-math id="M1"><![CDATA[\documentclass[12pt]{minimal}
\usepackage{wasysym}
\usepackage[substack]{amsmath}
\usepackage{amsfonts}
\usepackage{amssymb}
\usepackage{amsbsy}
\usepackage[mathscr]{eucal}
\usepackage{mathrsfs}
\DeclareFontFamily{T1}{linotext}{}
\DeclareFontShape{T1}{linotext}{m}{n} { &#x003C;-&#x003E; linotext }{}
\DeclareSymbolFont{linotext}{T1}{linotext}{m}{n}
\DeclareSymbolFontAlphabet{\mathLINOTEXT}{linotext}
\begin{document}
$$
{\mathrm{Acc/Acc:\hspace{.5em}}}\frac{{\mathit{ade2-202}}}{{\mathit{ADE2}}}\
hspace{.5em}\frac{{\mathit{ura3-59}}}{{\mathit{ura3-59}}}\hspace{.5em}\frac{{\
mathit{ADE1}}}{{\mathit{adel-201}}}\hspace{.5em}\frac{{\mathit{ter1-Acc}}}{{\
mathit{ter1-Acc}}}\hspace{.5em}\frac{{\mathit{MATa}}}{{\mathit{MAT{\alpha}}}}
$$
\end{document}]]>
</tex-math>
</disp-formula> TER1/ter1-Acc: Acc-29 crossed with ...</p>
...

.. note:: Equações que não estejam identificadas sob ``<app-group>`` devem ser inseridas obrigatoriamente após a primeira chamada no texto. Para material suplementar, analisar e identificar caso a caso.

.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
