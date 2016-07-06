.. _elemento-body:

<body>
======

Aparece em:

  :ref:`elemento-article`
  :ref:`elemento-sub-article`
  :ref:`elemento-response`

Ocorre:

  Uma vez


Compreende todo o conteúdo formal de desenvolvimento do artigo científico, ou seja texto, imagens, tabelas, figuras, gráficos, equações, fórmulas etc.

.. note:: Tabelas, figuras e equações que não estejam identificadas sob ``<app-group>`` devem ser inseridas obrigatoriamente após a primeira chamada no texto. Para material suplementar, analisar e identificar caso a caso.

Exemplo:

.. code-block:: xml

   ...
   <body>
        <sec sec-type="intro">
             <title>INTRODUCTION</title>
                  <p>Cyclin-dependent kinase-like 5 (CDKL5), which is also known as serine/threonine kinase 9 (STK9), is a protein kinase that is widely distributed in all tissues and highly expressed in the brain (<xref ref-type="bibr" rid="B10">Lin et al. 2005</xref>). CDKL5 is homologous to mitogen-activated protein kinases (MAPKs) and cyclin-dependent kinases (CDKs). Mutations in the gene that encodes CDKL5 cause intellectual disability, infantile spasms, and variant form of Rett syndrome, which is a neurodevelopmental disorder that is caused primarily by mutations in the methyl CpG binding protein 2 gene (<italic>MECP2</italic>) (<xref ref-type="bibr" rid="B5">Evans et al. 2005</xref>; <xref ref-type="bibr" rid="B7">Kalscheuer et al. 2003</xref>; <xref ref-type="bibr" rid="B11">Mari et al. 2005</xref>; <xref ref-type="bibr" rid="B17">Tao et al. 2004</xref>; <xref ref-type="bibr" rid="B18">Weaving et al. 2004</xref>). Because mutations in <italic>CDKL5</italic> and <italic>MECP2</italic> can cause similar phenotypes in patients, it is possible that CDKL5 and MeCP2 share the same molecular pathway in the central nervous system. Investigating the relationship of CDKL5 with MeCP2 and other interactors will help to further elucidate the critical roles of CDKL5 and MeCP2 in neural development, plasticity and neurological disorders. </p>
        </sec>
        <sec sec-type="materials|methods">
             <title>MATERIALS AND METHODS</title>
             <sec>
                  <title>Rat embryonic cortical neuron cultures</title>
                       <p>This study was approved by the Experimental Animal Ethics Committee of Peking University First Hospital (protocol number J201223). Primary cortical neurons were prepared from the brains of embryonic day 18 (E18) Sprague Dawley (SD) rats. Cell culture was performed as described previously (<xref ref-type="bibr" rid="B19">Zhang et al. 2006</xref>), with the following modifications. Cortical tissue from fetal rats was carefully dissected and digested with 0.25%Trypsin (Gibco) at 37℃ under 5%CO<sub>2</sub> for 5-8 min in 3.5 cm dishes. The digestion was terminated by the addition of 6-8 ml of Dulbecco Modified Eagle Medium (DMEM) (Gibco) supplemented with 10% FBS (Gibco). Then, the tissue was scattered with pipettes. The separated neurons were plated on poly-L-lysine-coated (Sigma) dishes and maintained first in DMEM with 10% FBS for 2-4 hours and then in Neurobasal<sup>(r)</sup> Medium (Gibco) supplemented with 2% B-27 Supplement (Gibco) and 1% L-Glutamine (200 mM, Gibco). Every other day, 50% of the medium volume was replaced.</p>
             </sec>
             <sec>
                  <title>Antibodies </title>
                  <p>The following primary antibodies were used in this study: rabbit polyclonal anti-CDKL5 (Abcam, ab191510), rabbit polyclonal anti-CDKL5 (Santa Cruz Biotechnology), mouse monoclonal anti-MeCP2 (Abcam, ab50005), mouse monoclonal anti-MAP2 (Abcam), rabbit monoclonal anti-Dnmt1 (Cell Signaling Technology), and rabbit monoclonal anti-β-Actin (Cell Signaling Technology). The secondary antibodies used were the HRP Goat anti-Mouse IgG Antibody (Abgent) and the HRP Goat anti-Rabbit IgG Antibody (Abgent). </p>
             </sec>
        </sec>
        <sec sec-type="results">
             <title>RESULTS</title>
             <p>To elucidate whether CDKL5 can bind to MeCP2 and Dnmt1 during rat neuronal in vitro differentiation, co-immunoprecipitation was performed. Incubation of polyclonal anti-CDKL5 with primary neuronal cell lysate samples at DIV4 and subsequent western blot analysis of MeCP2 and Dnmt1 revealed that an interaction occurs among endogenous CDKL5, MeCP2 and Dnmt1.</p>
        </sec>
   </body>
   ...


.. {"reviewed_on": "20160623", "by": "gandhalf_thewhite@hotmail.com"}
