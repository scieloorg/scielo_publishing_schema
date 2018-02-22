.. _elemento-alternatives:

<alternatives>
==============

+----------------------------------+--------------------+
| Aparece em                       | Ocorre             |
+==================================+====================+
| * :ref:`elemento-table-wrap`     | Zero ou mais vezes |
+----------------------------------+--------------------+
| * :ref:`elemento-disp-formula`   | Zero ou mais vezes |
+----------------------------------+--------------------+
| * :ref:`elemento-inline-formula` | Zero ou mais vezes |
+----------------------------------+--------------------+


Elemento usado para armazenar um grupo de alternativas para processamento de um determinado conjunto informacional em versões logicamente equivalentes (substituto), como por exemplo, uma tabela ou uma equação codificada e sua imagem SVG equivalente. Caso não exista mais de uma alternativa de visualização do conjunto informacional em questão, não se faz necessário a utilização da tag. 

.. note:: Em <alternatives> as imagens em <graphic> devem, obrigatoriamente, possuir a extensão .svg.

Exemplos:

  * :ref:`elemento-table-exemplo-1`
  * :ref:`elemento-disp-formula-exemplo-2`
  * :ref:`elemento-inline-formula-exemplo-3`

.. _elemento-table-exemplo-1:

Exemplo de <alternatives> em <table-wrap>:
------------------------------------------

.. code-block:: xml

    ...
    <table-wrap id="t5">
      <label>Tabela 5</label>
      <caption>
        <title>Alíquota menor para prestadores</title>
      </caption>
     <alternatives>
      <graphic xlink:href="nomedaimagemdatabela.svg"/>
      <table>
        <thead>
          <tr>
            <th rowspan="3">Proposta de Novas Tabelas - 2016</th>
          </tr>
          <tr>
            <th>Receita Bruta em 12 Meses - em R$</th>
            <th>Anexo I - Comércio</th>
            <th>Anexo II Indústria</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td>De R$ 225.000,01 a RS 450.000,00</td>
            <td>4,00%</td>
            <td>4,50%</td>
          </tr>
          <tr>
            <td>De R$ 450.000,01 a R$ 900.000,00</td>
            <td>8,25%</td>
            <td>8,00%</td>
          </tr>
          <tr>
            <td>De R$ 900.000,01 a R$ 1.800.000,00</td>
            <td>11,25%</td>
            <td>12,25%</td>
          </tr>
        </tbody>
      </table>
     </alternatives>
      <table-wrap-foot>
        <fn id="TFN1">
           <p>A informação de alíquota do anexo II é significativa</p>
        </fn>
      </table-wrap-foot>
    </table-wrap>
    ...
.. _elemento-disp-formula-exemplo-2:

Exemplo de <alternatives> em <disp-formula>:
--------------------------------------------

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

.. _elemento-inline-formula-exemplo-3:

Exemplo de <alternatives> em <inline-formula>:
----------------------------------------------

.. code-block:: xml

    ...
  <inline-formula>
    <alternatives>
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
     <graphic xlink:href="0103-507X-rbti-26-02-0089-ee10.svg"/>
    </alternatives>
  </inline-formula>
