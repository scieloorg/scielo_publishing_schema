.. _elemento-pub-date:

<pub-date>
==========

Este elemento possui :ref:`scielo-brasil`


Atributos obrigatórios:

  1. ``@date-type``
  2. ``@publication-format``

+------------------------------+-------------------+
| Aparece em                   | Ocorre            |
+==============================+===================+
| :ref:`elemento-article-meta` | Uma ou mais vezes |
+------------------------------+-------------------+


Representam as datas de publicação do artigo/número.


``<pub-date>`` deve estar acompanhada do atributo ``@date-type``, do tipo ``pub`` e ``collection`` quando necessário e do atributo e do atributo ``@publication-format`` obrigatoriemante com valor ``electronic`` sendo: 


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

Exemplo de ``<pub-date>`` em modalidade de `publicação contínua (PC) <http://www.scielo.org/local/Image/guiarpass.pdf>`_
-------------------------------------------------------------------------------------------------------------------------

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

Exemplo de ``<pub-date>`` em modalidade `ahead of print (AOP) <http://www.scielo.org/local/File/Guia_AOP.pdf>`_
----------------------------------------------------------------------------------------------------------------

.. code-block:: xml

    <pub-date publication-format="electronic" date-type="pub">
       <day>17</day>
       <month>02</month>
       <year>2019</year>
    </pub-date>


.. note::
 * Para datas do tipo pub, criar as tags :ref:`elemento-day` e :ref:`elemento-month` com informação 00 para que seja alterada posteriormente com a data efetiva da publicação pela unidade de produção.
 * Para datas do tipo collection, sempre preencher a data ao qual o fascículo pertence, seguindo sua periodicidade.
 * Para revistas que adotam `publicação contínua (PC) <http://www.scielo.org/local/Image/guiarpass.pdf>`_, só considerar o ano ao qual o fascículo pertence para data do tipo collection.
