.. _elemento-trans-abstract:

<trans-abstract>
----------------

Aparece em:

  :ref:`elemento-article-meta`
  :ref:`elemento-front-stub`

Atributos obrigatórios:

  1. ``@xml:lang``

Ocorre:

  Zero ou mais vezes

Contém o resumo traduzido do artigo, podendo apresentar os formatos simples ou estruturado, do mesmo modo que o elemento :ref:`elemento-abstract`. Se existente, deve ser inserida imediatamente após :ref:`elemento-abstract` e, obrigatoriamente, conter o atributo ``@xml:lang``.

Em ``<trans-abstract>`` deve ser inserida uma informação de rótulo no elemento ``<title>``.

Formato estruturado: Apresenta os principais pontos do texto dividido em seções.

Exemplo:

.. code-block:: xml

    ...
    <article-meta>
        ...
        <trans-abstract xml:lang="en">
            <title>Abstract</title>
            <sec>
                <title>Objective</title>
                <p>To analyze the association between socioeconomic situation, clinical characteristics referred and the family history of cardiovascular disease, with the Self-perceived health of young adults education and their implications for clinical characteristics observed.</p>
            </sec>
            <sec>
                <title>Method</title>
                <p>Analytical study conducted with 501 young adults who are students in countryside city in the Brazilian Northeast. We used binary logistic regression.</p>
            </sec>
        </trans-abstract>
        ...
    </article-meta>
    ...


Formato simples: Apresenta de forma sucinta os principais pontos do texto sem a divisão por seções.

Exemplo:


.. code-block:: xml

    ...
    <article-meta>
        ...
        <trans-abstract xml:lang="en">
            <title>Abstract</title>
            <p>In this paper we discuss the tutoring model adopted by the Public Institutions of Higher Education that integrate the Open University of Brazil (Universidade Aberta do Brasil - UAB) program. The starting point is the research and the actions developed by the authors in the past decade that are directly related to distance education in Brazil. The focus is on the classroom tutors who are responsible for assisting students in the presential center where they have support and who are selected through publishe.. notes in the virtual notice board of the institutions that offer higher education courses in a distinct mode of classroom teaching.</p>
        </trans-abstract>
        ...
    </article-meta>
    ...


.. {"reviewed_on": "20160629", "by": "gandhalf_thewhite@hotmail.com"}
