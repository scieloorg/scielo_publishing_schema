.. _elemento-aff:

<aff>
-----

Aparece em:

  :ref:`elemento-article-meta`
  :ref:`elemento-contrib-group`
  :ref:`elemento-front-stub`

Atributos obrigatórios:

  1. ``@id`` (ver :ref:`sugestao-atribuicao-id`)

Ocorre:

  Zero ou mais vezes

Considera-se como afiliação o vínculo institucional dos contribuintes do artigo naquele momento, seja pelo título em processo de outorga, por exemplo, *Mestrando(a)*, *Doutorando(a)*, *Pós-Graduando(a)* etc, como também pessoas vinculadas diretamente à instituição, como por exemplo, *Professor na Universidade X*, *Médico na instituição Y, Enfermeira no Hospital Z etc.

Dados de afiliação são importantes para localizar e mensurar a produção científica por país, estado, cidade, bem como por instituição e seus departamentos.

Recomenda-se especificar os nomes das instituições nas afiliações em sua forma original, sem tradução ou abreviaturas.

Ex. *Universidade de São Paulo*.

Quando ocorrer mais de uma forma, deve-se utilizar sempre o nome original.

Não configura vínculo institucional quando refere-se a título outorgado. Ex.: Doutor, Mestre ou Especialista em (área) pela Universidade (nome).

Exemplo:

.. code-block:: xml

    ...
    <aff id="aff01">
        <label>1</label>
        <institution content-type="orgname">Fundação Oswaldo Cruz</institution>
        <institution content-type="orgdiv1">Escola Nacional de Saúde Pública Sérgio Arouca</institution>
        <institution content-type="orgdiv2">Centro de Estudos da Saúde do Trabalhador e Ecologia Humana</institution>
        <addr-line>
            <named-content content-type="city">Manguinhos</named-content>
            <named-content content-type="state">RJ</named-content>
        </addr-line>
        <country country="BR">Brasil</country>
        <email>maurosilva@foo.com</email>
        <institution content-type="original">Prof. da Fundação Oswaldo Cruz; da Escola Nacional de Saúde Pública Sérgio Arouca, do Centro de Estudos da Saúde do Trabalhador e Ecologia Humana. RJ - Manguinhos / Brasil. maurosilva@foo.com </institution>
    </aff>
    ...


.. {"reviewed_on": "20160728", "by": "gandhalf_thewhite@hotmail.com"}
