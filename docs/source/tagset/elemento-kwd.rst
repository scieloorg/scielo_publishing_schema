.. _elemento-kwd:

<kwd>   
^^^^^

Aparece em
  :ref:`elemento-kwd-group`
 
Ocorre
  Uma ou mais vezes


Esta tag é inserida obrigatoriamente dentro da tag :ref:`elemento-kwd-group` e 
identifica cada palavra-chave individualmente.
 
Exemplo:

.. code-block:: xml
 
    ...
    <article-meta>
        ...
        <kwd-group xml:lang="pt">
            <title>Palavras-chave</title>
            <kwd>Broncoscopia</kwd>
            <kwd>Curvas de fluxo-volume expiratório máximo</kwd>
            <kwd>sensibilidade e especificidade</kwd>
            <kwd>Neoplasias pulmonares</kwd>    
        </kwd-group>
        <kwd-group xml:lang="en">
            <title>Keywords</title>
            <kwd>Bronchoscopy</kwd>
            <kwd>Maximal expiratory flow-volume curves</kwd>
            <kwd>Sensitivity and specificity</kwd>
            <kwd>Lung neoplasms</kwd>
        </kwd-group>
        ...
    </article-meta>
    ...
 
