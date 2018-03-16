.. _elemento-inline-formula:

<inline-formula>
================

+-------------------------+--------------------+
| Aparece em              | Ocorre             |
+=========================+====================+
| :ref:`elemento-product` | Zero ou mais vezes |
+-------------------------+--------------------+
| :ref:`elemento-body`    | Zero ou mais vezes |
+-------------------------+--------------------+
| :ref:`elemento-p`       | Zero ou mais vezes |
+-------------------------+--------------------+
| :ref:`elemento-sec`     | Zero ou mais vezes |
+-------------------------+--------------------+
| ``th``                  | Zero ou mais vezes |
+-------------------------+--------------------+
| ``td``                  | Zero ou mais vezes |
+-------------------------+--------------------+



Identifica equações e fórmulas exibidas em um parágrafo. A codificação pode ser escrita de acordo com :term:`W3C` em linguagem :term:`MathML` (http://www.w3.org/TR/MathML3/), sendo o elemento base ``<mml:math>`` ou com codificação TeX ou LaTeX.


Exemplo para codificar σˆ2* usando *MathML*:

.. code-block:: xml

    ...
    <p>Nulla velit magna, semper quis dignissim id, condimentum nec diam
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
    Nulla quis leo sed turpis congue finibus feugiat ut dui. Donec id tincidunt tellus. Nunc fermentum dolor et congue convallis. <p/>
    ...


.. {"reviewed_on": "20160626", "by": "gandhalf_thewhite@hotmail.com"}
