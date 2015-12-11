.. _errata:

Errata
======

Como regra, arquivos do tipo errata devem apresentar o valor "correction" no 
atributo ``@article-type``. O texto do elemento ``//subj-group[@subj-group-type="heading"]/subject`` 
deve refletir o sumário do número e no elemento :ref:`elemento-article-title` inserir como título "Errata" ou 
"Erratum", de acordo com o que está especificado no PDF.
Além disso, o elemento :ref:`elemento-related-article` deve, obrigatoriamente, aparecer no arquivo .xml. Veja:


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


.. note:: Inserir ``<related-article>`` abaixo das informações de ``<permissions>`` 
          ou acima de ``<counts>``.


Para Errata o elemento :ref:`elemento-related-article` obrigatoriamente deve apresentar os 
seguintes atributos: ``@related-article-type``; ``@id``; ``@xlink:href`` e 
``@ext-link-type="doi"``. 
Sendo que em ``@related-article-type`` o valor deverá ser "corrected-article".

No artigo a que a errata se refere, inserir uma nota de rodapé conforme o exemplo:

.. code-block:: xml

    ...
    <back>
        ...
        <fn-group>
            <fn fn-type="other">
                <label>Erratum</label>
                <p>Texto da errata</p>
            </fn>
        </fn-group>
        ...
    </back>
    ...


É possível a publicação de Erratas na modalidade Ahead Of Print, estas seguem as mesmas regras já definidas, com a diferença de que em :ref:`elemento-article-title` além da inserção da palavra Errata, Erratum, Corrigendum e etc conforme PDF, deve-se inserir dois ponto e título do artigo que possui a informação incorreta. O padrão do documento em si deve seguir as instruções de Ahead Of Print.


.. note:: Para mais informações, verificar o "Guia para o registro e publicação de errata, retratações e manifestações de preocupação" em: 
    http://www.scielo.org/php/level.php?lang=pt&component=56&item=65
