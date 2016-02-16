.. _elemento-sec:

<sec>
-----
Aparece em
  :ref:`elemento-body`

Ocorre
  Zero ou mais vezes

 
O corpo textual do artigo pode ser constituído por seções. 
Cada uma delas possui um elemento ``<title>`` seguido de um ou mais 
:ref:`elemento-p`.

:term:`Seções de primeiro nível` podem ser qualificadas de acordo com seu tipo por 
meio do atributo ``@sec-type``, cujos valores possíveis são:

+------------------------+------------------------------------------------+
| Valor                  | Descrição                                      |
+========================+================================================+
| cases                  | relatos/estudos de caso                        |
+------------------------+------------------------------------------------+
| conclusions            | conclusões/considerações finais/Final Remarkes |
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

 
Exemplo:
 
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
 

No caso de seções combinadas, ou seja, quando o título for composto por mais 
de um desses itens, o valor do atributo ``@sec-type`` deverá corresponder a 
cada um respectivamente, separados pelo caractere ``|``.
 
Exemplo:
 
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

 
As seções podem ser compostas por uma ou mais subseções, neste caso, 
cada subseção deverá ser marcada com tag ``<sec>`` dentro da seção maior.
 
Exemplo:
 
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

 
No caso da seção não possuir nenhum tipo padrão pode-se inserir a tag sem o 
atributo ``@sec-type``. 

Exemplo:
 
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

 
Para seções que apresentam marcador de numeração, identificar o dado dentro da tag <title>.
Exemplo:

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


.. note:: Não inserir a tag <label> para <sec>.

