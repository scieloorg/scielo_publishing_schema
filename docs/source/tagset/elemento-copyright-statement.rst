.. _elemento-copyright-statement:

<copyright-statement>
^^^^^^^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-permissions`
 
Ocorre
  Zero ou mais


O ``<copyright-statement>``, assim como o ``<license-p>`` são utilizados para 
fins de exibição. Esse elemento deve identificar a instituição a quem pertence 
os direitos. Normalmente a informação descrita aqui vem junto com o símbolo 
``©``.

Exemplo:

 .. code-block:: xml

    ...
     <article-meta>
       ...
        <permisssions>
           ...
            <copyright-statement>Copyright © 2014 SciELO</copyright-statement>
           ...
        </permissions>
        ...
     </article-meta>


Abaixo um exemplo completo do :ref:`elemento-permissions` em :ref:`elemento-article-meta`.

Exemplo:
 
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
 


**Exemplo de Figura com informação de licenciamento:**

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


**Exemplo de Tabela codificada com informação de licenciamento:**

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


**Exemplo de Tabela em imagem com informação de licenciamento:**

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
