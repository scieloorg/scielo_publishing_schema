Codificação e caracteres especiais
==================================

A especificação SciELO PS exige que os documentos :term:`XML` estejam codificados 
em :term:`UTF-8`, e que declarem esta codificação na :term:`Declaração do XML`::

  <?xml version="1.0" encoding="utf-8"?>


Caracteres especiais devem ser inseridos ou diretamente no documento ou por meio 
de referências numéricas em hexadecimal. Por exemplo, o caractere sigma maiúsculo 
deverá ser representado por ``Σ`` ou ``&#x03A3``.

Não é permitido o uso de referências à caracteres de uso privado da tabela 
Unicode. Estes são os caracteres cujas referências estão contidas no 
intervalo ``xE000 – xF8FF``.

Entidades XML também são aceitas e devem ser utilizadas para representar os
caracteres:

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

Verifique no link abaixo a tabela de caracteres Unicode:

<http://unicode-table.com/en/>