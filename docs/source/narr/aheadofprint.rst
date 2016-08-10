.. _ahead-of-print:

Ahead Of Print
==============

Todos os arquivos :term:`ahead of print` (AOP) devem apresentar o valor ``research-article`` em ``@article-type`` e em ``//subj-group[@subj-group-type="heading"]/subject`` inserir o texto ``Articles``.

Esse tipo de :term:`documento` não apresenta volume, número, nem paginação, portanto, os elementos :ref:`elemento-volume` e :ref:`elemento-issue` não devem ser utilizados e deve-se considerar o valor "00" para :ref:`elemento-fpage` e :ref:`elemento-lpage`.

Exemplo:

.. code-block:: xml

    <article article-type="research-article" dtd-version="1.0" specific-use="sps-1.0" xml:lang="es" xmlns:mml="http://www.w3.org/1998/Math/MathML" xmlns:xlink="http://www.w3.org/1999/xlink">
     ...
    <article-categories>
       <subj-group subj-group-type="heading">
           <subject>Articles</subject>
       </subj-group>
    </article-categories>
     ...
       <pub-date pub-type="epub">
           <day>12</day>
           <month>08</month>
           <year>2016</year>
       </pub-date>
       <fpage>00</fpage>
       <lpage>00</lpage>
     ...
    </article>

Para estes artigos, a data de publicação deve ter o atributo ``@pub-type`` apenas como ``epub`` e com todos os sub-elementos (:ref:`elemento-day`, :ref:`elemento-month` e :ref:`elemento-year`) preenchidos.

Exemplo:

.. code-block:: xml

    <article>
        ...
        <article-meta>
            <author-notes>
                ...
            </author-notes>
            <pub-date pub-type="epub">
                <day>13</day>
                <month>03</month>
                <year>2015</year>
            </pub-date>
        </article-meta>
        ...
    </article>


.. note:: Em AOP considerar sempre o elemento :ref:`elemento-month` para indicação de mês. Nunca se deve inserir o elemento :ref:`elemento-season`.


.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
