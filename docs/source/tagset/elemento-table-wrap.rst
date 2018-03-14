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


.. {"reviewed_on": "20160803", "by": "gandhalf_thewhite@hotmail.com"}
