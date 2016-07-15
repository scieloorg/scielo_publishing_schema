.. _elemento-fn-group:

<fn-group>
==========

Aparece em:

  :ref:`elemento-back`

Ocorre:

  Zero ou mais vezes

``<fn-group>`` faz parte do elemento :ref:`elemento-back` e deve conter todo o grupo de notas de rodapé mencionadas no :term:`documento`, que não representam notas de autor, as quais devem ser identificadas com :ref:`elemento-author-notes`. Este elemento pode possuir um único título identificado com ``<title>`` e uma ou mais notas :ref:`elemento-fn`.

Exemplo:

.. code-block:: xml

    ...
    <back>
        ...
        <fn-group>
            <title>Notas</title>
            <fn fn-type="supported-by" id="fn01">
                <label>*</label>
                <p>Vivamus sodales fermentum lorem, consectetur mollis lacus sollicitudin quis</p>
            </fn>
            <fn fn-type="presented-at" id="fn02">
                <label>**</label>
                <p>Donec et urna sed orci volutpat sollicitudin. Vestibulum quis tempor lacus. Nunc cursus, mi sed auctor pellentesque, orci tellus tincidunt arcu, eu imperdiet augue ligula eget justo.</p>
            </fn>
        </fn-group>
        ...
    </back>
    ...


.. {"reviewed_on": "20160624", "by": "gandhalf_thewhite@hotmail.com"}
