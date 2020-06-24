Codificação e caracteres especiais
==================================

A especificação :term:`SciELO PS` exige que os documentos :term:`XML` estejam codificados em :term:`UTF-8`, e que tenham indicada esta codificação na :term:`Declaração do XML`.

   ``<?xml version="1.0" encoding="utf-8"?>``


Caracteres especiais, quando utilizados, devem ser inseridos diretamente no documento ou por meio de referências numéricas em notação hexadecimal. Por exemplo, o caractere sigma maiúsculo deve ser representado por ``Σ`` ou ``&#x03A3;``.

.. note:: *SciELO PS* recomenda o uso de caracteres inseridos diretamente no XML em vez de notação hexadecimal.

Não é permitido o uso de referências a caracteres de uso privado da tabela :term:`Unicode` contidas no intervalo ``xE000 – xF8FF``.

Entidades :term:`XML` também são aceitas e devem ser utilizadas para representar os caracteres desejados:

+-----------+----------+------------------------------------------------------+
| Caractere | Entidade | Descrição                                            |
+===========+==========+======================================================+
| "         | &quot;   | Aspas como valor de atributo de elemento no XML.     |
+-----------+----------+------------------------------------------------------+
| '         | &apos;   | Apóstrofo como valor de atributo de elemento no XML. |
+-----------+----------+------------------------------------------------------+
| &         | &amp;    | & como valor de atributo ou texto de elemento no XML.|
+-----------+----------+------------------------------------------------------+
| <         | &lt;     | < como valor de atributo ou texto de elemento no XML.|
+-----------+----------+------------------------------------------------------+
| >         | &gt;     | > como valor de atributo ou texto de elemento no XML.|
+-----------+----------+------------------------------------------------------+

Para maiores informações ver a `tabela Unicode <https://unicode-table.com/en/>`_.


.. {"reviewed_on": "20160729", "by": "gandhalf_thewhite@hotmail.com"}
