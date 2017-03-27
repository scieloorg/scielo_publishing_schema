.. _scielo-brasil:

Regras Específicas para SciELO Brasil
=====================================

Para atender aos "Critérios, política e procedimentos para a admissão e a permanência de periódicos científicos na Coleção SciELO Brasil" alguns elementos apresentam restrições:


  * :ref:`elemento-scibrasil-article-id`
  * :ref:`elemento-scibrasil-license`
  * :ref:`elemento-scibrasil-disp`
  * :ref:`elemento-scibrasil-history`

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

De acordo com a política de acesso aberto adotada por SciELO Brasil, serão aceitas quaisquer licenças `Creative Commons <http://creativecommons.org/>`_

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



.. _elemento-scibrasil-disp:

Tabelas e equações codificadas
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Os elementos :ref:`elemento-disp-formula`, :ref:`elemento-inline-formula` e :ref:`elemento-table`, que identificam dados de equações e tabelas, devem ser codificados. O elemento :ref:`elemento-alternatives` pode ser usado para armazenar a versão em imagem desses elementos na extensão .svg.

.. _elemento-scibrasil-history:

<history>
^^^^^^^^^

É obrigatória a indicação nos artigos publicados das principais datas do processo de arbitragem, compreendendo pelo menos as datas de recebimento e de aprovação qa quais deverão conter dia, mês e ano.
