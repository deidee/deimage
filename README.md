
# ![deimage](https://deidee.com/logo.svg?str=deimage)

Dit is niet een plaatje. (Ja, wel).

## Het wat en waarom

Tegenwoordig zijn er verschillende platformen als [Lorem Picsum
](https://picsum.photos/) waarmee je snel en eenvoudig dummyfoto’s in een opmaak kunt plaatsen. Soms wil je echter ouderwetse wireframes zodat de afbeeldingen niet afleiden van de layout en niemand (lees: een klant) een technisch ontwerp verwart met een grafisch ontwerp.

Daar zijn ook oplossingen voor (zoals [Placeholder.com](https://placeholder.com/)), maar het probleem daarmee is dat je precies moet aangeven welke afmetingen een afbeelding heeft. In een tijd van dynamische, responsieve en adaptieve layouts is dat praktisch niet haalbaar. Je zou er ook voor kunnen kiezen één afmeting te kiezen en die automatisch te laten schalen, maar dan worden de lijnen lelijk en dat is voor ons als ontwerpers ook geen optie.

Daarom hebben we een afbeelding ontwikkeld die je elke willekeurige afmeting kunt geven en die daarvoor altijd dezelfde soort lijnen zal tekenen. Zo krijg je een uniform wireframe dat snel en lekker werkt, zoals de dummyfoto’s dat meer grafisch kunnen.

## Voorbeeld

![](https://hetcdn.nl/deidee/images/deimage.svg)

## Gebruik

Download [het bestand](https://hetcdn.nl/deidee/images/deimage.svg), of laad het direct in vanaf ons CDN:

```html
<img alt="" src="https://hetcdn.nl/deidee/images/deimage.svg">
```

Je kunt de afbeelding zelfs dynamisch de afmetingen laten tonen, maar dan moet je een ``iframe`` (of `object`) gebruiken in plaats van een `img` (of `picture`). Dit heeft te maken met het feit dat webbrowsers geen scriptjes in afbeeldingen vertrouwen (maar je wel hele externe webapplicaties in mag laden).

```html
<iframe src="https://hetcdn.nl/deidee/images/deimage.svg"></iframe>
```

## Aanpassen

Staan de kleuren je niet aan? Download [het bestand](https://hetcdn.nl/deidee/images/deimage.svg) en pas de waarden voor ``stroke`` en `fill` aan:

```svg
<?xml version="1.0" standalone="no"?>
<svg xmlns="http://www.w3.org/2000/svg">
    <svg viewBox="0 0 300 300" preserveAspectRatio="none">
        <rect fill="gainsboro" stroke="gray" stroke-width="2" width="300" height="300" vector-effect="non-scaling-stroke" />
        <line x1="0" y1="0" x2="300" y2="300" stroke="gray" stroke-width="1" vector-effect="non-scaling-stroke" />
        <line x1="0" y1="300" x2="300" y2="0" stroke="gray" stroke-width="1" vector-effect="non-scaling-stroke" />
    </svg>
    <svg viewBox="0 0 300 300" preserveAspectRatio="xMinYMid meet">
        <text fill="dimgray" id="dimensions" x="20" y="35" textLength="6em" />
    </svg>
    <script type="text/javascript"><![CDATA[
    const dimensions = document.getElementById('dimensions');

    window.onload = window.onresize = function() {
        dimensions.textContent = window.innerWidth + ' × ' + window.innerHeight ;
    }

    ]]></script>
</svg>
```
