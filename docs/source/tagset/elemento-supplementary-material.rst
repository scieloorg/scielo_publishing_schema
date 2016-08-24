.. _elemento-supplementary-material:

<supplementary-material>
========================

Aparece em:

  ``app-group``
  :ref:`elemento-app`
  :ref:`elemento-article-meta`
  :ref:`elemento-body`
  :ref:`elemento-boxed-text`
  :ref:`elemento-disp-quote`
  :ref:`elemento-front-stub`
  :ref:`elemento-glossary`
  ``license-p``
  :ref:`elemento-named-content`
  :ref:`elemento-p`
  :ref:`elemento-ref-list`
  :ref:`elemento-sec`
  

Atributos obrigatórios:

  1. ``@id`` (ver :ref:`sugestao-atribuicao-id`)
  2. ``@xlink:href``
  3. ``@mimetype``
  4. ``@mime-subtype``

Ocorre:

  Zero ou mais vezes


O material suplementar é um :term:`documento` que não faz parte do texto do artigo, mas que serviu como apoio para sua elaboração. Em ``<supplementary-material>`` é possível especificar tabelas, figuras, dados brutos de planilha, bancos de dados de genomas, quiz, equações, links, diálogos, listas, licenças e objetos multimídia como áudio e vídeo.

Este elemento pode ser descrito em :ref:`elemento-front`, em :ref:`elemento-article-meta`, em :ref:`elemento-body` como seção ou entre parágrafos, ou em :ref:`elemento-back` onde só poderá ser identificado dentro do grupo de apêndices, em (``app``).

Os atributos obrigatórios são:

* ``@id``: Utilizado como identificador único no artigo. Sua relevância aumenta quando há mais de um material suplementar e/ou quando o material   suplementar é referenciado no corpo do texto. Nesse caso, é necessário relacionar a chamada no texto com o "id" do material suplementar.
* ``@mimetype``: Especifica o tipo de mídia, como por exemplo, "vídeo" ou "aplicação".
* ``@mime-subtype``: Determina o formato da mídia (XVID, AVI, PDF etc).
* ``@xlink:href``: Indica o nome completo do arquivo, como por exemplo, ``http://sitio/arquivos/suplementar1.pdf``, ``entrevista.mov`` etc.


Exemplos:

 * :ref:`elemento-suppl-material-exemplo-1`
 * :ref:`elemento-suppl-material-exemplo-2`
 * :ref:`elemento-suppl-material-exemplo-3`
 * :ref:`elemento-suppl-material-exemplo-4`


.. _elemento-suppl-material-exemplo-1:

Exemplo de ``<supplementary-material>`` em :ref:`elemento-article-meta`:
------------------------------------------------------------------------

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


.. _elemento-suppl-material-exemplo-2:

Exemplo de ``<supplementary-material>`` no :ref:`elemento-p` envolvendo um objeto:
----------------------------------------------------------------------------------
    

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


.. _elemento-suppl-material-exemplo-3:

Exemplo de ``<supplementary-material>`` em :ref:`elemento-p`:
-------------------------------------------------------------


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


.. _elemento-suppl-material-exemplo-4:

Exemplo de ``<supplementary-material>`` em :ref:`elemento-back`:
----------------------------------------------------------------


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


.. note:: Este elemento, em :ref:`elemento-front`, deve ser inserido abaixo das informações de paginação ou antes do elemento :ref:`elemento-history`.


.. {"reviewed_on": "20160629", "by": "gandhalf_thewhite@hotmail.com"}
