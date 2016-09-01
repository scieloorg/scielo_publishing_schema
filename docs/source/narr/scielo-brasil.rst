.. _scielo-brasil:

SciELO Brasil
=============

Para atender aos "Critérios, política e procedimentos para a admissão e a permanência de periódicos científicos na Coleção SciELO Brasil" alguns elementos apresentam restrições:


  * :ref:`elemento-scibrasil-article-id`
  * :ref:`elemento-scibrasil-license`



`Critérios SciELO Brasil <http://www.scielo.br/avaliacao/20141003NovosCriterios_SciELO_Brasil.pdf>`_


.. _elemento-scibrasil-article-id:

<article-id>
^^^^^^^^^^^^

Em :ref:`elemento-article-id` o atributo ``@pub-id-type`` deve, obrigatoriamente, apresentar o valor "doi".
Exemplo:

.. code-block:: xml

	...
	<article-id pub-id-type="doi">10.1590/0100-29452016221</article-id>
	...
	


.. _elemento-scibrasil-license:

<license>
^^^^^^^^^

De acordo com a política de acesso aberto adotada por SciELO Brasil, serão aceitas apenas as licenças `Creative Commons <http://creativecommons.org/>`_  listadas na tabela abaixo:


+--------------------------------------------------------+-------------------------+
| Valor                                                  | Descrição               |
+========================================================+=========================+
| http://creativecommons.org/licenses/by/4.0/            | CC-BY versão 4.0        |
+--------------------------------------------------------+-------------------------+
| http://creativecommons.org/licenses/by/3.0/            | CC-BY versão 3.0        |
+--------------------------------------------------------+-------------------------+
| http://creativecommons.org/licenses/by-nc/4.0/         | CC-BY-NC versão 4.0     |
+--------------------------------------------------------+-------------------------+
| http://creativecommons.org/licenses/by-nc/3.0/         | CC-BY-NC versão 3.0     |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by-nc-nd/3.0/     | CC-BY-NC-ND versão 3.0  |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by-nc-nd/4.0/     | CC-BY-NC-ND versão 4.0  |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by/3.0/igo/       | BY/IGO versão 3.0       |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by-nc/3.0/igo/    | BY-NC/IGO versão 3.0    |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by-nc-nd/3.0/igo/ | BY-NC-ND/IGO versão 3.0 |
+--------------------------------------------------------+-------------------------+


A URL da licença deve ser inserida como valor do atributo ``@xlink:href`` de :ref:`elemento-license`. Exemplo:


.. code-block:: xml

	...
    <article-meta>
        ...
        <permissions>
            ...
            <license license-type="open-access"
                     xlink:href="http://creativecommons.org/licenses/by/4.0/"
                     xml:lang="en">
                <license-p>This is an open-access article distributed under the terms of the Creative Commons Attribution License, which permits unrestricted use, distribution, and reproduction in any medium, provided the original work is properly cited.</license-p>
            </license>
        </permissions>
      	...
    </article-meta>
    ...



.. note:: Considera-se a lista de licenças permitidas apenas para :ref:`elemento-article-meta`.
