.. _elemento-contrib:

<contrib>
=========

Aparece em:

  :ref:`elemento-contrib-group`

Atributos obrigatórios:

  1. ``@contrib-type``

Ocorre:

  Uma ou mais vezes


Identifica dados individuais, de grupo ou institucionais, de contribuintes do artigo, podendo ser inclusive anônimos. :ref:`elemento-name`, :ref:`elemento-collab`, :ref:`elemento-on-behalf-of`, :ref:`elemento-xref`, :ref:`elemento-role` e ``<anonymous>`` podem ser encontrados neste elemento.

O atributo ``@contrib-type`` define o tipo de contribuição e pode ter os valores:

+------------+----------------------------------------------------------------+
| Valor      | Descrição                                                      |
+============+================================================================+
| author     | Autor do conteúdo.                                             |
+------------+----------------------------------------------------------------+
| compiler   | Compilador - Indivíduo que compilou o conteúdo a partir de     |
|            | várias fontes.                                                 |
+------------+----------------------------------------------------------------+
| editor     | Editor do conteúdo.                                            |
+------------+----------------------------------------------------------------+
| translator | Tradutor do conteúdo.                                          |
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
  * Utilizar *AACR2* - *Código de Catalogação Anglo Americano* e/ou *Currículo Lattes* dos autores e avaliar formas de entrada autorizadas para nomes.
  * Para artigos que apresentam assinatura, - como editoriais, apresentação etc., repetir autores de ``<sig-block>`` em ``front/contrib`` caso não exista tal informação.
  * Em ``contrib`` o elemento :ref:`elemento-name` pode ou não ocorrer.


.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
