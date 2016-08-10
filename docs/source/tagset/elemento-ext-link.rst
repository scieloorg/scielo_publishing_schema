.. _elemento-ext-link:

<ext-link>
----------

Aparece em:

  :ref:`elemento-p`
  :ref:`elemento-element-citation`
  :ref:`elemento-comment`

Atributos obrigatórios:

  1. ``@ext-link-type``
  2. ``@xlink:href``

Ocorre:

  Zero ou mais vezes

Especifica referências a recursos disponíveis na internet. As únicas restrições quanto à sua utilização são:

* O *scheme* deve ser explícito, ou seja, deve começar com ``http://``, ``ftp://``,   ``urn:`` etc;
* Referências locais, por meio do *scheme* ``file://`` não são permitidas.

.. note:: O valor ``uri`` é obrigatório para o atributo ``@ext-link-type``.

Exemplo:

.. code-block:: xml

    ...
    <p>Neque porro quisquam est <ext-link ext-link-type="uri" xlink:href="http://www.scielo.org">www.scielo.org</ext-link> qui dolorem ipsum quia</p>
    ...


.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
