.. _elemento-article-title:

<article-title>
===============

Aparece em:

  :ref:`elemento-title-group`
  :ref:`elemento-element-citation`

Ocorre:

  zero ou uma vez

Utilizado para identificar o título do artigo em :ref:`elemento-article-meta` ou para especificar um título de documento nas referências em :ref:`elemento-element-citation`. Em ambos casos, o atributo ``@xml:lang`` não deve ser utilizado.

.. note:: ``<article-title>`` é obrigatório em :ref:`elemento-title-group`.


Exemplo 1:

.. code-block:: xml

    ...
    <title-group>
        <article-title>The teaching of temporomandibular disorders and  orofacial pain at undergraduate level in Brazilian dental schools</article-title>
    </title-group>
    ...

.. note:: Se o título do artigo ou da referência possuir um subtítulo, este deve ser marcado juntamente com o título sob ``<article-title>``. Não se deve marcar nenhum título e/ou subtítulo separadamente em outras tags. A mesma regra se aplica a :ref:`elemento-trans-title`.

Exemplo 2:

.. code-block:: xml

    ...
    <title-group>
        <article-title>Correlação entre sintomas e tempo de evolução do câncer do trato aerodigestivo superior com o estádio inicial e avançado</article-title>
    </title-group>
    ...


.. note:: Se o título da seção e o título do artigo forem iguais - como ocorre em alguns editoriais, erratas, cartas ao editor etc -, deve-se repetir a          informação no :ref:`elemento-front` e marcá-la com os elementos de título.


.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
