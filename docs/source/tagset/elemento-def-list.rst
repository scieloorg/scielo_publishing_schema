.. _elemento-def-list:

<def-list>
==========

Atributos obrigatórios:

  1. ``@id`` (Ver :ref:`sugestao-atribuicao-id`)


+----------------------------+--------------------+
| Aparece em                 | Ocorre             |
+============================+====================+
| :ref:`elemento-app`        | Zero ou mais vezes |
+----------------------------+--------------------+
| ``<app-group>``            | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-body`       | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-boxed-text` | Zero ou mais vezes |
+----------------------------+--------------------+
| ``<def-list>``             | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-glossary`   | Zero ou mais vezes |
+----------------------------+--------------------+
| ``<list-item>``            | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-p`          | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-ref-list`   | Zero ou mais vezes |
+----------------------------+--------------------+
| :ref:`elemento-sec`        | Zero ou mais vezes |
+----------------------------+--------------------+


Descreve uma lista de termos e suas definições, deve ser apresentada como texto e pode conter os seguintes elementos:

* ``<title>``
* ``<term-head>``
* ``<def-head>``
* ``<def-item>``
* ``<def-list>``

Em ``<def-item>`` usam-se os seguintes sub-elementos:

* ``<term>``: Identifica o termo da lista.
* ``<def>``: Descreve o termo da lista.


.. note:: Em ``<def>`` é obrigatório inserir a descrição dentro do elemento :ref:`elemento-p`.


O guia :ref:`sugestao-atribuicao-id` descreve o modo de composição do atributo ``@id``.

Exemplos:

  * :ref:`elemento-deflist-exemplo-1`
  * :ref:`elemento-deflist-exemplo-2`



.. _elemento-deflist-exemplo-1:

Exemplo de uma lista em ``<body>``:
-----------------------------------------

.. code-block:: xml

    ...
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
     ...


.. _elemento-deflist-exemplo-2:

Exemplo de uma lista com sublista em ``<glossary>``:
----------------------------------------------------

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


.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
