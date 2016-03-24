.. _elemento-date-in-citation:

<date-in-citation>
^^^^^^^^^^^^^^^^^^

Aparece em
  :ref:`elemento-element-citation`
 
Atributos obrigatórios 
 ``@content-type``

Ocorre 
  Zero ou mais vezes

Esta tag identifica a data de citação em uma referência. Deve sempre possuir 
o atributo ``@content-type`` com os tipos de data de acesso e data de
atualização do documento.

Exemplo 1:

.. code-block:: xml

    ...
    <element-citation>
        <date-in-citation content-type="access-date">cited 2007 Feb 21</date-in-citation>
    </element-citation>
    ...

Exemplo 2:

.. code-block:: xml

    ...
    <element-citation>
        <date-in-citation content-type="updated">2006 Jul 20</date-in-citation>
    </element-citation>
    ...

