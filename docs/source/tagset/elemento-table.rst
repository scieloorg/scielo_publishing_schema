.. _elemento-table:

<table>
-------

Aparece em:

  :ref:`elemento-table-wrap`

Ocorre:

  Uma vez


Elemento que identifica uma tabela codificada conforme o padrão :term:`NISO JATS table model`, com a adição das regras:

* O primeiro nível da estrutura não pode conter o elemento ``<tr>``, ex.: ``//table/tr``.
* Elemento ``<th>`` apenas como descendente de ``<thead>``.
* Elemento ``<td>`` apenas como descendente de ``<tbody>``.


Toda a formatação para exibição deve ser realizada conforme descrito no guia `Table Formatting <http://jats.nlm.nih.gov/publishing/tag-library/1.0/n-unw2.html#pub-tag-table-format>`_.


.. _elemento-table-traduzida:

Legenda Traduzida
^^^^^^^^^^^^^^^^^

Tabelas com legendas traduzidas, com mais de um rótulo (``<label>``) e legenda (``<caption>``), devem ser identificadas pelo elemento ``<table-wrap-group>``, o qual deve conter os elementos ``<table-wrap>`` para cada idioma.

Exemplos:

1. Exemplo de tabela codificada:

.. code-block:: xml

    ...
    <table-wrap-group id="t01">
        <table-wrap xml:lang="pt">
            <label>Tabela 1</label>
            <caption>
                <title>Caracterização química em óxidos do rejeito.</title>
            </caption>
        </table-wrap>
        <table-wrap xml:lang="en">
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
        </table-wrap>
    </table-wrap-group>
    ...


2. Exemplo de tabela como imagem:

.. code-block:: xml

    ...
    <table-wrap-group id="t03">
        <table-wrap xml:lang="pt">
            <label>Tabela 3</label>
            <caption>
                <title>Análise multivariada dos fatores de risco associados à readmissão - modelo 2</title>
            </caption>
        </table-wrap>
        <table-wrap id="en">
            <label>Table 3</label>
            <caption>
                <title>Multivariate analysis of risk factors associated with readmission - Model 2</title>
            </caption>
            <graphic xlink:href="1234-5678-rctb-45-05-0110-gt031.tif"/>
        </table-wrap>
    </table-wrap-group>
    ...


.. {"reviewed_on": "20160629", "by": "gandhalf_thewhite@hotmail.com"}
