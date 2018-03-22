.. _elemento-sig-block:

<sig-block>
===========

+----------------------+-----------------+
| Aparece em           | Ocorre          |
+======================+=================+
| :ref:`elemento-body` | Zero ou uma vez |
+----------------------+-----------------+



Contém um bloco de assinatura(s), normalmente utilizado em documentos editoriais. ``<sig-block>`` deve, obrigatoriamente, conter o elemento ``<sig>``. É permitido formatar o texto do bloco de assinatura com negrito (``<bold>``) ou itálico (``<italic>``). Para identificar as quebras de linha usa-se a tag ``<break/>``.

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

