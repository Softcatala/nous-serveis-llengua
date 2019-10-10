# Nous serveis lingüístics de Softcatalà

## Objectius
Crear nous serveis de consulta lingüística, relativament fàcils d'oferir, que poden ser d'utilitat per als usuaris de Softcatalà.

## Possibles serveis
* Separador i comptador de síl·labes. [Exemple, amb llibreria en Perl](https://riuraueditors.cat/separa-sillabes/) 
* Conversor de xifres a text. [Exemple](https://gent.softcatala.org/jmontane/coses/numbertext/), basat en [numbertext.org](https://numbertext.github.io/)
* Conversor a text d'expressions horàries dels 2 sistemes horaris usats en català: de campanar i de rellotge. 
* Cerques amb expressions regulars en el diccionari. Exemple de [visca.com](https://visca.com/dr/). Això es podria no limitar al DIEC, i mostrar l'existència del lema als diferents diccionaris, amb l'enllaç corresponent (DIEC, DNV?, GDLC i DCVB bàsicament, i potser el Viccionari)
* Conjugador verbal, o en general flexionador de qualsevol classe de paraules (verbs, noms, adjectius, pronoms, etc.). 
* Transcriptor fonètic. (Hi ha alguna eina feta.)
* Cercador amigable al [CLDR](http://cldr.unicode.org/), en diversos idiomes.
* Altres?

## Dubtes i qüestions que cal resoldre

* Com hauria de ser la integració en la web de Softcatalà. Una interfície per a cada servei o una interfície per a tots. 
* Oferim alguna cosa de valor o repetim serveis que ja existeixen (p. ex. Viccionari)?
  * Com a fet diferencial, aportem els diccionaris de Softcatalà, que tenen més formes que qualsevol altre diccionari (1,24 milions de formes, 143.000 lemes).

## Fonts de dades i eines existents
* Viccionari (418.000 entrades), amb flexió, definicions, transcripció fonètica...
* Diccionaris de Softcatalà/LanguageTool (1,24 milions de formes etiquetades), i diccionaris d'anàlisi i síntesi ja implementats. 
* [Wikidata:Lexicographical data](https://www.wikidata.org/wiki/Wikidata:Lexicographical_data), encara sense dades en català.
* [Segre (transcriptor fonètic de català)](http://nlp.lsi.upc.edu/freeling/demo/segre.php). No funciona.
* [BaDaTran](http://latel.upf.edu/cgi-bin/BaDaTran.cgi) (base de dades de transcripcions fonètiques d'alguns diccionaris de referència)
