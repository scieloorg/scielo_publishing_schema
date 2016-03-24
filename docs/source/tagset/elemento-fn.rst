.. _elemento-fn:

<fn>
----

Representa um complemento ou um comentário explicativo do que está sendo 
citado no texto, e deve ser identificado de acordo com sua natureza 
ao referenciar autores ou as demais partes do texto.


.. _elemento-fn-notas-autores:

Notas de autor
^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-author-notes`

Atributos obrigatórios
  1. fn-type
 
Ocorre
  Zero ou mais vezes


Notas de rodapé de autores são notas inseridas em :ref:`elemento-author-notes` 
e que obrigatoriamente possuem o atributo ``@fn-type``. 

Os valores possíveis para o atributo ``@fn-type`` são:
 
+---------------------------+--------------------------------------------------+
| Valor                     | Descrição                                        |
+===========================+==================================================+
| author                    | Outro tipo de nota relacionado a autor           |
+---------------------------+--------------------------------------------------+
| con                       | Informação de contribuição                       |
+---------------------------+--------------------------------------------------+
| conflict                  | Declaração de conflito de Interesse              |
+---------------------------+--------------------------------------------------+
| current-aff               | Afiliação atual do autor                         |
+---------------------------+--------------------------------------------------+
| deceased                  | Pessoa morreu desde que o artigo foi escrito     |
+---------------------------+--------------------------------------------------+
| edited-by                 | Autor é o editor                                 |
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
| presented-at              | Trabalho apresentado em Conferência, Colóquio etc|
+---------------------------+--------------------------------------------------+
| presented-by              | Informação de trabalho apresentado pelo autor    |
+---------------------------+--------------------------------------------------+
 

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

Aparece em
  :ref:`elemento-fn-group`

Atributos obrigatórios
  1. fn-type

Ocorre
  Uma ou mais vezes


Representa um complemento ou um comentário explicativo do que está sendo 
citado no texto.
 
As notas que devem ser consideradas para entrar como nota de rodapé de
:ref:`elemento-back`, são quaisquer notas que não fazem nenhum tipo de
referência aos autores, as quais deverão ser identificadas em
:ref:`elemento-fn-notas-autores`.
 
Notas em :ref:`elemento-back` devem ser identificadas dentro do grupo 
:ref:`elemento-fn-group`.
 
Consulte a :ref:`sugestao-atribuicao-id` para instruções sobre a composição do 
atributo ``@id``.
 
Para notas que apresentam uma etiqueta de identificação (1, 2, a, b, ``*``, e etc)
marque com a tag :ref:`elemento-label`. A tag :ref:`elemento-label` não
pode estar dentro de :ref:`elemento-p`.

Os valores possíveis para o atributo ``@fn-type`` são:
 
+-------------------------+--------------------------------------------------+
| Valor                   | Descrição                                        |
+=========================+==================================================+
| abbr                    | Representa abreviaturas de termos e nomes        |
|                         | próprios utilizadas ao longo do texto. Caso      |
|                         | esteja falando de abreviaturas de nomes dos      |
|                         | autores, inserir nota em                         |
|                         | :ref:`elemento-author-notes` em                  |
|                         | :ref:`elemento-front`                            |
+-------------------------+--------------------------------------------------+
| com                     | Representa nota de algum tipo de comunicado      |
|                         | relevante para a realização do artigo            |
+-------------------------+--------------------------------------------------+
| financial-disclosure    | Declaração de financiamento ou negação e         |
|                         | aceitação de recursos recebidos em apoio às      |
|                         | pesquisa em que um artigo é baseado. Serve também|
|                         | para informações de financiamento que possuem    |
|                         | um número de contrato ou que só informam se "sim"|
|                         | ou "não" houve financiamento                     |
+-------------------------+--------------------------------------------------+
| supported-by            | Indica que a pesquisa sobre a qual o artigo é    |
|                         | baseado foi apoiada por alguma entidade,         |
|                         | instituição ou pessoa física. Considerar neste   |
|                         | tipo, informações de financiamento que não       |
|                         | possuem número de contrato                       |
+-------------------------+--------------------------------------------------+
| presented-at            | Indica que o artigo foi apresentado em algum     |
|                         | evento científico                                |
+-------------------------+--------------------------------------------------+
| supplementary-material  | Indica ou descreve o material suplementar do     |
|                         | artigo                                           |
+-------------------------+--------------------------------------------------+
| other                   | Especifica aquelas notas diferentes das          |
|                         | relacionados acima. É possível também ter este   |
|                         | tipo de nota em :ref:`elemento-author-notes`     |
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

Aparece em
  :ref:`elemento-table-wrap-foot`


Atributos obrigatórios
  1. id

Ocorre
  Uma ou mais vezes

Notas de rodapé de tabelas são notas inseridas em :ref:`elemento-table-wrap-foot` e que obrigatoriamente possuem o atributo @id.
Consulte a :ref:`sugestao-atribuicao-id` para instruções sobre a composição do atributo ``@id``.


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

