.. _elemento-sig-block:

<sig-block>
-----------

Aparece em
  :ref:`elemento-body`

Ocorre
  Zero ou uma vez


Tag que identifica um bloco de assinatura(s), normalmente utilizada em 
documentos do tipo editorial. A tag de ``<sig-block>`` deve obrigatoriamente 
conter a tag ``<sig>``. É possível formatar o texto do bloco de assinatura 
com negrito ``<bold>`` ou itálico ``<italic>``. Para as quebras de linhas 
deve-se usar a tag ``<break/>`` como mostram os exemplos a seguir:

Exemplo:
 
.. code-block:: xml
 
    ...
    <sig-block>
        <sig>
            <bold>Harry Weasley</bold>
            <break/>
            <italic>Editor Chefe</italic>
            <break/>
            Profeta Diário
            <break/>
        </sig>
    </sig-block>
    ...


.. note:: Para arquivos que apresentam apenas uma assinatura ao final do documento, é preciso repetir os nomes que constam na assinatura em front/contrib e marcá-los como autores.

