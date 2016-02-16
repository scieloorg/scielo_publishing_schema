.. _elemento-author-notes:
 
<author-notes>
--------------       

Aparece em
  :ref:`elemento-article-meta`
 
Ocorre
  Zero ou mais vezes


A tag de notas de autor deve ser utilizada para identificar informações como 
correspondência, contribuição igualitária, conflitos de interesses, 
ou seja, notas sobre autor.

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
 
