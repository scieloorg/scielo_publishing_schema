.. _elemento-inline-graphic:
 
<inline-graphic>
----------------
 
Aparece em
  :ref:`elemento-product`, 
  :ref:`elemento-body`,
  :ref:`elemento-p`,
  :ref:`elemento-sec`,
  ``th``,
  ``td``
 
Ocorre
  Zero ou mais vezes


Elemento utilizado para identificar equações em imagem que estejam posicionadas em linha, ou seja, em meio a um parágrafo.
 
Consulte a :ref:`sugestao-atribuicao-id` para instruções sobre a composição do atributo ``@id``.
 
Exemplo:

.. code-block:: xml
 
    ...
    <p>We also used an enrichment factor for surface waters (EF<sub>w</sub>) based on the equation:<inline-graphic xlink:href="1234-5678-rctb-45-05-0110-e01.tif"/>. The EF<sub>s</sub> and EF<sub>w</sub> quantified the concentration of the element of interest (C<sub>i</sub>) in the sample, in relation to the (natural) geochemical background.</p>
    ...

