.. _elemento-glossary:
 
<glossary>
----------

Aparece em
  :ref:`elemento-app`,
  :ref:`elemento-back`,
  :ref:`elemento-boxed-text`,
  ``<glossary>``


Ocorre
  Zero ou mais vezes


Elemento ``<glossary>`` é utilizado com a finalidade de descrever um glossário para documento. O conteúdo desse elemento geralmente é uma lista de definições, apresentando elementos de ``<def-list>``. Nesse caso, utilizar as regras de :ref:`elemento-def-list`.

Consulte a :ref:`sugestao-atribuicao-id` para instruções sobre a composição do atributo ``@id``.


Exemplo em back:
 
.. code-block:: xml

  <back>
    <glossary id="gl1">
      <label>Glossário</label>
      <def-list>
        <def-item>
          <term>PEL</term>
          <def>
            <p>Passivo Externo Líquido</p>
          </def>
        </def-item>
        <def-item>
          <term>PEL1</term>
          <def>
            <p>Passivo Externo Líquido1</p>
          </def>
        </def-item>
        <def-item>
          <term>PEL2</term>
          <def>
            <p>Passivo Externo Líquido2</p>
          </def>
        </def-item>
        <def-item>
          <term>DCCA</term>
          <def>
            <p>déficit acumulado na conta corrente do balanço de pagamentos</p>
          </def>
        </def-item>
      </def-list>
    </glossary>
  </back>


Exemplo em apêndice:
 
.. code-block:: xml

  <back>
    <app-group>
      <app id="app01">
      <label>Glossário</label>
        <glossary id="gl2">
          <def-list>
            <def-item>
              <term>Metabólito</term>
              <def>
                <p>É qualquer intermediário ou produto resultante do metabolismo.</p>
              </def>
            </def-item>
            <def-item>
              <term>Potência</term>
              <def>
                <p>É a dose de uma droga requerida para produzir um efeito específico de dada intensidade, comparada a um padrão de referência</p>
              </def>
            </def-item>
            <def-item>
              <term>Relação estrutura-atividade</term>
              <def>
                <p>É a relação entre estrutura química e atividade farmacológica para uma série de composto</p>
              </def>
            </def-item>
          </def-list>
        </glossary>
      </app>
    </app-group>
  </back>


Exemplo em boxed-text:
 
.. code-block:: xml

  ...
  <boxed-text id="bx2">
    <sec>
      <title>Box 1. De Humanis corporis fabrica libri septem, or the <italic>Fabrica</italic>, and others.</title>
      <p><italic>De humani corporis fabrica libri septem,  </italic> the <italic>Fabrica</italic>,1<sup>st  </sup>edition, came to light in 1543, by the printer Johannes Oporinus, from Basel. It is one of the most influential books on human anatomy, and considered one of the great scientific and artistic oeuvre of mankind. The <italic>Fabrica</italic> is illustrated with detailed illustrations, printed with woodcut engravings, in Venice, with the identity of the artist is uncertain.</p>
      <p>The <italic>Fabrica,</italic> 2<sup>nd</sup> edition, released in 1555, dedicated to Charles V, is considered more sumptuous than the 1<sup>st  </sup>one. There are also corrections, decrease of redundancies, as well as inclusion of physiological experiments, by means of nervous section, e.g., section of the recurrent nerve, with consequent laryngeal paralysis.</p>
      <p><italic>De Humani corporis fabrica librorum Epitome</italic>, the <italic>Epitome</italic>, printed in 1543, was intended by Vesalius to be a very brief descriptive book, being a remarkable condensation of the 1<sup>st</sup> edition of the main book. It has 6 chapters, the 5<sup>th</sup> concerned with "The brain and the nervous system".  </p>
    </sec>
    <glossary>
      <def-list id="d1">
        <title>Nomenclature</title>
        <def-item>
          <term>u</term>
          <def>
            <p>time domain vertical displacement</p>
          </def>
        </def-item>
        <def-item>
          <term>û</term>
          <def>
            <p>frequency domain vertical displacement</p>
          </def>
        </def-item>
        <def-item>
          <term>E</term>
          <def>
            <p>Young´s Modulus</p>
          </def>
        </def-item>
      </def-list>
    </glossary>
  </boxed-text>
 ...


No elemento ``glossary`` pode ser inserido o atributo ``@id``.  
Consulte a Sugestão de atribuição de @id para instruções sobre a composição do atributo @id.
 
O glossário pode ser apresentado como imagem, utilizando a tag ``<graphic>``,
ou como texto.

.. note:: Não inserir pontuação nos elementos ``<term>`` ou ``<def>``.

