.. _elemento-inline-formula:
 
<inline-formula>
----------------
 
Aparece em
  :ref:`elemento-product`, 
  :ref:`elemento-body`,
  :ref:`elemento-p`,
  :ref:`elemento-sec`,
  ``th``,
  ``td``
 
Ocorre
  Zero ou mais vezes


Elemento utilizado para identificar equações codificadas em linha. Nesse caso, a codificação pode ser feita de acordo com :term:`W3C` em linguagem :term:`MathML` 
(http://www.w3.org/TR/MathML3/), sendo o elemento base ``<mml:math>`` ou com outros tipos de codificação, exemplo: caracteres ASCII, TeX ou LaTeX.
 
**Exemplo**: para codificar  σˆ2*
 
.. code-block:: xml

    ... 
    <inline-formula>
        <mml:math id="e03">
            <mml:mrow>
                <mml:msup>
                    <mml:mover accent="true">
                        <mml:mi>σ</mml:mi>
                        <mml:mo>ˆ</mml:mo>
                    </mml:mover>
                    <mml:mn>2</mml:mn>
                </mml:msup>
            </mml:mrow>
        </mml:math>
    </inline-formula>
    ...
 
