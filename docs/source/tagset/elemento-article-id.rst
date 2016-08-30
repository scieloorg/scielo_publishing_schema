.. _elemento-article-id:

<article-id>
============

Aparece em:

  :ref:`elemento-article-meta`

Atributos obrigatórios:

  1. ``@pub-id-type``

Ocorre:

  Uma ou mais vezes


Identificador único do artigo em uma base de dados.

O elemento deve, obrigatoriamente, apresentar o atributo ``@pub-id-type``, o qual é utilizado para nomear o tipo de identificador.

O atributo ``@pub-id-type`` permite os seguintes valores:

+--------------------+----------------------------------------------------------+
| Valor              | Descrição                                                |
+====================+==========================================================+
| doi                | *Digital Object Identifier*.                             |
+--------------------+----------------------------------------------------------+
| publisher-id       | Pode ser utilizado como identificador designado pela     |
|                    | Coleção *SciELO*.                                        |
+--------------------+----------------------------------------------------------+
| other              | Utilizado para ordenar documentos *Rolling Pass* e       |
|                    | *Ahead Of Print* (Para uso durante o período de migração |
|                    | de tecnologia).                                          |
+--------------------+----------------------------------------------------------+

Para *SciELO Brasil* é obrigatório o uso de ``@pub-id-type=”doi”`` como identificador único do artigo.

Exemplo:

.. code-block:: xml

    ...
    <article-meta>
        ...
        <article-id pub-id-type="doi">10.1590/0074-0276130047</article-id>
        ...
    </article-meta>
    ...


.. {"reviewed_on": "20160803", "by": "gandhalf_thewhite@hotmail.com"}
