.. _elemento-ext-link:

<ext-link>
----------

Aparece em
  :ref:`elemento-p`,
  :ref:`elemento-element-citation`, 
  :ref:`elemento-comment`,

Atributos obrigatórios
  1. ext-link-type="uri"
  2. xlink:href
 
Ocorre
  Zero ou mais vezes

Utilizado para especificar referências a recursos disponíveis na internet. As 
únicas restrições quanto à sua utilização são:

* O *scheme* deve ser explícito, i.e., deve começar com ``http://``, ``ftp://``, 
  ``urn:`` etc.
* Referências locais, por meio do *scheme* ``file://`` não são permitidas.


Exemplo:
 
.. code-block:: xml
 
    ...
    <p>Neque porro quisquam est <ext-link ext-link-type="uri" xlink:href="http://www.scielo.org">www.scielo.org</ext-link> qui dolorem ipsum quia</p>
    ...
 
