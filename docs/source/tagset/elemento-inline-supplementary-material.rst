.. _elemento-inline-supplementary-material:

<inline-supplementary-material>
-------------------------------

Aparece em
  :ref:`elemento-article-meta`, 
  :ref:`elemento-p`, 
  :ref:`elemento-app`
 
Atributos obrigatórios
  1. xlink:href
  2. mimetype
  3. mime-subtype
 
Ocorre
  Zero ou mais vezes

Esta tag tem a mesma função da tag :ref:`elemento-supplementary-material`, mas é 
utilizada quando a menção do material suplementar está em linha, ou seja descrita 
em um parágrafo.

Seus atributos obrigatórios são:

* ``@mimetype:``: Utilizado para especificar o tipo de mídia como “vídeo”, “aplicação” dentre outros.
* ``@mime-subtype``: Utilizado para especificar o formato da mídia.
* ``@xlink:href``: Utilizado para indicar do nome completo do arquivo, tais como: pdf, vídeo, zip e etc.


.. note:: Para consultar valores dos atributos ``@mimetype`` e ``@mime-subtype``, 
          consultar http://www.iana.org/assignments/media-types/media-types.xhtml

Exemplo 1:

.. code-block:: xml

    <p>Devido a esse elevado percentual de dados omissos, possivelmente não influenciaram no resultado final do <inline-supplementary-material xlink:href="0103-507X-rbti-26-02-0130-suppl1.pdf" mimetype="application" mime-subtype="pdf">Material Suplementar</inline-supplementary-material></p>


Exemplo 2:

.. code-block:: xml

    <p>Nunc faucibus orci ut bibendum mollis. Nunc rutrum ullamcorper neque sit amet venenatis. Praesent mattis <inline-supplementary-material xlink:href="0103-507X-rbti-26-02-0130-suppl1.pdf" mimetype="video" mime-subtype="avi"/> elit id augue tincidunt, sit amet ornare nibh laoreet. Morbi et odio a libero facilisis dapibus id vitae orci.</p>

