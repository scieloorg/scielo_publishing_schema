.. _elemento-article-title:

<article-title>
===============

Este elemento possui :ref:`scielo-brasil`


+----------------------------------+-----------------+
| Aparece em                       | Ocorre          |
+==================================+=================+
| :ref:`elemento-title-group`      | uma vez         |
+----------------------------------+-----------------+
| :ref:`elemento-element-citation` | zero ou uma vez |
+----------------------------------+-----------------+


Utilizado para identificar o título do artigo em :ref:`elemento-title-group` ou para especificar um título de documento nas referências em :ref:`elemento-element-citation`. Em ambos casos, o atributo ``@xml:lang`` não deve ser utilizado.



Exemplos:

  * :ref:`elemento-article-title-exemplo-1`
  * :ref:`elemento-article-title-exemplo-2`


.. _elemento-article-title-exemplo-1:

Exemplo de ``<article-title>`` nos dados iniciais do documento:
---------------------------------------------------------------

.. code-block:: xml

    ...
    <title-group>
        <article-title>The teaching of temporomandibular disorders and  orofacial pain at undergraduate level in Brazilian dental schools</article-title>
    </title-group>
    ...

.. note:: Se o título do artigo ou da referência possuir um subtítulo, este deve ser marcado juntamente com o título sob ``<article-title>``. Não se deve marcar nenhum título e/ou subtítulo separadamente em outras tags.


.. _elemento-article-title-exemplo-2:

Exemplo de ``<article-title>`` em Referência Bibliográfica:
-----------------------------------------------------------

.. code-block:: xml

    <element-citation publication-type="journal">
         ...
       <article-title>Framing processes and social movements: an overview and assessment</article-title>
         ...
    </element-citation>


