.. _elemento-pub-date:

<pub-date>
==========

Atributos obrigatórios:

  1. ``@pub-type``

+------------------------------+-----------------------+
| Aparece em                   | Ocorre                |
+==============================+=======================+
| :ref:`elemento-article-meta` | Uma ou mais vezes     |
+------------------------------+-----------------------+


Representam as datas de publicação do artigo/número.

O :ref:`elemento-pub-date` deve comtemplar obrigatoriamente duas datas (com exceção de artigos em `ahead of print (AOP) <https://wp.scielo.org/wp-content/uploads/guia_AOP.pdf>`_), a primeira delas com atributo ``@pub-type`` com valor "epub" e a segunda com valor "collection", sendo:


+---------------+---------------------------------------------+------------------------------------+
| ``@pub-type`` | Descrição                                   | Tipos de Datas                     |
+===============+=============================================+====================================+
|      epub     | Data efetiva de publicação em SciELO.       | dia + mês + ano                    |
+---------------+---------------------------------------------+------------------------------------+
|  collection   | Data do fascículo ao qual pertence o artigo.| ano OU; mês + ano OU; season + ano.|
+---------------+---------------------------------------------+------------------------------------+


Exemplos:

    * :ref:`elemento-pubdate-exemplo-1`
    * :ref:`elemento-pubdate-exemplo-2`
    * :ref:`elemento-pubdate-exemplo-3`
    * :ref:`elemento-pubdate-exemplo-4`
    

.. _elemento-pubdate-exemplo-1: 

Exemplo de ``<pub-date>`` em publicação regular 1:
--------------------------------------------------

.. code-block:: xml

    <pub-date pub-type="epub">
       <day>01</day>
       <month>01</month>
       <year>2018</year>
    </pub-date>
    <pub-date pub-type="collection">
       <season>Jan-Feb</season>
       <year>2018</year>
    </pub-date>


.. _elemento-pubdate-exemplo-2: 

Exemplo de ``<pub-date>`` em publicação regular 2:
--------------------------------------------------

.. code-block:: xml

    <pub-date pub-type="epub">
       <day>01</day>
       <month>01</month>
       <year>2018</year>
    </pub-date>
    <pub-date pub-type="collection">
       <month>01</month>
       <year>2018</year>
    </pub-date>


.. _elemento-pubdate-exemplo-3: 

Exemplo de ``<pub-date>`` em modalidade de `publicação contínua (PC) <https://wp.scielo.org/wp-content/uploads/guia_pc.pdf>`_
--------------------------------------------------------------------------------------------------------------------------------------

.. code-block:: xml

    <pub-date pub-type="epub">
       <day>01</day>
       <month>12</month>
       <year>2018</year>
    </pub-date>
    <pub-date pub-type="collection">      
       <year>2019</year>
    </pub-date>


.. _elemento-pubdate-exemplo-4:

Exemplo de ``<pub-date>`` em modalidade `ahead of print (AOP) <https://wp.scielo.org/wp-content/uploads/guia_AOP.pdf>`_
---------------------------------------------------------------------------------------------------------------------------------

.. code-block:: xml

    <pub-date pub-type="epub">
       <day>17</day>
       <month>02</month>
       <year>2019</year>
    </pub-date>


.. note::
 * Sempre que houver uma data do tipo "collection" obrigatoriamente deve-se ter uma data do tipo "epub";
 * Para datas do tipo "epub", criar as tags :ref:`elemento-day` e :ref:`elemento-month` com informação 00 ou qualquer outra data para que seja alterada posteriormente com a data efetiva da publicação pela unidade de produção SciELO;
 * Todos os artigos publicados em SciELO devem contemplar obrigatoriamente duas datas de :ref:`elemento-pub-date` (com exceção de artigos em `ahead of print (AOP) <https://wp.scielo.org/wp-content/uploads/guia_AOP.pdf>`_);
 * Para datas do tipo "collection", sempre preencher a data a qual o fascículo pertence, seguindo sua periodicidade;
 * Para revistas que adotam `publicação contínua (PC) <https://wp.scielo.org/wp-content/uploads/guia_pc.pdf>`_, só considerar o ano a qual o fascículo pertence para data do tipo "collection".

