.. _elemento-funding-source:

<funding-source>
================

Aparece em:

  :ref:`elemento-award-group`

Ocorre:

  Uma ou mais vezes


Elemento contido em :ref:`elemento-award-group` onde deve ser especificado o órgão e/ou instituição financiadora, caso exista.

Exemplo:

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
