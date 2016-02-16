.. _elemento-person-group:

<person-group>
^^^^^^^^^^^^^^ 

Aparece em
  :ref:`elemento-product`,
  :ref:`elemento-element-citation`
  
Atributos obrigatórios 
  1. person-group-type

Ocorre 
  Zero ou mais vezes


Identifica o grupo ou o indivíduo criador/elaborador do documento. 
As tags :ref:`elemento-collab`, :ref:`elemento-role`, 
:ref:`elemento-name` e :ref:`elemento-etal`, no caso de existirem, devem ser 
identificadas apenas em ``person-group``. 

Os valores possíveis para o atributo ``@person-group-type`` são:

+-----------+---------------+
| Valor     | Descrição     |
+===========+===============+
| author    | valor padrão  |
+-----------+---------------+
| compiler  | compilador    |
+-----------+---------------+
| editor    | editor        |
+-----------+---------------+
| translator| tradutor      |
+-----------+---------------+

Exemplo:
 
.. code-block:: xml

    ...
    <ref>
        <element-citation publication-type="book">
            <person-group person-group-type="author">
                <name>
                    <surname>Silva</surname>
                    <given-names>Jaqueline Figueiredo da</given-names>
                </name>
                <collab>Instituto Brasil Leitor</collab>
                ...
            </person-group>
            ...
        </element-citation>
        ...
    </ref>
    ...

.. note:: Em ``person-group`` o elemento :ref:`elemento-name` ocorre Zero ou Mais vezes
