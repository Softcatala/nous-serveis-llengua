# Nous serveis lingüístics de Softcatalà

## Objectius
Crear nous serveis de consulta lingüística, relativament fàcils d'oferir, que poden ser d'utilitat per als usuaris de Softcatalà.

## Possibles serveis
* Separador i comptador de síl·labes. [Exemple, amb llibreria en Perl](https://riuraueditors.cat/separa-sillabes/) 
* Conversor de xifres a text. [Exemple](https://gent.softcatala.org/jmontane/coses/numbertext/), basat en [numbertext.org](https://numbertext.github.io/)
* Conversor a text d'expressions horàries dels 2 sistemes horaris usats en català: de campanar i de rellotge. 
* Cerques amb expressions regulars en el diccionari. Exemple de [visca.com](https://visca.com/dr/). Això es podria no limitar al DIEC, i mostrar l'existència del lema als diferents diccionaris, amb l'enllaç corresponent (DIEC, DNV?, GDLC i DCVB bàsicament, i potser el Viccionari). També podria permetre escoltar pronunciacions de Common Voice (veure p. ex. https://orga.cat/commonvoice/)
* Diccionari de rimes. Relacionat amb les cerques amb expressions regulars, però una mica més sofisticat. 
* Conjugador verbal, o en general flexionador de qualsevol classe de paraules (verbs, noms, adjectius, pronoms, etc.). 
* Transcripció fonètica: consulta de diccionaris o generació. 
* Cercador amigable al [CLDR](http://cldr.unicode.org/), potser en diversos idiomes.
* Conversor d'unitats. Potser es podria aprofitar [ConvertAll](http://convertall.bellz.org/) ([en línia](http://convertall-js.bellz.org/), a [GitHub](https://github.com/doug-101/ConvertAll-js)), i de pas [contribuir la traducció](https://github.com/doug-101/ConvertAll/issues/8).
* Altres?

## Dubtes i qüestions que cal resoldre

* Com hauria de ser la integració en la web de Softcatalà. Una interfície per a cada servei o una interfície per a tots. 
* Oferim alguna cosa de valor o repetim serveis que ja existeixen (p. ex. Viccionari)?
  * Com a fet diferencial, aportem els diccionaris de Softcatalà, que tenen més formes que qualsevol altre diccionari (1,24 milions de formes, 143.000 lemes).

## Fonts de dades i eines existents
* Viccionari (418.000 entrades), amb flexió, definicions, transcripció fonètica...
* Diccionaris de Softcatalà/LanguageTool (1,24 milions de formes etiquetades), i diccionaris d'anàlisi i síntesi ja implementats. 
* [Wikidata:Lexicographical data](https://www.wikidata.org/wiki/Wikidata:Lexicographical_data), encara sense dades en català.
* Per a transcripció fonètica: 
  * [BaDaTran](http://latel.upf.edu/cgi-bin/BaDaTran.cgi) (base de dades de transcripcions fonètiques d'alguns diccionaris de referència)
  * [Segre (transcriptor fonètic de català)](http://nlp.lsi.upc.edu/freeling/demo/segre.php). No funciona.
  * [TextAFon](https://sites.google.com/site/juanmariagarrido/research/projects-1/texafon), executable amb llicència GNU, però sense codi font (!).
  * Les funcions de transcripció fonètica de [eSpeack](http://espeak.sourceforge.net/) o [FestCat](http://festcat.talp.cat/).

## Tasques i assignació
* Integració dels diferents serveis en la web de Softcatalà 
  * Qui: Xavi
  * Estat
    * En cada lloc
  
* Conversor a text d'expressions horàries
  * Qui: Jordi Mas
  * Estat
    * Versió preliminar: https://www.softcatala.org/hora-en-catala/
  * Queda
    * Integrar el JS en la construcció del web
    * Unificar el UI (dos botons dalt de tot: hora actual vs hora en formulari)

* Separador i comptador de síl·labes
  * Qui: Jaume Ortolà
  * Estat
    * Disseny preliminar (en JavaScript): https://www.softcatala.org/sillabes/
  * Queda
    * Pujars els fitxers JS al servidor de Softcatalà
    * Disseny apropiat (reduir la mida del formulari)
    * Comprovar scroll en Firefox
    
* Cercador avançat de paraules
  * Qui: Jaume Ortolà
  * Estat
    * Implementació preliminar: https://riuraueditors.cat/advanced-word-search-cat/
  * Queda
    * Integració en Softcatalà
    * Disseny apropiat
    
* API per obtenir eficientment l'existència d'un terme en diferents fonts, amb els seus enllaços corresponents
  * Qui: Pere Orga
  * Estat
    * Implementació preliminar (DIEC, GDLC, DCVB, Common Voice): https://github.com/pereorga/dictionary-api
  * Queda
    * DNV, PCCD, DSFF? DDLC? CTILC? Viccionari? CiT? Termcat? sinònims Softcatalà? sinònims IEC? sinònims Franquesa?
    * Fer una demo simple
    * Integrar en aplicacions existents (p. ex. en el cercador avançat de paraules)

* Convertidor d'unitats
  * Qui: Pere Orga
  * Estat
    * Implementació preliminar: https://orga.cat/unitats/
  * Queda
    * Revisar la traducció
    * Si es decideix integrar, probablement simplificar (o refer) la interfície
