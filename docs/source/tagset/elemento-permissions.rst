.. _elemento-permissions:

<permissions>
=============

Aparece em:

  :ref:`elemento-article-meta`
  :ref:`elemento-boxed-text`
  :ref:`elemento-disp-quote`
  :ref:`elemento-fig`
  ``<graphic>``
  :ref:`elemento-media`
  :ref:`elemento-supplementary-material`
  :ref:`elemento-table-wrap`
  :ref:`elemento-verse-group`


Ocorre:

  1. Uma vez em :ref:`elemento-article-meta`
  2. Zero ou mais vezes nos demais elementos

A permissão é um conjunto de condições sob as quais o conteúdo do artigo pode ser usado, acessado e distribuído.

A tabela abaixo demonstra o tipo de objeto no texto, que elementos apresentam :ref:`elemento-permissions` e qual o tipo de permissão envolvida nestes.

+----------------------+--------------------------+---------------------------------------+
| Objeto do Documento  | Elementos que podem      | O que a permissão envolve             |
|                      | apresentar <permisssions>|                                       |
+======================+==========================+=======================================+
| Caixa de Texto       | <boxed-text>             | O próprio elemento                    |
+----------------------+--------------------------+---------------------------------------+
| Citação              | <disp-quote>             | O próprio elemento                    |
+----------------------+--------------------------+---------------------------------------+
| Figura               | <fig>                    | Toda a figura e arquivos relacionados |
+----------------------+--------------------------+---------------------------------------+
| Gráfico/Imagem       | <graphic>                | O arquivo da imagem (`@xlink:href`) e |
|                      |                          | sua descrição                         |
+----------------------+--------------------------+---------------------------------------+
| Mídia                | <media>                  | O arquivo mídia (`@xlink:href`) e     |
|                      |                          | sua descrição                         |
+----------------------+--------------------------+---------------------------------------+
| Material Suplementar | <supplementary-material> | O arquivo suplementar e sua descrição |
+----------------------+--------------------------+---------------------------------------+
| Tabelas, legendas e  | <table-wrap>             | A tabela, rótulo, legenda e           |
| notas                |                          | notas de rodapé de tabela             |
+----------------------+--------------------------+---------------------------------------+
| Grupo de Versos      | <verse-group>            | O próprio elemento                    |
+----------------------+--------------------------+---------------------------------------+


Exemplos:

  * :ref:`elemento-permissions-exemplo-1`
  * :ref:`elemento-permissions-exemplo-2`
  * :ref:`elemento-permissions-exemplo-3`
  * :ref:`elemento-permissions-exemplo-4`


.. _elemento-permissions-exemplo-1:

1. em :ref:`elemento-article-meta`:

.. code-block:: xml

    ...
    <article-meta>
        ...
        <permissions>
            <copyright-statement>Copyright © 2014 SciELO</copyright-statement>
            <copyright-year>2014</copyright-year>
            <copyright-holder>SciELO</copyright-holder>
            <license license-type="open-access" xlink:href="http://creativecommons.org/licenses/by-nc/4.0/" xml:lang="en">
                <license-p>The JATS Standard is copyrighted by NISO, but all of the non-normative information found on this repository is in the CC BY-NC 4.0</license-p>
            </license>
        </permissions>
        ...
    </article-meta>
    ...


.. _elemento-permissions-exemplo-2:

2. em ``<fig>``:

.. code-block:: xml

    ...
    <fig id="f01">
        <label>Fig. 1</label>
        <caption>
            <title>título da imagem</title>
        </caption>
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
        <permissions>
            <copyright-statement>Copyright © 2014 SciELO</copyright-statement>
            <copyright-year>2014</copyright-year>
            <copyright-holder>SciELO</copyright-holder>
            <license license-type="open-access" xlink:href="http://creativecommons.org/licenses/by-nc-sa/4.0/" xml:lang="en">
                <license-p>This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.</license-p>
            </license>
        </permissions>
    </fig>
    ...


.. _elemento-permissions-exemplo-3:

3. em ``<table-wrap>``:

.. code-block:: xml

   ...
   <table-wrap>
      <label>Table 1</label>
      <caption>
         <title>Chemical characterization of the oxides of the tailing</title>
      </caption>
      <table frame="hsides" rules="groups">
         <thead>
             <tr>
                <th>Variável</th>
                <th>Resultados (N=880)</th>
             </tr>
          </thead>
          <tbody>
             <tr>
                <td align="center">Gênero</td>
                <td align="center"/>
             </tr>
             <tr>
                <td align="center">Masculino</td>
                <td align="center">411 (46,7)</td>
             </tr>
             <tr>
                <td align="center">Feminino</td>
                <td align="center">469 (53,3)</td>
             </tr>
          </tbody>
      </table>
      <permissions>
            <copyright-statement>Copyright © 2014 SciELO</copyright-statement>
            <copyright-year>2014</copyright-year>
            <copyright-holder>SciELO</copyright-holder>
            <license license-type="open-access" xlink:href="http://creativecommons.org/licenses/by-nc-sa/4.0/" xml:lang="en">
                <license-p>This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.</license-p>
            </license>
      </permissions>
   </table-wrap>


.. _elemento-permissions-exemplo-4:

4. referente imagem dentro de ``<table-wrap>``:

.. code-block:: xml

   ...
   <table-wrap>
      <label>Table 3</label>
      <caption>
         <title>Multivariate analysis of risk factors associated with readmission - Model 2</title>
      </caption>
         <graphic xlink:href="1234-5678-rctb-45-05-0110-gt031.tif"/>
         <permissions>
            <copyright-statement>Copyright © 2014 SciELO</copyright-statement>
            <copyright-year>2014</copyright-year>
            <copyright-holder>SciELO</copyright-holder>
            <license license-type="open-access" xlink:href="http://creativecommons.org/licenses/by-nc-sa/4.0/" xml:lang="en">
                <license-p>This work is licensed under a Creative Commons Attribution-NonCommercial-ShareAlike 4.0 International License.</license-p>
            </license>
         </permissions>
   </table-wrap>


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
