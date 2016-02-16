.. _elemento-fig:

<fig>
-----

Aparece em
  :ref:`elemento-p`,
  :ref:`elemento-app`,
  :ref:`elemento-supplementary-material`,
  :ref:`elemento-fig`,
  :ref:`elemento-glossary`.

Atributos obrigatórios
  1. id (ver :ref:`sugestao-atribuicao-id`)
 
Ocorre
  Zero ou mais vezes


As figuras de um artigo são identificadas por meio da tag ``<fig>``. 
Com essa tag é possível especificar label, caption, graphic, links, e objetos 
multimídia como vídeo, áudio e filme.
 
As imagens podem ter ou não legendas. Para imagens sem legendas é necessário 
marcá-la como ``<fig>`` e identificá-la com a tag ``<graphic>``.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <fig id="f01">
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
    </fig>
    ...
 
A tag ``<graphic>`` é utilizada para identificar alguns tipos de 
arquivos. Seus atributos são:
 
* **@xlink:href:** utilizado para especificar o nome completo da imagem referenciada
 
Para figuras com legendas a marcação deve envolver toda a informação de 
imagem, inclusive sua descrição, com a tag ``<fig>``. Dentro de ``<fig>`` 
serão identificados o rótulo da figura :ref:`elemento-label` e mais a tag de 
:ref:`elemento-caption` com a tag :ref:`elemento-p` com o título da figura.
 
Exemplo:
 
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
 
Essa tag pode ter os seguintes atributos: ``@fig-type``, ``@id``, ``@xml:lang``. 
Os atributos mais frequentes são:
 
* **@fig-type:** utilizado para especificar o tipo de imagem. Os tipos 
  podem ser muitos como: Graphic, Cartoon, Chart, Diagram, Drawing, Exihibit, 
  Illustration, Map etc. Contudo o tipo só será definido caso o label da 
  figura apresente um tipo diferente de "fig." "figure".
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <fig fig-type="map" id="f01">
        <label>Map 1</label>
        <caption>
            <title>Título do Mapa<title>
        </caption>
    </fig>
    ...
 
Se a figura não possuir um tipo específico, deve-se manter a tag sem o atributo.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <fig id="f01">
        <label>Fig 1</label>
        <caption>
            <title>Título da Figura<title>
        </caption>
    </fig>
    ...
 
* **@id:** identificador da tag. É possível fazer referência cruzada no 
  :term:`documento`; esse atributo deve ter valor único no arquivo e é possível 
  fazer link relacionado a um "rid".
 
 
Exemplo:

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

Legendas Traduzidas
^^^^^^^^^^^^^^^^^^^

Figuras que apresentam legendas traduzidas, com mais de 1 label e caption, 
devem ser identificadas pelo elemento ``<fig-group>`` o qual deve envolver os 
elementos ``<fig>`` de cada idioma. Veja:

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

