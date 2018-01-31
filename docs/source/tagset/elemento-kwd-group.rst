.. _elemento-kwd-group:

<kwd-group>
===========

Atributos obrigatórios:

  1. ``@xml:lang``

+------------------------------+--------------------+
| Aparece em                   | Ocorre             |
+==============================+====================+
| :ref:`elemento-article-meta` | Zero ou mais vezes |
+------------------------------+--------------------+
| :ref:`elemento-front-stub`   | Zero ou mais vezes |
+------------------------------+--------------------+



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
