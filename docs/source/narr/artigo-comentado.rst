.. _artigo-comentado:

Comentário de artigo
====================

Artigos cujo tema é outro artigo ou artigos devem apresentar o valor ``article-commentary`` no atributo @article-type em :ref:`elemento-article`. 

O elemento :ref:`elemento-related-article` é utilizado para referenciar o artigo comentado.

Exemplo:

.. code-block:: xml

    ...
    <article xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:mml="http://www.w3.org/1998/Math/MathML" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" specific-use="sps-1.5" dtd-version="1.0" article-type="article-commentary" xml:lang="en">
        <front>
            ...
            <article-meta>
            ...
                </permissions>
                <related-article related-article-type="commentary-article" id="r01" vol="109" page="87-92"/>
                ...
            </article-meta>
        ...
    </article>


.. note:: ``<related-article>`` deve ser inserido abaixo das informações de ``<permissions>`` ou acima de ``<counts>``.

Para artigo relacionado, o elemento :ref:`elemento-related-article` deve conter os seguintes atributos: ``@related-article-type`` com o valor ``commentary-article``; ``@id``; ``@vol`` e ``@page`` com a informação do intervalo de paginação do documento.


.. {"reviewed_on": "20160729", "by": "gandhalf_thewhite@hotmail.com"}
