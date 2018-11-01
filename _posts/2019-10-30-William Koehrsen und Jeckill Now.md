[Jeckyll](https://jekyllrb.com) ist ein statischer Websitengenerator. D.h. eine "Maschine" die analog einem gedruckten Buch mit HTML und CSS Internetseiten erstellt. 2008 von Tom Preston-Werner - einem der Gründer von GitHub - [erfunden](https://en.wikipedia.org/wiki/Jekyll_(software)), ist es inzwischen einer der populärsten statischen Seitengeneratoren.  

William Koehrsen hat nun auf GitHub eine Vorlage ("Repository") namens ["Jeckyll Now"](https://github.com/barryclark/jekyll-now) erstellt, welche frei kopiert ("forken") weden darf. In diesem [Artikel](https://towardsdatascience.com/five-minutes-to-your-own-website-fd0b43cbd886) stellt er die Behauptung auf, dass man damit in fünf Minunten einen funktionieren Blog im Internet hat. D.h. man kann direkt anfangen mit Markdown Blogposts zu schreiben, welche ungefähr [so](http://www.jekyllnow.com) aussehen. Zum Beispiel mit Visual Studio Code, meinem bevorzugten Editor.  Daher sollte es klar sein, dass der Einsatz von "Jeckyll" mit GitHub gedacht ist. Man kann die Blogposts online erstellen bzw. editieren oder in einem lokalen Editor und einem abschliessenden Datenabgleich ("Sync") mit GitHub.  

Dieser Artikel schildert meine Erfahungen sowie mein Einstieg in Jeckyll bzw. "Jeckyll Now" mit diesem Blog. Weder bin ich Entwickler, noch Webdesigner. Ich habe in den vergangenen Jahrzehnten ein paar Stunden in HTML, CSS, JavaScript und ASP / ASP.Net verbracht. Wenn technische Aussagen nicht korrekt oder nicht präzise sind, freue ich mich über ein Feedback. Korrektur asap. Der Artikel erklärt das Vorgehen genügend detailiert, so das jemand mit Browsern und Webservices vertraut ist, innert 15 Minuten am Ziel ist.  

Ein guter Einstieg ist die Datei "Readme.md". Dort wird erklärt (en), wie die Software funktioniert. Bzw. wo man den Blog konfigurieren kann. Dort wird u.a. auch auf diesen Artikel von ["Smashingmagazine"](https://www.smashingmagazine.com/2014/08/build-blog-jekyll-github-pages/) verwiesen. Die Verzeichnis und Dateistruktur sieht so aus:  
![Projektstruktur](https://github.com/PeterGyger/petergyger.github.io/blob/master/Ein_neuer_Anfang_mit_Jekyll-Now/Verzeichnisstruktur.png)  

Mittels des "Tree" Befehls der Windows CLI (cmd.exe) wird im ersten Teil die Verzeichnisstruktur angezeigt. Im zweiten Teil - "tree /f" werden auch die einzelnen Dateien in den Verzeichnissen angezeigt.  Dieses dient quasi als Landkarte des Projektes. Nachfolgend die Änderungen die ich in meinem Blogprojekt vorgenommen habe.

# Hintergrundfarbe ändern
Wie leicht vorstellbar ist, wird für die Darstellung CSS verwendet. Im Stammverzeichnis hat es die CSS Datei: "style.scss". Der Anfang der Datei sieht so aus:  

```
---
---

//
// IMPORTS
//

@import "reset";
@import "variables";
// Syntax highlighting @import is at the bottom of this file

/**************/
/* BASE RULES */
/**************/

html {
  font-size: 100%;
}

body {
	background: $white;
  font: 18px/1.4 $helvetica;
  color: $darkGray;
}
```  




