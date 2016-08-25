.. _elemento-sec:

<sec>
=====

Aparece em:

  :ref:`elemento-body`
  :ref:`elemento-sec`

Ocorre:

  Zero ou mais vezes


O corpo textual do artigo pode ser constituído por seções. Cada uma delas tendo um elemento ``<title>`` seguido de um ou mais parágrafos (:ref:`elemento-p`).

:term:`Seções de primeiro nível` que condizem com a lista de valores abaixo devem, obrigatoriamente, apresentar um atributo ``@sec-type``. Caso haja *seção de primeiro nível* com nome diferente do que consta na tabela, o referido atributo não deve ser inserido.


+------------------------+------------------------------------------------+
| Valor                  | Descrição                                      |
+========================+================================================+
| cases                  | relatos/estudos de caso                        |
+------------------------+------------------------------------------------+
| conclusions            | conclusões/considerações finais/Final Remarks  |
+------------------------+------------------------------------------------+
| discussion             | discussões                                     |
+------------------------+------------------------------------------------+
| intro                  | introdução/sinopse                             |
+------------------------+------------------------------------------------+
| materials              | materiais                                      |
+------------------------+------------------------------------------------+
| methods                | metodologia/método                             |
+------------------------+------------------------------------------------+
| results                | resultados                                     |
+------------------------+------------------------------------------------+
| supplementary-material | material suplementar                           |
+------------------------+------------------------------------------------+


Exemplos:

  * :ref:`elemento-sec-exemplo-1`
  * :ref:`elemento-sec-exemplo-2`
  * :ref:`elemento-sec-exemplo-3`
  * :ref:`elemento-sec-exemplo-4`
  * :ref:`elemento-sec-exemplo-5`


.. _elemento-sec-exemplo-1:

Exemplo de ``<sec>`` do tipo simples:
-------------------------------------

.. code-block:: xml

    ...
    <body>
        ...
        <sec sec-type="intro">
            <title>Introduction</title>
            <p>Central airway obstruction (CAO) is a pathological process that leads to airflow limitation at the level of the glottis, subglottis, trachea, and main bronchi. Correct diagnosis and treatment of CAO is an area of interest and concern for health professionals,given that this disease has the potential to cause significant morbidity and mortality.</p>
            ...
        </sec>
        ...
    </body>
    ...


.. _elemento-sec-exemplo-2:

Exemplo de ``<sec>`` com seções combinadas:
-------------------------------------------

No caso de seções combinadas, ou seja, quando o título for composto por mais de um desses itens, o valor do atributo ``@sec-type`` deverá corresponder a cada um, respectivamente, separados pelo caractere ``|`` (pipe).


.. code-block:: xml

    ...
    <body>
        ...
        <sec sec-type="materials|methods">
            <title>Materials and Methods</title>
            <p>Between November of 2009 and April of 2010, we conducted a prospective, observational, cross-sectional study. The target population consisted of patients for whom bronchoscopy was clinically indicated. The patients were consecutively selected for the sample on the...</p>
            ...
        </sec>
        ...
    </body>
    ...

.. _elemento-sec-exemplo-3:

Exemplo de subseção de primeiro nível:
--------------------------------------

As seções podem ser compostas por uma ou mais subseções. Nesses casos, cada subseção deverá ser marcada com o elemento ``<sec>`` dentro da seção de nível superior.


.. code-block:: xml

    ...
    <body>
        ...
        <sec sec-type="methods">
            <title>Methodology</title>
            <sec>
                <title>Methodology in Science</title>
                <p>Each patient underwent a brief physical examination, and the degree of dyspnea was determined by the Medical Research Council (MRC) 5-point scale.</p>
                ...
            </sec>
        </sec>
        ...
    </body>
    ...

.. _elemento-sec-exemplo-4:

Exemplo de ``<sec>``sem tipo padrão:
------------------------------------

Seções sem tipo padrão podem ser declaradas sem o atributo ``@sec-type``.


.. code-block:: xml

    ...
    <body>
        ...
        <sec>
            <title>Biologia Marinha</title>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Morbi pharetra lacinia orci at adipiscing.</p>
            ...
        <sec>
        ...
    </body>
    ...


.. _elemento-sec-exemplo-5:

Exemplo de seção com marcador de numeração:
-------------------------------------------

Seções que apresentam marcador de numeração são identificadas juntamente com o texto no elemento ``<title>``.


.. code-block:: xml

    ...
    <body>
        ...
        <sec sec-type="intro">
            <title>1. Introdução</title>
            <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Mauris non sollicitudin nulla.</p>
            ...
        </sec>
        ...
    </body>
    ...


.. note:: Não inserir o elemento ``<label>`` para ``<sec>``.


.. {"reviewed_on": "20160629", "by": "gandhalf_thewhite@hotmail.com"}
