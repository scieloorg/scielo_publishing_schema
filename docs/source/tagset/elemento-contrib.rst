.. _elemento-contrib:
 
<contrib>
^^^^^^^^^

Aparece em
  :ref:`elemento-contrib-group`
 
Atributos obrigatórios
  1. contrib-type
 
Ocorre
  Uma ou mais vezes


Em ``<contrib>`` especifica-se o indivíduo ou instituição que contribuiu para 
o artigo. Pode ser anônimo ou ter um ou vários autores, inclusive autores 
institucionais. Tags como :ref:`elemento-name`, :ref:`elemento-collab`, :ref:`elemento-on-behalf-of`, 
:ref:`elemento-xref`, :ref:`elemento-role` e ``<anonymous>`` podem ser encontradas neste elemento. 
 
O atributo ``@contrib-type`` pode possuir os valores:

+------------+----------------------------------------------------------------+
| Valor      | Descrição                                                      |
+============+================================================================+
| author     | Autor do conteúdo                                              |
+------------+----------------------------------------------------------------+
| compiler   | Compilador - pessoa que montou um trabalho composto de várias  |
|            | fontes                                                         |
+------------+----------------------------------------------------------------+
| editor     | Editor do conteúdo                                             |
+------------+----------------------------------------------------------------+
| translator | Tradutor do conteúdo                                           |
+------------+----------------------------------------------------------------+

 
Exemplo:
 
.. code-block:: xml
 
    ...
    <contrib-group>
        <contrib contrib-type="author">
            <name>
                <surname>Freitas</surname>
                <given-names>Ismael Forte</given-names>
                <suffix>Júnior</suffix>
            </name>
            <xref ref-type="aff" rid="aff01">1</xref>
        </contrib>
        ...
    </contrib-group>
    ...
 
.. note:: 
  * Observar normas para entrada de nomes (*AACR2* - Código de Catalogação
    Anglo Americano e/ou Currículo Lattes dos autores, avaliar formas de entrada autorizadas).
  * Para artigos que apresentam assinatura, como editoriais, apresentação etc. 
    repetir autores de <sig-block> em front/contrib caso não exista informação de autor.
  * Em ``contrib`` o :ref:`elemento-name` ocorre Zero ou Uma vez.
