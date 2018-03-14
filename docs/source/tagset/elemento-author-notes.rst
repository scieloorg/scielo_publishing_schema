.. _elemento-author-notes:

<author-notes>
==============

+------------------------------+-----------------+
| Aparece em                   | Ocorre          |
+==============================+=================+
| :ref:`elemento-article-meta` | Zero ou uma vez |
+------------------------------+-----------------+
| :ref:`elemento-front-stub`   | Zero ou uma vez |
+------------------------------+-----------------+

Identifica notas relacionadas ao autor, tais como: correspondência, contribuição igualitária etc.


Exemplo:

.. code-block:: xml

    ...
    <article-meta>
        ...
        <author-notes>
            <corresp id="c01"><bold>Correspondence:</bold> Maria Silva, Avenida Senador Felinto Muller,s/n - Cidade Universitária, 79070-192 Campo Grande - MS Brasil,<email>maria.ra@foo.com</email></corresp>
            <fn fn-type="conflict">
                <p>Conflict of interest: none</p>
            </fn>
        </author-notes>
        ...
    </article-meta>
    ...


.. {"reviewed_on": "20170720", "by": "aline.cristina@scielo.org"}
