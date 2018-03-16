.. _elemento-inline-graphic:

<inline-graphic>
================

+-------------------------+--------------------+
| Aparece em              | Ocorre             |
+=========================+====================+
| :ref:`elemento-product` | Zero ou mais vezes |
+-------------------------+--------------------+
| :ref:`elemento-body`    | Zero ou mais vezes |
+-------------------------+--------------------+
| :ref:`elemento-p`       | Zero ou mais vezes |
+-------------------------+--------------------+
| :ref:`elemento-sec`     | Zero ou mais vezes |
+-------------------------+--------------------+
| ``th``                  | Zero ou mais vezes |
+-------------------------+--------------------+
| ``td``                  | Zero ou mais vezes |
+-------------------------+--------------------+


Usado para identificar caracteres que não possuem codificação em um parágrafo.


.. note:: Para maiores informações verificar `Codificação e caracteres especiais <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/latest/narr/caracteres.html>`_.


Exemplo:

.. code-block:: xml

    ...
    <p>We also used an enrichment factor for surface waters (EF<sub>w</sub>) based on the equation:<inline-graphic xlink:href="1234-5678-rctb-45-05-0110-e01.tif"/>. The EF<sub>s</sub> and EF<sub>w</sub> quantified the concentration of the element of interest (C<sub>i</sub>) in the sample, in relation to the (natural) geochemical background.</p>
    ...
    


.. {"reviewed_on": "20160626", "by": "gandhalf_thewhite@hotmail.com"}
