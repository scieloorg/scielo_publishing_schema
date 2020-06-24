.. _elemento-license:

<license>
=========


Atributos obrigatórios:

  1. ``@license-type="open-access"``
  2. ``@xlink:href``
  3. ``@xml:lang``

+-----------------------------+-------------------+
| Aparece em                  | Ocorre            |
+=============================+===================+
| :ref:`elemento-permissions` | Uma ou mais vezes |
+-----------------------------+-------------------+



Indica a licença de uso (:term:`Creative Commons`) adotada pelo artigo, por meio de referência à URL onde o texto da licença encontra-se disponível.
Cada tipo de licença define regras que regulam uso, distribuição e adaptação da obra. Mais informações podem ser consultadas no site `Creative Commons <https://creativecommons.org/>`_.

O valor para ``@xml:lang`` deve ser o correspondente ao idioma do texto da licença, identificado pelo elemento ``<license-p>``.
Obrigatoriamente, deve haver um ``<license-p>`` no idioma original do artigo ou em inglês.


Exemplo:

.. code-block:: xml

    ...
    <article-meta>
        ...
        <permissions>
            ...
            <license license-type="open-access"
                     xlink:href="https://creativecommons.org/licenses/by/4.0/"
                     xml:lang="en">
                <license-p>This is an article published in open access under a Creative Commons license.</license-p>
            </license>
            <license license-type="open-access"
                     xlink:href="https://creativecommons.org/licenses/by/4.0/"
                     xml:lang="pt">
                <license-p>Este é um artigo publicado em acesso aberto sob uma licença Creative Commons.</license-p>
            </license>
            <license license-type="open-access"
                     xlink:href="https://creativecommons.org/licenses/by/4.0/"
                     xml:lang="es">
                <license-p>Este es un artículo publicado en acceso abierto bajo una licencia Creative Commons.</license-p>
            </license>
        </permissions>
        ...
    </article-meta>
    ...


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
