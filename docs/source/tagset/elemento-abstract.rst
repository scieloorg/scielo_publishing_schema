.. _elemento-abstract:

<abstract>
==========

+------------------------------+--------------------+
| Aparece em                   | Ocorre             |
+==============================+====================+
| :ref:`elemento-article-meta` | Zero ou mais vezes |
+------------------------------+--------------------+



Elemento que identifica o resumo de um artigo. Não deve conter o atributo ``@xml:lang``. Embora ``<abstract>`` possa não ocorrer, faz-se obrigatório quando :ref:`elemento-article` for declarado com atributo ``@article-type="research-article"`` ou ``@article-type="review-article"``.

Opcionalmente, além do resumo tradicional, pode-se utilizar um Resumo Visual (Visual Abstract). Para este caso declarar em ``<abstract>`` o atributo ``@abstract-type="graphical"`` com atributo ``@xml:lang``.


``<abstract>`` contém obrigatoriamente um elemento ``<title>`` que especifica o título do resumo.

 Exemplos:

* Estruturado: Possui grupos de textos organizados em seções identificadas com um título (Por exemplo: Introdução, Objetivos, Métodos e Resultados).

 
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

* Resumo Visual (Visual Abstract): Imagem que representa o texto do resumo de um artigo.


  .. code-block:: xml

      ...
      <abstract abstract-type="graphical" xml:lang="en">
        <title>Visual Abstract</title>
          <p>
            <fig id="vf01">                 
               <caption>
                  <title>Título</title>  
               </caption>  
               <graphic xlink:href="1234-5678-zwy-12-04-0123-vs01.tif"/>                 
            </fig>
          </p>  
      </abstract>
      ...

.. note:: Para mais informações sobre Resumo Visual, recomendamos leitura do texto `"Use of a VISUAL ABSTRACT to Disseminate Scientific Research <https://static1.squarespace.com/static/5854aaa044024321a353bb0d/t/5a527aa89140b76bbfb2028a/1515354827682/VisualAbstract_Primer_v4_1.pdf>`_ de Andrew M. Ibrahim, 2018. 

.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
