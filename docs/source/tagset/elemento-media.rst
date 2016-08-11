.. _elemento-media:

<media>
=======

Aparece em:

  :ref:`elemento-p`
  :ref:`elemento-fig`
  :ref:`elemento-app`

Atributos obrigatórios:

  1. ``@mime-subtype``
  2. ``@xlink:href``
  3. ``@mime-type``

Ocorre:

  Zero ou mais vezes


``<media>`` é usado para especificar arquivos multimídia como, por exemplo:

- vídeos;
- áudios;
- filmes;
- animações.

``@mimetype`` é usado para especificar o tipo de mídia, por exemplo, "vídeo" ou "aplicação". ``@mime-subtype`` é usado para especificar o formato da mídia.

Exemplos:

1. forma geral:

.. code-block:: xml

    <media mimetype="video"
           mime-subtype="mp4"
           xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/>


2. Em parágrafo:

.. code-block:: xml

    <p>Within the limitations of this study, it may be concluded that remaining
    tooth wall thickness did not influence the fatigue resistance of
    molars restored with CAD/CAM ceramic inlays <media mimetype="video"
    mime-subtype="mp4" xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/></p>


3. Em figura:

.. code-block:: xml

    <p>
        <fig id="f01">
            <label>Figure 1</label>
            <caption>
                <title>descrição da fig.<title>
            </caption>
            <media xlink:href="1234-5678-rctb-45-05-0110-m01.avi" mimetype="video" mime-subtype="avi"/>
        </fig>
    </p>


4. Em :ref:`elemento-sec` do tipo material suplementar:

.. code-block:: xml

    <sec sec-type="supplementary-material">
        <title>Supplementary Material</title>
        <supplementary-material id="m1">
            <caption>
                <title>legenda</title>
            </caption>
            <media mimetype="application" mime-subtype="pdf" xlink:href="1234-5678-rctb-45-05-0110-m01.pdf"/>
        </supplementary-material>
    </sec>


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
