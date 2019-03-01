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

+-----------+-------------+
| Valor     | Descrição   |
+===========+=============+
| author    | autor       |
+-----------+-------------+
| compiler  | compilador  |
+-----------+-------------+


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
  * Utilizar *AACR2* - *Código de Catalogação Anglo Americano*, *Registro de ORCID* e/ou *Currículo Lattes* dos autores e avaliar formas de entrada autorizadas para nomes.
  * Outros tipos de contribuidores como tradutor, ilustrador, assistente de pesquisa, editor etc, devem ser identificados em :ref:`elemento-author-notes`, com :ref:`elemento-fn` e ``@fn-type ="other"``, para editor do artigo ou fascículo usar ``@fn-type ="edited-by"``.

  