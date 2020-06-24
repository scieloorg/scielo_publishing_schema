.. _elemento-supplementary-material:

<supplementary-material>
========================


Atributos obrigatórios:

  1. ``@id`` (ver :ref:`sugestao-atribuicao-id`)
  2. ``@xlink:href``
  3. ``@mimetype``
  4. ``@mime-subtype``

+-------------------------------+--------------------+
| Aparece em                    | Ocorre             |
+===============================+====================+
| ``app-group``                 | Zero ou mais vezes |
+-------------------------------+--------------------+
| :ref:`elemento-app`           | Zero ou mais vezes |
+-------------------------------+--------------------+
| :ref:`elemento-article-meta`  | Zero ou mais vezes |
+-------------------------------+--------------------+
| :ref:`elemento-body`          | Zero ou mais vezes |
+-------------------------------+--------------------+
| :ref:`elemento-boxed-text`    | Zero ou mais vezes |
+-------------------------------+--------------------+
| :ref:`elemento-disp-quote`    | Zero ou mais vezes |
+-------------------------------+--------------------+
| :ref:`elemento-front-stub`    | Zero ou mais vezes |
+-------------------------------+--------------------+
| :ref:`elemento-glossary`      | Zero ou mais vezes |
+-------------------------------+--------------------+
| ``license-p``                 | Zero ou mais vezes |
+-------------------------------+--------------------+
| :ref:`elemento-p`             | Zero ou mais vezes |
+-------------------------------+--------------------+
| :ref:`elemento-ref-list`      | Zero ou mais vezes |
+-------------------------------+--------------------+
| :ref:`elemento-sec`           | Zero ou mais vezes |
+-------------------------------+--------------------+


Material suplementar é usado para adicionar informações a um artigo, fornecendo por exemplo, objetos multimídia, tabelas ou figuras adicionais, listas, dados brutos em planilha etc.


* ``@id``: Utilizado como identificador único no artigo.
* ``@mimetype``: Especifica o tipo de mídia, como por exemplo, "vídeo", "aplicação" etc.
* ``@mime-subtype``: Determina o formato da mídia, como por exemplo "mp4", "pdf" etc).
* ``@xlink:href``: Indica a nomeação do arquivo que está sendo referenciado.


.. note:: 
 * Este elemento, em :ref:`elemento-front`, deve ser inserido abaixo das informações de paginação ou antes do elemento :ref:`elemento-history`.
 * Em https://www.iana.org/assignments/media-types/media-types.xhtml há informação detalhada sobre os valores dos atributos ``@mimetype`` e ``@mime-subtype``.
 * Recomendamos por segurança, que seja utilizado o formato "pdf" para adicionar material suplementar.
 * Para vídeos o formato "mp4" é obrigatório.



Exemplos:

 * :ref:`elemento-supplementary-material-exemplo-1`
 * :ref:`elemento-supplementary-material-exemplo-2`
 * :ref:`elemento-supplementary-material-exemplo-3`
 * :ref:`elemento-supplementary-material-exemplo-4`


.. _elemento-supplementary-material-exemplo-1:

Exemplo de ``<supplementary-material>`` em ``<front>``
------------------------------------------------------

.. code-block:: xml

    ...
    <front>
        ...
        <article-meta>
            ...
            <fpage>237</fpage>
            <lpage>259</lpage>
            <supplementary-material id="suppl01" mimetype="application" mime-subtype="pdf" xlink:href="1234-5678-rctb-45-05-0110-suppl01.pdf"/>
            ...
        </article-meta>
        ...
    </front>
    ...



.. _elemento-supplementary-material-exemplo-2:

Exemplo de ``<supplementary-material>`` envolvendo objeto em ``<body>``
-----------------------------------------------------------------------

.. code-block:: xml
    
    ...
    <body>
        ...
        <p>
            <supplementary-material id="suppl02" mimetype="image" mime-subtype="tiff" xlink:href="11234-5678-rctb-45-05-0110-suppl01.tif">
                <label>Fig 1.</label>
                <caption>
                    <title>Supplementary material A</title>
                </caption>
            </supplementary-material>
        </p>
        ...
    </body>
    ...


       
.. _elemento-supplementary-material-exemplo-3:

Exemplo de ``<supplementary-material>`` em ``<p>`` de ``<body>``
----------------------------------------------------------------


.. code-block:: xml
    
    ...
    <body>
        ...
        <p>
            <supplementary-material id="suppl03" mimetype="application" mime-subtype="pdf" xlink:href="1234-5678-rctb-45-05-0110-suppl01.pdf"/>
        </p>
      ...
    </body>
    ...



.. _elemento-supplementary-material-exemplo-4:

Exemplo de ``<supplementary-material>`` em ``<back>``
-----------------------------------------------------


.. code-block:: xml
    
    ...
    <back>
        <app-group>
            <app id="app01">
                <label>S-1</label>
                <supplementary-material id="suppl04" mimetype="image" mime-subtype="tiff" xlink:href="11234-5678-rctb-45-05-0110-suppl01.tif">
                    <label>Fig 1.</label>
                    <caption>
                        <title>Supplementary material A</title>
                    </caption>
                </supplementary-material>
            </app>
            <app id="app02">
                <label>S-2</label>
                <supplementary-material id="suppl05" mimetype="image" mime-subtype="tiff" xlink:href="11234-5678-rctb-45-05-0110-suppl02.tif"/>
            </app>
        </app-group>
        ...
    </back>
    ...





