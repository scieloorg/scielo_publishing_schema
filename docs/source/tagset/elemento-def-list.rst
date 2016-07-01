.. _elemento-def-list:

<def-list>
----------

Aparece em:

  :ref:`elemento-app`
  ``<app-group>``
  :ref:`elemento-body`
  :ref:`elemento-boxed-text`
  ``<def-list>``
  :ref:`elemento-glossary`
  ``<list-item>``
  :ref:`elemento-p`
  :ref:`elemento-ref-list`
  :ref:`elemento-sec`

Atributos obrigatórios:

  1. ``@id``


Ocorre:

  Zero ou mais vezes



Descreve uma lista de termos e suas respectivas definições, que deve ser apresentada como texto contendo os seguintes elementos:

* ``<title>``
* ``<term-head>``
* ``<def-head>``
* ``<def-item>``
* ``<def-list>``

Em ``<def-item>`` usam-se os seguintes sub-elementos:

* ``<term>``: Identifica a palavra, frase, equação etc., que está sendo definida ou descrita.
* ``<def>``: Descrição, explicação da palavra ou frase em ``<term>``. Nesse contexto deve-se, obrigatoriamente, inserir o elemento :ref:`elemento-p`.


O guia :ref:`sugestao-atribuicao-id` descreve o modo de composição do atributo ``@id``.

Exemplos:

1. em ``<body>``:

.. code-block:: xml

  <body>
    <def-list id="d1">
      <def-item>
        <term>Angina pectoris (Angina de peito)</term>
        <def>
          <p>Sensação de angústia, de opressão torácica, devido a um fornecimento insuficiente de oxigênio ao coração.</p>
        </def>
      </def-item>
      <def-item>
        <term>Antagonista</term>
        <def>
            <p>É uma droga ou um composto que opõe os efeitos fisiológicos de outro composto. Em nível de receptor, é uma entidade química que opõe as respostas associadas à ativação do receptor, normalmente induzidas por outro agente bioativo.</p>
        </def>
      </def-item>
      <def-item>
        <term>Biodisponibilidade</term>
          <def>
            <p>Termo que expressa a taxa ou concentração de fármaco que atinge a circulação sistêmica a partir do seu sítio de administração.</p>
          </def>
      </def-item>
    </def-list>
  </body>


2. em sublista de definições:

.. code-block:: xml

    ...
    <def-list id="d2">
      <label>Glossário</label>
      <def-item>
        <term>I</term>
        <def>
          <p>moment of inertia</p>
        </def>
      </def-item>
      <def-item>
        <term>V</term>
        <def>
          <p>shear force</p>
        </def>
      </def-item>
        <def-list>
          <def-item>
            <term>D<sub>E</sub>50</term>
            <def>
              <p>Dose do fármaco necessária para atingir 50% do efeito farmacológico desejado</p>
            </def>
          </def-item>
          <def-item>
            <term>Depuração</term>
            <def>
              <p>Indica a taxa de remoção de uma substância do sangue quando ele atravessa um órgão, por ex., fígado ou rim.</p>
            </def>
          </def-item>
        </def-list>
    </def-list>
    ...

.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
