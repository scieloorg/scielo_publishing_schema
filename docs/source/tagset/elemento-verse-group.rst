.. _elemento-verse-group:

<verse-group>
=============

Aparece em:

  :ref:`elemento-app`
  ``<app-group>``
  :ref:`elemento-body`
  :ref:`elemento-boxed-text`
  :ref:`elemento-disp-quote`
  :ref:`elemento-p`
  :ref:`elemento-ref-list`
  :ref:`elemento-sec`
  :ref:`elemento-supplementary-material`
  :ref:`elemento-verse-group`

Ocorre:

  Zero ou mais vezes


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
