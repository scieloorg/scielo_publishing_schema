.. _elemento-corresp:

<corresp>
---------
 
Aparece em
  :ref:`elemento-author-notes`
 
Ocorre
  Zero ou mais vezes


Esta tag representa as informações de correspondência de um dos autores 
do artigo. Pode ou não possuir um :ref:`elemento-label` e também o atributo 
``@id``. É possível marcar o ``<email>`` caso inserido.
 
Consulte a :ref:`sugestao-atribuicao-id` para instruções sobre a composição do 
atributo ``@id``.
 
Exemplo:

.. code-block:: xml
 
    ...
    <author-notes>
        ...
        <corresp id="c01">Dr. Edmundo Figueira Departamento de Fisioterapia, Universidade FISP - São Paulo, Brasil. E-mail: <email>contato@foo.com</email></corresp>
        ...
    </author-notes>
    ...
 
.. note:: Esta tag não necessita da inserção de parágrafo :ref:`elemento-p`.
 
