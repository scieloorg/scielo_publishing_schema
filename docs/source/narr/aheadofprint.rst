.. _ahead-of-print:

Ahead Of Print
==============

*Ahead of Print* (AOP) são artigos publicados separadamente antes da composição dos números e por este motivo não apresentam volume, número nem paginação, portanto, os elementos :ref:`elemento-volume`, :ref:`elemento-issue`, :ref:`elemento-fpage` e :ref:`elemento-lpage` ou :ref:`elemento-elocation-id` não devem ser utilizados.

A data de publicação deste tipo de dpcumento sempre será compostas por :ref:`elemento-day`, :ref:`elemento-month` e :ref:`elemento-year` e o atributo ``@date-type`` em :ref:`elemento-pub-date` sempre terá o valor de publicação eletrônica em SciELO do tipo "pub" mais o atributo ``@publication-format`` com o valor "electronic".


Exemplo:

.. code-block:: xml

    <article article-type="research-article" dtd-version="1.0" specific-use="sps-1.8" xml:lang="pt" xmlns:mml="http://www.w3.org/1998/Math/MathML" xmlns:xlink="http://www.w3.org/1999/xlink">
     ...
    <article-categories>
       <subj-group subj-group-type="heading">
           <subject>Artigo Original</subject>
       </subj-group>
    </article-categories>
     ...
       <pub-date publication-format="electronic" date-type="pub">
         <day>17</day>
         <month>02</month>
         <year>2019</year>
       </pub-date>
     ...
    </article>


.. note::
 * Quem determina a data específica de publicação em SciELO é a unidade de produção, no entanto a inserção dos elementos :ref:`elemento-day`, :ref:`elemento-month` e :ref:`elemento-year` são obrigatórios, portanto pode ser inserido qualquer data.
 * Em AOP não é permitido o uso de :ref:`elemento-season` em :ref:`elemento-pub-date`.
 * O valor de ``article-type`` em :ref:`elemento-article` deve corresponder ao tipo de documento que está sendo publicado e não pode ser alterado quando o AOP entrar em um fascículo.
 * A seção descrita em ``subject`` pode ser variável entre a versão AOP e a versão final no fascículo.
 * Mais informações podem ser obtidas no `Guia para a publicação avançada de artigos Ahead of Print (AOP) no SciELO <http://www.scielo.org/local/File/Guia_AOP.pdf>`_ .



