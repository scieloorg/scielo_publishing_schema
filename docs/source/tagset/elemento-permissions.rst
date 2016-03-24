.. _elemento-permissions:

<permissions>
-------------

Aparece em
  :ref:`elemento-article-meta`, 
  :ref:`elemento-boxed-text`, 
  :ref:`elemento-disp-quote`, 
  :ref:`elemento-fig`,
  ``<graphic>``, 
  :ref:`elemento-media`, 
  :ref:`elemento-supplementary-material`, 
  :ref:`elemento-table-wrap`, 
  :ref:`elemento-verse-group`.

 
Ocorre
  Uma vez em :ref:`elemento-article-meta`

  Zero ou mais vezes nos demais elementos



A permissão é um conjunto de condições sob as quais o conteúdo do artigo 
pode ser usado, acessado e distribuído.


Tabela - :ref:`elemento-permissions` aparece em:

+---------------------------+---------------------------+---------------------------------------------------------+
| Objeto do Documento       | Elementos que podem       | O que a permissão                                       |
|                           | apresentar <permisssions> | envolve                                                 |
+===========================+===========================+=========================================================+
| Caixa de Texto            | <boxed-text>              | A própria tag                                           |
+---------------------------+---------------------------+---------------------------------------------------------+
| Citação                   | <disp-quote>              | A própria tag                                           |
+---------------------------+---------------------------+---------------------------------------------------------+
| Figura                    | <fig>                     | Toda a figura e arquivos relacionados                   |
+---------------------------+---------------------------+---------------------------------------------------------+
| Gráfico/Imagem            | <graphic>                 | O arquivo da imagem (`@xlink:href`) e sua descrição     |
+---------------------------+---------------------------+---------------------------------------------------------+
| Mídia                     | <media>                   | O arquivo mídia (`@xlink:href`) e sua descrição         |
+---------------------------+---------------------------+---------------------------------------------------------+
| Material Suplementar      | <supplementary-material>  | O arquivo suplementar e sua descrição                   |
+---------------------------+---------------------------+---------------------------------------------------------+
| Tabelas, legendas e notas | <table-wrap>              | A tabela, legenda, label e notas de rodapé de tabela    |
+---------------------------+---------------------------+---------------------------------------------------------+
| Grupo de Versos           | <verse-group>             | A própria tag                                           |
+---------------------------+---------------------------+---------------------------------------------------------+

