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



Identifica as figuras de um artigo. Nesse elemento é possível especificar ``<label>``, ``<caption>``, ``<graphic>``, ``<links>`` e objetos multimídia como vídeo, áudio e filme.
``<fig>`` pode ainda conter os seguintes atributos: ``@fig-type`` e ``@xml:lang``.

O elemento ``<graphic>`` é utilizado para identificar alguns tipos de arquivo e tem como atributo ``@xlink:href:`` que é utilizado para especificar o nome completo da imagem referenciada.



O atributo ``@id:`` permite fazer referência cruzada no :term:`documento` (link relacionado a um "rid"), desde que o atributo tenha um valor único no arquivo.

Exemplos:

    * :ref:`elemento-fig-exemplo-1`
    * :ref:`elemento-fig-exemplo-2`
    * :ref:`elemento-fig-exemplo-3`
    * :ref:`elemento-fig-exemplo-4`
    * :ref:`elemento-fig-exemplo-5`
    * :ref:`elemento-fig-exemplo-6`



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

Para figuras com legenda a marcação deve ocorrer para toda a informação da imagem, inclusive sua descrição com o elemento ``<fig>``. Dentro de ``<fig>`` serão identificados o rótulo da figura (:ref:`elemento-label`) e a legenda (:ref:`elemento-caption`) com o título da figura em ``<title>``.

.. code-block:: xml

    ...
    <fig id="f01">
        <label>Fig. 1</label>
        <caption>
            <title>título da imagem</title>
        </caption>
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
    </fig>
    ...


.. _elemento-fig-exemplo-3:

Exemplo de Figura com label específico:
---------------------------------------

O atributo ``@fig-type:`` é utilizado para especificar o tipo de imagem, que pode ser: Graphic, Cartoon, Chart, Diagram, Drawing, Exhibit, Illustration, Map etc. Contudo o tipo só será definido caso o ``<label>`` apresente um conteúdo diferente de "fig." ou "figure".

.. code-block:: xml

    ...
    <fig fig-type="map" id="f01">
        <label>Map 1</label>
        <caption>
            <title>Título do Mapa<title>
        </caption>
    </fig>
    ...

Se a figura não possuir um tipo específico, deve-se manter o elemento sem o atributo.


.. _elemento-fig-exemplo-4:

Exemplo de Figura sem tipo definido:
------------------------------------

.. code-block:: xml

    ...
    <fig id="f01">
        <label>Fig 1</label>
        <caption>
            <title>Título da Figura<title>
        </caption>
    </fig>
    ...


.. _elemento-fig-exemplo-5:

Exemplo completo de Figura com atributo ``@id``:
------------------------------------------------

.. code-block:: xml

    ...
    <fig id="f01">
        <label>FIGURE 1</label>
        <caption>
            <title>Título da figura</title>
        </caption>
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
    </fig>


.. _elemento-fig-traduzido:

Legendas traduzidas
-------------------

Figuras que apresentam legendas traduzidas (com mais de um :ref:`elemento-label` e :ref:`elemento-caption`), devem ser identificadas com o elemento ``<fig-group>``, o qual deve conter os elementos ``<fig>`` para cada idioma utilizando o atributo ``@xml:lang``.


.. _elemento-fig-exemplo-6:

Exemplo de Figura com legenda traduzida:
````````````````````````````````````````

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




.. note:: Figuras que não estejam identificadas sob ``<app-group>`` devem ser inseridas obrigatoriamente após a primeira chamada no texto. Para material suplementar, analisar e identificar caso a caso.

.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
