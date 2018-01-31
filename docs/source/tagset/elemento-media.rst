.. _elemento-media:

<media>
=======

Atributos obrigatórios:

  1. ``@mime-subtype``
  2. ``@xlink:href``
  3. ``@mime-type``

+----------------------------+--------------------+
| Aparece em                 | Ocorre             |
+============================+====================+
| :ref:`elemento-app`        | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-body`       | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-fig`        | Zero ou mais vezes |
+----------------------------+--------------------+
| ``<fig-group>``            | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-p`          | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-sec`        | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-table-wrap` | Zero ou mais vezes |
+----------------------------+--------------------+



``<media>`` é usado para especificar arquivos multimídia como, por exemplo:

- vídeos;
- áudios;
- filmes;
- animações.

``@mimetype`` é usado para especificar o tipo de mídia, por exemplo, "vídeo" ou "aplicação". ``@mime-subtype`` é usado para especificar o formato da mídia.

.. note:: Para vídeos o formato mp4 é obrigatório.

Exemplos:

 * :ref:`elemento-media-exemplo-1`
 * :ref:`elemento-media-exemplo-2`
 * :ref:`elemento-media-exemplo-3`
 * :ref:`elemento-media-exemplo-4`


.. _elemento-media-exemplo-1:

Exemplo de Media generalizado:
------------------------------

.. code-block:: xml

    <media mimetype="video"
           mime-subtype="mp4"
           xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/>


.. _elemento-media-exemplo-2:

Exemplo de Media em :ref:`elemento-p`:
--------------------------------------

.. code-block:: xml

    <p>Within the limitations of this study, it may be concluded that remaining
    tooth wall thickness did not influence the fatigue resistance of
    molars restored with CAD/CAM ceramic inlays <media mimetype="video"
    mime-subtype="mp4" xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/></p>


.. _elemento-media-exemplo-3:

Exemplo de Media em :ref:`elemento-fig`:
----------------------------------------

.. code-block:: xml

    <p>
        <fig id="f01">
            <label>Figure 1</label>
            <caption>
                <title>descrição da fig.<title>
            </caption>
            <media xlink:href="1234-5678-rctb-45-05-0110-m01.mp4" mimetype="video" mime-subtype="mp4"/>
        </fig>
    </p>


.. _elemento-media-exemplo-4:

Exemplo de Media em :ref:`elemento-sec` do tipo Material Suplementar:
---------------------------------------------------------------------

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


.. {"reviewed_on": "20170828", "by": "carolina.tanigushi@scielo.org"}
