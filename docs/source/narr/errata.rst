.. _errata:

Errata
======

Como regra, arquivos do tipo *errata* devem apresentar o valor ``correction`` no atributo ``@article-type``. O texto do elemento ``//subj-group[@subj-group-type="heading"]/subject`` deve conter a seção apresentada no sumário do número e, no elemento :ref:`elemento-article-title` deve figurar como título ``Errata`` ou ``Erratum``, de acordo com o que está especificado no *PDF*.

O elemento :ref:`elemento-related-article` é utilizado para referenciar o artigo que se deseja retificar.

Exemplo:

.. code-block:: xml

    ...
    <article article-type="correction"
             specific-use="sps-1.2"
             dtd-version="1.0"
             xml:lang="en"
             xmlns:xlink="http://www.w3.org/1999/xlink">
        <front>
            <article-meta>
                <article-id pub-id-type="doi">10.1590/abd1806-4841.20142998e</article-id>
                <article-categories>
                    <subj-group subj-group-type="heading">
                        <subject>Erratum</subject>
                    </subj-group>
                    ...
                </article-categories>
                <title-group>
                    <article-title>Errata</article-title>
                </title-group>
                ...
                <permissions>
                    ...
                </permissions>
                <related-article related-article-type="corrected-article"
                                 id="ra1"
                                 xlink:href="10.1590/abd1806-4841.20142998"
                                 ext-link-type="doi"/>
                <counts>
                    ...
                </counts>
                ...
            </article-meta>
            ...
        </front>
        ...
    </article>


.. note:: ``<related-article>`` deve ser inserido abaixo das informações de ``<permissions>`` ou acima de ``<counts>``.


Para ``Errata`` o elemento :ref:`elemento-related-article` deve, obrigatoriamente, apresentar os seguintes atributos: ``@related-article-type``; ``@id``; ``@xlink:href`` e ``@ext-link-type``.

Os valores possíveis para ``@ext-link-type`` são:

* ``doi``
* ``scielo-pid``
* ``scielo-aid``

``@related-article-type`` deverá ter o valor "corrected-article".

No artigo ao qual a errata se refere, deve-se inserir uma nota de rodapé com ``@fn-type`` com valor ``other`` e os demais elementos relativos à errata.

Exemplo:

.. code-block:: xml

    ...
    <back>
        ...
        <fn-group>
          <fn fn-type="other">
            <label>Errata</label>
              <p>Texto da errata</p>
            </fn>
        </fn-group>
        ...
    </back>
    ...


É possível a publicação de *Erratas* na modalidade :ref:`ahead-of-print` seguindo-se as regras anteriormente definidas. A única diferença é que em :ref:`elemento-article-title`, além da inserção da palavra ``Errata``, ``Erratum``, ``Corrigendum`` etc., (conforme PDF), deve-se inserir dois pontos e o título do artigo a ser corrigido. O padrão do documento em si deve seguir as instruções de :term:`ahead of print`.

.. note:: Mais informações podem ser encontradas no "Guia para o registro e publicação de errata, retratações e manifestações de preocupação" disponível `nesse endereço <http://www.scielo.org/php/level.php?lang=pt&component=56&item=65>`_.


.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
