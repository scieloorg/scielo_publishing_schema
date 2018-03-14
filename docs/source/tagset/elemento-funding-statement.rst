.. _elemento-funding-statement:

<funding-statement>
===================

+-------------------------------+-----------------+
| Aparece em                    | Ocorre          |
+===============================+=================+
| :ref:`elemento-funding-group` | Zero ou uma vez |
+-------------------------------+-----------------+



Contém os dados de financiamento exatamente como apresentado na nota de rodapé.

Este elemento só deverá ser inserido quando as informações de financiamento forem apresentadas em :ref:`elemento-fn`.

Exemplo:

.. code-block:: xml

    <front>
        ...
        <article-meta>
            ...
            <kwd-group>
                ...
            </kwd-group>
            <funding-group>
                <award-group>
                    <funding-source>Coordenação de Aperfeiçoamento de Pessoal de Nível Superior</funding-source>
		    <funding-source> Fundação de Amparo à Pesquisa do Estado de São Paulo</funding-source>
                    <award-id>04/08142-0</award-id>
                </award-group>
                <funding-statement>This study was supported in part by Coordenação
                de Aperfeiçoamento de Pessoal de Nível Superior (Capes — Brasília,
                Brazil), Fundação de Amparo à Pesquisa do Estado de São Paulo (FAPESP —
                Grant no. 04/08142-0; São Paulo, Brazil)</funding-statement>
            </funding-group>
            ...
        </article-meta>
        ...
    </front>
    ...
    <back>
        ...
        <fn-group>
            <fn id="fn01" fn-type="financial-disclosure">
                <p>This study was supported in part by Coordenação de Aperfeiçoamento
                de Pessoal de Nível Superior (Capes — Brasília, Brazil), Fundação
                de Amparo à Pesquisa do Estado de São Paulo (FAPESP —
                Grant no. 04/08142-0; São Paulo, Brazil)</p>
            </fn>
        </fn-group>
        ...
    </back>


.. note:: Nota de financiamento COM NÚMERO DE CONTRATO, deve ser identificada dentro de :ref:`elemento-back` em :ref:`elemento-fn-group` com :ref:`elemento-fn` do tipo ``@fn-type="financial-disclosure"``.


.. note:: Nota de apoio a pesquisa SEM NÚMERO DE CONTRATO. Deve ser identificada dentro de :ref:`elemento-back` em :ref:`elemento-fn-group` com :ref:`elemento-fn` do tipo ``@fn-type="supported-by"``.


.. {"reviewed_on": "20170720", "by": "aline.cristina@scielo.org"}
