.. _elemento-ack:

<ack>
=====

Aparece em:

  :ref:`elemento-back`

Ocorre:

  Zero ou mais vezes

Seção de agradecimentos. Frequentemente indica os dados de financiamento da pesquisa como descrito em :ref:`elemento-funding-group`.

No caso de ter um título (ex. "Agradecimentos" ou "Acknowledgment") identifica-se com o elemento ``<title>`` (`JATS versão 1.0 <http://jats.nlm.nih.gov/publishing/1.0/>`_). Também é possível utilizar o elemento :ref:`elemento-p` para identificar os parágrafos do texto.

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

.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
