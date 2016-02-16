.. _elemento-aff:

<aff>
-----

Aparece em
  :ref:`elemento-article-meta`
  :ref:`elemento-contrib-group`
  :ref:`elemento-front-stub`

Atributos obrigatórios
  1. id (ver :ref:`sugestao-atribuicao-id`)
 
Ocorre
  Zero ou mais vezes


Considera-se como afiliação o vínculo institucional dos contribuintes do artigo 
naquele momento. 

Os dados de afiliação são importantes para localizar e mensurar a produção 
científica por país, estado, cidade, bem como por instituição e seus 
departamentos. Recomenda-se que os nomes das instituições das afiliações 
sejam especificadas em sua forma original, sem tradução ou abreviações de 
seus nomes. Ou seja, por exemplo, identificar preferencialmente 
**Universidade de São Paulo** a USP, ou University of São Paulo, ou 
Saint Paul University, entre outras possíveis formas. 
Por isso, quando ocorre no documento de existir mais de uma forma, usar a original.
 
Não configura vínculo institucional quando o dado é apresentado da seguinte 
forma: Doutor, Mestre ou Especialista em XXX pela Universidade YYY. Seria 
identificado como afiliação caso o dado esteja como Mestrando(a), Doutorando(a), 
Pós-Graduando(a) etc, configurando o vínculo com instituição naquele momento 
específico.
 
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
 
