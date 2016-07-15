.. _elemento-fpage:

<fpage>
=======

Aparece em:

  :ref:`elemento-article-meta`
  :ref:`elemento-element-citation`

Ocorre:

  Zero ou uma vez


Indica a paginação inicial do artigo. No caso de :term:`ahead-of-print`, deve ser preenchido com ``00``.

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


Este elemento também pode ser utilizada com o atributo ``@seq`` para números onde mais de um artigo inicia-se na mesma página. Uma sequência alfanumérica deve diferenciar um artigo dos outros na mesma página. Por exemplo, o primeiro artigo que começar na página 82 pode receber a sequência "82a"; a letra sequencial seria "a" seguido de "b" para um segundo artigo e assim por diante.

Exemplo:

.. code-block:: xml

    ...
    <article-meta>
        ...
        <fpage seq="a">82</fpage>
        <lpage>82</lpage>
        ...
    </article-meta>
    ...


.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
