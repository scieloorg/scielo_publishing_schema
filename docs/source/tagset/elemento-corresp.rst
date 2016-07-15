.. _elemento-corresp:

<corresp>
=========

Aparece em:

  :ref:`elemento-author-notes`

Ocorre:

  Zero ou mais vezes

Elemento que concentra informação de correspondência de um autor do artigo. Pode ou não conter um elemento :ref:`elemento-label`. O atributo  ``@id`` também é opcional. É possível ainda marcar a informação de correio eletrônico com ``<email>`` caso exista.

O guia :ref:`sugestao-atribuicao-id` descreve o modo de composição do atributo ``@id``.

Exemplo:

.. code-block:: xml

    ...
    <author-notes>
        ...
        <corresp id="c01">Dr. Edmundo Figueira Departamento de Fisioterapia, Universidade FISP - São Paulo, Brasil. E-mail: <email>contato@foo.com</email></corresp>
        ...
    </author-notes>
    ...

.. note:: Para este elemento não é necessário utilizar parágrafo (:ref:`elemento-p`).


.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
