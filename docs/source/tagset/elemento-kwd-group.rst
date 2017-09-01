.. _elemento-kwd-group:

<kwd-group>
===========

Aparece em:

  :ref:`elemento-article-meta`
  :ref:`elemento-front-stub`

Atributos obrigatórios:

  1. ``@xml:lang``

Ocorre:

  Zero ou mais vezes


Identifica o grupo de palavras-chave do artigo por idioma. Contém, obrigatoriamente, o atributo ``@xml:lang``. ``<kwd-group>`` deve ter ainda um título identificando o grupo por meio do elemento ``title``.

.. code-block:: xml

    ...
    <article-meta>
        ...
        <kwd-group xml:lang="pt">
            <title>Palavra-chave</title>
            <kwd>Broncoscopia</kwd>
        </kwd-group>
        ...
    </article-meta>
    ...


.. {"reviewed_on": "20170720", "by": "aline.cristina@scielo.org"}
