.. _elemento-fn:

<fn>
====

Elemento usado para marcação de nota, deverá ser utilizado em 3 contextos: notas de autor, notas gerais e notas de tabela.

Notas que apresentam uma etiqueta de identificação (1, 2, a, b, ``*``, e etc) devem ser marcadas com o elemento :ref:`elemento-label`.

O guia :ref:`sugestao-atribuicao-id` descreve o modo de composição do atributo ``@id``.


  * :ref:`elemento-fn-notas-autores`
  * :ref:`elemento-fn-notas-gerais`
  * :ref:`elemento-fn-notas-tabela`


.. _elemento-fn-notas-autores:

Notas de autor
--------------

Atributos obrigatórios:

  1. ``@fn-type``

+------------------------------+--------------------+
| Aparece em                   | Ocorre             |
+==============================+====================+
| :ref:`elemento-author-notes` | Zero ou mais vezes |
+------------------------------+--------------------+


Notas com referência ao(s) autor(es) do documento. Obrigatoriamente possuem o atributo ``@fn-type``.


Os valores possíveis para ``@fn-type`` são:

+---------------------------+--------------------------------------------------+
| Valor                     | Descrição                                        |
+===========================+==================================================+
| con                       | Informação de contribuição                       |
+---------------------------+--------------------------------------------------+
| conflict                  | Declaração de conflito de interesse              |
+---------------------------+--------------------------------------------------+
| current-aff               | Afiliação atual do autor                         |
+---------------------------+--------------------------------------------------+
| deceased                  | Pessoa falecida desde que o artigo foi escrito   |
+---------------------------+--------------------------------------------------+
| edited-by                 | Editor do artigo                                 |
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
------------

Atributos obrigatórios:

  1. ``@fn-type``

+--------------------------+-------------------+
| Aparece em               | Ocorre            |
+==============================+===============+
| :ref:`elemento-fn-group` | Uma ou mais vezes |
+--------------------------+-------------------+


Notas gerais usualmente referenciam informação do próprio documento e da pesquisa.

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

Notas de Tabelas
----------------

Atributos obrigatórios:

  1. ``@id``

+---------------------------------+-------------------+
| Aparece em                      | Ocorre            |
+=================================+===================+
| :ref:`elemento-table-wrap-foot` | Uma ou mais vezes |
+---------------------------------+-------------------+


Notas de tabelas obrigatoriamente possuem o atributo ``@id``.


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


.. {"reviewed_on": "20170901", "by": "carolina.tanigushi@scielo.org"}
