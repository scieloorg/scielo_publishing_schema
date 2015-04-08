Press Release
=============


Arquivos do tipo Press Release (relacionados à um artigo) devem apresentar o valor 
"in-brief" em ``@article-type`` e em ``//subj-group[@subj-group-type="heading"]/subject`` 
considerar "Press Release". Em volume e número considerar o mesmo do artigo 
relacionado ao Press Release, porém acrescentar em ``<issue>`` a informação "pr".
A tag ``<related-article>`` apresentará atributos e valores diferentes para esse tipo de arquivo. Veja:

.. code-block:: xml

    <article article-type="in-brief" 
             xmlns:xlink="http://www.w3.org/1999/xlink" 
             dtd-version="1.0" 
             specific-use="sps-1.2" 
             xml:lang="en">
        <front>
            <article-meta>
                <article-categories>
                    <subj-group subj-group-type="heading">
                        <subject>Press Release</subject>
                    </subj-group>
                </article-categories>
                <volume>21</volume>
                <issue>2 pr</issue>
                ...
                <permissions>
                    ...
                </permissions>
                <related-article related-article-type="article-reference" 
                                 id="pr01" 
                                 xlink:href="10.1590/S0104-59702014000200002" 
                                 ext-link-type="doi"/>
                <counts>
                    ...
                </counts>
                ...
            </article-meta>
            ...
        </front>
        ...
    </article>

Para Press Release o elemento ``<related-article>`` obrigatoriamente deve 
apresentar os seguintes atributos: ``@related-article-type``; ``@id``; ``@xlink:href`` 
e ``@ext-link-type="doi"``. Sendo que em ``@related-article-type`` o valor 
deverá ser ``"article-reference"``.


No artigo relacionado ao Press Release, inserir o seguinte elemento:

.. code-block:: xml
   
   ...
   </permissions>
   <related-article related-article-type="press-release" id="pr05" specific-use="processing-only"/>
   <abstract>
      ...

No artigo relacionado o elemento ``<related-article>`` obrigatoriamente deve apresentar os seguintes atributos: @related-article; @id; specific-use=". Sendo que em @related-article o valor deverá ser "press-release".

O Press Release de fascículo não apresenta o elemento ``<related-article>``. Considerar apenas o valor "in-brief" para @article-type, em ``<subject>`` inserir "Press Release" e no elemento ``<issue>`` adicionar a informação "pr". Veja:


.. code-block:: xml

    ...
    <article xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:mml="http://www.w3.org/1998/Math/MathML" dtd-version="1.0" article-type="in-brief" specific-use="sps-1.2" xml:lang="pt">
        ...
        <article-categories>
        <subj-group subj-group-type="heading">
            <subject>Press Release</subject>
            ...
        </pub-date>
      <volume>18</volume>
      <issue>50 pr</issue>
      ...

