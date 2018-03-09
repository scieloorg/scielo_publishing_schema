.. _elemento-trans-title:

<trans-title>
=============

Aparece em:

  :ref:`elemento-trans-title-group`

Ocorre:

  Uma vez


Identifica o título traduzido do artigo. Obrigatório o uso do atributo ``@xml:lang``.


Exemplo:

.. code-block:: xml

    ...
    <title-group>
        <article-title>Between spiritual wellbeing and spiritual distress: possible related factors in elderly patients with cancer</article-title>
        <trans-title-group xml:lang="pt">
            <trans-title>Entre o bem-estar espiritual e a angústia espiritual: possíveis fatores relacionados a idosos com cancro</trans-title>
        </trans-title-group>
        <trans-title-group xml:lang="es">
            <trans-title>Entre el bienestar espiritual y el sufrimiento espiritual: posibles factores relacionados en ancianos con câncer</trans-title>
        </trans-title-group>
    </title-group>
    ...

.. note:: Se o título traduzido do artigo possuir um subtítulo, este deve ser marcado juntamente com o título sob ``<trans-title>``. Não se deve marcar nenhum título e/ou subtítulo separadamente em outras tags.


.. {"reviewed_on": "20160629", "by": "gandhalf_thewhite@hotmail.com"}
