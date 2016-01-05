.. _artigo-comentado:

Artigo Comentado
================

Artigos que apresentam resposta que está diretamente relacionado ao artigo 
principal devem apresentar um elemento :ref:`elemento-related-article`. 
Para isso, no artigo principal o atributo ``@article-type`` deve ter como valor 
**article-commentary**.


Em :ref:`elemento-response`, inserir o elemento :ref:`elemento-related-article`.
Exemplo:

.. code-block:: xml

   ...
   <article xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:mml="http://www.w3.org/1998/Math/MathML" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" specific-use="sps-1.2" dtd-version="1.0" article-type="article-commentary" xml:lang="en">
     ...
     <back>
       ...
     </back>
     <response response-type="reply" id="r01">
       <front-stub>
         ...
         <related-article related-article-type="commentary-article" id="r01" vol="109" page="87-92"/>
         <counts>
         ...
       </front-stub>
     </response>
   </article>


Para artigo relacionado, o elemento :ref:`elemento-related-article` deve 
apresentar os seguintes atributos: ``@related-article-type`` com o valor 
``commentary-article``; ``@id``; ``@vol`` e ``@page`` com a informação do 
intervalo de paginação do documento.

