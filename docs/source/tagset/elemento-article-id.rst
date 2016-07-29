.. _elemento-article-id:

<article-id>
^^^^^^^^^^^^

Aparece em:

  :ref:`elemento-article-meta`

Atributos obrigatórios:

  1. ``@pub-id-type``

Ocorre:

  Uma ou mais vezes


Identificador único do :term:`documento` em uma base de dados.
O elemento deve, obrigatoriamente, apresentar o atributo ``@pub-id-type``, o qual é utilizado para nomear o tipo de identificador.

O atributo ``@pub-id-type`` permite os seguintes valores:

+--------------------+----------------------------------------------------------+
| Valor              | Descrição                                                |
+====================+==========================================================+
| doi                | *Digital Object Identifier*: Identificador único para    |
|                    | documentos de *SciELO Brasil*.                           |
+--------------------+----------------------------------------------------------+
| publisher-id       | Pode ser utilizado como identificador único para         |
|                    | documentos sem *DOI* (Rede SciELO).                      |
+--------------------+----------------------------------------------------------+
| other              | Utilizado para ordenar documentos *Rolling Pass* e       |
|                    | *Ahead Of Print*.                                        |
+--------------------+----------------------------------------------------------+

Para *SciELO Brasil* é obrigatório o uso de ``@pub-id-type=”doi”`` como identificador único do documento.

Exemplo:

.. code-block:: xml

    ...
    <article-meta>
        ...
        <article-id pub-id-type="doi">10.1590/0074-0276130047</article-id>
        ...
    </article-meta>
    ...


.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
