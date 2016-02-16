.. _elemento-issn:
 
<issn>
^^^^^^

Aparece em
  :ref:`elemento-journal-meta`, :ref:`elemento-element-citation`
 
Atributos obrigatórios em :ref:`elemento-front`
  1. pub-type='ppub' ou pub-type='epub'
 
Ocorre
  Uma ou mais vezes


O ISSN é um código numérico, único, que identifica uma publicação seriada 
a qual é definida pela norma :term:`ISO 3297:2007`. Normalmente cada tipo de 
suporte utilizado pelo periódico possui um número específico. 

É possível também encontrar esta informação em :ref:`elemento-back` dentro de 
:ref:`elemento-element-citation` nas referências, mas não se faz o uso de 
nenhum atributo neste caso.

.. note:: Consulte o :ref:`arquivo de metadados dos periódicos <journal-meta-csv>` 
          como referência na identificação dos elementos.

Os valores permitidos para o atributo ``@pub-type`` são:

+-------+-------------------------+
| Valor | Descrição               |
+=======+=========================+
| ppub  | ISSN da versão impressa |
+-------+-------------------------+
| epub  | ISSN da versão digital  |
+-------+-------------------------+
 
No caso de estarem disponíveis, ambos os ISSNs deverão ser identificados, 
conforme o exemplo:
 
.. code-block:: xml
    
    ...
    <journal-meta>
        ...
        <issn pub-type="epub">1808-8686</issn>
        <issn pub-type="ppub">1808-8694</issn>
        ...
    </journal-meta>
    ...

