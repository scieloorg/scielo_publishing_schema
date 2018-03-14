.. _elemento-size:

<size>
======

Atributos obrigatórios:

  1. ``@units="pages"``

+----------------------------------+-----------------+
| Aparece em                       | Ocorre          |
+==================================+=================+
| :ref:`elemento-element-citation` | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-product`          | Zero ou uma vez |
+----------------------------------+-----------------+



Identifica a quantidade total de páginas de um :term:`documento` mencionado numa referência. Deve ser utilizado com o atributo ``@units="pages"``.

Exemplo:

.. code-block:: xml

    ...
    <element-citation publication-type="book">
         <publisher-name>Guanabara Koogan</publisher-name>
         <year>1997</year>
         <size units="pages">2647 p</size>
    </element-citation>
    ...


.. {"reviewed_on": "20160629", "by": "gandhalf_thewhite@hotmail.com"}
