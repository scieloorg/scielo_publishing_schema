.. _elemento-publisher-name:

<publisher-name>
================

Aparece em:

  :ref:`elemento-element-citation`
  :ref:`elemento-product`
  :ref:`elemento-publisher`

Ocorre:

  Zero ou mais vezes


Representa o nome da casa publicadora ou editora.

Exemplos:

  * :ref:`elemento-pub-name-exemplo-1`
  * :ref:`elemento-pub-name-exemplo-2`


.. _elemento-pub-name-exemplo-1:

Exemplo de ``<publisher-name>`` em :ref:`elemento-journal-meta`:
----------------------------------------------------------------

.. code-block:: xml

    ...
    <publisher>
        <publisher-name>Escola Nacional de Saúde Pública Sergio Arouca, Fundação Oswaldo Cruz</publisher-name>
    </publisher>
    ...

.. _elemento-pub-name-exemplo-2:

Exemplo de ``<publisher-name>`` em :ref:`elemento-element-citation`:
--------------------------------------------------------------------

.. code-block:: xml

    ...
    <element-citation publication-type="book">
               ...
        <publisher-name>National Academy of Science</publisher-name>
        <fpage>223</fpage>
        <lpage>244</lpage>
    </element-citation>
    ...


.. {"reviewed_on": "20160729", "by": "gandhalf_thewhite@hotmail.com"}
