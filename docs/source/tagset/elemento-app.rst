.. _elemento-app:

<app>
=====

Aparece em:

  `<app-group>`

Atributos obrigatórios:

  1. ``@id`` (Ver :ref:`sugestao-atribuicao-id`)

Ocorre:

  Zero ou mais vezes

Utilizado para indicar um apêndice ao documento. Exige o elemento :ref:`elemento-label` como título do apêndice. O elemento ``<app-group>`` deve sempre ser usado como agrupador do elemento ``<app>`` mesmo se houver somente uma ocorrência deste último.

Exemplos:

  * :ref:`elemento-app-exemplo-1`
  * :ref:`elemento-app-exemplo-2`
  * :ref:`elemento-app-exemplo-3`
  * :ref:`elemento-app-exemplo-4`
  * :ref:`elemento-app-exemplo-5`
  * :ref:`elemento-app-exemplo-6`
  * :ref:`elemento-app-exemplo-7`


.. _elemento-app-exemplo-1:

Exemplo de apêndice com texto
-----------------------------

.. code-block:: xml

    ...
    <app-group>
          <app id="app01">
              <label>Apêndice</label>
              <p>Vivamus fermentum elit et pellentesque iaculis. Curabitur egestas rhoncus purus quis iaculis. Sed laoreet id leo eu tristique. Etiam hendrerit nibh in tincidunt mattis. Sed et volutpat nulla, eget semper tellus. Nullam imperdiet fringilla diam, nec mollis elit sagittis a. Nam euismod sagittis posuere.</p>
          </app>
    </app-group>
    ...

.. _elemento-app-exemplo-2:

Exemplo de apêndice com imagem (fotografia, figura, tabela, quadro, equação e etc)
----------------------------------------------------------------------------------

.. code-block:: xml

    ...
    <app-group>
        <app id="app01">
              <label>Appendix 1</label>
              <title>Questionnaire for SciELO</title>
              <graphic xlink:href="1234-5678-rctb-45-05-0110-app01.tif"/>
        </app>
    </app-group>
    ...


.. _elemento-app-exemplo-3:

Exemplo de apêndice com link externo (endereço do tipo URI)
-----------------------------------------------------------

.. code-block:: xml

    ...
    <app-group>
        <app id="app01">
            <label>Appendix 1</label>
            <p>Para mais informações <ext-link ext-link-type="uri" xlink:href="http://www.scielo.org">clique aqui</ext-link> para verificar o pdf.</p>
        </app>
    </app-group>
    ...


.. _elemento-app-exemplo-4:

Exemplo de apêndice com tabela
------------------------------

.. code-block:: xml

    ...
    <app-group>
      <app id="app01">
      <label>Appendix</label>
            <table-wrap>
              <label>Table 1</label>
              <caption>
                  <title>Título da tabela</title>
              </caption>
              <table frame="hsides" rules="all">
                  <colgroup width="XX%">
                      <col/>
                      <col/>
                      <col/>
                  </colgroup>
                  <thead>
                      <tr>
                           <th style="background-color:#e5e5e5">xxxxx</th>
                           <th style="background-color:#e5e5e5">xxxxx</th>
                           <th style="background-color:#e5e5e5">xxxxxx</th>
                      </tr>
                  </thead>
                  <tbody>
                      <tr>
                           <td align="center">xxxxx</td>
                           <td align="center">xxxx</td>
                           <td align="center">xxxx</td>
                      </tr>
                  </tbody>
              </table>
            </table-wrap>
      </app>
    </app-group>
    ...


.. _elemento-app-exemplo-5:

Exemplo de apêndice misto (figura mais tabela)
----------------------------------------------

.. code-block:: xml

    ...
    <app-group>
        <app id="app01">
            <label>Appendix 1</label>
            <title>Questionnaire for SciELO</title>
            <graphic xlink:href="1234-5678-rctb-45-05-0110-app01.tif"/>
        </app>
        <app id="app02">
            <label>Appendix 2</label>
            <table-wrap>
                <label>Supplementary Table S1</label>
                <caption>
                    <title>Título da tabela</title>
                </caption>
                <table frame="hsides" rules="all">
                    <colgroup width="XX%">
                        <col/>
                        <col/>
                        <col/>
                    </colgroup>
                    <thead>
                        <tr>
                            <th style="background-color:#e5e5e5">xxxxx</th>
                            <th style="background-color:#e5e5e5">xxxxx</th>
                            <th style="background-color:#e5e5e5">xxxxxx</th>
                        </tr>
                    </thead>
                    <tbody>
                        <tr>
                            <td align="center">xxxxx</td>
                            <td align="center">xxxx</td>
                            <td align="center">xxxx</td>
                        </tr>
                    </tbody>
                </table>
            </table-wrap>
        </app>
    </app-group>
    ...


.. _elemento-app-exemplo-6:

Exemplo de apêndice misto (texto mais figura)
---------------------------------------------

.. code-block:: xml

    ...
    <app-group>
        <app id="app01">
            <label>Appendix 1</label>
            <title>Questionnaire for student inclusion</title>
            <graphic xlink:href="1234-5678-rctb-45-05-0110-app01.tif"/>
        </app>
        <app id="app02">
            <label>Appendix 2</label>
            <p>Pellentesque sollicitudin, purus nec ultricies tristique, purus nisi imperdiet enim, nec mollis augue odio sit amet augue. Lorem ipsum dolor sit amet, consectetur adipiscing elit. Ut cursus ipsum non nisi faucibus suscipit. Cras ut venenatis tellus.</p>
        </app>
    </app-group>
    ...


.. _elemento-app-exemplo-7:

Exemplo de apêndice com vídeo
-----------------------------

.. code-block:: xml

    ...
    <app-group>
          <app id="app01">
              <label>Apêndice 1</label>
              <supplementary-material id="suppl01">
              <media xlink:href="1234-5678-rctb-45-05-0110-m01.avi" mimetype="video" mime-subtype="avi"/>
              </supplementary-material>
          </app>
    </app-group>
    ...


.. {"reviewed_on": "20170720", "by": "aline.cristina@scielo.org"}
