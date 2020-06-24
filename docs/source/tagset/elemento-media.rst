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

``@mimetype``: Especifica o tipo de mídia, como por exemplo, "vídeo", "áudio", etc.

``@mime-subtype``: Determina o formato da mídia, como por exemplo, "mp4", "avi", etc.

.. note::
 * Em https://www.iana.org/assignments/media-types/media-types.xhtml há informação detalhada sobre os valores dos atributos ``@mimetype`` e ``@mime-subtype``.
 * Para vídeos o formato mp4 é obrigatório.

Exemplos:

 * :ref:`elemento-media-exemplo-1`
 * :ref:`elemento-media-exemplo-2`


.. _elemento-media-exemplo-1:

Exemplo de Media em ``<p>``:
--------------------------------------

.. code-block:: xml

    <p>Within the limitations of this study, it may be concluded that remaining
    tooth wall thickness did not influence the fatigue resistance of
    molars restored with CAD/CAM ceramic inlays <media mimetype="video"
    mime-subtype="mp4" xlink:href="1234-5678-rctb-45-05-0110-m01.mp4"/></p>


.. _elemento-media-exemplo-2:

Exemplo de Media em ``<fig>``:
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

    