.. _elemento-funding-source:

<funding-source>
================

+-----------------------------+-------------------+
| Aparece em                  | Ocorre            |
+=============================+===================+
| :ref:`elemento-award-group` | Uma ou mais vezes |
+-----------------------------+-------------------+



Elemento onde deve ser especificado o órgão ou instituição financiadora.

Exemplos:

  * :ref:`elemento-fundingsource-exemplo-1`
  * :ref:`elemento-fundingsource-exemplo-2`


.. _elemento-fundingsource-exemplo-1:

Exemplo de 1 ``<funding-source>`` para 1 ``<award-id>`` :
-------------------------------------------------------------------

.. code-block:: xml

    ...
    <article-meta>
        ...
        <funding-group>
            <award-group>
                <funding-source>CNPq</funding-source>
                <award-id>1685X6-7</award-id>
            </award-group>
        </funding-group>
        ...
    </article-meta>
    ...



.. _elemento-fundingsource-exemplo-2:

Exemplo de 2 ``<funding-source>`` para 1 ``<award-id>`` :
-------------------------------------------------------------------

Um mesmo número de contrato pode ter mais de uma instituição financiadora.

Exemplo:

.. code-block:: xml

    ...
    <article-meta>
       ...
       <funding-group>
          <award-group>
             <funding-source>CNPq</funding-source>
             <funding-source>FAPESP</funding-source>
             <award-id>#09/06953-4</award-id>
          </award-group>
       </funding-group>
       ...
    </article-meta>
    ...


.. {"reviewed_on": "20160625", "by": "gandhalf_thewhite@hotmail.com"}
