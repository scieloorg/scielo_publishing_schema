.. _retratacao:

Retratação
==========

Arquivos do tipo retratação e retratação parcial devem apresentar em :ref:`elemento-article` o atributo ``@article-type`` o valor ``"retraction"`` ou ``"partial-retraction"``. A seção em ``<subject>`` deve conter a informação apresentada no PDF da retratação ou retratação parcial. O elemento :ref:`elemento-article-title` deve conter a informação ARTIGO RETRATADO ou ARTIGO PARCIALMENTE RETRATADO para texto no idioma em português, RETRACTED ARTICLE ou ARTICLE PARTIAL RETRACTION, para texto no idioma em inglês e ARTÍCULO RETRACTADO ou ARTÍCULO PARCIALMENTE RETRACTADO, para texto no idioma em espanhol, e devem estar entre colchetes, mais dois pontos e o título do artigo que está sendo retratado.

O elemento :ref:`elemento-related-article` pode ser usado uma ou mais vezes e é utilizado para referenciar o artigo que sofre a retratação e deve conter obrigatoriamente os atributos:

 * ``@related-article-type`` com valor "retracted-article" ou "partial-retraction"
 * ``@id``
 * ``@xLink:href`` com número DOI do artigo que está sendo retratado
 * ``@ext-link-type`` com valor "doi"
 

Exemplo:
 
.. code-block:: xml


     	<front>
        ...
       <article-meta>
            	<article-id pub-id-type="doi">10.1590/123456720182998</article-id>
            		<article-categories>
                			<subj-group subj-group-type="heading">
                    			<subject>Retratação</subject>
                			</subj-group>
                			...
            		</article-categories>
            	<title-group>
                		<article-title>[ARTIGO RETRATADO]: título do artigo retratado</article-title>
            	</title-group>
            	...
         	 	</permissions>
            		<related-article related-article-type="retracted-article" id="r01" xlink:href="10.1590/a9012345620172123" ext-link-type="doi"/>
     	...
     	</front>
     	<body>
         		<p>Texto da Retratação</p>
          </body>
     	...
     </article>
 
 
.. note:: 
 * :ref:`elemento-related-article` deve ser inserido abaixo das informações de :ref:`elemento-permissions`.
 * O XML do artigo retratado ou parcialmente retratado é alterado pela equipe SciELO. 
 * Mais informações podem ser obtidas no `Guia para o registro e publicação de retratação <https://wp.scielo.org/wp-content/uploads/guia_retratacao.pdf>`_.


