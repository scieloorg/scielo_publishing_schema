.. _elemento-fig:

<fig>
=====


Atributos obrigatórios:

  1. ``@id`` (ver :ref:`sugestao-atribuicao-id`)

+----------------------------------------+--------------------+
| Aparece em                             | Ocorre             |
+========================================+====================+
| :ref:`elemento-app`                    | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-body`                   | Zero ou mais vezes |
+----------------------------------------+--------------------+
| ``<fig-group>``                        | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-glossary`               | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-p`                      | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-supplementary-material` | Zero ou mais vezes |
+----------------------------------------+--------------------+



Identifica figura(s) de um artigo. Nesse elemento é possível especificar :ref:`elemento-label`, :ref:`elemento-caption`, ``<graphic>`` e :ref:`elemento-attrib`. ``<fig>`` pode ainda conter os seguintes atributos: ``@fig-type`` e ``@xml:lang``.

O elemento ``<graphic>`` é utilizado para identificar os tipos de arquivo que podem ser .tif, .jpg ou .png e tem como atributo ``@xlink:href:`` que é utilizado para especificar o nome completo da imagem referenciada.


O atributo ``@id:`` permite fazer referência cruzada no :term:`documento` (link relacionado a um "rid"), desde que o atributo tenha um valor único no arquivo.

Exemplos:

    * :ref:`elemento-fig-exemplo-1`
    * :ref:`elemento-fig-exemplo-2`
    * :ref:`elemento-fig-exemplo-3`
    * :ref:`elemento-fig-exemplo-4`
    * :ref:`elemento-fig-exemplo-5`



.. _elemento-fig-exemplo-1:

Exemplo de Figura sem label e caption:
--------------------------------------

As imagens podem ou não ter legendas. Para imagens sem legenda é necessário marcá-la como ``<fig>`` e identificá-la com o elemento ``<graphic>``.

.. code-block:: xml

    ...
    <fig id="f01">
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
    </fig>
    ...



.. _elemento-fig-exemplo-2:

Exemplo de Figura com label e caption:
--------------------------------------

Para figuras com legenda, dentro de ``<fig>`` serão identificados :ref:`elemento-label` e :ref:`elemento-caption` com o título da figura em ``<title>``.


.. code-block:: xml

    ...
    <fig id="f03">
        <label>Fig. 3</label>
        <caption>
            <title>título da imagem</title>
        </caption>
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf03.tif"/>
    </fig>
    ...


.. _elemento-fig-exemplo-3:

Exemplo de Figura com label específico:
---------------------------------------

O atributo ``@fig-type:`` é utilizado para especificar o tipo de imagem, que pode ser:

+------------+--------------+
| Descrição  | Valor        |
+============+==============+
| gráfico    | graphic      |
+------------+--------------+
| quadro     | chart        |
+------------+--------------+
| diagrama   | diagram      |
+------------+--------------+
| desenho    | drawing      |
+------------+--------------+
| ilustração | illustration |
+------------+--------------+
| mapa       | map          |
+------------+--------------+

Contudo o tipo só será definido caso o :ref:`elemento-label` apresente um conteúdo diferente de fig, figure, figura.


.. code-block:: xml

    ...
    <fig fig-type="map" id="f01">
        <label>Map 1</label>
        <caption>
            <title>Título do Mapa<title>
        </caption>
        <graphic xlink:href="1234-5678-zwy-12-04-0123-gf01.tif"/>
    </fig>
    ...

Se a figura não possuir um tipo específico, deve-se manter o elemento sem o atributo.



.. _elemento-fig-exemplo-4:

Exemplo de figura com informação de fonte :ref:`elemento-attrib`:
-----------------------------------------------------------------

.. code-block:: xml

    ...
    <fig id="f02">
        <label>FIGURE 2</label>
        <caption>
            <title>Título da figura</title>
        </caption>
        <graphic xlink:href="1234-5678-zwy-12-04-0123-gf02.tif"/>
        <attrib>Fonte: IBGE (2018)</attrib>
    </fig>


.. _elemento-fig-exemplo-5:

Exemplo de Figura com legenda traduzida:
````````````````````````````````````````

Figuras que apresentam legendas traduzidas (com mais de um :ref:`elemento-label` e :ref:`elemento-caption`), devem ser identificadas com o elemento ``<fig-group>``, o qual deve conter os elementos ``<fig>`` para cada idioma utilizando o atributo ``@xml:lang``.


.. code-block:: xml

    ...
    <fig-group id="f1">
        <fig xml:lang="pt">
            <label>Figura 1</label>
            <caption>
                <title>Caracterização química em óxidos do rejeito.</title>
            </caption>
        </fig>
        <fig xml:lang="en">
            <label>Figure 1</label>
            <caption>
                <title>Chemical characterization of the oxides of the tailing.</title>
            </caption>
        </fig>
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf05.tif"/>
    </fig-group>
    ...



.. note:: Figuras que não estejam identificadas sob ``<app-group>`` devem ser inseridas obrigatoriamente após a primeira chamada no texto.

.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
