.. _elemento-table-wrap-foot:

<table-wrap-foot>
^^^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-table-wrap`

Ocorre
  Zero ou mais vezes


Em ``<table-wrap-foot>`` é possível fazer a identificação de nota de rodapé de 
tabela por meio de tags :ref:`elemento-fn`, que devem apresentar obrigatoriamente o 
atributo ``@id``.
 
Consulte a :ref:`sugestao-atribuicao-id` para instruções sobre a composição do 
atributo ``@id``.
 
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
 
