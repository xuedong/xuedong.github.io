---
layout: post
title: Suites Automatiques
date:   2017-11-21 15:38:39
categories: formal_language
---

<html xml:lang="fr" >
<head><title>Suites automatiques</title>
<meta http-equiv="Content-Type" content="text/html; charset=iso-8859-1">
<meta name="generator" content="TeX4ht (http://www.tug.org/tex4ht/)">
<meta name="originator" content="TeX4ht (http://www.tug.org/tex4ht/)">
<!-- html -->
<meta name="src" content="suites_automatiques.tex">
<link rel="stylesheet" type="text/css" href="/static/css/suites_automatiques.css">
</head>


<body>
<div class="maketitle">

<h2 class="titleHead">Suites automatiques</h2>
      <div class="author" ><span
class="ecrm-1440">Xuedong Shang</span>
<br /><span
class="ecrm-1440">21 novembre 2017</span></div>
   </div>
   <h3 class="likesectionHead"><a
 id="x1-1000"></a>Table des matières</h3>
   <div class="tableofcontents">
   <span class="sectionToc" >1 <a
href="#x1-20001" id="QQ2-1-2">Définitions et exemples</a></span>
<br />   &#x00A0;<span class="subsectionToc" >1.1 <a
href="#x1-30001.1" id="QQ2-1-3">La suite de Thue-Morse</a></span>
<br />   &#x00A0;<span class="subsectionToc" >1.2 <a
href="#x1-40001.2" id="QQ2-1-5">La suite de Rudin-Shapiro</a></span>
<br />   <span class="sectionToc" >2 <a
href="#x1-50002" id="QQ2-1-7">Théorème de Cobham</a></span>
<br />   &#x00A0;<span class="subsectionToc" >2.1 <a
href="#x1-60002.1" id="QQ2-1-8">Le <span
class="cmmi-12">q</span>-noyau</a></span>
<br />   &#x00A0;<span class="subsectionToc" >2.2 <a
href="#x1-70002.2" id="QQ2-1-9">Théorème de Cobham</a></span>
<br />   <span class="sectionToc" >3 <a
href="#x1-80003" id="QQ2-1-10">Théorème de Christol</a></span>
<br />   &#x00A0;<span class="subsectionToc" >3.1 <a
href="#x1-90003.1" id="QQ2-1-11">Opérateur de Cartier</a></span>
<br />   &#x00A0;<span class="subsectionToc" >3.2 <a
href="#x1-100003.2" id="QQ2-1-12">Théorème de Christol</a></span>
<br />   <span class="sectionToc" >4 <a
href="#x1-110004" id="QQ2-1-13">Divers</a></span>
   </div>
   <div class="abstract">
   <div class="center">
<!--l. 74--><p class="noindent" >
<!--l. 74--><p class="noindent" ><span
class="ecbx-1095">R</span><span
class="ecbx-1095">ésum</span><span
class="ecbx-1095">é</span></div>
<!--l. 74--><p class="noindent" >


      <!--l. 75--><p class="indent" >    <span
class="ecrm-1095">Nous donnons ici, dans ce petit rapport, un premier traitement, tr</span><span
class="ecrm-1095">ès bref, des suites</span>
      <span
class="ecrm-1095">engendr</span><span
class="ecrm-1095">ées par un automate, mod</span><span
class="ecrm-1095">èle le plus simple de machine. Une suite automatique</span>
      <span
class="ecrm-1095">n&#8217;est pas n</span><span
class="ecrm-1095">écessairement tr</span><span
class="ecrm-1095">ès simple ou r</span><span
class="ecrm-1095">éguli</span><span
class="ecrm-1095">ère (ultimement p</span><span
class="ecrm-1095">ériodique par exemple)</span>
      <span
class="ecrm-1095">malgr</span><span
class="ecrm-1095">é le fait que cela soit d</span><span
class="ecrm-1095">ûe </span><span
class="ecrm-1095">à un automate dont les </span><span
class="ecrm-1095">états sont finis. La prem</span><span
class="ecrm-1095">ère</span>
      <span
class="ecrm-1095">partie de ce rapport est consacr</span><span
class="ecrm-1095">ée </span><span
class="ecrm-1095">à une premi</span><span
class="ecrm-1095">ère aper</span><span
class="ecrm-1095">çu des suites automatiques</span>
      <span
class="ecrm-1095">avec  quelques  exemples  connus.  Puis  nous  traiterons  quelques  caract</span><span
class="ecrm-1095">érisations  de</span>
      <span
class="ecrm-1095">l&#8217;automaticit</span><span
class="ecrm-1095">é  en  cherchant  les  liens  entre  les  automates  et  leurs  suite  engendr</span><span
class="ecrm-1095">ée</span>
      <span
class="ecrm-1095">associ</span><span
class="ecrm-1095">ée. </span><span
class="ecrm-1095">À la fin, nous donnerons certains r</span><span
class="ecrm-1095">ésultats divers sur les suites automatiques.</span>
</div>
<!--l. 78--><p class="noindent" >
   <h3 class="sectionHead"><span class="titlemark">1   </span> <a
 id="x1-20001"></a>Définitions et exemples</h3>
<!--l. 79--><p class="noindent" >On va commencer par définir la <span
class="ecti-1200">k</span>-automaticité et donner deux exemples de suites 2-automatiques.
Ces suites présenteront des similarité dont les liens seront développés dans la partie
suivante.
<!--l. 81--><p class="indent" >   Les automates que l&#8217;on va utiliser sont déterministes et complets. L&#8217;ensemble des états sera
noté <span
class="cmmi-12">Q </span>et au lieu d&#8217;avoir certains états finaux on dispose d&#8217;une fonction de sortie <span
class="cmmi-12">&#x03C4; </span>qui à chaque
état associe un valeur "de sortie".
   <div class="newtheorem">
<!--l. 83--><p class="noindent" ><span class="head">
<a
 id="x1-2001r1"></a>
<span
class="ecbx-1200">D</span><span
class="ecbx-1200">éfinition 1.</span>  </span>Un automate fini est la donnée de <span
class="cmsy-10x-x-120">{</span><span
class="cmmi-12">Q, </span><span
class="cmr-12">&#x03A3;</span><span
class="cmmi-12">,&#x03B4;,i,&#x03C4;, </span><span
class="cmr-12">&#x0393;</span><span
class="cmsy-10x-x-120">} </span>où <span
class="cmmi-12">Q </span>est l&#8217;ensemble des
états, <span
class="cmmi-12">i </span><span
class="cmsy-10x-x-120">&#x2208; </span><span
class="cmmi-12">Q </span>est l&#8217;état initial, <span
class="cmr-12">&#x03A3; </span>est l&#8217;alphabet d&#8217;entrée, <span
class="cmmi-12">&#x03B4; </span>la fonction de transition de <span
class="cmmi-12">Q </span><span
class="cmsy-10x-x-120">&#x00D7; </span><span
class="cmr-12">&#x03A3;</span>
dans <span
class="cmmi-12">Q</span>. <span
class="cmr-12">&#x0393; </span>l&#8217;alphabet de sortie et <span
class="cmmi-12">&#x03C4; </span>la fonction de sortie de <span
class="cmmi-12">Q </span>dans <span
class="cmr-12">&#x0393;</span>.
   </div>
<!--l. 89--><p class="indent" >   On remarque que pour obtenir un automate usuel, il suffit de prendre <span
class="cmr-12">&#x0393; = </span><span
class="cmsy-10x-x-120">{</span><span
class="cmr-12">0</span><span
class="cmmi-12">, </span><span
class="cmr-12">1</span><span
class="cmsy-10x-x-120">} </span>et de
considérer <span
class="cmmi-12">q </span>état final si et seulement si <span
class="cmmi-12">&#x03C4;</span><span
class="cmr-12">(</span><span
class="cmmi-12">q</span><span
class="cmr-12">) = 1</span>. Dans la suite, on n&#8217;introduit plus l&#8217;alphabet de
sortie <span
class="cmr-12">&#x0393; </span>dans l&#8217;automate s&#8217;il n&#8217;y pas d&#8217;ambiguïté.
   <div class="newtheorem">
<!--l. 91--><p class="noindent" ><span class="head">
<a
 id="x1-2002r2"></a>
<span
class="ecbx-1200">D</span><span
class="ecbx-1200">éfinition 2.</span>  </span>Soit <span
class="ecti-1200">k </span>un entier <span
class="cmsy-10x-x-120">&#x2265; </span>2. On dit qu&#8217;une suite (<span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub> est <span
class="ecti-1200">k</span>-automatique s&#8217;il existe un
automate <span
class="cmsy-10x-x-120"><img
src="/assets/suites_automatiques/cmsy10-c-41.png" alt="A" class="10-120x-x-41" /> </span>= <span
class="cmsy-10x-x-120">{</span><span
class="cmmi-12">Q, </span><span
class="cmr-12">&#x03A3;</span><span
class="cmmi-12">,&#x03B4;,i,&#x03C4;</span><span
class="cmsy-10x-x-120">} </span>tel que :


   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques0x.png" alt="&#x2200;n, &#x03C4;(&#x03B4;(i,&#x27E8;n&#x27E9;k)) = un
" class="math-display" ></center>
<!--l. 96--><p class="nopar" >
où <span
class="cmsy-10x-x-120">&#x27E8;</span><span
class="cmmi-12">n</span><span
class="cmsy-10x-x-120">&#x27E9;</span><sub><span
class="cmmi-8">k</span></sub> désigne l&#8217;écriture en base <span
class="ecti-1200">k </span>de n <span
class="ecbx-1200">à partir du chiffre de poids faible</span>. Si on lit dans
l&#8217;automate <span
class="cmsy-10x-x-120"><img
src="/assets/suites_automatiques/cmsy10-c-41.png" alt="A" class="10-120x-x-41" /> </span>la suite constituée des chiffres de <span
class="cmmi-12">n </span>en base <span
class="cmmi-12">k </span>à partir du chiffre de poids faible, on
tombe sur un état dont la valeur de sortie est <span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub>. Il est tout à fait naturel de considérer que la
fonction de sortie est à valeur dans le même ensemble que la suite et que les arêtes de l&#8217;automate
sont étiqueées par <span
class="cmsy-10x-x-120">{</span><span
class="cmr-12">0</span><span
class="cmmi-12">, </span><span
class="cmr-12">1</span><span
class="cmmi-12">,</span><img
src="/assets/suites_automatiques/suites_automatiques1x.png" alt="&#x22C5;&#x22C5;&#x22C5;"  class="@cdots" ><span style="margin-left:0.3em" class="thinspace"></span><span
class="cmmi-12">,k </span><span
class="cmsy-10x-x-120">- </span><span
class="cmr-12">1</span><span
class="cmsy-10x-x-120">}</span>.
   </div>
   <div class="newtheorem">
<!--l. 105--><p class="noindent" ><span class="head">
<a
 id="x1-2003r3"></a>
<span
class="ecti-1200">Remarque </span>3<span
class="ecti-1200">.</span>  </span>Un tel automate est appelé <span
class="cmmi-12">k</span>-automate, et on peut ainsi dire qu&#8217;une suite est
<span
class="cmmi-12">k</span>-automatique si elle est engendrée par un <span
class="cmmi-12">k</span>-automate.
   </div>
<!--l. 110--><p class="noindent" >
   <h4 class="subsectionHead"><span class="titlemark">1.1   </span> <a
 id="x1-30001.1"></a>La suite de Thue-Morse</h4>
<!--l. 111--><p class="noindent" >La suite de Thue-Morse (appelée souvent suite de Prouhet-Thue-Morse chez les francophones) fut
décrite pour la première fois par le mathématicien français Eugène Prouhet en 1851. Il la utilisa
pour donner une solution à un problème de théorie des nombres qui s&#8217;appelle le problème de
Prouhet-Tarry-Escott. La suite fut redécouverte par le mathématicien norvégien Axel Thue dans
un article publié en 1906 qui est l&#8217;article fondateur de la combinatoire des mots. Puis Marston
Morse, en 1922, donna une nouvelle interprétation de la suite, dans le cadre de la géométrie
différentielle.
   <div class="newtheorem">
<!--l. 113--><p class="noindent" ><span class="head">
<a
 id="x1-3001r4"></a>
<span
class="ecbx-1200">D</span><span
class="ecbx-1200">éfinition 4.</span>  </span>On définit la suite de Thue-Morse, <span
class="cmr-12">(</span><span
class="cmmi-12">t</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub> de la façon suivante :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques2x.png" alt="       t0 = 0,
   &#x2200;n &#x2265; 0,t2n = tn,
&#x2200;n &#x2265;  0,t2n+1 = 1 - tn


" class="math-display" ></center>
<!--l. 121--><p class="nopar" >
On donne ses premiers termes ci-dessous : 0110100110<span
class="cmmi-12">&#x2026;</span>
   </div>
<!--l. 125--><p class="indent" >   On voit que, d&#8217;après la définition de <span
class="cmmi-12">t</span>, <span
class="cmmi-12">t</span><sub><span
class="cmmi-8">n</span></sub> correspond à la somme des chiffres dans l&#8217;écriture en base
2 de <span
class="cmmi-12">n </span>modulo 2. La suite de Thue-Morse est ainsi 2-automatique ; elle est engendrée par l&#8217;automate
suivant <span class="footnote-mark"><a
href="/assets/suites_automatiques/suites_automatiques2.html#fn1x0"><sup class="textsuperscript">1</sup></a></span><a
 id="x1-3002f1"></a>  :
<!--l. 127--><p class="indent" >   <hr class="figure"><div class="figure"
>


<a
 id="x1-30031"></a>


<div class="center">
<!--l. 128--><p class="noindent" >
<!--l. 130--><p class="center" ><img
src="/assets/suites_automatiques/suites_automatiques3x.png" alt="PICT" >
</div>
<br /> <div class="caption"><span class="id"><span
class="eccc1200-"><span
class="small-caps">f</span><span
class="small-caps">i</span><span
class="small-caps">g</span><span
class="small-caps">u</span><span
class="small-caps">r</span><span
class="small-caps">e</span></span>&#x00A0;1: </span><span  
class="content">L&#8217;automate de Thue-Morse.</span></div><!--tex4ht:label?: x1-30031 -->


<!--l. 142--><p class="indent" >   </div><hr class="endfigure">
<!--l. 144--><p class="indent" >   Donnons une autre manière pour définir la suite de Thue-Morse. On considère le morphisme
2-uniforme <span class="footnote-mark"><a
href="/assets/suites_automatiques/suites_automatiques3.html#fn2x0"><sup class="textsuperscript">2</sup></a></span><a
 id="x1-3004f2"></a>
<span
class="cmmi-12">&#x03C3; </span><span
class="cmr-12">: </span><span
class="cmsy-10x-x-120">{</span><span
class="cmr-12">0</span><span
class="cmmi-12">, </span><span
class="cmr-12">1</span><span
class="cmsy-10x-x-120">}</span><sup><span
class="cmsy-8"></span></sup> <span
class="cmsy-10x-x-120">&#x2192;{</span><span
class="cmr-12">0</span><span
class="cmmi-12">, </span><span
class="cmr-12">1</span><span
class="cmsy-10x-x-120">}</span><sup><span
class="cmsy-8"></span></sup> donné par :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques4x.png" alt="&#x03C3;(0) = 01
&#x03C3;(1) = 10
" class="math-display" ></center>
<!--l. 150--><p class="nopar" >
La suite <span
class="cmr-12">(</span><span
class="cmmi-12">&#x03C3;</span><sup><span
class="cmmi-8">n</span></sup><span
class="cmr-12">(0))</span><sub>
<span
class="cmmi-8">n</span></sub> converge simplement vers <span
class="cmmi-12">t</span>. Il en résulte que <span
class="cmmi-12">t </span>est point fixe de <span
class="cmmi-12">&#x03C3;</span>.
   <h4 class="subsectionHead"><span class="titlemark">1.2   </span> <a
 id="x1-40001.2"></a>La suite de Rudin-Shapiro</h4>
<!--l. 154--><p class="noindent" >La suite de Rudin-Shapiro, aussi appelée la suite de Golay-Rudin-Shapiro est une suite
automatique nommée par Marcel Golay, Walter Rudin et Harold S.Shapiro, qui l&#8217;ont décourvert
indépendemment.
   <div class="newtheorem">
<!--l. 156--><p class="noindent" ><span class="head">
<a
 id="x1-4001r5"></a>
<span
class="ecbx-1200">D</span><span
class="ecbx-1200">éfinition 5.</span>  </span>On définit la suite de Rudin-Shapiro <span
class="cmr-12">(</span><span
class="cmmi-12">r</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub> de la façon suivante :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques5x.png" alt="         r0 = 0,
    &#x2200;n  &#x2265; 0,r   = r ,
             2n    n
   &#x2200;n  &#x2265; 0,r4n+1 = rn,
&#x2200;n &#x2265;  0,r4n+3 = 1 - r2n+1.
" class="math-display" ></center>
<!--l. 165--><p class="nopar" >
Ses premiers termes sont les suivants : 000100100001<span
class="cmmi-12">&#x2026;</span>
   </div>
<!--l. 169--><p class="indent" >   Il s&#8217;agit encore d&#8217;une suite 2-automatique. Elle est engendrée par l&#8217;automate suivant :
<!--l. 171--><p class="indent" >   <hr class="figure"><div class="figure"
>


<a
 id="x1-40022"></a>


<div class="center">
<!--l. 172--><p class="noindent" >
<!--l. 174--><p class="center" ><img
src="/assets/suites_automatiques/suites_automatiques6x.png" alt="PICT" >
</div>
<br /> <div class="caption"><span class="id"><span
class="eccc1200-"><span
class="small-caps">f</span><span
class="small-caps">i</span><span
class="small-caps">g</span><span
class="small-caps">u</span><span
class="small-caps">r</span><span
class="small-caps">e</span></span>&#x00A0;2: </span><span  
class="content">L&#8217;automate de Rudin-Shapiro.</span></div><!--tex4ht:label?: x1-40022 -->


<!--l. 192--><p class="indent" >   </div><hr class="endfigure">
<!--l. 194--><p class="indent" >   Cette suite donne le nombre d&#8217;occurrences de "11" dans l&#8217;écriture de <span
class="cmmi-12">n </span>en base 2, le tout
modulo 2. On ne peut pas trouver comme pour la suite de Thue-Morse un morphisme 2-uniforme
dont la suite soit point fixe. Il faut d&#8217;abord "agrandir" l&#8217;alphabet. Définissons un morphisme <span
class="cmmi-12">&#x03C3; </span>sur
l&#8217;alphabet <span
class="cmsy-10x-x-120">{</span><span
class="cmmi-12">A,B,C,D</span><span
class="cmsy-10x-x-120">} </span>par :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques7x.png" alt="&#x03C3;(A ) = AB

&#x03C3;(B ) = AC
&#x03C3;(C ) = DB
&#x03C3;(D ) = DC
" class="math-display" ></center>
<!--l. 202--><p class="nopar" >
La limite simple de <span
class="cmmi-12">&#x03C3;</span><sup><span
class="cmmi-8">n</span></sup><span
class="cmr-12">(</span><span
class="cmmi-12">A</span><span
class="cmr-12">) </span>est de la forme suivante :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques8x.png" alt="ABACABDBABACDCAC             &#x22C5;&#x22C5;&#x22C5;
" class="math-display" ></center>
<!--l. 208--><p class="nopar" >
La suite de Rudin-Shapiro s&#8217;obtient alors en prenant l&#8217;image du point fixe pour <span
class="cmmi-12">&#x03C3; </span>par la projection
<span
class="cmmi-12">&#x03C0; </span><span
class="cmr-12">: </span><span
class="cmsy-10x-x-120">{</span><span
class="cmmi-12">A,B,C,D</span><span
class="cmsy-10x-x-120">}&#x2192;{</span><span
class="cmr-12">0</span><span
class="cmmi-12">, </span><span
class="cmr-12">1</span><span
class="cmsy-10x-x-120">} </span>définie par :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques9x.png" alt="&#x03C0; (A ) = &#x03C0;(B ) = 0

&#x03C0;(C ) = &#x03C0;(D ) = 1
" class="math-display" ></center>
<!--l. 215--><p class="nopar" >
   <h3 class="sectionHead"><span class="titlemark">2   </span> <a
 id="x1-50002"></a>Théorème de Cobham</h3>
<!--l. 219--><p class="noindent" >
   <h4 class="subsectionHead"><span class="titlemark">2.1   </span> <a
 id="x1-60002.1"></a>Le <span
class="cmmi-12">q</span>-noyau</h4>
<!--l. 221--><p class="noindent" >Au niveau des ressemblances entre les deux suites, il est pertinent d&#8217;introduire certaines
définitions.
   <div class="newtheorem">
<!--l. 223--><p class="noindent" ><span class="head">


<a
 id="x1-6001r6"></a>
<span
class="ecbx-1200">D</span><span
class="ecbx-1200">éfinition 6.</span>  </span>Soit <span
class="cmmi-12">u </span>une suite donnée et <span
class="cmmi-12">k </span><span
class="cmsy-10x-x-120">&#x2208; </span><span
class="msbm-10x-x-120">&#x2115;</span>. le <span
class="cmmi-12">q</span>-noyau que l&#8217;on notera désormais <span
class="cmmi-12">K</span><sub><span
class="cmmi-8">u</span></sub><sup><span
class="cmr-8">(</span><span
class="cmmi-8">q</span><span
class="cmr-8">)</span></sup> (ou
plus simplement <span
class="cmmi-12">K</span><sub><span
class="cmmi-8">u</span></sub> s&#8217;il n&#8217;y a pas d&#8217;ambiguïté) est :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques10x.png" alt="  (q)        &#x03B1;
Ku  =  {(u(q n + r))n | &#x03B1; &#x2208; &#x2115;, 0 &#x2264; r &#x003C; &#x03B1; }
" class="math-display" ></center>
<!--l. 228--><p class="nopar" >
   </div>
<!--l. 231--><p class="indent" >   Le <span
class="cmmi-12">q</span>-noyau nous intéresse lorsqu&#8217;il n&#8217;est pas "trop gros" et qu&#8217;il contraint les suites à coïncider
avec leurs propres sous-suites extraites de pas <span
class="cmmi-12">q</span><sup><span
class="cmmi-8">k</span></sup>. Or il y a au plus un nombre dénombrable de telle
suite, on s&#8217;intéresse alors au cas fini.
<!--l. 233--><p class="indent" >   Lorsque le <span
class="cmmi-12">q</span>-noyau est fini, il est facile de le calculer par machine. Il suffit de construire
récursivement les ensembles <span
class="cmmi-12">X</span><sub><span
class="cmmi-8">k</span></sub> donnés par :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques11x.png" alt="X0 =  {(an)n&#x2265;0}etXk+1  = Xk &#x222A; {(bqn+r)n|(bn)n &#x2208; Xk, r &#x2208; [0,q - 1]}.  " class="math-display" ></center>
S&#8217;il existe <span
class="cmmi-12">k </span>tel que <span
class="cmmi-12">X</span><sub><span
class="cmmi-8">k</span></sub> <span
class="cmr-12">= </span><span
class="cmmi-12">X</span><sub><span
class="cmmi-8">k</span><span
class="cmr-8">+1</span></sub> alors c&#8217;est la valeur du <span
class="cmmi-12">q</span>-noyau, ce dernier est alors
fini.
   <div class="newtheorem">
<!--l. 237--><p class="noindent" ><span class="head">
<a
 id="x1-6002r7"></a>
<span
class="ecbx-1200">Proposition 7.</span>  </span><span
class="ecti-1200">Le 2-noyau de la suite de Thue-Morse est fini.</span>
   </div>
<!--l. 241--><p class="indent" >
   <div class="proof">
<!--l. 242--><p class="indent" >   <span class="head">


<span
class="ecti-1200">D</span><span
class="ecti-1200">émonstration.</span> </span>On a
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques12x.png" alt="X1 = { (t2n)n,(t2n+1)n} = {(tn)n,(1 - tn)n}
" class="math-display" ></center> Donc <span
class="cmmi-12">K</span><sub><span
class="cmmi-8">t</span></sub> <span
class="cmr-12">= </span><span
class="cmsy-10x-x-120">{</span><span
class="cmr-12">(</span><span
class="cmmi-12">t</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmmi-12">, </span><span
class="cmr-12">(1 </span><span
class="cmsy-10x-x-120">- </span><span
class="cmmi-12">t</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmsy-10x-x-120">} </span>dont le 2-noyau est fini.                                               __
   </div>
   <div class="newtheorem">
<!--l. 246--><p class="noindent" ><span class="head">
<a
 id="x1-6003r8"></a>
<span
class="ecbx-1200">Proposition 8.</span>  </span><span
class="ecti-1200">Le 2-noyau de la suite de Rudin-Shapiro est fini.</span>
   </div>
<!--l. 250--><p class="indent" >
   <div class="proof">
<!--l. 251--><p class="indent" >   <span class="head">
<span
class="ecti-1200">D</span><span
class="ecti-1200">émonstration.</span> </span>On a
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques13x.png" alt="X1 =  {(rn)n, (r2n+1)n}
" class="math-display" ></center> Puis


   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques14x.png" alt="X2  = {(rn)n,(r2n+1)n,(r4n+3)n}
" class="math-display" ></center> Ensuite
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques15x.png" alt="X3 =  {(rn)n,(r2n+1 )n, (r4n+3)n,(r8n+3)n}
" class="math-display" ></center> Enfin
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques16x.png" alt="X4 =  {(rn)n,(r2n+1)n,(r4n+3 )n,(r8n+3)n} = X3
" class="math-display" ></center> D&#8217;où le 2-noyau <span
class="cmmi-12">K</span><sub><span
class="cmmi-8">r</span></sub> <span
class="cmr-12">= </span><span
class="cmsy-10x-x-120">{</span><span
class="cmr-12">(</span><span
class="cmmi-12">r</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmmi-12">, </span><span
class="cmr-12">(</span><span
class="cmmi-12">r</span><sub><span
class="cmr-8">2</span><span
class="cmmi-8">n</span><span
class="cmr-8">+1</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmmi-12">, </span><span
class="cmr-12">(</span><span
class="cmmi-12">r</span><sub><span
class="cmr-8">4</span><span
class="cmmi-8">n</span><span
class="cmr-8">+3</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmmi-12">, </span><span
class="cmr-12">(</span><span
class="cmmi-12">r</span><sub><span
class="cmr-8">8</span><span
class="cmmi-8">n</span><span
class="cmr-8">+3</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmsy-10x-x-120">} </span>est fini.                               __
   </div>
<!--l. 258--><p class="noindent" >
   <h4 class="subsectionHead"><span class="titlemark">2.2   </span> <a
 id="x1-70002.2"></a>Théorème de Cobham</h4>
<!--l. 260--><p class="noindent" >Donnons maintenant un lien avec les morphismes <span
class="cmmi-12">q</span>-uniformes.
   <div class="newtheorem">
<!--l. 262--><p class="noindent" ><span class="head">
<a
 id="x1-7001r9"></a>


<span
class="ecbx-1200">D</span><span
class="ecbx-1200">éfinition 9.</span>  </span>Une suite <span
class="cmmi-12">u </span>à valeur dans un alphabet <span
class="cmr-12">&#x03A3; </span>est dite <span
class="ecti-1200">l&#8217;image d&#8217;un point fixe d&#8217;un</span>
<span
class="ecti-1200">point fixe d&#8217;un morphisme k-uniforme </span><span
class="cmmi-12">&#x03C3; </span><span
class="cmr-12">: &#x03A3;</span><sup><span
class="cmsy-8">&#x2032;</span></sup> <span
class="cmsy-10x-x-120">&#x2192; </span><span
class="cmr-12">&#x03A3;</span><sup><span
class="cmsy-8">&#x2032;</span></sup> s&#8217;il existe <span
class="cmmi-12">w </span><span
class="cmsy-10x-x-120">&#x2208; </span><span
class="cmr-12">&#x03A3;</span><sup><span
class="cmsy-8">&#x2032;</span><span
class="msbm-10x-x-80">&#x2115;</span></sup>  point fixe de <span
class="cmmi-12">&#x03C3; </span>et <span
class="cmmi-12">&#x03C0;</span>
projection de <span
class="cmr-12">&#x03A3;</span><sup><span
class="cmsy-8">&#x2032;</span></sup> dans <span
class="cmr-12">&#x03A3; </span>tels que <span
class="cmsy-10x-x-120">&#x2200;</span><span
class="cmmi-12">n </span><span
class="cmsy-10x-x-120">&#x2208; </span><span
class="msbm-10x-x-120">&#x2115;</span><span
class="cmmi-12">,u</span><sub>
<span
class="cmmi-8">n</span></sub> <span
class="cmr-12">= </span><span
class="cmmi-12">&#x03C0;</span><span
class="cmr-12">(</span><span
class="cmmi-12">w</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span>.
   </div>
<!--l. 269--><p class="indent" >   En écrivant le fait d&#8217;être un point fixe lettre à lettre on obtient la caractérisation suivante qui
sera souvent utile.
   <div class="newtheorem">
<!--l. 271--><p class="noindent" ><span class="head">
<a
 id="x1-7002r10"></a>
<span
class="ecbx-1200">Lemme 10.</span>  </span> <span
class="ecti-1200">Si </span><span
class="cmmi-12">&#x03C3; </span><span
class="ecti-1200">est un morphisme </span><span
class="cmmi-12">q</span><span
class="ecti-1200">-uniforme d&#8217;un alphabet </span><span
class="cmr-12">&#x03A3; </span><span
class="ecti-1200">dans lui m</span><span
class="ecti-1200">ême, alors </span><span
class="cmmi-12">w </span><span
class="ecti-1200">en est un</span>
<span
class="ecti-1200">point fixe si et seulement si :</span>
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques17x.png" alt="&#x2200;n  &#x2208; &#x2115;,&#x2200;r &#x2264;  q,&#x03C3;(w  ) =  w
                    n r    qn+r
" class="math-display" ></center>
<!--l. 276--><p class="nopar" >
   </div>
<!--l. 279--><p class="indent" >   Le lemme est facile à démontrer d&#8217;une façon très intuitive. Les deux suites <span
class="cmmi-12">t </span>et <span
class="cmmi-12">r </span>sont image de
point fixe d&#8217;un morphisme 2-uniforme. On est à présent en mesure de donner une généralisation
qui porte le nom de Cobham :
   <div class="newtheorem">
<!--l. 281--><p class="noindent" ><span class="head">
<a
 id="x1-7003r11"></a>
<span
class="ecbx-1200">Proposition 11 </span>(Cobham, 1972)<span
class="ecbx-1200">.</span>  </span><span
class="ecti-1200">Soient </span><span
class="cmmi-12">q </span><span
class="cmsy-10x-x-120">&#x2208;</span> <span
class="msbm-10x-x-120">&#x2115;</span><sup><span
class="cmsy-8"></span></sup> <span
class="ecti-1200">et </span><span
class="cmr-12">(</span><span
class="cmmi-12">u</span><sub>
<span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub> <span
class="ecti-1200">une suite </span><span
class="ecti-1200">à valeurs dans </span><span
class="cmsy-10x-x-120">{</span><span
class="cmr-12">0</span><span
class="cmmi-12">,</span><img
src="/assets/suites_automatiques/suites_automatiques18x.png" alt="&#x22C5;&#x22C5;&#x22C5;"  class="@cdots" ><span style="margin-left:0.3em" class="thinspace"></span><span
class="cmmi-12">,q </span><span
class="cmsy-10x-x-120">- </span><span
class="cmr-12">1</span><span
class="cmsy-10x-x-120">}</span><span
class="ecti-1200">,</span>
<span
class="ecti-1200">alors les trois assertions suivantes sont </span><span
class="ecti-1200">équivalentes :</span>
       <ol  class="enumerate1" >
       <li
  class="enumerate" id="x1-7005x1"><span
class="ecti-1200">la suite </span><span
class="cmr-12">(</span><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub> <span
class="ecti-1200">est </span><span
class="cmmi-12">q</span><span
class="ecti-1200">-automatique</span>
       </li>
       <li
  class="enumerate" id="x1-7007x2"><span
class="ecti-1200">le </span><span
class="cmmi-12">q</span><span
class="ecti-1200">-noyau </span><span
class="cmmi-12">K</span><sub><span
class="cmmi-8">u</span></sub> <span
class="ecti-1200">de </span><span
class="cmmi-12">u </span><span
class="ecti-1200">est fini</span>
       </li>
       <li
  class="enumerate" id="x1-7009x3"><span
class="ecti-1200">la suite </span><span
class="cmr-12">(</span><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub> <span
class="ecti-1200">est image d&#8217;un point fixe d&#8217;un morphisme </span><span
class="cmmi-12">q</span><span
class="ecti-1200">-uniforme</span></li></ol>
   </div>
<!--l. 291--><p class="indent" >


   <div class="proof">
<!--l. 292--><p class="indent" >   <span class="head">
<span
class="ecti-1200">D</span><span
class="ecti-1200">émonstration.</span> </span><span
class="cmmi-12">i</span><span
class="cmr-12">) </span><span
class="cmsy-10x-x-120">&#x21D2; </span><span
class="cmmi-12">ii</span><span
class="cmr-12">)</span>. On dispose d&#8217;un <span
class="cmmi-12">k</span>-automate <span
class="cmsy-10x-x-120"><img
src="/assets/suites_automatiques/cmsy10-c-41.png" alt="A" class="10-120x-x-41" /> </span>= <span
class="cmsy-10x-x-120">{</span><span
class="cmmi-12">Q, </span><span
class="cmr-12">&#x03A3;</span><span
class="cmmi-12">,&#x03B4;,i,&#x03C4;</span><span
class="cmsy-10x-x-120">} </span>qui engendre <span
class="cmr-12">(</span><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub>.
On rappelle que <span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub> <span
class="cmr-12">= </span><span
class="cmmi-12">&#x03C4;</span><span
class="cmr-12">(</span><span
class="cmmi-12">&#x03B4;</span><span
class="cmr-12">(</span><span
class="cmmi-12">q</span><sub><span
class="cmr-8">0</span></sub><span
class="cmmi-12">,</span><span
class="cmsy-10x-x-120">&#x27E8;</span><span
class="cmmi-12">n</span><span
class="cmsy-10x-x-120">&#x27E9;</span><sub><span
class="cmmi-8">q</span></sub><span
class="cmr-12">))</span>. Or pour <span
class="cmmi-12">i </span><span
class="cmsy-10x-x-120">&#x2265; </span><span
class="cmr-12">0</span><span
class="cmmi-12">, </span><span
class="cmr-12">0 </span><span
class="cmsy-10x-x-120">&#x2264; </span><span
class="cmmi-12">j &#x003C; i</span>, <span
class="cmr-12">(</span><span
class="cmmi-12">q</span><sup><span
class="cmmi-8">i</span></sup><span
class="cmmi-12">n</span><span
class="cmr-12">+</span><span
class="cmmi-12">j</span><span
class="cmr-12">)</span><sub>
<span
class="cmmi-8">q</span></sub> <span
class="cmr-12">= </span><span
class="cmmi-12">j</span><span
class="cmr-12">0</span><span
class="cmmi-12">&#x2026;</span><span
class="cmr-12">0</span><span
class="cmsy-10x-x-120">&#x27E8;</span><span
class="cmmi-12">n</span><span
class="cmsy-10x-x-120">&#x27E9;</span><sub><span
class="cmmi-8">q</span></sub> <span
class="cmr-12">= </span><span
class="cmmi-12">w</span><span
class="cmsy-10x-x-120">&#x27E8;</span><span
class="cmmi-12">n</span><span
class="cmsy-10x-x-120">&#x27E9;</span><sub><span
class="cmmi-8">q</span></sub>
où l&#8217;on note <span
class="cmmi-12">w </span><span
class="cmr-12">= </span><span
class="cmmi-12">j</span><span
class="cmr-12">0</span><sup><span
class="cmmi-8">i</span><span
class="cmsy-8">-</span><span
class="cmr-8">1</span></sup>. On a alors <span
class="cmmi-12">u</span><sub>
<span
class="cmmi-8">q</span><sup><span
class="cmmi-6">i</span></sup><span
class="cmmi-8">n</span><span
class="cmr-8">+</span><span
class="cmmi-8">j</span></sub> <span
class="cmr-12">= </span><span
class="cmmi-12">&#x03C4;</span><span
class="cmr-12">(</span><span
class="cmmi-12">&#x03B4;</span><span
class="cmr-12">(</span><span
class="cmmi-12">q</span><sub><span
class="cmr-8">0</span></sub><span
class="cmmi-12">,w</span><span
class="cmsy-10x-x-120">&#x27E8;</span><span
class="cmmi-12">n</span><span
class="cmsy-10x-x-120">&#x27E9;</span><sub><span
class="cmmi-8">q</span></sub><span
class="cmr-12">)) = </span><span
class="cmmi-12">&#x03C4;</span><span
class="cmr-12">(</span><span
class="cmmi-12">&#x03B4;</span><span
class="cmr-12">(</span><span
class="cmmi-12">&#x03B4;</span><span
class="cmr-12">(</span><span
class="cmmi-12">q</span><sub><span
class="cmr-8">0</span></sub><span
class="cmmi-12">,w</span><span
class="cmr-12">)</span><span
class="cmmi-12">,</span><span
class="cmsy-10x-x-120">&#x27E8;</span><span
class="cmmi-12">n</span><span
class="cmsy-10x-x-120">&#x27E9;</span><sub><span
class="cmmi-8">q</span></sub><span
class="cmr-12">))</span><span
class="cmmi-12">.</span>
<!--l. 298--><p class="indent" >   Comme il y a un nombre fini d&#8217;états, ainsi que <span
class="cmmi-12">&#x03B4;</span><span
class="cmr-12">(</span><span
class="cmmi-12">q</span><sub><span
class="cmr-8">0</span></sub><span
class="cmmi-12">,w</span><span
class="cmr-12">) </span>selon que <span
class="cmmi-12">i </span>et <span
class="cmmi-12">j </span>varient. Le <span
class="cmmi-12">q</span>-noyau
est alors bien fini.
<!--l. 301--><p class="indent" >   <span
class="cmmi-12">ii</span><span
class="cmr-12">)  </span><span
class="cmsy-10x-x-120">&#x21D2; </span><span
class="cmmi-12">iii</span><span
class="cmr-12">)</span>. Le <span
class="cmmi-12">q</span>-noyau étant fini supposé de cardinal <span
class="cmmi-12">d</span>, on peut alors écrire <span
class="cmmi-12">K</span><sub><span
class="cmmi-8">u</span></sub>  <span
class="cmr-12">=</span>
<span
class="cmsy-10x-x-120">{</span><span
class="cmr-12">(</span><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><sup><span
class="cmr-8">(1)</span></sup><span
class="cmr-12">)</span><sub>
<span
class="cmmi-8">n</span></sub><span
class="cmmi-12">, </span><span
class="cmr-12">(</span><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><sup><span
class="cmr-8">(2)</span></sup><span
class="cmr-12">)</span><sub>
<span
class="cmmi-8">n</span></sub><span
class="cmmi-12">,</span><span
class="cmmi-12">&#x2026;</span><span
class="cmmi-12">, </span><span
class="cmr-12">(</span><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><sup><span
class="cmr-8">(</span><span
class="cmmi-8">d</span><span
class="cmr-8">)</span></sup><span
class="cmr-12">)</span><sub>
<span
class="cmmi-8">n</span></sub><span
class="cmsy-10x-x-120">} </span>avec <span
class="cmr-12">(</span><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><sup><span
class="cmr-8">(1)</span></sup><span
class="cmr-12">)</span><sub>
<span
class="cmmi-8">n</span></sub> <span
class="cmr-12">= (</span><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub>. On définit une suite <span
class="cmr-12">(</span><span
class="cmmi-12">V</span> <sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub> sur l&#8217;alphabet
<span
class="cmr-12">&#x03A3;</span><sup><span
class="cmmi-8">d</span></sup> par <span
class="cmsy-10x-x-120">&#x2200;</span><span
class="cmmi-12">n </span><span
class="cmsy-10x-x-120">&#x2208; </span><span
class="msbm-10x-x-120">&#x2115;</span>, <span
class="cmmi-12">V</span> <sub>
<span
class="cmmi-8">n</span></sub> <span
class="cmr-12">= (</span><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><sup><span
class="cmr-8">(1)</span></sup><span
class="cmmi-12">,u</span><sub>
<span
class="cmmi-8">n</span></sub><sup><span
class="cmr-8">(2)</span></sup><span
class="cmmi-12">,</span><span
class="cmmi-12">&#x2026;</span><span
class="cmmi-12">,u</span><sub>
<span
class="cmmi-8">n</span></sub><sup><span
class="cmr-8">(</span><span
class="cmmi-8">d</span><span
class="cmr-8">)</span></sup><span
class="cmr-12">)</span>. Pour <span
class="cmmi-12">j </span><span
class="cmsy-10x-x-120">&#x2208; </span><span
class="cmr-12">[0</span><span
class="cmmi-12">,q</span><span
class="cmsy-10x-x-120">-</span><span
class="cmr-12">1]</span>, on dispose d&#8217;une application :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques19x.png" alt="      d     d
&#x03C3;j : &#x03A3;  &#x2192;  &#x03A3;  telleque &#x2200;n  &#x2208; &#x2115;,Vqn+j =  &#x03C3;j(Vn)
" class="math-display" ></center> On considère le morphisme <span
class="cmmi-12">&#x03C3; </span><span
class="cmr-12">: (&#x03A3;</span><sup><span
class="cmmi-8">d</span></sup><span
class="cmr-12">)</span><sup><span
class="cmsy-8"></span></sup> <span
class="cmsy-10x-x-120">&#x2192; </span><span
class="cmr-12">(&#x03A3;</span><sup><span
class="cmmi-8">d</span></sup><span
class="cmr-12">)</span><sup><span
class="cmsy-8"></span></sup> défini par :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques20x.png" alt="        d
&#x2200;V  &#x2208; &#x03A3;  ,&#x03C3;(V ) = &#x03C3;0(V)&#x03C3;1 (V )&#x22C5;&#x22C5;&#x22C5; &#x03C3;q-1(V).
" class="math-display" ></center>
<!--l. 309--><p class="indent" >   Il est aisé à voir que le morphisme <span
class="cmmi-12">h </span>est <span
class="cmmi-12">q</span>-uniforme, et par le <span
class="ecbx-1200">lemme </span><a
href="#x1-7002r10"><span
class="ecbx-1200">10</span><!--tex4ht:ref: uniforme --></a>, la suite <span
class="cmr-12">(</span><span
class="cmmi-12">V</span> <sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub>est
point fixe de <span
class="cmmi-12">&#x03C3;</span>. <span
class="cmr-12">(</span><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub> est l&#8217;image de <span
class="cmr-12">(</span><span
class="cmmi-12">V</span> <sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub> par la projection sur la première coordonnée.
<!--l. 313--><p class="indent" >   <span
class="cmmi-12">iii</span><span
class="cmr-12">) </span><span
class="cmsy-10x-x-120">&#x21D2; </span><span
class="cmmi-12">i</span><span
class="cmr-12">)</span>. On pose <span
class="cmr-12">(</span><span
class="cmmi-12">v</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub> <span
class="cmr-12">= </span><span
class="cmmi-12">&#x03C3;</span><sup><span
class="cmsy-8">&#x221E;</span></sup><span
class="cmr-12">(</span><span
class="cmmi-12">v</span><span
class="cmr-12">)</span><span class="footnote-mark"><a
href="/assets/suites_automatiques/suites_automatiques4.html#fn3x0"><sup class="textsuperscript">3</sup></a></span><a
 id="x1-7010f3"></a> ,
c&#8217;est-à-dire le point fixe de <span
class="cmmi-12">&#x03C3; </span>où <span
class="cmmi-12">&#x03C3; </span>est un morphisme <span
class="cmmi-12">q</span>-uniforme sur l&#8217;alphabet <span
class="cmr-12">&#x03A3;</span><sup><span
class="cmsy-8">&#x2032;</span></sup> et posons
aussi une application <span
class="cmmi-12">f </span>telle que <span
class="cmsy-10x-x-120">&#x2200;</span><span
class="cmmi-12">n,u</span><sub><span
class="cmmi-8">n</span></sub> <span
class="cmr-12">= </span><span
class="cmmi-12">f</span><span
class="cmr-12">(</span><span
class="cmmi-12">v</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span>.
<!--l. 318--><p class="indent" >   Consiérons maintenant l&#8217;automate <span
class="cmsy-10x-x-120"><img
src="/assets/suites_automatiques/cmsy10-c-41.png" alt="A" class="10-120x-x-41" /> </span>= <span
class="cmsy-10x-x-120">{</span><span
class="cmr-12">&#x03A3;</span><sup><span
class="cmsy-8">&#x2032;</span></sup><span
class="cmmi-12">, </span><span
class="cmr-12">&#x03A3;</span><span
class="cmmi-12">,&#x03B4;,v,f</span><span
class="cmsy-10x-x-120">} </span>où la fonction de transition <span
class="cmmi-12">&#x03B4; </span>est
définie par : <span
class="cmmi-12">&#x03C3;</span><span
class="cmr-12">(</span><span
class="cmmi-12">x</span><span
class="cmr-12">) = </span><span
class="cmmi-12">&#x03B4;</span><span
class="cmr-12">(</span><span
class="cmmi-12">x, </span><span
class="cmr-12">0)</span><span
class="cmmi-12">&#x03B4;</span><span
class="cmr-12">(</span><span
class="cmmi-12">x, </span><span
class="cmr-12">1)</span><img
src="/assets/suites_automatiques/suites_automatiques21x.png" alt="&#x22C5;&#x22C5;&#x22C5;"  class="@cdots" ><span
class="cmmi-12">&#x03B4;</span><span
class="cmr-12">(</span><span
class="cmmi-12">x,q </span><span
class="cmsy-10x-x-120">- </span><span
class="cmr-12">1)</span>. On a alors <span
class="cmsy-10x-x-120">&#x2200;</span><span
class="cmmi-12">n </span><span
class="cmsy-10x-x-120">&#x2208; </span><span
class="msbm-10x-x-120">&#x2115;</span><span
class="cmmi-12">,u</span><sub><span
class="cmmi-8">n</span></sub> <span
class="cmr-12">= </span><span
class="cmmi-12">f</span><span
class="cmr-12">(</span><span
class="cmmi-12">&#x03B4;</span><span
class="cmr-12">(</span><span
class="cmmi-12">v,</span><span
class="cmsy-10x-x-120">&#x27E8;</span><span
class="cmmi-12">n</span><span
class="cmsy-10x-x-120">&#x27E9;</span><sub><span
class="cmmi-8">q</span></sub><span
class="cmr-12">))</span>. En
effet, on montre par récurrence que :


   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques22x.png" alt="&#x2200;k, &#x03C3;k(v) = &#x03B4;(v,&#x27E8;0&#x27E9;q)&#x03B4;(v,&#x27E8;1&#x27E9;q)&#x22C5;&#x22C5;&#x22C5;&#x03B4;(v,&#x27E8;qk - 1&#x27E9;q).
" class="math-display" ></center>
<!--l. 324--><p class="indent" >   L&#8217;initialisation est claire. Pour l&#8217;héritage, on a :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques23x.png" alt="&#x03C3;k+1(v)  = &#x03C3; (&#x03B4;(v,&#x27E8;0&#x27E9;q)&#x03B4;(v, &#x27E8;1 &#x27E9;q) &#x22C5;&#x22C5;&#x22C5;&#x03B4;(v,&#x27E8;qk - 1 &#x27E9;q))
         = &#x03B4;(&#x03B4;(v,&#x27E8;0&#x27E9;q),0)&#x22C5; &#x22C5;&#x22C5;&#x03B4;(&#x03B4; (v, &#x27E8;0 &#x27E9;q),q - 1)&#x22C5;&#x22C5; &#x22C5;&#x03B4;(&#x03B4; (v, &#x27E8;qk - 1&#x27E9;q),0)&#x22C5;&#x22C5;&#x22C5;&#x03B4; (&#x03B4; (v, &#x27E8;qk - 1&#x27E9;q),q - 1)
         = &#x03B4;(v, &#x27E8;0 &#x27E9;) &#x22C5;&#x22C5;&#x22C5;&#x03B4;(v,&#x27E8;q - 1 &#x27E9;) &#x22C5;&#x22C5;&#x22C5;&#x03B4;(v,&#x27E8;qk+1 - q&#x27E9;) &#x22C5;&#x22C5;&#x22C5;&#x03B4;(v,&#x27E8;qk+1 - q + (q - 1)&#x27E9; ).
                  q               q                   q                           q
" class="math-display" ></center>
<!--l. 333--><p class="nopar" >
<!--l. 335--><p class="indent" >   Donc <span
class="cmr-12">(</span><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub> est bien engendrée par le <span
class="cmmi-12">q</span>-automate <span
class="cmsy-10x-x-120"><img
src="/assets/suites_automatiques/cmsy10-c-41.png" alt="A" class="10-120x-x-41" /></span>.                                             __
   </div>
<!--l. 338--><p class="noindent" >
   <h3 class="sectionHead"><span class="titlemark">3   </span> <a
 id="x1-80003"></a>Théorème de Christol</h3>
<!--l. 339--><p class="noindent" >Nous présentons dans cette partie un résultat de Gilles Christol. Auparavant, les suites considérées
sont <span
class="cmmi-12">q</span>-automatiques, avec <span
class="cmmi-12">q </span><span
class="cmr-12">= </span><span
class="cmmi-12">p</span><sup><span
class="cmmi-8">n</span></sup> et <span
class="cmmi-12">p </span>premier. Le théorème donne une caractérisation
surprenante du fait d&#8217;être automatique en terme d&#8217;algébricité (voir <span class="cite">[<a
href="#XAllouche05">1</a>]</span>) de série sur le corps
<span
class="msbm-10x-x-120">F</span><sub><span
class="cmmi-8">q</span></sub><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><span
class="cmr-12">)</span>. <span class="footnote-mark"><a
href="/assets/suites_automatiques/suites_automatiques5.html#fn4x0"><sup class="textsuperscript">4</sup></a></span><a
 id="x1-8001f4"></a>
Plus précisément, le théorème donne une équivalence entre l&#8217;algébricité d&#8217;une série formelle à
coefficients dans un corps fini et la nature automatique de la suite des coefficients. On va, dans un
premier temps, définir un opérateur qui porte le nom de Cartier.
   <h4 class="subsectionHead"><span class="titlemark">3.1   </span> <a
 id="x1-90003.1"></a>Opérateur de Cartier</h4>
<!--l. 343--><p class="noindent" >Notons <span
class="msbm-10x-x-120">F</span><sub><span
class="cmmi-8">q</span></sub><span
class="cmr-12">[[</span><span
class="cmmi-12">X</span><span
class="cmr-12">]] </span>l&#8217;ensemble des séries formelles à coefficients dans <span
class="msbm-10x-x-120">F</span><sub><span
class="cmmi-8">q</span></sub>. Soit <span
class="cmmi-12">u </span>une suite à valeur dans
<span
class="msbm-10x-x-120">F</span><sub><span
class="cmmi-8">q</span></sub>, on note :


   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques24x.png" alt="             &#x2211;&#x221E;      n
F (u) = Fu =     unX   .
             n=0
" class="math-display" ></center>
<!--l. 345--><p class="indent" >   Pour éclaircir l&#8217;idée, regardons les deux exemples suivantes :
   <div class="newtheorem">
<!--l. 347--><p class="noindent" ><span class="head">
<a
 id="x1-9001r12"></a>
<span
class="ecti-1200">Exemple </span>12<span
class="ecti-1200">.</span>  </span>On se place dans <span
class="msbm-10x-x-120">F</span><sub><span
class="cmr-8">2</span></sub> <span class="footnote-mark"><a
href="/assets/suites_automatiques/suites_automatiques6.html#fn5x0"><sup class="textsuperscript">5</sup></a></span><a
 id="x1-9002f5"></a> .
En utilisant la définition de la suite de Thue-Morse <span
class="cmmi-12">t</span>, il vient :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques25x.png" alt="F (X ) =  &#x2211;   tXn   =  &#x2211;   t X2n  + &#x2211;   t    X2n+1
 t          n n        &#x2211; n  2n  2n   &#x2211;   n 22nn++11   &#x2211;       2n+1
                    =    n tn2X   +X   nX      +2   n tnX
                    =  F (X ) + 1+X2-+  XF (X  )
                    =  (1 + X )F(X2 ) + 1X+X2.
" class="math-display" ></center>
<!--l. 357--><p class="nopar" >
<span
class="cmmi-12">F </span>est donc algébrique sur le corps <span
class="msbm-10x-x-120">F</span><sub><span
class="cmr-8">2</span></sub><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><span
class="cmr-12">) </span>des fractions rationnelles modulo 2. Elle est racine du
polynôme <span
class="cmmi-12">P </span>à coefficients dans <span
class="msbm-10x-x-120">F</span><sub><span
class="cmr-8">2</span></sub><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><span
class="cmr-12">) </span>:
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques26x.png" alt="                            X
P(Y ) = (1 + X )Y2 + Y +  ------2.
                          1 + X
" class="math-display" ></center>
   </div>
   <div class="newtheorem">
<!--l. 363--><p class="noindent" ><span class="head">
<a
 id="x1-9003r13"></a>


<span
class="ecti-1200">Exemple </span>13<span
class="ecti-1200">.</span>  </span>Par  des  calculs  analogues,  on  obtient  la  relation  suivante  pour  la  suite  de
Rudin-Shapiro <span
class="cmmi-12">r </span>:
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques27x.png" alt="(1 + X )5F (X )2 + (1 + X )4F (X ) + X3 = 0.
" class="math-display" ></center>
   </div>
<!--l. 368--><p class="indent" >   Avant de continuer, il sera utile d&#8217;introduire une famille d&#8217;opérateurs sur les séries formelles qui
portent le nom de l&#8217;opérateur de Cartier.
   <div class="newtheorem">
<!--l. 370--><p class="noindent" ><span class="head">
<a
 id="x1-9004r14"></a>
<span
class="ecbx-1200">D</span><span
class="ecbx-1200">éfinition 14 </span>(Cartier)<span
class="ecbx-1200">.</span>  </span>Soit <span
class="cmmi-12">r </span><span
class="cmsy-10x-x-120">&#x2208;{</span><span
class="cmr-12">0</span><span
class="cmmi-12">,</span><img
src="/assets/suites_automatiques/suites_automatiques28x.png" alt="&#x22C5;&#x22C5;&#x22C5;"  class="@cdots" ><span style="margin-left:0.3em" class="thinspace"></span><span
class="cmmi-12">,q </span><span
class="cmsy-10x-x-120">- </span><span
class="cmr-12">1</span><span
class="cmsy-10x-x-120">}</span><span
class="cmmi-12">. </span>On définit l&#8217;opérateur <span
class="cmr-12">&#x039B;</span><sub><span
class="cmmi-8">r</span></sub> :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques29x.png" alt="    &#x2211;                      &#x2211;
&#x039B;r :    anXn  &#x2208; Fq [[X ]] &#x21A6;&#x2192;     aqn+rXn.
      n                     n
" class="math-display" ></center>
   </div>
<!--l. 375--><p class="indent" >   Le lemme suivant se vérifie facilement.
   <div class="newtheorem">
<!--l. 377--><p class="noindent" ><span class="head">
<a
 id="x1-9005r15"></a>


<span
class="ecbx-1200">Lemme 15.</span>  </span><span
class="ecti-1200">Soit </span><span
class="cmmi-12">r </span><span
class="cmsy-10x-x-120">&#x2208;{</span><span
class="cmr-12">0</span><span
class="cmmi-12">,</span><img
src="/assets/suites_automatiques/suites_automatiques30x.png" alt="&#x22C5;&#x22C5;&#x22C5;"  class="@cdots" ><span style="margin-left:0.3em" class="thinspace"></span><span
class="cmmi-12">,q </span><span
class="cmsy-10x-x-120">- </span><span
class="cmr-12">1</span><span
class="cmsy-10x-x-120">} </span><span
class="ecti-1200">et </span><span
class="cmmi-12">F,G </span><span
class="cmsy-10x-x-120">&#x2208; </span><span
class="msbm-10x-x-120">F</span><sub><span
class="cmmi-8">q</span></sub><span
class="cmr-12">[[</span><span
class="cmmi-12">X</span><span
class="cmr-12">]]</span><span
class="cmmi-12">. </span><span
class="ecti-1200">Alors :</span>
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques31x.png" alt="&#x039B;r(F Gq) = &#x039B;r (F)G.
" class="math-display" ></center>
   </div>
<!--l. 382--><p class="indent" >   Précisons maintenant ce que veut dire être algégrique sur <span
class="msbm-10x-x-120">F</span><sub><span
class="cmmi-8">q</span></sub><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><span
class="cmr-12">) </span>pour une série formelle
<span
class="cmmi-12">F</span>.
   <div class="newtheorem">
<!--l. 384--><p class="noindent" ><span class="head">
<a
 id="x1-9006r16"></a>
<span
class="ecbx-1200">Lemme 16.</span>  </span> <span
class="ecti-1200">Soit </span><span
class="cmmi-12">F  </span><span
class="cmr-12">=</span>  <span
class="cmex-10x-x-120">&#x2211;</span>
  <sub><span
class="cmmi-8">n</span></sub><span
class="cmmi-12">a</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmmi-12">X</span><sup><span
class="cmmi-8">n</span></sup>  <span
class="ecti-1200">une s</span><span
class="ecti-1200">érie formelle </span><span
class="ecti-1200">à coefficients dans </span><span
class="msbm-10x-x-120">F</span><sub>
<span
class="cmmi-8">q</span></sub><span
class="ecti-1200">, alors </span><span
class="cmmi-12">F  </span><span
class="ecti-1200">est</span>
<span
class="ecti-1200">alg</span><span
class="ecti-1200">ébrique si et seulement si on peut trouver des polyn</span><span
class="ecti-1200">ômes </span><span
class="cmmi-12">B</span><sub><span
class="cmr-8">0</span></sub><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><span
class="cmr-12">)</span><span
class="cmmi-12">,B</span><sub><span
class="cmr-8">1</span></sub><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><span
class="cmr-12">)</span><span
class="cmmi-12">,</span><img
src="/assets/suites_automatiques/suites_automatiques32x.png" alt="&#x22C5;&#x22C5;&#x22C5;"  class="@cdots" ><span style="margin-left:0.3em" class="thinspace"></span><span
class="cmmi-12">,B</span><sub><span
class="cmmi-8">k</span></sub><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><span
class="cmr-12">)</span><span
class="ecti-1200">, non</span>
<span
class="ecti-1200">tous nuls tels que :</span>
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques33x.png" alt="B0F  + B1F  q + &#x22C5;&#x22C5;&#x22C5; + BkF qk = 0
" class="math-display" ></center> <span
class="ecti-1200">On peut supposer en outre que </span><span
class="cmmi-12">B</span><sub><span
class="cmr-8">0</span></sub><span
class="cmmi-12">&#x2260;</span><span
class="cmr-12">0</span><span
class="ecti-1200">.</span>
   </div>
<!--l. 391--><p class="indent" >
   <div class="proof">
<!--l. 392--><p class="indent" >   <span class="head">


<span
class="ecti-1200">D</span><span
class="ecti-1200">émonstration.</span> </span>Si <span
class="cmmi-12">F </span>est algébrique sur <span
class="msbm-10x-x-120">F</span><sub><span
class="cmmi-8">q</span></sub><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><span
class="cmr-12">)</span>, la famille <span
class="cmr-12">(</span><span
class="cmmi-12">F</span><sup><span
class="cmmi-8">q</span><sup><span
class="cmmi-6">k</span></sup></sup><span
class="cmr-12">)</span><sub>
<span
class="cmmi-8">k</span><span
class="cmsy-8">&#x2265;</span><span
class="cmr-8">0</span></sub> est liée, d&#8217;où une relation
de combinaison linéaire non triviale de la forme de l&#8217;énoncé. Réciproquement une telle liaison
implique l&#8217;algébricité de <span
class="cmmi-12">F</span>. Il reste à montrer que <span
class="cmmi-12">B</span><sub><span
class="cmr-8">0</span></sub> n&#8217;est pas nul.
<!--l. 396--><p class="indent" >   Prenons <span
class="cmmi-12">k </span><span
class="cmsy-10x-x-120">&#x2208; </span><span
class="msbm-10x-x-120">&#x2115; </span>minimal tel que l&#8217;on ait une relation de liaison non triviale comme ci-dessus
et montrons par l&#8217;absurde que <span
class="cmmi-12">B</span><sub><span
class="cmr-8">0</span></sub> <span
class="cmr-12">= 0 </span>:
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques34x.png" alt="                  k
B1F q + &#x22C5;&#x22C5;&#x22C5; + BkF q = 0
" class="math-display" ></center> Puis, en utilisant le lemme plus haut :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques35x.png" alt="       q             qk                             qk-1
&#x039B;r(B1F   + &#x22C5;&#x22C5;&#x22C5; + BkF   ) = &#x039B;r(B1)F  + &#x22C5;&#x22C5;&#x22C5; + &#x039B;r (Bk)F    = 0
" class="math-display" ></center> Ce qui contredit alors la minimalité de <span
class="cmmi-12">k</span>.                                                              __
   </div>
<!--l. 403--><p class="noindent" >
   <h4 class="subsectionHead"><span class="titlemark">3.2   </span> <a
 id="x1-100003.2"></a>Théorème de Christol</h4>
   <div class="newtheorem">
<!--l. 405--><p class="noindent" ><span class="head">
<a
 id="x1-10001r17"></a>
<span
class="ecbx-1200">Th</span><span
class="ecbx-1200">éor</span><span
class="ecbx-1200">ème 17 </span>(Christol, 1979)<span
class="ecbx-1200">.</span>  </span><span class="footnote-mark"><a
href="/assets/suites_automatiques/suites_automatiques7.html#fn6x0"><sup class="textsuperscript">6</sup></a></span><a
 id="x1-10002f6"></a>
<span
class="ecti-1200">Soit </span><span
class="cmmi-12">p </span><span
class="cmsy-10x-x-120">&#x2265; </span><span
class="cmr-12">2 </span><span
class="ecti-1200">un nombre premier et </span><span
class="cmmi-12">q </span><span
class="ecti-1200">une puissance de </span><span
class="cmmi-12">p</span><span
class="ecti-1200">. Une suite </span><span
class="cmmi-12">u </span><span
class="ecti-1200">à valeurs dans </span><span
class="msbm-10x-x-120">F</span><sub><span
class="cmmi-8">q</span></sub> <span
class="ecti-1200">est</span>
<span
class="cmmi-12">q</span><span
class="ecti-1200">-automatique si et seulement si la s</span><span
class="ecti-1200">érie formelle </span><span
class="cmmi-12">F</span><span
class="cmr-12">(</span><span
class="cmmi-12">u</span><span
class="cmr-12">) =</span> <span
class="cmex-10x-x-120">&#x2211;</span>
  <sub><span
class="cmmi-8">n</span></sub><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmmi-12">X</span><sup><span
class="cmmi-8">n</span></sup> <span
class="ecti-1200">est alg</span><span
class="ecti-1200">ébrique sur </span><span
class="msbm-10x-x-120">F</span><sub>
<span
class="cmmi-8">q</span></sub><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><span
class="cmr-12">)</span><span
class="ecti-1200">.</span>


   </div>
<!--l. 411--><p class="noindent" >
   <div class="proof">
<!--l. 412--><p class="indent" >   <span class="head">
<span
class="ecti-1200">D</span><span
class="ecti-1200">émonstration.</span> </span><span
class="cmr-12">(</span><span
class="cmsy-10x-x-120">&#x21D2;</span><span
class="cmr-12">)</span>. Soit <span
class="cmmi-12">u </span>une suite <span
class="cmmi-12">q</span>-automatique. On se servira de l&#8217;équivalence prouvée
par Cobham : le <span
class="cmmi-12">q</span>-noyau <span
class="cmmi-12">K</span><sub><span
class="cmmi-8">u</span></sub> est fini. Posons alors <span
class="cmmi-12">d </span><span
class="cmr-12">= </span><span
class="cmmi-12">Card</span><span
class="cmr-12">(</span><span
class="cmmi-12">K</span><sub><span
class="cmmi-8">u</span></sub><span
class="cmr-12">)</span>.
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques36x.png" alt="        q-1
        &#x2211;    r &#x2211;          nq
F (u ) =    X      uqn+rX
        r=0     n
" class="math-display" ></center> Comme on a dans <span
class="msbm-10x-x-120">F</span><sub><span
class="cmmi-8">q</span></sub>, <span
class="cmmi-12">G</span><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><sup><span
class="cmmi-8">q</span></sup><span
class="cmr-12">) = </span><span
class="cmmi-12">G</span><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><span
class="cmr-12">)</span><sup><span
class="cmmi-8">q</span></sup> où <span
class="cmmi-12">G </span>est un polynôme
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques37x.png" alt="        q&#x2211;-1    &#x2211;
F (u) =     Xr (   uqn+rXn )q
        r=0      n
" class="math-display" ></center> Ce qui montre que :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques38x.png" alt="                      q
F(u ) &#x2208; V ectv&#x2208;Ku&#x27E8;F (v) &#x27E9;
" class="math-display" ></center> On peut ainsi répéter le processus de la même manière :


   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques39x.png" alt="&#x2200;k &#x2264;  d : F (u )qk &#x2208; V ectv&#x2208;K &#x27E8;F (v)qk+1&#x27E9;
                          u
" class="math-display" ></center> Et donc par une récurrence simple, on obtient :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques40x.png" alt="              k                  d+1
&#x2200;k &#x2264;  d : F (u )q &#x2208; V ectv&#x2208;Ku&#x27E8;F (v)q &#x27E9;
" class="math-display" ></center> Mais <span
class="cmmi-12">V ect</span><sub><span
class="cmmi-8">v</span><span
class="cmsy-8">&#x2208;</span><span
class="cmmi-8">K</span><sub><span
class="cmmi-6">u</span></sub></sub><span
class="cmsy-10x-x-120">&#x27E8;</span><span
class="cmmi-12">F</span><span
class="cmr-12">(</span><span
class="cmmi-12">v</span><span
class="cmr-12">)</span><sup><span
class="cmmi-8">q</span><sup><span
class="cmmi-6">d</span><span
class="cmr-6">+1</span></sup></sup><span
class="cmsy-10x-x-120">&#x27E9; </span>est de dimension au plus <span
class="cmmi-12">d</span>, la famille <span
class="cmsy-10x-x-120">{</span><span
class="cmmi-12">F</span><span
class="cmr-12">(</span><span
class="cmmi-12">u</span><span
class="cmr-12">)</span><span
class="cmmi-12">,F</span><span
class="cmr-12">(</span><span
class="cmmi-12">u</span><span
class="cmr-12">)</span><sup><span
class="cmmi-8">q</span></sup><span
class="cmmi-12">,</span><img
src="/assets/suites_automatiques/suites_automatiques41x.png" alt="&#x22C5;&#x22C5;&#x22C5;"  class="@cdots" ><span style="margin-left:0.3em" class="thinspace"></span><span
class="cmmi-12">,F</span><span
class="cmr-12">(</span><span
class="cmmi-12">u</span><span
class="cmr-12">)</span><sup><span
class="cmmi-8">q</span><sup><span
class="cmmi-6">d</span></sup></sup><span
class="cmsy-10x-x-120">}</span>
est liée. <span
class="cmmi-12">F</span><span
class="cmr-12">(</span><span
class="cmmi-12">u</span><span
class="cmr-12">) =</span> <span
class="cmex-10x-x-120">&#x2211;</span>
  <sub><span
class="cmmi-8">n</span></sub><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmmi-12">X</span><sup><span
class="cmmi-8">n</span></sup> est donc algébrique sur <span
class="msbm-10x-x-120">F</span><sub>
<span
class="cmmi-8">q</span></sub><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><span
class="cmr-12">)</span>.
<!--l. 426--><p class="indent" >   <span
class="cmr-12">(</span><span
class="cmsy-10x-x-120">&#x21D0;</span><span
class="cmr-12">)</span>. Réciproquement, si la série formelle <span
class="cmmi-12">F</span><span
class="cmr-12">(</span><span
class="cmmi-12">u</span><span
class="cmr-12">) </span>est algébrique sur <span
class="msbm-10x-x-120">F</span><sub><span
class="cmmi-8">q</span></sub><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><span
class="cmr-12">)</span>, d&#8217;après le
<span
class="cmbx-12">lemme</span><span
class="cmbx-12">&#x00A0;</span><a
href="#x1-9006r16"><span
class="cmbx-12">16</span><!--tex4ht:ref: liaison --></a>, on peut trouver des polyômes <span
class="cmmi-12">B</span><sub><span
class="cmmi-8">i</span></sub> avec <span
class="cmmi-12">B</span><sub><span
class="cmr-8">0</span></sub> non nul tels que :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques42x.png" alt="&#x2211;k               i
   Bi (X )Fu(X )q = 0
i=0  " class="math-display" ></center>
Posons <span
class="cmmi-12">G</span><sub><span
class="cmmi-8">u</span></sub> <span
class="cmr-12">= </span><span
class="cmmi-12">F</span><sub><span
class="cmmi-8">u</span></sub><span
class="cmmi-12">&#x2215;B</span><sub><span
class="cmr-8">0</span></sub>. Il vient <span
class="cmmi-12">G</span><sub><span
class="cmmi-8">u</span></sub> <span
class="cmr-12">=</span> <span
class="cmex-10x-x-120">&#x2211;</span>
  <sub><span
class="cmmi-8">i</span><span
class="cmr-8">=0</span></sub><sup><span
class="cmmi-8">k</span></sup><span
class="cmmi-12">C</span><sub>
<span
class="cmmi-8">i</span></sub><span
class="cmmi-12">G</span><sub><span
class="cmmi-8">u</span></sub><sup><span
class="cmmi-8">q</span><sup><span
class="cmmi-6">i</span></sup></sup> où <span
class="cmsy-10x-x-120">&#x2200;</span><span
class="cmmi-12">i </span><span
class="cmsy-10x-x-120">&#x2208;{</span><span
class="cmr-12">1</span><span
class="cmmi-12">,</span><span
class="cmmi-12">&#x2026;</span><span
class="cmmi-12">,k</span><span
class="cmsy-10x-x-120">}</span><span
class="cmmi-12">,C</span><sub>
<span
class="cmmi-8">i</span></sub> <span
class="cmr-12">= </span><span
class="cmsy-10x-x-120">-</span><span
class="cmmi-12">B</span><sub><span
class="cmmi-8">i</span></sub><span
class="cmmi-12">B</span><sub><span
class="cmr-8">0</span></sub><sup><span
class="cmmi-8">q</span><sup><span
class="cmmi-6">i</span></sup><span
class="cmsy-8">-</span><span
class="cmr-8">2</span></sup>. Posons ensuite
<span
class="cmmi-12">N </span><span
class="cmr-12">= </span><span
class="cmmi-12">max</span><span
class="cmsy-10x-x-120">{</span><span
class="cmmi-12">deg</span><span
class="cmr-12">(</span><span
class="cmmi-12">B</span><sub><span
class="cmr-8">0</span></sub><span
class="cmr-12">)</span><span
class="cmmi-12">,deg</span><span
class="cmr-12">(</span><span
class="cmmi-12">C</span><sub><span
class="cmr-8">1</span></sub><span
class="cmr-12">)</span><span
class="cmmi-12">,</span><img
src="/assets/suites_automatiques/suites_automatiques43x.png" alt="&#x22C5;&#x22C5;&#x22C5;"  class="@cdots" ><span style="margin-left:0.3em" class="thinspace"></span><span
class="cmmi-12">,deg</span><span
class="cmr-12">(</span><span
class="cmmi-12">C</span><sub><span
class="cmmi-8">k</span></sub><span
class="cmr-12">)</span><span
class="cmsy-10x-x-120">} </span>et <span
class="cmsy-10x-x-120"><img
src="/assets/suites_automatiques/cmsy10-c-48.png" alt="H" class="10-120x-x-48" /> </span>l&#8217;ensemble défini par :
   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques44x.png" alt="                        &#x2211;          i
H  =  {H  &#x2208; Fq[[X ]]|H  =    ki=0 DiGqu etDi &#x2208;  Fq[X ],deg (Di ) &#x2264; N }.
" class="math-display" ></center>
<!--l. 437--><p class="nopar" >
<span
class="cmsy-10x-x-120"><img
src="/assets/suites_automatiques/cmsy10-c-48.png" alt="H" class="10-120x-x-48" /> </span>est un ensemble fini contenant <span
class="cmmi-12">F</span><sub><span
class="cmmi-8">u</span></sub>. Pour montrer que <span
class="cmmi-12">K</span><sub><span
class="cmmi-8">u</span></sub> est fini, il suffit de montrer que <span
class="cmsy-10x-x-120">&#x2200;</span><span
class="cmmi-12">r &#x003C; q</span>,
<span
class="cmsy-10x-x-120"><img
src="/assets/suites_automatiques/cmsy10-c-48.png" alt="H" class="10-120x-x-48" /> </span>est stable par <span
class="cmr-12">&#x039B;</span><sub><span
class="cmmi-8">r</span></sub>. Soit alors <span
class="cmmi-12">H </span>un élément de <span
class="cmsy-10x-x-120"><img
src="/assets/suites_automatiques/cmsy10-c-48.png" alt="H" class="10-120x-x-48" /></span>, on a :


   <center class="math-display" >
<img
src="/assets/suites_automatiques/suites_automatiques45x.png" alt="                     &#x2211;k       i       &#x2211;k                i    &#x2211;k                 i-1
&#x039B;r (H ) = &#x039B;r (D0Gu +     DiGqu ) = &#x039B;r (  (D0Gu  + Di )Gqu ) =    &#x039B; (D0Ci +  Di)Gqu
                     i=1              i=1                    i=1  " class="math-display" ></center>
Comme pour tout <span
class="cmmi-12">i</span>, on a <span
class="cmmi-12">deg</span><span
class="cmr-12">(</span><span
class="cmmi-12">D</span><sub><span
class="cmr-8">0</span></sub><span
class="cmmi-12">C</span><sub><span
class="cmmi-8">i</span></sub> <span
class="cmr-12">+ </span><span
class="cmmi-12">D</span><sub><span
class="cmmi-8">i</span></sub><span
class="cmr-12">) </span><span
class="cmsy-10x-x-120">&#x2264;</span> <span
class="cmmi-12">deg</span><span
class="cmr-12">(</span><span
class="cmmi-12">D</span><sub><span
class="cmr-8">0</span></sub><span
class="cmmi-12">C</span><sub><span
class="cmmi-8">i</span></sub> <span
class="cmr-12">+ </span><span
class="cmmi-12">D</span><sub><span
class="cmmi-8">i</span></sub><span
class="cmr-12">)</span><span
class="cmmi-12">&#x2215;q </span><span
class="cmsy-10x-x-120">&#x2264;</span> <span
class="cmr-12">2</span><span
class="cmmi-12">N</span><span
class="cmmi-12">&#x2215;q </span><span
class="cmsy-10x-x-120">&#x2264; </span><span
class="cmmi-12">N</span>, donc <span
class="cmr-12">&#x039B;</span><sub><span
class="cmmi-8">r</span></sub><span
class="cmr-12">(</span><span
class="cmmi-12">H</span><span
class="cmr-12">) </span><span
class="cmsy-10x-x-120">&#x2208;</span>
<span
class="cmsy-10x-x-120"><img
src="/assets/suites_automatiques/cmsy10-c-48.png" alt="H" class="10-120x-x-48" /></span>.                                                                                                                  __
   </div>
<!--l. 446--><p class="noindent" >
   <h3 class="sectionHead"><span class="titlemark">4   </span> <a
 id="x1-110004"></a>Divers</h3>
<!--l. 447--><p class="noindent" >Dans cette partie, nous donnons quelques autres résultats importants sur les suites
automatiques. Cobham a démontré le résultat qui suit dont on trouvera une démonstration dans
<span class="cite">[<a
href="#XAllouche03">2</a>]</span> :
   <div class="newtheorem">
<!--l. 449--><p class="noindent" ><span class="head">
<a
 id="x1-11001r18"></a>
<span
class="ecbx-1200">Th</span><span
class="ecbx-1200">éor</span><span
class="ecbx-1200">ème 18.</span>  </span><span
class="ecti-1200">Soit </span><span
class="cmmi-12">k </span><span
class="ecti-1200">et </span><span
class="cmmi-12">l </span><span
class="ecti-1200">deux entiers multiplicativement ind</span><span
class="ecti-1200">épendants</span><span class="footnote-mark"><a
href="/assets/suites_automatiques/suites_automatiques8.html#fn7x0"><sup class="textsuperscript">7</sup></a></span><a
 id="x1-11002f7"></a>
<span
class="ecti-1200">et soit </span><span
class="cmmi-12">u </span><span
class="ecti-1200">une suite </span><span
class="cmmi-12">k </span><span
class="ecti-1200">et </span><span
class="cmmi-12">l</span><span
class="ecti-1200">-automatique, alors </span><span
class="cmmi-12">u </span><span
class="ecti-1200">est ultimement p</span><span
class="ecti-1200">ériodique.</span>
   </div>
   <div class="newtheorem">
<!--l. 455--><p class="noindent" ><span class="head">
<a
 id="x1-11003r19"></a>
<span
class="ecbx-1200">Corollaire 19.</span>  </span><span
class="ecti-1200">Soit </span><span
class="cmmi-12">q</span><sub><span
class="cmr-8">1</span></sub>  <span
class="ecti-1200">et </span><span
class="cmmi-12">q</span><sub><span
class="cmr-8">2</span></sub>  <span
class="ecti-1200">multiplicativement ind</span><span
class="ecti-1200">épendants et soit </span><span
class="cmmi-12">u </span><span
class="ecti-1200">une suite telle que</span>
<span
class="cmmi-12">F</span><sub><span
class="cmmi-8">u</span></sub> <span
class="ecti-1200">soit </span><span
class="ecti-1200">à la fois alg</span><span
class="ecti-1200">ébrique sur </span><span
class="msbm-10x-x-120">F</span><sub><span
class="cmmi-8">q</span><span
class="cmr-8">1</span></sub> <span
class="ecti-1200">et </span><span
class="msbm-10x-x-120">F</span><sub><span
class="cmmi-8">q</span><span
class="cmr-8">2</span></sub><span
class="ecti-1200">, alors </span><span
class="cmmi-12">u </span><span
class="ecti-1200">est ultimement p</span><span
class="ecti-1200">ériodique.</span>
   </div>
<!--l. 461--><p class="indent" >
   <div class="proof">
<!--l. 462--><p class="indent" >   <span class="head">


<span
class="ecti-1200">D</span><span
class="ecti-1200">émonstration.</span> </span>En vertu du théorème précédent et celui de Christol.                          __
   </div>
<!--l. 465--><p class="indent" >   En particulier, les suites de Thue-Morse et de Rudin-Shapiro ne sont pas
3-automatiques. <span class="footnote-mark"><a
href="/assets/suites_automatiques/suites_automatiques9.html#fn8x0"><sup class="textsuperscript">8</sup></a></span><a
 id="x1-11004f8"></a>
Il est donc intéressant de comparer ce corollaire à la conjecture suivante.
   <div class="newtheorem">
<!--l. 467--><p class="noindent" ><span class="head">
<a
 id="x1-11005r20"></a>
<span
class="ecbx-1200">Conjecture 20.</span>  </span><span
class="ecti-1200">Soit </span><span
class="cmr-12">(</span><span
class="cmmi-12">u</span><sub><span
class="cmmi-8">n</span></sub><span
class="cmr-12">)</span><sub><span
class="cmmi-8">n</span></sub> <span
class="cmsy-10x-x-120">&#x2208;{</span><span
class="cmr-12">0</span><span
class="cmmi-12">, </span><span
class="cmr-12">1</span><span
class="cmsy-10x-x-120">}</span><sup><span
class="msbm-10x-x-80">&#x2115;</span></sup>  <span
class="ecti-1200">telle que les deux nombres r</span><span
class="ecti-1200">éels</span> <span
class="cmex-10x-x-120">&#x2211;</span>
  <sub><span
class="cmmi-8">n</span><span
class="cmsy-8">&#x2208;</span><span
class="cmmi-8">N</span></sub><img
src="/assets/suites_automatiques/suites_automatiques46x.png" alt="un-
2n"  class="frac" align="middle"> <span
class="ecti-1200">et</span> <span
class="cmex-10x-x-120">&#x2211;</span>
  <sub><span
class="cmmi-8">n</span><span
class="cmsy-8">&#x2208;</span><span
class="cmmi-8">N</span></sub><img
src="/assets/suites_automatiques/suites_automatiques47x.png" alt="un
3n"  class="frac" align="middle">
<span
class="ecti-1200">sont alg</span><span
class="ecti-1200">ébriques sur </span><span
class="msbm-10x-x-120">&#x211A;</span><span
class="ecti-1200">, alors ces deux nombres sont rationnels.</span>
   </div>
<!--l. 472--><p class="indent" >   Par ailleurs, on montre que si deux suites <span
class="cmmi-12">u </span>et <span
class="cmmi-12">v </span>à valeurs dans <span
class="cmsy-10x-x-120">{</span><span
class="cmr-12">0</span><span
class="cmmi-12">,</span><span
class="cmmi-12">&#x2026;</span><span
class="cmmi-12">,q </span><span
class="cmsy-10x-x-120">- </span><span
class="cmr-12">1</span><span
class="cmsy-10x-x-120">} </span>sont
<span
class="cmmi-12">q</span>-automatiques, leur produit <span
class="cmmi-12">uv </span>l&#8217;est aussi. En appliquant le théorème de Christol, on
a :
   <div class="newtheorem">
<!--l. 474--><p class="noindent" ><span class="head">
<a
 id="x1-11006r21"></a>
<span
class="ecbx-1200">Corollaire 21.</span>  </span><span
class="ecti-1200">Soient </span><span
class="cmmi-12">u </span><span
class="ecti-1200">et </span><span
class="cmmi-12">v </span><span
class="ecti-1200">à valeurs dans </span><span
class="cmsy-10x-x-120">{</span><span
class="cmr-12">0</span><span
class="cmmi-12">,</span><span
class="cmmi-12">&#x2026;</span><span
class="cmmi-12">,q</span><span
class="cmsy-10x-x-120">-</span><span
class="cmr-12">1</span><span
class="cmsy-10x-x-120">} </span><span
class="ecti-1200">telles que </span><span
class="cmmi-12">F</span><sub><span
class="cmmi-8">u</span></sub> <span
class="ecti-1200">et </span><span
class="cmmi-12">F</span><sub><span
class="cmmi-8">v</span></sub> <span
class="ecti-1200">sont alg</span><span
class="ecti-1200">ébriques</span>
<span
class="ecti-1200">sur </span><span
class="msbm-10x-x-120">F</span><sub><span
class="cmmi-8">q</span></sub><span
class="cmr-12">(</span><span
class="cmmi-12">X</span><span
class="cmr-12">)</span><span
class="ecti-1200">, alors le produit d&#8217;Hadamard</span><span class="footnote-mark"><a
href="/assets/suites_automatiques/suites_automatiques10.html#fn9x0"><sup class="textsuperscript">9</sup></a></span><a
 id="x1-11007f9"></a>
<span
class="ecti-1200">de </span><span
class="cmmi-12">F</span><sub><span
class="cmmi-8">u</span></sub> <span
class="ecti-1200">et </span><span
class="cmmi-12">F</span><sub><span
class="cmmi-8">v</span></sub> <span
class="ecti-1200">est aussi alg</span><span
class="ecti-1200">ébrique que l&#8217;on note </span><span
class="cmmi-12">F</span><sub><span
class="cmmi-8">uv</span></sub><span
class="ecti-1200">.</span>
   </div>
<!--l. 480--><p class="indent" >   Le lien entre les automates et l&#8217;algébricité laisse entrevoir un champ de recherche en théorie des
nombres et en algèbre.
   <h3 class="likesectionHead"><a
 id="x1-120004"></a>Références</h3>
<!--l. 1--><p class="noindent" >
   <div class="thebibliography">
   <p class="bibitem" ><span class="biblabel">
 [1]<span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span><a
 id="XAllouche05"></a>J-P.Allouche.   Automates et algébricité.   In <span
class="ecti-1200">Journal de Th</span><span
class="ecti-1200">éorie des Nombres de</span>
   <span
class="ecti-1200">BORDEAUX</span>, volume&#x00A0;17, pages 1&#8211;11. Université Bordeaux 1, 2005.


   </p>
   <p class="bibitem" ><span class="biblabel">
 [2]<span class="bibsp">&#x00A0;&#x00A0;&#x00A0;</span></span><a
 id="XAllouche03"></a>J-P.Allouche and J.Shallit.  <span
class="ecti-1200">Automatic sequences</span>, volume&#x00A0;1.  Cambridge University
   Press, 2003.
</p>
   </div>

</body></html>
