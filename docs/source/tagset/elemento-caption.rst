.. _elemento-caption:

<caption>
---------
 
Aparece em
  :ref:`elemento-disp-formula`,
  :ref:`elemento-fig`, 
  :ref:`elemento-table-wrap`,
  :ref:`elemento-media`,
  :ref:`elemento-supplementary-material`

Ocorre
  Zero ou mais vezes


Tag que representa uma descrição de tabela, figura ou objeto similar.
 
O elemento ``<caption>`` deve envolver a tag ``<title>`` com a descrição textual da legenda dos objetos mencionados.
 
Exemplo:
 
.. code-block:: xml
 
    ...
    <fig id="f03">
        <label>Figura 3</label>
        <caption>
            <title>Percentual de atividade mitocondrial (método MTT) das células dos diferentes grupos experimentais em relação às células do grupo controle</title>
        </caption>
        <graphic xlink:href="1234-5678-rctb-45-05-0110-gf01.tif"/>
    </fig>
    ...
 
