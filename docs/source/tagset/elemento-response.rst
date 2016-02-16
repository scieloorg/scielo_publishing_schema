.. _elemento-response:

<response>
----------

Aparece em
  :ref:`elemento-article`,
  :ref:`elemento-sub-article`


Atributos obrigatórios
  1. response-type
  2. id
  3. xml:lang


Ocorre
  Zero ou mais vezes


Utilizada para apresentar uma resposta ao artigo principal que está diretamente relacionado ao artigo principal, por exemplo, resposta de uma carta ou apresenta opinião contrária de um artigo publicado.
Para esse elemento, recomendamos utilizar também a tag :ref:`elemento-front-stub`.

Para ``@response-type``, os valores que podem ser utilizados são:

+------------------------+-----------------------------------------+
| Valor                  | Descrição                               |
+========================+=========================================+
| addendum               | Adendo - Informação adicional           |
+------------------------+-----------------------------------------+
| discussion             | Discussão relacionado a um número       |
|                        | específico                              |
+------------------------+-----------------------------------------+
| reply                  | resposta a um artigo                    |
+------------------------+-----------------------------------------+

Exemplo da tag completa:

.. code-block:: xml
 
    ...
    <article>
      ...
      <response response-type="reply" xml:lang="en" id="R1">
          ...
      </response>
    </article>
    ...


