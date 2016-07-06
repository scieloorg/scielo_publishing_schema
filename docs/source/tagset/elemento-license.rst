.. _elemento-license:

<license>
^^^^^^^^^

Aparece em:

  :ref:`elemento-permissions`

Atributos obrigatórios:

  1. ``@license-type="open-access"``
  2. ``@xlink:href``
  3. ``@xml:lang``

Ocorre:

  Uma ou mais vezes


Indica a licença de uso (:term:`Creative Commons`) adotada pelo artigo, por meio de referência à URL onde o texto da licença encontra-se disponível.

Cada tipo de licença define regras que regulam uso, distribuição e adaptação da obra. Mais informações podem ser consultadas no site `Creative Commons <http://creativecommons.org/>`_.


Os valores possíveis para ``@xlink:href`` são:

+--------------------------------------------------------+-------------------------+
| Valor                                                  | Descrição               |
+========================================================+=========================+
| http://creativecommons.org/licenses/by/4.0/            | CC-BY versão 4.0        |
+--------------------------------------------------------+-------------------------+
| http://creativecommons.org/licenses/by/3.0/            | CC-BY versão 3.0        |
+--------------------------------------------------------+-------------------------+
| http://creativecommons.org/licenses/by-nc/4.0/         | CC-BY-NC versão 4.0     |
+--------------------------------------------------------+-------------------------+
| http://creativecommons.org/licenses/by-nc/3.0/         | CC-BY-NC versão 3.0     |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by-nc-nd/3.0/     | CC-BY-NC-ND versão 3.0  |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by-nc-nd/4.0/     | CC-BY-NC-ND versão 4.0  |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by/3.0/igo/       | BY/IGO versão 3.0       |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by-nc/3.0/igo/    | BY-NC/IGO versão 3.0    |
+--------------------------------------------------------+-------------------------+
| https://creativecommons.org/licenses/by-nc-nd/3.0/igo/ | BY-NC-ND/IGO versão 3.0 |
+--------------------------------------------------------+-------------------------+

.. note:: Considera-se a lista acima apenas para :ref:`elemento-article-meta`.

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
                     xlink:href="http://creativecommons.org/licenses/by/4.0/"
                     xml:lang="en">
                <license-p>This is an open-access article distributed under the terms of the Creative Commons Attribution License, which permits unrestricted use, distribution, and reproduction in any medium, provided the original work is properly cited.</license-p>
            </license>
            <license license-type="open-access"
                     xlink:href="http://creativecommons.org/licenses/by/4.0/"
                     xml:lang="pt">
                <license-p>Este artigo está licenciado com uma Licença Creative Commons que permite uso irrestrito, distribuição, e reprodução em qualquer mídia, desde que a obra original seja citada adequadamente.</license-p>
            </license>
            <license license-type="open-access"
                     xlink:href="http://creativecommons.org/licenses/by/4.0/"
                     xml:lang="es">
                <license-p>Este es un artículo de acceso abierto distribuido bajo los términos de la licencia Creative Commons Attribution License, que permite el uso ilimitado, distribución y reproducción en cualquier medio, siempre que el artículo original esté debidamente citado.</license-p>
            </license>
        </permissions>
        ...
    </article-meta>
    ...


.. {"reviewed_on": "20160627", "by": "gandhalf_thewhite@hotmail.com"}
