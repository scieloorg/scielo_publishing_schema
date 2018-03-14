.. _elemento-verse-group:

<verse-group>
=============

+----------------------------------------+--------------------+
| Aparece em                             | Ocorre             |
+========================================+====================+
| :ref:`elemento-app`                    | Zero ou mais vezes |
+----------------------------------------+--------------------+
| ``<app-group>``                        | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-body`                   | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-boxed-text`             | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-disp-quote`             | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-p`                      | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-ref-list`               | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-sec`                    | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-supplementary-material` | Zero ou mais vezes |
+----------------------------------------+--------------------+
| :ref:`elemento-verse-group`            | Zero ou mais vezes |
+----------------------------------------+--------------------+



Elemento utilizado para apresentar poemas, versos ou músicas. Nele também podem ser inseridos os elementos :ref:`elemento-attrib` para identificação do autor e :ref:`elemento-label` para identificação do título do poema, verso etc.


Exemplo:

.. code-block:: xml

    ...
    <verse-group>
      <label>Porque é que um sono agita</label>
        <verse-line>E, num fiel regresso</verse-line>
        <verse-line>Ao que já era bruma,</verse-line>
        <verse-line>Sonolento me apresso</verse-line>
        <verse-line>Para coisa nenhuma.</verse-line>
        <attrib>Fernando Pessoa</attrib>
    </verse-group>
    ...


.. {"reviewed_on": "20160629", "by": "gandhalf_thewhite@hotmail.com"}
