.. _elemento-response:

<response>
----------

Aparece em:

  :ref:`elemento-article`
  :ref:`elemento-sub-article`


Atributos obrigatórios:

  1. ``@response-type``
  2. ``@id``
  3. ``@xml:lang``


Ocorre:

  Zero ou mais vezes


Utilizado para apresentar uma resposta diretamente relacionada ao artigo principal, por exemplo, resposta de uma carta ou opinião contrária de um artigo publicado.

Para esse elemento recomenda-se utilizar também o elemento :ref:`elemento-front-stub`.

Para ``@response-type`` os valores possíveis são:

+------------------------+-----------------------------------------+
| Valor                  | Descrição                               |
+========================+=========================================+
| addendum               | Adendo - Informação adicional           |
+------------------------+-----------------------------------------+
| discussion             | Discussão relacionada a um número       |
|                        | específico                              |
+------------------------+-----------------------------------------+
| reply                  | Resposta a um artigo                    |
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


.. {"reviewed_on": "20160628", "by": "gandhalf_thewhite@hotmail.com"}
