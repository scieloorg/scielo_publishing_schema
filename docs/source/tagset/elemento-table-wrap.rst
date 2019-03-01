.. _elemento-table-wrap:

<table-wrap>
============


Atributos obrigatórios:

  1. ``@id`` (ver :ref:`sugestao-atribuicao-id`)

+----------------------------------------+--------------------+
| Aparece em                             | Ocorre             |
+========================================+====================+
| :ref:`elemento-app`                    | Zero ou mais vezes |
+----------------------------------------+--------------------+
| ``<app-group>``                        | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-body`                   | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-glossary`               | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-p`                      | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-sec`                    | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-supplementary-material` | Zero ou mais vezes |
+----------------------------------------+--------------------+



Especifica todas as partes de uma única tabela, incluindo :ref:`elemento-label`, :ref:`elemento-caption` e :ref:`elemento-table-wrap-foot`, caso exista.


Exemplo:

.. code-block:: xml

    ...
    <table-wrap id="t5">
      <label>Tabela 5</label>
      <caption>
        <title>Alíquota menor para prestadores</title>
      </caption>
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
      <table-wrap-foot>
        <fn id="TFN1">
           <p>A informação de alíquota do anexo II é significativa</p>
        </fn>
      </table-wrap-foot>
    </table-wrap>
    ...


Recomenda-se o uso de :ref:`elemento-alternatives` obrigatoriamente em formato .svg.


Exemplo:

.. code-block:: xml

    <table-wrap id="t2">
      <label>Tabela 2:</label>
      <caption>
        <title>Produção de tecidos de algodão da Fábrica Votorantim, do estado de São Paulo e do restante do Brasil, 1918-1930 - em milhões de metros</title>
      </caption>
      <alternatives>
        <graphic xlink:href="1980-5381-neco-28-02-579-gt02.svg"/>
        <table>
          <colgroup>
            <col/>
            <col/>
            <col/>
            <col/>
            <col/>
            <col/>
            <col/>
            <col/>
            <col/>
            <col/>
          </colgroup>
        <thead>
         <tr>
          <th align="left"> </th>
          <th align="center">1918</th>
          <th align="center">1919</th>
          <th align="center">1920</th>
          <th align="center">1921</th>
          <th align="center">1922</th>
          <th align="center">1923</th>
          <th align="center">1925</th>
          <th align="center">1929</th>
          <th align="center">1930</th>
         </tr>
      </thead>
      <tbody>
        <tr>
         <td align="left">Resto do país</td>
         <td align="center">347</td>
         <td align="center">409</td>
         <td align="center">400</td>
         <td align="center">355</td>
         <td align="center">410</td>
         <td align="center">452</td>
         <td align="center">330</td>
         <td align="center">329</td>
         <td align="center">341</td>
        </tr>
      <tr>
        <td align="left">Estado de São Paulo</td>
        <td align="center">147</td>
        <td align="center">175</td>
        <td align="center">187</td>
        <td align="center">198</td>
        <td align="center">217</td>
        <td align="center">488</td>
        <td align="center">206</td>
        <td align="center">149</td>
        <td align="center">135</td>
       </tr>
       <tr>
        <td align="left">Votorantim</td>
        <td align="center">13</td>
        <td align="center">11</td>
        <td align="center">16</td>
        <td align="center">16</td>
        <td align="center">21</td>
        <td align="center">24</td>
        <td align="center">20</td>
        <td align="center">16</td>
        <td align="center">17</td>
       </tr>
      </tbody>
    </table>
      </alternatives>
    <table-wrap-foot>
       <fn id="TFN3">
         <p>Fonte: Cano (1981, p. 293); SÃO PAULO. <italic>Diário Oficial do Estado de São Paulo</italic>, 30/06/1922, p. 1922; 15/02/1923, p. 1923; 14/02/1925, p. 1233; 12/02/1926, p. 1243; 22/03/1931 p. 2327.</p>
      </fn>
     </table-wrap-foot>
    </table-wrap>


.. {"reviewed_on": "20160803", "by": "gandhalf_thewhite@hotmail.com"}
