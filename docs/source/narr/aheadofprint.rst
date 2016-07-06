.. _ahead-of-print:

Ahead Of Print
==============

Todos os arquivos *Ahead Of Print* (AOP) devem apresentar o valor ``research-article`` em ``@article-type`` e em ``//subj-group[@subj-group-type="heading"]/subject`` conter o valor ``Articles``.

Esse tipo de :term:`documento` não apresenta volume, número, nem paginação, portanto, os elementos :ref:`elemento-volume` e :ref:`elemento-issue` não devem ser utilizados e deve-se considerar o valor "00" para paginação.

Exemplo:

.. code-block:: xml

    <article>
        ...
        <article-meta>
            <pub-date pub-type="epub">
                ...
            </pub-date>
            <fpage>000</fpage>
            <lpage>000</lpage>
        </article-meta>
        ...
    </article>


Para estes arquivos, a data de publicação deve ter o atributo ``@pub-type`` apenas como ``epub`` e com todos os sub-elementos (:ref:`elemento-day`, :ref:`elemento-month` e :ref:`elemento-year`) preenchidos.

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


.. {"reviewed_on": "20160630", "by": "gandhalf_thewhite@hotmail.com"}
