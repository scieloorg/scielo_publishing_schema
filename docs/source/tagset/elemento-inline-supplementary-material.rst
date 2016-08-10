.. _elemento-inline-supplementary-material:

<inline-supplementary-material>
-------------------------------

Aparece em:

  :ref:`elemento-article-meta`
  :ref:`elemento-p`
  :ref:`elemento-app`

Atributos obrigatórios:

  1. ``@xlink:href``
  2. ``@mimetype``
  3. ``@mime-subtype``

Ocorre:

  Zero ou mais vezes

Tem a mesma função do elemento :ref:`elemento-supplementary-material`, mas é utilizado somente quando a menção ao material suplementar está em linha, ou seja, descrita em um parágrafo.

Os atributos obrigatórios são:

* ``@mimetype:``: Especifica o tipo de mídia como, por exemplo, “vídeo”, “aplicação”, entre outros.
* ``@mime-subtype``: Identifica o formato da mídia.
* ``@xlink:href``: Contém o nome completo do arquivo de mídia, por exemplo, "artigo.pdf", "video.mov", "arquivo.zip" etc.

.. note:: No endereço http://www.iana.org/assignments/media-types/media-types.xhtml há informação detalhada sobre os valores dos atributos ``@mimetype`` e ``@mime-subtype``.

Exemplo 1:

.. code-block:: xml

    <p>Devido a esse elevado percentual de dados omissos, possivelmente não influenciaram no resultado final do <inline-supplementary-material xlink:href="0103-507X-rbti-26-02-0130-suppl1.pdf" mimetype="application" mime-subtype="pdf">Material Suplementar</inline-supplementary-material></p>


Exemplo 2:

.. code-block:: xml

    <p>Nunc faucibus orci ut bibendum mollis. Nunc rutrum ullamcorper neque sit amet venenatis. Praesent mattis <inline-supplementary-material xlink:href="0103-507X-rbti-26-02-0130-suppl1.pdf" mimetype="video" mime-subtype="avi"/> elit id augue tincidunt, sit amet ornare nibh laoreet. Morbi et odio a libero facilisis dapibus id vitae orci.</p>



.. {"reviewed_on": "20160626", "by": "gandhalf_thewhite@hotmail.com"}
