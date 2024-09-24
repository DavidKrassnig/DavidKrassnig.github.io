Jedes Projekt hat eine wunderschöne Funktionen-Showcase-Seite.
Es ist einfach, Bilder in einem flexiblen 3-Spalten-Rasterformat einzufügen.
Machen Sie Ihre Fotos 1/3, 2/3 oder in voller Breite.

Um Ihrem Projekt auf der Portfolio-Seite einen Hintergrund zu geben, fügen Sie einfach das img-Tag in den Front Matter ein, wie folgt:

    ---
    layout: page
    title: Projekt
    description: Ein Projekt mit einem Hintergrundbild
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/1.jpg" title="Beispielbild" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="Beispielbild" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="Beispielbild" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Bildunterschriften sind einfach. Links führt eine Straße durch einen Tunnel. In der Mitte fallen Blätter künstlerisch bei einem Hipster-Fotoshooting. Rechts, bei einem anderen Hipster-Fotoshooting, hält ein Holzfäller eine Handvoll Kiefernnadeln.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="Beispielbild" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Auch dieses Bild kann eine Bildunterschrift haben. Es ist wie Magie.
</div>

Sie können auch normalen Text zwischen Ihren Bilderreihen platzieren.
Angenommen, Sie möchten ein wenig über Ihr Projekt schreiben, bevor Sie den Rest der Bilder veröffentlichen.
Sie beschreiben, wie Sie für Ihr Projekt geschuftet, geschwitzt, *geblutet* haben, und dann... enthüllen Sie dessen Glanz in der nächsten Reihe von Bildern.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="Beispielbild" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="Beispielbild" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Sie können auch künstlerisch gestaltete Bilder im Verhältnis 2/3 + 1/3 haben, wie diese.
</div>


Der Code ist einfach.
Umschließen Sie Ihre Bilder einfach mit `<div class="col-sm">` und platzieren Sie sie innerhalb von `<div class="row">` (lesen Sie mehr über das <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Bootstrap Grid</a>-System).
Um Bilder responsiv zu gestalten, fügen Sie jeder ein `img-fluid`-Klasse hinzu; für abgerundete Ecken und Schatten verwenden Sie die Klassen `rounded` und `z-depth-1`.
Hier ist der Code für die letzte Bilderreihe oben:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="Beispielbild" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="Beispielbild" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
