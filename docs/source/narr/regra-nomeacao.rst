Regras de Nomeação de Arquivos
==============================

Para envio de pacotes XML é necessário seguir as instruções do `Guia de Entrega de Pacote para Publicação em SciELO <http://www.scielo.org/local/File/Entrega_de_Pacote_para_Publicacao.pdf>`_ . Está documentado as seguintes regras de nomeação:


    * :ref:`elemento-regra-exemplo-1`
    * :ref:`elemento-regra-exemplo-2`
    * :ref:`elemento-regra-exemplo-3`


.. important::
    +---------------------+----------------------------------------------------+
    | *ISSN:*             | Número do periódico registrado no ISSN. (Se houver |
    |                     | mais de um, dar preferência ao eletrônico)         |
    +---------------------+----------------------------------------------------+
    | *Acrônimo:*         | Sigla do periódico na SciELO                       |
    +---------------------+----------------------------------------------------+
    | *Volume:*           | v= volume do fascículo                             |
    +---------------------+----------------------------------------------------+
    | *Número:*           | n= Número do fascículo                             |
    +---------------------+----------------------------------------------------+
    | *Número especial:*  | nspe = Número especial do fascículo                |
    +---------------------+----------------------------------------------------+
    | *Suplemento:*       | s = Suplemento do fascículo                        |
    +---------------------+----------------------------------------------------+
    | *Paginação:*        | Informação da primeira página do artigo            |
    +---------------------+----------------------------------------------------+
    | *Elocation:*        | Paginação eletrônica do artigo                     |
    +---------------------+----------------------------------------------------+
    | *Nome da imagem:*   | Prefixo com uma numeração sequencial (ver          |
    |                     | :ref:`sugestao-atribuicao-id`)                     |
    +---------------------+----------------------------------------------------+
    | *Extensão:*         | As extensões aceitas pela SciELO são: .tif, .jpg,  |
    |                     | .png e svg.                                        | 
    +---------------------+----------------------------------------------------+
    | *DOI:*              | Sistema de identificação de objetos digitais       |                                   
    +---------------------+----------------------------------------------------+


.. note:: 
 * Deve-se sempre usar traço sem espaço para separação dos itens.
 * Nunca usar underline para nomeação de pastas ou arquivos.
 * Usado dados fictícios para criação dos exemplos:  "scie" como acrônimo de periódico e "0124-4567" para número de ISSN.



.. _elemento-regra-exemplo-1:

Nomeação de pastas
------------------

Todos os arquivos de um pacote, incluindo XML, PDF, imagens, mídias e material suplementar, caso existam, devem estar na mesma pasta nomeada conforme o padrão. 


Exemplos:

    * :ref:`elemento-regranomeia-exemplo-1`
    * :ref:`elemento-regranomeia-exemplo-2`
    * :ref:`elemento-regranomeia-exemplo-3`
    * :ref:`elemento-regranomeia-exemplo-4`
    * :ref:`elemento-regranomeia-exemplo-5`
    * :ref:`elemento-regranomeia-exemplo-6`
    * :ref:`elemento-regranomeia-exemplo-7`
    * :ref:`elemento-regranomeia-exemplo-8`
    * :ref:`elemento-regranomeia-exemplo-9`



.. _elemento-regranomeia-exemplo-1:

Regra para volume e número
^^^^^^^^^^^^^^^^^^^^^^^^^^

scie v10n3

Regra:

    ``ISSN-acrônimo-volume-número``

Exemplo:

    ``0124-4567-scie-10-03``



.. _elemento-regranomeia-exemplo-2:

Regra para volume sem número
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

scie v10

Regra:

    ``ISSN-acrônimo-número``

Exemplo:

    ``0124-4567-scie-10``



.. _elemento-regranomeia-exemplo-3:

Regra para número sem volume
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

scie n03

Regra:

    ``ISSN-acrônimo-número``

Exemplo:

    ``0124-4567-scie-03``



.. _elemento-regranomeia-exemplo-4:

Para publicação de número especial
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

scie v10nspe01

Regra:

    ``ISSN-acrônimo-volume-spe + nº de ordem``

Exemplo:

    ``0124-4567-scie-10-spe01``



.. _elemento-regranomeia-exemplo-5:

Para publicação de suplemento de volume
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

scie v10s01

Regra:

    ``ISSN-acrônimo-volume-s + nº de ordem``

Exemplo:

    ``0124-4567-scie-10-s01``



.. _elemento-regranomeia-exemplo-6:

Para publicação de suplemento de número
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

scie v10n03s01

Regra:

    ``ISSN-acrônimo-volume-número-s + nº de ordem``

Exemplo:

    ``0124-4567-scie-10-03-s01``


.. _elemento-regranomeia-exemplo-7:

Regra para *Ahead Of Print*
^^^^^^^^^^^^^^^^^^^^^^^^^^^

scie nahead2018 lote 01

Regra:

    ``ISSN-acrônimo-nahead-nº lote``

Exemplo:

    ``0124-4567-scie-nahead0118``


* Para lote, usar regra de dois dígitos sequenciais, 01, 02, 03 etc, mais dois últimos dígitos do ano de publicação: primeiro lote 01 de 2018 = lote 0118


.. _elemento-regranomeia-exemplo-8:

Regra para Publicação Contínua com um volume ao ano
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

scie v41 lote 01

Regra:

    ``ISSN-acrônimo-volume-nº lote``

Exemplo:

    ``0124-4567-scie-41-01``


* Para lote, usar regra de dois dígitos sequenciais, 01, 02, 03 etc.



.. _elemento-regranomeia-exemplo-9:

Regra para Publicação Contínua com um volume e número
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

scie v41n02 lote 01

Regra:

    ``ISSN-acrônimo-volume-nº lote``

Exemplo:

    ``0124-4567-scie-41-02-01``


* Para lote, usar regra de dois dígitos sequenciais, 01, 02, 03 etc.




.. _elemento-regra-exemplo-2:

Nomeação de arquivos
--------------------

Todos os arquivos de um pacote, incluindo XML, PDF, imagens, mídias e material suplementar, caso existam, devem estar com nomeação padrão.


Exemplos:

    * :ref:`elemento-nomeia-arquivo-exemplo-1`
    * :ref:`elemento-nomeia-arquivo-exemplo-2`
    * :ref:`elemento-nomeia-arquivo-exemplo-3`
    * :ref:`elemento-nomeia-arquivo-exemplo-4`
    * :ref:`elemento-nomeia-arquivo-exemplo-5`
    * :ref:`elemento-nomeia-arquivo-exemplo-6`
    * :ref:`elemento-nomeia-arquivo-exemplo-7`
    * :ref:`elemento-nomeia-arquivo-exemplo-8`
    * :ref:`elemento-nomeia-arquivo-exemplo-9`


.. _elemento-nomeia-arquivo-exemplo-1:

Regra para volume e número
^^^^^^^^^^^^^^^^^^^^^^^^^^

Regra:

    ``ISSN-acrônimo-volume-número-paginação``

Exemplo:

    ``0124-4567-scie-10-03-365``



.. _elemento-nomeia-arquivo-exemplo-2:

Regra para volume sem número
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Regra:

    ``ISSN-acrônimo-volume-paginação``

Exemplo:

    ``0124-4567-scie-10-365``



.. _elemento-nomeia-arquivo-exemplo-3:

Regra para número sem volume
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Regra:

    ``ISSN-acrônimo-número-paginação``

Exemplo:

    ``0124-4567-scie-03-365``



.. _elemento-nomeia-arquivo-exemplo-4:

Para publicação de número especial
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Regra:

    ``ISSN-acrônimo-volume-spe + nº de ordem-paginação``

Exemplo:

    ``0124-4567-scie-10-spe01-365``



.. _elemento-nomeia-arquivo-exemplo-5:

Para publicação de suplemento de volume
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Regra:

    ``ISSN-acrônimo-volume-s + nº de ordem-paginação``

Exemplo:

    ``0124-4567-scie-10-s01-365``


.. _elemento-nomeia-arquivo-exemplo-6:

Para publicação de suplemento de número
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

scie v10n03s01

Regra:

    ``ISSN-acrônimo-volume-número-s + nº de ordem-paginação``

Exemplo:

    ``0124-4567-scie-10-03-s01-365``



.. _elemento-nomeia-arquivo-exemplo-7:

Regra para *Ahead Of Print*
^^^^^^^^^^^^^^^^^^^^^^^^^^^

Regra:

    ``ISSN-acrônimo-número doi sem prefixo``

Exemplo:

    ``0124-4567-scie-S0123-45672018050``


* DOI completo = 10.1590/S0123-45672018050. Mais informações consultar `Orientação para criação e apresentação do DOI <http://www.scielo.org/local/File/Orientacao_para_criacao_e_apresentacao_do_DOI.pdf>`_ .


.. _elemento-nomeia-arquivo-exemplo-8:

Regra para Publicação Contínua com um volume ao ano
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Regra:

    ``ISSN-acrônimo-volume-elocation``

Exemplo:

    ``0124-4567-scie-41-01-e0123``



.. _elemento-nomeia-arquivo-exemplo-9:

Regra para Publicação Contínua com um volume e número
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Regra:

    ``ISSN-acrônimo-volume-elocation``

Exemplo:

    ``0124-4567-scie-41-02-01-e234``




.. _elemento-regra-exemplo-3:

Nomeação para casos especiais
-----------------------------


Alguns artigos podem conter documentos adicionais. Para estes, as regras devem seguir a nomeação dos fascículos ao qual estão inseridos, com volume, publicação contínua etc (descrito como XXXXX nos exemplos) mais as informações que seguem:


Exemplos:

    * :ref:`elemento-nomeia-especial-exemplo-1`
    * :ref:`elemento-nomeia-especial-exemplo-2`


.. _elemento-nomeia-especial-exemplo-1:


Regra para arquivo com material suplementar
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Regra:

    ``ISSN-acrônimo-XXXXX-paginação ou elocation-suppl + nº de ordem``

Exemplo:

    ``0124-4567-scie-XXXXX-e0123-suppl01``



.. _elemento-nomeia-especial-exemplo-2:


Regra para arquivo com apêndice
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Regra:

    ``ISSN-acrônimo-XXXXX-paginação ou elocation-app + nº de ordem``

Exemplo:

    ``0124-4567-scie-XXXXX-365-appl01``






