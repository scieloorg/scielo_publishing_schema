Regras de Nomeação de Arquivos
==============================

Nomeação de Pasta para Envio
----------------------------

Todos os arquivos, incluindo *XML*, *PDF* e imagens referentes ao número em questão devem estar na mesma pasta nomeada conforme o padrão abaixo:

Para Número:

    ``ISSN-acrônimo-volume-número``

Exemplo:

    ``0447-032X-rbcsr-30-01``

Para *Ahead Of Print* considerar:

    ``ISSN-acrônimo-lote``

O lote é composto pelo número do pacote (01, 02...12,13 etc) + os 2 (dois) dígitos finais do ano corrente.

Exemplo:

    ``0104-5970-hcsm-0315``

Arquivo XML
-----------

Para a nomeação de arquivos *XML* utilizar a estrutura determinada pelo :term:`SciELO PS`:

Para Número:

    ``ISSN``-``acrônimo``-``volume``-``número``-``paginação``

Exemplo:

    ``0037-8682-rsbmt-48-01-00033.xml``


Para Ahead-Of-Print:

    ``ISSN``-``acrônimo``-``NúmerodeDoiSemoPrefixo``

Exemplo:

    ``0104-5970-hcsm-2015005000011.xml``


Imagens
-------

<<<<<<< HEAD
Em imagens (que podem ser figuras, tabelas, equações, apêndices e etc), utilizar a seguinte estrutura de nomeação tanto para as que se encontram dentro do XML quanto para as da pasta do pacote do número ou lote de :term:`ahead-of-print`.
=======
Em imagens (que podem ser figuras, tabelas, equações, apêndices etc), utilizar a seguinte estrutura de nomeação tanto para as que se encontram dentro do XML quanto para as da pasta do pacote do número ou lote de :term:`ahead-of-print`.
>>>>>>> pack-3

Para Número:

    ``ISSN``-``acrônimo``-``volume``-``número``-``paginação``-``nomedaimagem.extensãodaimagem``

Exemplo:

    ``1807-5932-clin-69-05-0308-gf01.tif``


Para Ahead-Of-Print:

    ``ISSN``-``acrônimo``-``númerodedoisemoprefixo.extensãodaimagem``

Exemplo:

    ``0074-0276-mioc-00740276130057-gf01.tif``


Imagens traduzidas:

    ``ISSN``-``acrônimo``-``volume``-``número``-``paginação``-``nomedaimagem``-``idioma``.``extensãodaimagem``

Exemplo:

    ``0104-1169-rlae-23-01-00001-gf01-es.tif``

PDF
---

Os PDFs também devem seguir a estrutura de nomeação de arquivos determinada pelo :term:`SciELO PS`.

Para Número:

    ``ISSN``-``acrônimo``-``volume``-``número``-``paginação``

Exemplo:

    ``0102-0935-abmvz-67-01-00037.pdf``


Para Ahead Of Print:

    ``ISSN``-``acrônimo``-``NúmeroDoiSemoPrefixo``

Exemplo:

    ``1414-431X-bjmbr-1414-431X20154155.pdf``


PDFs traduzidos:

    ``ISSN``-``acrônimo``-``volume``-``número``-``paginação``-``idioma``

Exemplo:

    ``0104-1169-rlae-23-01-00003-es.pdf``


Casos Especiais
---------------

+-----------------------+----------------------------------------------------------------------------+--------------------------------------------+
|                       |                                                                            |                                            |
|    Tipo de Arquivo    |     Regra de Nomeação                                                      |             Exemplo                        |
|                       |     (.xml, .pdf e img)                                                     |                                            |
+=======================+============================================================================+============================================+
|                       |                                                                            |                                            |
|                       | ISSN-acronimo-vol-nº-``s+nºde ordem``-paginação (.xml)                     | 0066-782X-abc-101-06-``s1``-0001.xml       |
|                       |                                                                            |                                            |
| Suplemento de Número  | ISSN-acronimo-vol-nº-``s+nºde ordem``-paginação-nome da imagem (extensão)  | 0066-782X-abc-101-06-``s1``-0001-gf01.tif  |
|                       |                                                                            |                                            |
|                       | ISSN-acronimo-vol-nº-``s+nºde ordem``-paginação (.pdf)                     | 0066-782X-abc-101-06-``s1``-0001.pdf       |
|                       |                                                                            |                                            |
+-----------------------+----------------------------------------------------------------------------+--------------------------------------------+
|                       |                                                                            |                                            |
|                       | ISSN-acronimo-vol-``s+nºde ordem``-nº-paginação (.xml)                     | 0066-782X-rlpf-13-``s1``-0012.xml          |
|                       |                                                                            |                                            |
| Suplemento de volume  | ISSN-acronimo-vol-``s+nºde ordem``-paginação-nome da imagem (extensão)     | 0066-782X-rlpf-13-``s1``-0012-gf02.tif     |
|                       |                                                                            |                                            |
|                       | ISSN-acronimo-vol-``s+nºde ordem``-nº-paginação (.pdf)                     | 0066-782X-rlpf-13-``s1``-0012.pdf          |
|                       |                                                                            |                                            |
+-----------------------+----------------------------------------------------------------------------+--------------------------------------------+
|                       |                                                                            |                                            |
|                       | ISSN-acronimo-``nº``-paginação (.xml)                                      | 0101-4358-er-``55``-00189.xml              |
|                       |                                                                            |                                            |
| Número sem volume     | ISSN-acronimo-``nº``-paginação-nome da imagem (extensão)                   | 0101-4358-er-``55``-00189-gf1.jpg          |
|                       |                                                                            |                                            |
|                       | ISSN-acronimo-``nº``-paginação (.pdf)                                      | 0101-4358-er-``55``-00189.pdf              |
|                       |                                                                            |                                            |
+-----------------------+----------------------------------------------------------------------------+--------------------------------------------+
|                       |                                                                            |                                            |
|                       | ISSN-acronimo-vol-``spe``-paginação (.xml)                                 | 1984-0292-fractal-26-``spe``-0645.xml      |
|                       |                                                                            |                                            |
| Volume especial       | ISSN-acronimo-vol-``spe``-paginação-nome da imagem (extensão)              | 1984-0292-fractal-26-``spe``-0645-gf01.tif |
|                       |                                                                            |                                            |
|                       | ISSN-acronimo-vol-``spe``-paginação (.pdf)                                 | 1984-0292-fractal-26-``spe``-0645.pdf      |
|                       |                                                                            |                                            |
+-----------------------+----------------------------------------------------------------------------+--------------------------------------------+
|                       |                                                                            |                                            |
|                       | ISSN-acronimo-nº-``spe``-paginação (.xml)                                  | 0101-4358-er-04-``spe``-00015.xml          |
|                       |                                                                            |                                            |
| Número especial       | ISSN-acronimo-nº-``spe``-paginação-nome da imagem (extensão)               | 0101-4358-er-04-``spe``-00015-gf1.png      |
|                       |                                                                            |                                            |
|                       | ISSN-acronimo-nº-``spe``-paginação (.pdf)                                  | 0101-4358-er-04-``spe``-00015.pdf          |
+-----------------------+----------------------------------------------------------------------------+--------------------------------------------+
|                       |                                                                            |                                            |
| Arquivo com           | ISSN-acronimo-vol-nº-paginação-``suppl + nº de ordem``                     | 1983-3083-refuem-24-03-0316-``suppl01``.pdf|
| Material Suplementar  |                                                                            |                                            |
+-----------------------+----------------------------------------------------------------------------+--------------------------------------------+
|                       |                                                                            |                                            |
| Arquivo com           | ISSN-acronimo-vol-nº-paginação-``app + nº de ordem``                       | 1983-3083-refuem-24-03-0316-``app01``.pdf  |
| Apêndice              |                                                                            |                                            |
+-----------------------+----------------------------------------------------------------------------+--------------------------------------------+


.. note:: Cada item deve ser separado por um hífen e deve, obrigatoriamente, manter visível a extensão da imagem após o "ponto", optando, preferencialmente, por imagens em formato *tif*.


.. important::
    +---------------------+---------------------------------------------------------+
    | *ISSN:*             | Se houver mais de um, dar preferência ao impresso.      |
    +---------------------+---------------------------------------------------------+
    | *Acrônimo:*         | Sigla do periódico na SciELO                            |
    +---------------------+---------------------------------------------------------+
    | *Volume:*           | Volume do número                                        |
    +---------------------+---------------------------------------------------------+
    | *Número:*           | Número ou suplemento do número                          |
    +---------------------+---------------------------------------------------------+
    | *Paginação:*        | Manter a informação da primeira página                  |
    +---------------------+---------------------------------------------------------+
    | *Nome da imagem:*   | Prefixo com uma numeração sequencial                    |
    |                     | (ver :ref:`sugestao-atribuicao-id`)                     |
    +---------------------+---------------------------------------------------------+
    | *Extensão:*         | As extensões aceitas pela SciELO são: .tif, .jpg, .jpeg,|
    |                     | .gif, .png e/ou eps.                                    |
    +---------------------+---------------------------------------------------------+


.. {"reviewed_on": "20160630", "by": "gandhalf_thewhite@hotmail.com"}
