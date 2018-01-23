.. _elemento-name:

<name>
======

+------------------------------+--------------------+
| Aparece em                   | Ocorre             |
+==============================+====================+
| :ref:`elemento-contrib`      | Zero ou mais vezes |
+------------------------------+--------------------+
| :ref:`elemento-person-group` | Zero ou mais vezes |
+------------------------------+--------------------+



``<name>`` é usado para especificar o nome pessoal de um contribuinte autoral.

Os elementos possíveis em ``<name>`` são: :ref:`elemento-surname`, :ref:`elemento-given-names`, :ref:`elemento-prefix`, :ref:`elemento-suffix`, e devem, obrigatoriamente, seguir esta sequência na descrição.

Exemplos:

  * :ref:`elemento-name-exemplo-1`
  * :ref:`elemento-name-exemplo-2`


.. _elemento-name-exemplo-1:

Exemplo de ``<name>`` em ``<contrib>``:
---------------------------------------

.. code-block:: xml

   ...
   <contrib contrib-type="author">
        <name>
             <surname>Amon</surname>
             <given-names>Joseph J.</given-names>
        </name>
   </contrib>
   ...


.. _elemento-name-exemplo-2:

Exemplo de ``<name>`` em ``<person-group>``:
--------------------------------------------

.. code-block:: xml

   ...
   <person-group person-group-type="author">
        <name>
             <surname>Silva</surname>
             <given-names>Jaqueline Figueiredo da</given-names>
        </name>
   </person-group>
   ...


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
