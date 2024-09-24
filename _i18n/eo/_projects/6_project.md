Ĉiu projekto havas belan prezentan paĝon por montri ĝiajn trajtojn.
Estas facile inkludi bildojn en fleksebla 3-kolumna plidetalhoma formato.
Faru viajn fotojn 1/3, 2/3 aŭ plenlargaj.

Por doni fonon al via projekto en la portfolia paĝo, simple aldonu la img-etikedon al la antaŭa materialo kiel jene:

    ---
    layout: page
    title: projekto
    description: projekto kun fona bildo
    img: /assets/img/12.jpg
    ---

<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/1.jpg" title="ekzempla bildo" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/3.jpg" title="ekzempla bildo" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="ekzempla bildo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Facile aldonu bildotekstojn. Maldekstre, vojo iras tra tunelo. Meze, folioj artiste falas en hipstra fotoŝuto. Dekstre, en alia hipstra fotoŝuto, lignhakisto tenas manplenan da pinfoli-oj.
</div>
<div class="row">
    <div class="col-sm mt-3 mt-md-0">
        {% include figure.html path="assets/img/5.jpg" title="ekzempla bildo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Ĉi tiu bildo ankaŭ povas havi bildotekston. Ĝi estas kiel magio.
</div>

Vi ankaŭ povas meti regulan tekston inter viaj vicoj de bildoj.
Diru, ke vi volis iom skribi pri via projekto antaŭ ol vi afiŝas la ceterajn bildojn.
Vi priskribas, kiel vi laboris, sudegis, *sangis* pro via projekto, kaj poste... vi malkaŝas ĝian gloron en la sekvanta vico de bildoj.


<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="ekzempla bildo" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="ekzempla bildo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
<div class="caption">
    Ankaŭ eblas havi artiste stilitajn bildojn 2/3 + 1/3, kiel ĉi tiuj.
</div>


La kodo estas simpla.
Simple voku viajn bildojn per `<div class="col-sm">` kaj metu ilin ene de `<div class="row">` (legu pli pri la <a href="https://getbootstrap.com/docs/4.4/layout/grid/">Grid-sistemo de Bootstrap</a>).
Por fari bildojn respondecaj, aldonu la klasojn `img-fluid` al ĉiu; por ronda angulo kaj ombroj, uzu la klasojn `rounded` kaj `z-depth-1`.
Jen la kodo por la lasta vico de bildoj supre:

{% raw %}
```html
<div class="row justify-content-sm-center">
    <div class="col-sm-8 mt-3 mt-md-0">
        {% include figure.html path="assets/img/6.jpg" title="ekzempla bildo" class="img-fluid rounded z-depth-1" %}
    </div>
    <div class="col-sm-4 mt-3 mt-md-0">
        {% include figure.html path="assets/img/11.jpg" title="ekzempla bildo" class="img-fluid rounded z-depth-1" %}
    </div>
</div>
```
{% endraw %}
