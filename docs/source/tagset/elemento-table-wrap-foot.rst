.. _elemento-table-wrap-foot:

<table-wrap-foot>
=================

+----------------------------+-----------------+
| Aparece em                 | Ocorre          |
+============================+=================+
| :ref:`elemento-table-wrap` | Zero ou uma vez |
+----------------------------+-----------------+



``<table-wrap-foot>`` permite identificar uma nota de rodapé de tabela por meio de elementos do tipo :ref:`elemento-fn`.

A nota de rodapé poderá ser relacionada com alguma informação no corpo da tabela.

Exemplo:

.. code-block:: xml

    ...
    <table-wrap id="t01">
        <label>Table 1</label>
        <caption>
            <title>Título da tabela.</title>
        </caption>
        <table>
            ...
        </table>
        <table-wrap-foot>
            <fn id="TFN01">
                <label>*</label>
                <p>text</p>
            </fn>
        </table-wrap-foot>
    </table-wrap>
    ...


.. {"reviewed_on": "20170901", "by": "carolina.tanigushi@scielo.org"}
