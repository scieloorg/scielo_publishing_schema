.. _elemento-fn:

<fn>
----

Representa um complemento ou um comentário explicativo do que está sendo citado no texto e deve ser identificado de acordo com sua natureza.


.. _elemento-fn-notas-autores:

Notas de autor
^^^^^^^^^^^^^^

Aparece em:

  :ref:`elemento-author-notes`

Atributos obrigatórios:

  1. ``@fn-type``

Ocorre:

  Zero ou mais vezes


Notas de rodapé de autores são inseridas em :ref:`elemento-author-notes` e, obrigatoriamente, possuem o atributo ``@fn-type``.

Os valores possíveis para ``@fn-type`` são:

+---------------------------+--------------------------------------------------+
| Valor                     | Descrição                                        |
+===========================+==================================================+
| author                    | Outro tipo de nota relacionada a autor           |
+---------------------------+--------------------------------------------------+
| con                       | Informação de contribuição                       |
+---------------------------+--------------------------------------------------+
| conflict                  | Declaração de conflito de interesse              |
+---------------------------+--------------------------------------------------+
| current-aff               | Afiliação atual do autor                         |
+---------------------------+--------------------------------------------------+
| deceased                  | Pessoa falecida desde que o artigo foi escrito   |
+---------------------------+--------------------------------------------------+
| edited-by                 | O autor é o editor                               |
+---------------------------+--------------------------------------------------+
| equal                     | Informação de contribuição igualitária           |
+---------------------------+--------------------------------------------------+
| on-leave                  | Autor está ausente (sabático ou outro)           |
+---------------------------+--------------------------------------------------+
| participating-researchers | Autor foi um pesquisador para o artigo           |
+---------------------------+--------------------------------------------------+
| present-address           | Endereço atual do autor                          |
+---------------------------+--------------------------------------------------+
| previously-at             | Afiliação anterior do autor                      |
+---------------------------+--------------------------------------------------+
| study-group-members       | Autor foi um membro do grupo de estudos para a   |
|                           | pesquisa                                         |
+---------------------------+--------------------------------------------------+
| other                     | Especifica aquelas notas diferentes das          |
|                           | relacionados acima. É possível também ter este   |
|                           | tipo de nota em :ref:`elemento-fn-group` em      |
|                           | :ref:`elemento-back`                             |
+---------------------------+--------------------------------------------------+
| presented-at              | Trabalho apresentado em conferência, colóquio etc|
+---------------------------+--------------------------------------------------+
| presented-by              | Informação de trabalho apresentado pelo autor    |
+---------------------------+--------------------------------------------------+

Exemplo:

.. code-block:: xml

    ...
    <author-notes>
        <corresp id="c01">
            <label>*</label>
            <bold>Correspondence</bold>: Dr. Edmundo Figueira Departamento de Fisioterapia, Universidade FISP - Hogwarts,  Brasil. E-mail: <email>contato@foo.com</email>
        </corresp>
        <fn fn-type="conflict">
            <p>Não há conflito de interesse entre os autores do artigo.</p>
        </fn>
        <fn fn-type="equal">
            <p>Todos os autores tiveram contribuição igualitária na criação do artigo.</p>
        </fn>
    </author-notes>
    ...


.. _elemento-fn-notas-gerais:

Notas gerais
^^^^^^^^^^^^

Aparece em:

  :ref:`elemento-fn-group`

Atributos obrigatórios:

  1. ``@fn-type``

Ocorre:

  Uma ou mais vezes


Representa um complemento ou um comentário explicativo do que está sendo citado no texto.

As notas que devem ser consideradas como nota de rodapé de :ref:`elemento-back`, são aquelas que não fazem qualquer tipo de referência aos autores, as quais deverão ser identificadas em :ref:`elemento-fn-notas-autores`.

Notas marcadas em :ref:`elemento-back` devem ser identificadas dentro do grupo :ref:`elemento-fn-group`.

O guia :ref:`sugestao-atribuicao-id` descreve o modo de composição do atributo ``@id``.

Notas que apresentam uma etiqueta de identificação (1, 2, a, b, ``*``, e etc) devem ser marcadas com o elemento :ref:`elemento-label`. Este elemento não pode ocorrer dentro de :ref:`elemento-p`.

Os valores possíveis para ``@fn-type`` são:

+-------------------------+--------------------------------------------------+
| Valor                   | Descrição                                        |
+=========================+==================================================+
| abbr                    | Representa abreviaturas de termos e nomes        |
|                         | próprios utilizadas ao longo do texto. Caso      |
|                         | esteja falando de abreviaturas de nomes dos      |
|                         | autores, deve-se inserir nota em                 |
|                         | :ref:`elemento-author-notes` em                  |
|                         | :ref:`elemento-front`.                           |
+-------------------------+--------------------------------------------------+
| com                     | Representa nota de algum tipo de comunicado      |
|                         | relevante para a realização do artigo.           |
+-------------------------+--------------------------------------------------+
| financial-disclosure    | Declaração de financiamento ou negação e         |
|                         | aceitação de recursos recebidos em apoio à       |
|                         | pesquisa na qual um artigo é baseado.            |
|                         | Presta-se também para informações de             |
|                         | financiamento que possuem um número de contrato  |
|                         | ou que só informam se houve ou não financiamento |
|                         | com "sim" ou "não".                              |
+-------------------------+--------------------------------------------------+
| supported-by            | Indica que a pesquisa sobre a qual o artigo é    |
|                         | baseado foi apoiada por alguma entidade,         |
|                         | instituição ou pessoa física. Consideram-se neste|
|                         | tipo, informações de financiamento que não       |
|                         | possuem número de contrato.                      |
+-------------------------+--------------------------------------------------+
| presented-at            | Indica que o artigo foi apresentado em algum     |
|                         | evento científico.                               |
+-------------------------+--------------------------------------------------+
| supplementary-material  | Indica ou descreve o material suplementar do     |
|                         | artigo.                                          |
+-------------------------+--------------------------------------------------+
| other                   | Especifica toda e qualquer nota diferente das    |
|                         | relacionados acima. É possível também ter este   |
|                         | tipo de nota em :ref:`elemento-author-notes`.    |
+-------------------------+--------------------------------------------------+


Exemplo:

.. code-block:: xml

    ...
    <fn-group>
        <fn fn-type="financial-disclosure" id="fn01">
            <label>1</label>
            <p>Declaração de financiamento: sim</p>
        </fn>
        <fn fn-type="presented-at" id="fn02">
            <label>**</label>
            <p>Artigo foi apresentado na XVIII Conferência Internacional de Biblioteconomia 2014</p>
        </fn>
    </fn-group>
    ...


.. _elemento-fn-notas-tabela:

Nota de Tabela
^^^^^^^^^^^^^^

Aparece em:

  :ref:`elemento-table-wrap-foot`


Atributos obrigatórios:

  1. ``@id``

Ocorre:

  Uma ou mais vezes

Notas de rodapé de tabelas são incluídas em :ref:`elemento-table-wrap-foot` e, obrigatoriamente, possuem o atributo ``@id``.

O guia :ref:`sugestao-atribuicao-id` descreve o modo de composição do atributo ``@id``.


Exemplo:

.. code-block:: xml

    ...
    <table-wrap id="t05">
      ...
      <table-wrap-foot>
        <fn id="TFN1">
          <label>*</label>
          <p>All diagnoses at admission (sepsis, cardiovascular, respiratory, neurological, gastrointestinal, and emergency surgery) were grouped except for elective surgery.</p>
        </fn>
      </table-wrap-foot>
    </table-wrap>
    ...


.. {"reviewed_on": "20160729", "by": "gandhalf_thewhite@hotmail.com"}
