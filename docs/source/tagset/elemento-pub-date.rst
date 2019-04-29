.. _elemento-pub-date:

<pub-date>
==========


Atributos obrigatórios:

  1. ``@date-type="pub"``
  2. ``@publication-format="electronic"``

+------------------------------+-------------------+
| Aparece em                   | Ocorre            |
+==============================+===================+
| :ref:`elemento-article-meta` | Uma ou mais vezes |
+------------------------------+-------------------+


Representam as datas de publicação do artigo/número.


O :ref:`elemento-pub-date` deve estar acompanhado do atributo ``@date-type`` com os valores "pub" e "collection" e do atributo ``@publication-format`` com valor "electronic". Sempre que houver um ``@date-type`` do tipo "collection" obrigatoriamente deve existir um ``@date-type`` do tipo "pub", sendo: 


+---------------+---------------------------------------------+------------------------------------+
|``@date-type`` | Descrição                                   | Tipos de Datas                     |
+===============+=============================================+====================================+
|      pub      | Data efetiva de publicação em SciELO.       | dia + mês + ano                    |
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

    <pub-date publication-format="electronic" date-type="pub">
       <day>01</day>
       <month>01</month>
       <year>2018</year>
    </pub-date>
    <pub-date publication-format="electronic" date-type="collection">
       <season>Jan-Feb</season>
       <year>2018</year>
    </pub-date>


.. _elemento-pubdate-exemplo-2: 

Exemplo de ``<pub-date>`` em publicação regular 2:
--------------------------------------------------

.. code-block:: xml

    <pub-date publication-format="electronic" date-type="pub">
       <day>01</day>
       <month>01</month>
       <year>2018</year>
    </pub-date>
     <pub-date publication-format="electronic" date-type="collection">
       <month>01</month>
       <year>2018</year>
    </pub-date>


.. _elemento-pubdate-exemplo-3: 

Exemplo de ``<pub-date>`` em modalidade de `publicação contínua (PC) <https://wp.scielo.org/wp-content/uploads/guia_pc.pdf>`_
-------------------------------------------------------------------------------------------------------------------------------

.. code-block:: xml

    <pub-date publication-format="electronic" date-type="pub">
       <day>01</day>
       <month>12</month>
       <year>2018</year>
    </pub-date>
     <pub-date publication-format="electronic" date-type="collection">      
       <year>2019</year>
    </pub-date>


.. _elemento-pubdate-exemplo-4:

Exemplo de ``<pub-date>`` em modalidade `ahead of print (AOP) <https://wp.scielo.org/wp-content/uploads/guia_AOP.pdf>`_
-------------------------------------------------------------------------------------------------------------------------

.. code-block:: xml

    <pub-date publication-format="electronic" date-type="pub">
       <day>17</day>
       <month>02</month>
       <year>2019</year>
    </pub-date>


.. note::
 * Para datas do tipo "pub", criar as tags :ref:`elemento-day` e :ref:`elemento-month` com informação 00 ou qualquer outra data para que seja alterada posteriormente com a data efetiva da publicação pela unidade de produção SciELO;
 * Todos os artigos publicados em SciELO devem contemplar obrigatoriamente duas datas de :ref:`elemento-pub-date` (com exceção de artigos em `AOP <https://wp.scielo.org/wp-content/uploads/guia_AOP.pdf>`_);
 * Para datas do tipo "collection", sempre preencher a data a qual o fascículo pertence, seguindo sua periodicidade;
 * Para revistas que adotam `publicação contínua (PC) <https://wp.scielo.org/wp-content/uploads/guia_pc.pdf>`_, só considerar o ano a qual o fascículo pertence para data do tipo "collection".
