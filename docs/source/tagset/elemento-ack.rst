.. _elemento-ack:

<ack>
-----

Aparece em
  :ref:`elemento-back`

Ocorre
  Zero ou mais vezes

A seção de agradecimentos quando aparecer no documento deve ser marcada dentro
de :ref:`elemento-back`.
 
É em agradecimentos que frequentemente os dados de financiamento da pesquisa são 
indicados, como descrito em :ref:`elemento-funding-group`
em :ref:`elemento-front`.
 
Todo o conteúdo de agradecimentos deverá ser identificado com a tag ``<ack>``, 
caso haja o título "Agradecimentos" ou "Acknowledgment" identifique-o com a tag
``<title>``. Em ``<ack>`` é possível especificar um ou mais parágrafos
:ref:`elemento-p`.

Exemplo:
 
.. code-block:: xml

    ...
    <back>
        <ack>
            <title>Agradecimentos</title>
            <p>Texto de agradecimentos, pode ou não conter dados de financiamento</p>
        </ack>
    </back>
    ...

.. note:: Não inserir a tag :ref:`elemento-sec` para identificação da seção
          agradecimentos.

