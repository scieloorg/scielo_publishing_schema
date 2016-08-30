.. _elemento-ack:

<ack>
=====

Aparece em:

  :ref:`elemento-back`

Ocorre:

  Zero ou mais vezes

Seção de agradecimentos. Frequentemente indica os dados de financiamento da pesquisa como descrito em :ref:`elemento-funding-group`.

No caso de ter um título (ex. "Agradecimentos" ou "Acknowledgment") identifica-se com o elemento ``<title>``. O elemento :ref:`elemento-p` é utilizado para identificar parágrafos do texto.

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

.. note:: Não se deve inserir o elemento :ref:`elemento-sec` para identificar uma seção de agradecimentos.

.. {"reviewed_on": "20160729", "by": "gandhalf_thewhite@hotmail.com"}
