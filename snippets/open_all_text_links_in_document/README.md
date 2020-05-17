# Alle Text-Links auf einer Webseite im Sekundentakt in neuen Browser-Tabs öffnen (JavaScript Snippet)

## Vorbedingungen

- Die Website, oder streng genommen Textdatei enthält nur Links die untereinander aufgelistet sind
- Der Browser hat keinen Popup-Blocker der das Öffnen von Tabs verhindert
	- Notfalls beim Blockieren erlauben
	- Nach Erlaubniserteilung erneut versuchen
- JavaScript/Scripting Ausführung muss erlaubt sein (ist standardmäßig der Fall)
	- Falls Erweiterungen/Plugins installiert sind, auch hier die Erlaubnis zur Ausführung gewähren
- Der Rechner sollte es verkraften können die Anzahl der Links in Tabs zu öffnen
	- Arbeitsspeicher sollte ausreichend vorhanden sein
	- Der PC kann sehr langsam werden oder der Browser nach Erreichen der Arbeitsspeicher-Grenze abstürzen

## JavaScript Snippet

Das folgende JavaScript Snippet komplett kopieren und auf der Zielseite in die Browser Adresszeile einfügen:

```
javascript:document.body.innerText.split(String.fromCharCode(10)).forEach((l,i)=>setTimeout(()=>window.open(l),i*1500))
```

Als Ergebnis werden sekündlich neue Tabs mit den auf der Website aufgelisteten Links in Textform geöffnet!

**Nochmals die Warnung:** Bitte nur auf Webseiten ausführen die nichts anderes als die Links in Textform enthalten, sonnst wird versucht jeglichen Text in neuen Tabs zu öffnen! Der Browser/Rechner muss soviele geöffnete Tabs verkraften können, wie aufgezählte Links vorhanden sind.