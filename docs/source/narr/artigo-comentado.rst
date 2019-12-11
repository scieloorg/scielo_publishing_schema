.. _artigo-comentado:

Comentário de artigo
====================

Representam artigos cujo tema são outros artigos. Estes documentos devem apresentar o valor ``article-commentary`` no atributo ``@article-type`` em :ref:`elemento-article`. O elemento :ref:`elemento-related-article` pode ocorrer uma ou mais vezes e é utilizado para referenciar o artigo comentado e deve conter obrigatoriamente os atributos:


 * ``@related-article-type`` com o valor ``commentary-article``
 * ``@id``
 * ``@xlink:href`` com número DOI do artigo que está sendo comentado
 * ``@ext-link-type`` com valor ``doi``
 * ``@vol``
 * ``@page`` ou ``@elocation-id``


Exemplo:

.. code-block:: xml

    ...
    <article xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:mml="http://www.w3.org/1998/Math/MathML" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" specific-use="sps-1.8" dtd-version="1.0" article-type="article-commentary" xml:lang="en">
        <front>
            ...
            <article-meta>
            ...
                </permissions>
                <related-article related-article-type="commentary-article" id="r01" xlink:href="10.1590/123456720182998" ext-link-type="doi" vol="109" page="87-92"/>
                ...
            </article-meta>
        ...
    </article>


.. note:: ``<related-article>`` deve ser inserido abaixo das informações de ``<permissions>``.




