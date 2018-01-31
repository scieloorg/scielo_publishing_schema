.. _elemento-ext-link:

<ext-link>
==========

Atributos obrigatórios:

  1. ``@ext-link-type``
  2. ``@xlink:href``

+----------------------------------+--------------------+
| Aparece em                       | Ocorre             |
+==================================+====================+
| :ref:`elemento-comment`          | Zero ou mais vezes |
+----------------------------------+--------------------+
| :ref:`elemento-element-citation` | Zero ou mais vezes |
+----------------------------------+--------------------+
| :ref:`elemento-p`                | Zero ou mais vezes |
+----------------------------------+--------------------+
| :ref:`elemento-product`          | Zero ou mais vezes |
+----------------------------------+--------------------+


Especifica referências a recursos disponíveis na internet. As únicas restrições quanto à sua utilização são:

* O *scheme* deve ser explícito, ou seja, deve começar com ``http://``, ``ftp://``,   ``urn:`` etc;
* Referências locais, por meio do *scheme* ``file://`` não são permitidas.

Os valores possíveis para o ``@ext-link-type`` são:

* uri
* clinical-trial

.. versionchanged:: 1.5.1
   O valor ``ClinicalTrial``, do atributo ``@ext-link-type``, foi substituído por ``clinical-trial``.


Exemplo URL:

.. code-block:: xml

    ...
    <p>Neque porro quisquam est <ext-link ext-link-type="uri" xlink:href="http://www.scielo.org">www.scielo.org</ext-link> qui dolorem ipsum quia</p>
    ...


Exemplo Ensaio Clínico:

.. code-block:: xml

  ...
    <ext-link ext-link-type="clinical-trial" xlink:href="https://clinicaltrials.gov/ct2/show/NCT01995279?term=NCT01995279">NCT01995279</ext-link>
  ...
    

.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
