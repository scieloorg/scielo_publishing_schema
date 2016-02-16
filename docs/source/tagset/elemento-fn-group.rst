.. _elemento-fn-group:

<fn-group>
----------

Aparece em
  :ref:`elemento-back`

Ocorre
  Zero ou mais vezes

A tag de grupo de notas é um elemento de :ref:`elemento-back` e deve conter todo
o grupo de notas de rodapé mencionadas no :term:`documento` que não representem notas de
autor, as quais deverão ser identificadas em :ref:`elemento-author-notes`. Pode 
possuir um único título identificado com a tag ``<title>``  e uma ou mais notas 
:ref:`elemento-fn`.
 
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

