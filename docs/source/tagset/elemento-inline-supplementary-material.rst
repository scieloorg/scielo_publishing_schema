.. _elemento-inline-supplementary-material:

<inline-supplementary-material>
===============================

Atributos obrigatórios:

  1. ``@xlink:href``
  2. ``@mimetype``
  3. ``@mime-subtype``

+------------------------------+--------------------+
| Aparece em                   | Ocorre             |
+==============================+====================+
| :ref:`elemento-article-meta` | Zero ou mais vezes |
+------------------------------+--------------------+
| :ref:`elemento-p`            | Zero ou mais vezes |
+------------------------------+--------------------+
| :ref:`elemento-app`          | Zero ou mais vezes |
+------------------------------+--------------------+


O elemento ``<inline-supplementary-material>`` é usado para adicionar informações a um artigo quando identificado em um parágrafo, fornecendo por exemplo, objetos multimídia, tabelas ou figuras adicionais, listas, dados brutos em planilha etc

Os atributos obrigatórios são:

* ``@mimetype:``: Especifica o tipo de mídia como, por exemplo, “vídeo”, “aplicação” etc.
* ``@mime-subtype``: Determina o formato da mídia, como por exemplo, "mp4", "pdf" etc.
* ``@xlink:href``: Indica a nomeação do arquivo que está sendo referenciado.


.. note:: 
 * No endereço https://www.iana.org/assignments/media-types/media-types.xhtml há informação detalhada sobre os valores dos atributos ``@mimetype`` e ``@mime-subtype``.
 * Recomendamos por segurança, que seja utilizado o formato "pdf" para adicionar material suplementar.
 * Para vídeos o formato mp4 é obrigatório.


 Exemplos:

  * :ref:`elemento-inlinesm-exemplo-1`
  * :ref:`elemento-inlinesm-exemplo-2`

.. _elemento-inlinesm-exemplo-1:


Exemplo de <inline-supplementary-material> envolvendo texto:
-------------------------------------------------------------

.. code-block:: xml

    <p>Devido a esse elevado percentual de dados omissos, possivelmente não influenciaram no resultado final do <inline-supplementary-material xlink:href="0103-507X-rbti-26-02-0130-suppl1.pdf" mimetype="application" mime-subtype="pdf">Material Suplementar</inline-supplementary-material></p>
    

.. _elemento-inlinesm-exemplo-2:


Exemplo de <inline-supplementary-material> sem texto:
------------------------------------------------------

.. code-block:: xml

    <p>Nunc faucibus orci ut bibendum mollis. Nunc rutrum ullamcorper neque sit amet venenatis. Praesent mattis <inline-supplementary-material xlink:href="0103-507X-rbti-26-02-0130-suppl1.pdf" mimetype="video" mime-subtype="avi"/> elit id augue tincidunt, sit amet ornare nibh laoreet. Morbi et odio a libero facilisis dapibus id vitae orci.</p>


