.. _elemento-abstract:

<abstract>
==========

Aparece em:

  :ref:`elemento-article-meta`

Ocorre:

  Zero ou mais vezes


Elemento que identifica o resumo de um artigo. Não deve conter o atributo ``@xml:lang``. Embora ``<abstract>`` possa não ocorrer, faz-se obrigatório quando :ref:`elemento-article` for declarado com atributo ``@article-type="research-article"`` ou ``@article-type="review-article"``.

``<abstract>`` contém obrigatoriamente um elemento ``<title>`` que especifica o título do resumo.

Os resumos dos artigos publicados na *SciELO* normalmente se apresentam em dois formatos:

* Estruturado: Possui grupos de textos organizados em seções identificadas com um título (Por exemplo: Introdução, Objetivos, Métodos e Resultados).

  Exemplo:

  .. code-block:: xml

      ...
      <article-meta>
          ...
          <abstract>
            <title>Resumo</title>
              <sec>
                  <title>Objetivo</title>
                  <p>Verificar a sensibilidade e especificidade das curvas de fluxo-volume na detecção de obstrução da via aérea central (OVAC), e se os critérios qualitativos e quantitativos da curva se relacionam com a localização, o tipo e o grau de obstrução.</p>
              </sec>
              <sec>
                  <title>Métodos</title>
                  <p>Durante quatro meses foram selecionados, consecutivamente, indivíduos com indicação para broncoscopia. Todos efetuaram avaliação clínica, preenchimento de escala de dispneia, curva de fluxo-volume e broncoscopia num intervalo de uma semana. Quatro revisores classificaram a morfologia da curva sem conhecimento dos dados quantitativos, clínicos e broncoscopicos. Um quinto revisor averiguou os critérios morfológicos e quantitativos.</p>
              </sec>
          </abstract>
          ...
      </article-meta>
      ...

* Simples: Apresenta de forma sucinta os principais pontos do texto sem a divisão por seções.

  Exemplo:

  .. code-block:: xml

      ...
      <article-meta>
          ...
          <abstract>
            <title>Resumo</title>
              <p>Verificar a sensibilidade e especificidade das curvas de fluxo-volume na detecção de obstrução da via aérea central (OVAC), e se os critérios qualitativos e quantitativos da curva se relacionam com a localização, o tipo e o grau de obstrução. Métodos: Durante quatro meses foram selecionados, consecutivamente, indivíduos com indicação para broncoscopia. Todos efetuaram avaliação clínica, preenchimento de escala de dispneia, curva de fluxo-volume e broncoscopia num intervalo de uma semana. Quatro revisores classificaram a morfologia da curva sem conhecimento dos dados quantitativos, clínicos e broncoscopicos. Um quinto revisor averiguou os critérios morfológicos e quantitativos.</p>
          </abstract>
          ...
      </article-meta>
      ...

.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
