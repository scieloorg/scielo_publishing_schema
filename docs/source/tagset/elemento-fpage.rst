.. _elemento-fpage:

<fpage>
=======

+----------------------------------+-----------------+
| Aparece em                       | Ocorre          |
+==================================+=================+
| :ref:`elemento-article-meta`     | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-element-citation` | Zero ou uma vez |
+----------------------------------+-----------------+


Indica a paginação inicial do artigo. 


Exemplo:

.. code-block:: xml

    ...
    <article-meta>
        ...
        <fpage>17</fpage>
        <lpage>21</lpage>
        ...
    </article-meta>
    ...


Este elemento também pode ser utilizado com o atributo ``@seq`` para números onde mais de um artigo inicia-se na mesma página. Uma sequência alfanumérica deve diferenciar um artigo dos outros na mesma página. Por exemplo, o primeiro artigo que começar na página 82 pode receber a sequência "82a"; a letra sequencial seria "a" seguido de "b" para um segundo artigo e assim por diante.

Exemplo:

.. code-block:: xml

    ...
    <article-meta>
        ...
        <fpage seq="a">82</fpage>
        <lpage>83</lpage>
        ...
    </article-meta>
    ...


.. {"reviewed_on": "20160729", "by": "gandhalf_thewhite@hotmail.com"}
