# Forløb 8
## Biblioteket pakkes ned i en Jar

Jeres bibliotek er ikke et rigtigt bibliotek før det er pakket ned i en JAR-file.
JAR står for "Java Archive", og processing er jo bare Java nedenunder motorhjelmen, så en JAR fil er altså et måde at lave et bibliotek på i processing.


------------------------------------------------------------------------------------------------------------------------------------------------------


## 1. Lav din egen JAR
Det er muligt at konstruere en JAR fil i en konsol, men vi vælger et lille "hack" og får processing til det.    

Metoden har jeg beskrevet nedenfor:   
1. Vælg "File"
2. Vælg "Export Application..."
3. I dialog-boksen vælg "windows" (også selv om du anvender mac eller noget andet)
4. Når processing er færdig med at eksportere applikationen åbnes eksport-mappen
5. I eksport-mappen vælges "application.windows64" og derefter "lib"
6. I mappen "lib" ligger din JAR fil - den hedder det samme som din applikation

Video forklaring:    
<iframe width="560" height="315" src="https://www.youtube.com/embed/iScvXVpLOAI" title="FiltrerOgSelectData" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


------------------------------------------------------------------------------------------------------------------------------------------------------


## 2. Overfør din JAR over i en anden applikation
Hele ideen med at pakke alt din biblioteks-kode ned i en JAR er at den nemt kan anvendes af andre, som et slags bibliotek ;-)   

Det eneste man skal gøre, for at anvende en JAR, er at trække JAR'en ind i sin applikation, processing vil nu lava en mappe, der hedder "code" og placere
Jar-filen der, og det er herefter muligt at anvende alt det kode der er inde i JAR-filen.

Video forklaring:   
<iframe width="560" height="315" src="https://www.youtube.com/embed/oxlU4Ghkc08" title="FiltrerOgSelectData" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


------------------------------------------------------------------------------------------------------------------------------------------------------


## 3. Anvend kode fra en JAR

Nedenfor ses et eksempel på kode, der anvender klasser og metoder fra JAR-filen.
*Bemærk dog at dine klasser sandsynligvis hedder noget andet!!!*:

```java
 //GUIBib er selve bibliotek-programmets navn!
GUIBib bib = new GUIBib();

//Læg mærke til at GUIHandler klassen er "inde" i GUILib,
//derfor denne specielle måde at lave en GUIHandler
GUIBib.GUIHandler handler = bib.new GUIHandler();

//Kanp er også inde i "GUIBib"
GUIBib.Knap k;

void setup(){
  k = handler.createKnap();
}
```


Video forklaring:    
<iframe width="560" height="315" src="https://www.youtube.com/embed/gYuJdr9r1k0" title="FiltrerOgSelectData" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>


------------------------------------------------------------------------------------------------------------------------------------------------------


## JAR KODEN FEJLER - OG LØSNING!

Men hvis man prøver at anvende JAR-filen bliver man blevet begravet i exceptions!!! hvorfor???  
****Problem: Processing-koden inde i JAR filen anvender det forkerte processing-objekt!****
****Løsning: Omskrive koden biblioteket!****

```java
PApplet p;//øverst i biblioteks koden
```
```java
class Knap{
  void tegnKnap(){
    p.rect(10,10,10,10);  //processing-kode i biblioteket,- skriv "p." foran!!
  }
}
```
```java
GUIBib bib = new GUIBib();
GUIBib.GUIHandler handler = bib.new GUIHandler();
GUIBib.Knap k;
void setup(){
  bib.p = this;   //Gemmer den "rigtige" processing inde i Biblioteket
  //osv.
}
```

Video forklaring:    
<iframe width="560" height="315" src="https://www.youtube.com/embed/oZEs4unZWo0" title="FiltrerOgSelectData" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
