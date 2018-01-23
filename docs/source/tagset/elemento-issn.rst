.. _elemento-issn:

<issn>
======

Atributos obrigatórios (em :ref:`elemento-front`):

  1. ``@pub-type='ppub'`` ou ``@pub-type='epub'``

+----------------------------------+-------------------+
| Aparece em                       | Ocorre            |
+==================================+===================+
| :ref:`elemento-journal-meta`     | Uma ou mais vezes |
+----------------------------------+-------------------+
| :ref:`elemento-element-citation` | Uma ou mais vezes |
+----------------------------------+-------------------+



:term:`ISSN` é um código numérico, único, que identifica uma publicação seriada definida pela norma :term:`ISO 3297:2007`.

Normalmente, cada tipo de suporte utilizado pelo periódico implica em um código ISSN específico.

Também se pode encontrar esta informação em :ref:`elemento-back` dentro de :ref:`elemento-element-citation` nas referências, mas não se faz uso de  nenhum atributo neste caso.

.. note:: Pode-se consultar o :ref:`arquivo de metadados dos periódicos <journal-meta-csv>` como referência na identificação dos elementos.

Os valores permitidos  ``@pub-type`` são:

+-------+-------------------------+
| Valor | Descrição               |
+=======+=========================+
| ppub  | ISSN da versão impressa |
+-------+-------------------------+
| epub  | ISSN da versão digital  |
+-------+-------------------------+

Caso estejam disponíveis, ambos ISSNs deverão ser identificados.


Exemplos:

 * :ref:`elemento-issn-exemplo-1`
 * :ref:`elemento-issn-exemplo-2`


.. _elemento-issn-exemplo-1:

Exemplo de ISSN em ``<journal-meta>``:
--------------------------------------

.. code-block:: xml

    ...
    <journal-meta>
        ...
        <issn pub-type="epub">1808-8686</issn>
        <issn pub-type="ppub">1808-8694</issn>
        ...
    </journal-meta>
    ...


.. _elemento-issn-exemplo-2:

Exemplo de ISSN em ``<element-citation>``:
------------------------------------------

.. code-block:: xml

  ...
    <element-citation publication-type="journal">
       ...
      <source>Chronic Respiratory Disease</source>
      <volume>vol. 1</volume>
      <year>2004</year>
      <issn>1479-9723</issn>
    </element-citation>
  ...


.. {"reviewed_on": "20160626", "by": "gandhalf_thewhite@hotmail.com"}
