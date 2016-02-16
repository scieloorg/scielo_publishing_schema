.. _elemento-app:

<app>
-----

Aparece em
  :ref:`elemento-back`

Atributos obrigatório 
  1. id (Ver :ref:`sugestao-atribuicao-id`)
 
Ocorre
  Zero ou mais vezes

Utilizado para indicar a presença de um apêndice ao documento. Para a marcação
básica de um apêndice devemos levar em consideração duas tags importantes, a de
grupo de apêndice ``app-group`` e de apêndice propriamente dito
``<app>``. Deve ser inserida uma informação de
etiqueta :ref:`elemento-label` em ``<app>``.

 
Exemplo:
  
  app01... app10, app11;
 
Exemplo de Apêndice com texto:
 
.. code-block:: xml
 
    ...
    <app-group>
          <app id="app01">
              <label>Apêndice</label>
              <p>Vivamus fermentum elit et pellentesque iaculis. Curabitur egestas rhoncus purus quis iaculis. Sed laoreet id leo eu tristique. Etiam hendrerit nibh in tincidunt mattis. Sed et volutpat nulla, eget semper tellus. Nullam imperdiet fringilla diam, nec mollis elit sagittis a. Nam euismod sagittis posuere.</p>
          </app>
    </app-group>
    ...


Exemplo de Apêndice com imagem (Pode ser imagem de figura, tabela, quadro, equação e etc):
 
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

Exemplo de Apêndice com link externo (ext-link do tipo uri):
 
.. code-block:: xml
 
    ...
    <app-group>
        <app id="app01">                
            <label>Appendix 1</label>
            <p>Para mais informações <ext-link ext-link-type="uri" xlink:href="http://www.scielo.org">clique aqui</ext-link> para verificar o pdf.</p>
        </app>
    </app-group>
    ...
 
Exemplo de Apêndice com tabela:
 
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

Exemplo de Apêndice misto (figura mais tabela)
 
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
 
Exemplo de Apêndice misto (texto mais figura):
 
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
 
Exemplo de Apêndice com vídeo:

.. code-block:: xml
 
    ...
    <app-group>
          <app id="app01">
              <label>suplemento eletrônico</label>
              <supplementary-material id="suppl01">
              <media xlink:href="1234-5678-rctb-45-05-0110-m01.avi" mimetype="video" mime-subtype="avi"/>
              </supplementary-material>
          </app>
    </app-group>
    ...
 
.. note:: Obrigatoriamente o elemento :ref:`elemento-app` deve estar inserido em ``<app-group>``.,

