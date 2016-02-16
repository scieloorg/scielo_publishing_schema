.. _elemento-article-title:

<article-title>
^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-title-group`, 
  :ref:`elemento-element-citation`
 
Ocorre
  zero ou uma vez


Esta tag pode ser utilizada para especificar o título do artigo em si 
em :ref:`elemento-article-meta`, ou para especificar um título de documento 
nas referências em :ref:`elemento-element-citation`. Em ambos os casos, o 
atributo ``@xml:lang`` não deve ser utilizado.

.. note:: O elemento ``<article-title>`` é obrigatório em :ref:`elemento-title-group`, .

 
Exemplo:
 
.. code-block:: xml
 
    ...
    <title-group>
        <article-title>The teaching of temporomandibular disorders and  orofacial pain at undergraduate level in Brazilian dental schools</article-title>
    </title-group>
    ...

.. note:: Se o título do artigo ou da referência possuir um subtítulo, ele deve 
          ser marcado junto a tag ``<article-title>``. Não se deve marcar 
          nenhum texto separadamente em outras tags 
          (a mesma regra se aplica a :ref:`elemento-trans-title`).
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <title-group>
        <article-title>Correlação entre sintomas e tempo de evolução do câncer do trato aerodigestivo superior com o estádio inicial e avançado</article-title>
    </title-group>
    ...


.. note:: Se o título da seção for igual ao título do artigo (exemplo de alguns 
          editoriais, erratas, cartas ao editor), repetir a informação no front 
          e marcá-la com as tags de título. 

