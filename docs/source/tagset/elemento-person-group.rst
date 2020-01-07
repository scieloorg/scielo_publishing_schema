.. _elemento-person-group:

<person-group>
==============

Atributos obrigatórios:

  1. ``@person-group-type``

+----------------------------------+--------------------+
| Aparece em                       | Ocorre             |
+==================================+====================+
| :ref:`elemento-element-citation` | Zero ou mais vezes |
+----------------------------------+--------------------+
| :ref:`elemento-product`          | Zero ou mais vezes |
+----------------------------------+--------------------+


Identifica grupo ou indivíduo criador/elaborador do :term:`documento`. Caso existam, os elementos :ref:`elemento-collab`, :ref:`elemento-role`, :ref:`elemento-name` e :ref:`elemento-etal`, somente devem ser identificados em ``<person-group>``.

Os valores possíveis para ``@person-group-type`` são:

+--------------------+----------------------------------------------------------------+
| Valor              | Descrição                                                      |
+====================+================================================================+
| author             | Autor do conteúdo.                                             |
+--------------------+----------------------------------------------------------------+
| compiler           | Adaptador - Indivíduo que compilou o conteúdo a partir de      |
|                    | várias fontes.                                                 |
+--------------------+----------------------------------------------------------------+
| editor             | Editor do artigo ou fascículo.                                 |
+--------------------+----------------------------------------------------------------+
| illustrator        | Ilustrador do conteúdo.                                        |
+--------------------+----------------------------------------------------------------+
| translator         | Tradutor do conteúdo.                                          |
+--------------------+----------------------------------------------------------------+
| research-assistant | Assistente de pesquisa do artigo.                              |
+--------------------+----------------------------------------------------------------+


Exemplo:

.. code-block:: xml

    ...
    <ref>
        <element-citation publication-type="book">
            <person-group person-group-type="author">
                <name>
                    <surname>Silva</surname>
                    <given-names>Jaqueline Figueiredo da</given-names>
                </name>
                <collab>Instituto Brasil Leitor</collab>
                ...
            </person-group>
            ...
        </element-citation>
        ...
    </ref>
    ...

.. note::
  * Recomendamos utilizar Registro de :term:`ORCID` e/ou *Currículo Lattes* dos autores para 
    avaliar formas de entrada para nomes.

  