.. _elemento-version:

<version>
=========


+----------------------------------+-----------------+
| Aparece em                       | Ocorre          |
+==================================+=================+
| :ref:`elemento-product`          | Zero ou uma vez |
+----------------------------------+-----------------+
| :ref:`elemento-element-citation` | Zero ou uma vez |
+----------------------------------+-----------------+


Identifica a versão de um software ou base de dados.

Exemplo:

.. code-block:: xml

   ...
   <element-citation publication-type="database">
        <source>DialogWeb [Internet]</source>
        <version>Version 2.5</version>
        <publisher-loc>Cary (NC)</publisher-loc>
        <publisher-name>The Dialog Corporation</publisher-name>
        <year>c1997 -  </year>
        <date-in-citation>cited 2007 Feb 1</date-in-citation>
        <comment>Available from:
        <ext-link ext-link-type="uri" xlink:href="http://www.dialogweb.com/">http://www.dialogweb.com/</ext-link>.
     </comment>
   </element-citation>
   ...

.. note:: Elemento válido apenas na versão 1.1 da JATS. Consulte exemplo de declaração para a versão JATS v1.1 em `!DOCTYPE <http://docs.scielo.org/projects/scielo-publishing-schema/pt_BR/1.7-branch/tagset/xml-doctype.html>`_.

.. {"reviewed_on": "20170904", "by": "carolina.tanigushi@scielo.org"}
