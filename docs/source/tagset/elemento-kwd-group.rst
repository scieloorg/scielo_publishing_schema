.. _elemento-kwd-group:

<kwd-group>
-----------

Aparece em
  :ref:`elemento-article-meta`
 
Atributos obrigatórios
  1. xml:lang
 
Ocorre
  Zero ou mais vezes


Identifica o grupo de palavras-chave do artigo por idioma. Deve 
conter o atributo ``@xml:lang``.
Em ``<kwd-group>`` deve ser inserida uma informação de etiqueta ``title``. 

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
 
