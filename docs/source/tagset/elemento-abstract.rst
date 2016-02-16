.. _elemento-abstract:

<abstract>
----------

Aparece em
  :ref:`elemento-article-meta`
 
Ocorre
  Zero ou mais vezes


Tag que identifica o resumo do artigo e não deve conter informação de 
atributo ``@xml:lang``. Embora em via de regra esse elemento ocorra 
zero ou mais vezes, ele se faz obrigatório quando :ref:`elemento-article` for declarado
com o atributo ``@article-type="research-article"`` ou ``@article-type="review-article"``.
Em ``<abstract>`` deve ser inserido um elemento ``title`` para especificar o título do resumo.

Os resumos apresentados nos artigos publicados na SciELO normalmente 
apresentam-se em dois formatos:
 
* Estruturado: Quando possui seções 
  (Ex.: Introdução, Objetivos, Métodos e Resultado). Cada grupo apresentado 
  no resumo será identificado como seção e cada seção terá seu título.
 
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

* Simples: Quando apresenta de forma sucinta os principais pontos do 
  texto sem a divisão por seções. 
 
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

