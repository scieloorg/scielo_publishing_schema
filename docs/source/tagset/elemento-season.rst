.. _elemento-season:

<season>
========

+----------------------------------+-----------------+
| Aparece em                       | Ocorre          |
+==================================+=================+
| :ref:`elemento-element-citation` | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-product`          | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-pub-date`         | Zero ou uma vez |
+----------------------------------+-----------------+



Este elemento pode ser encontrado em :ref:`elemento-pub-date` para identificação de intervalo de meses do ano (ver nota informativa) e em :ref:`elemento-element-citation` e :ref:`elemento-product`) para identificação de estação do ano em uma referência bibliográfica.

Exemplos:

    * :ref:`elemento-season-exemplo-1`
    * :ref:`elemento-season-exemplo-2`


.. _elemento-season-exemplo-1:

Exemplo de ``<season>`` como estações do ano:
---------------------------------------------

.. code-block:: xml

    ...
    <back>
        ...
        <ref-list>
            <ref>
                ...
                <season>Outono</season>
                ...
            </ref>
        </ref-list>
        ...
    </back>


.. _elemento-season-exemplo-2:

Exemplo de ``<season>`` como intervalo de meses:
------------------------------------------------

.. code-block:: xml

    ...
    <front>
        ...
        <article-meta>
            ...
            <pub-date publication-format="electronic" date-type="collection">
              <season>Jan-Feb</season>
              <year>2018</year>
            </pub-date>
            ...
        </article-meta>
        ...
    </front>
    ...


.. note:: Para abreviatura dos meses em um intervalo, deve-se utilizar a abreviatura dos mesmos em inglês, com 3 caracteres, separados por hífen. As abreviaturas são: ``Jan``, ``Feb``, ``Mar``, ``Apr``, ``May``, ``Jun``, ``Jul``, ``Aug``, ``Sep``, ``Oct``, ``Nov`` e ``Dec``.


.. {"reviewed_on": "20160729", "by": "gandhalf_thewhite@hotmail.com"}
