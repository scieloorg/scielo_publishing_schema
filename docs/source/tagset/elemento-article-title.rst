.. _elemento-article-title:

<article-title>
===============

Aparece em:

  :ref:`elemento-title-group`
  :ref:`elemento-element-citation`

Ocorre:

  zero ou uma vez

Utilizado para identificar o título do artigo em :ref:`elemento-title-group` ou para especificar um título de documento nas referências em :ref:`elemento-element-citation`. Em ambos casos, o atributo ``@xml:lang`` não deve ser utilizado.

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

    <element-citation publication-type="journal">
         ...
       <article-title>Framing processes and social movements: an overview and assessment</article-title>
         ...
    </element-citation>


.. note:: Caso haja coincidência entre os títulos da seção e do artigo, a informação será marcada tanto em :ref:`elemento-article-categories` como em ``<article-title>``.


.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
