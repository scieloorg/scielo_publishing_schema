.. _elemento-article-id:

<article-id>
============

Atributos obrigatórios:

  1. ``@pub-id-type``

+------------------------------+-------------------+
| Aparece em                   | Ocorre            |
+==============================+===================+
| :ref:`elemento-article-meta` | Uma ou mais vezes |
+------------------------------+-------------------+



Identificador único do artigo em uma base de dados.

O elemento deve, obrigatoriamente, apresentar o atributo ``@pub-id-type``, o qual é utilizado para nomear o tipo de identificador.

O atributo ``@pub-id-type`` permite os seguintes valores:

+--------------------+-------------------------------------------------------+
| Valor              | Descrição                                             |
+====================+=======================================================+
| doi                | *Digital Object Identifier*.                          |
+--------------------+-------------------------------------------------------+
| publisher-id       | Pode ser utilizado como identificador designado pela  |
|                    | Coleção *SciELO*.                                     |
+--------------------+-------------------------------------------------------+
| other              | Utilizado para ordenar documentos nas modalidades de  |
|                    | Publicação Contínua (PC) e *Ahead Of Print* (AOP).    |
+--------------------+-------------------------------------------------------+

Para *SciELO* Brasil consulte:

:ref:`scielo-brasil`



