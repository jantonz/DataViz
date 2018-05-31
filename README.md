## Benvinguts/des a la pàgina del curs _Business Intelligence i Data Viz amb Teableau i Power BI_

Des d'aquí podreu seguir el curs sencer. És un bon lloc per començar a aprendre BI!

Aquesta web utilitza [Markdown](https://daringfireball.net/projects/markdown/) i està penjada a [GitHub](https://github.com/jantonz/DataViz). Un cop completat el curs podreu proposar canvis a la web i podran ser implementats a la següent edició. En llenguatge GitHub, els vostres _commits_ podran ser _pushed_ a la _branch_ principal.

Comencem fent un 
## **[wordcloud](https://www.wordclouds.com)**

# 1. Introducció al Business Intelligence

>Business Intelligence (BI) is a way of structuring, analyzing, and leveraging data. Organizations use BI to better understand their own business and to connect that understanding with their strategic decision-making.
>
>BI systems are built using specialized databases and software, but successful BI goes further than technology alone. When implemented well, BI supports an analytic culture in an organization. BI gives decision-makers the tools and methods to turn flat information into deeper understanding and informed action.
>
>   <cite>McGill University</cite>

![](https://tugasindividu.weebly.com/uploads/4/5/0/4/45049411/2797634_orig.jpg)

# 2. Tableau

## 2.1. Instal·lació de Tableau

Per començar amb el BI i Data Viz ens descarregarem Tableau.

Tableau és un softoware de pagament però he aconseguit llicències per aquest curs. Per activar-les, haureu de:
- [Descarregar la última versió de Tableau aquí](https://www.tableau.com/tft/activation).
- Clica al link anterior i apreta a Get Sarted. En el formulari, poseu el vostre mail a Business E-mail i escriu Barcelona Activa com a Organization.
- Activa el software amb la llicència proporcionada a classe.

Si voleu continuar utilitzant Tableau després que s'acabi el curs podeu demanar individualment una llicència d'estudiant (Tableau for Students) vàlida durant un any [aquí](https://community.tableau.com/community/students/).

## 2.2. Primers passos a Tableau

En obrir el programa se'ns obre la pàgina d'inici:

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Connect1.png)

1. La **icona de Tableau** ![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Connect2.png)
2. **Connect** ens permet connectar Tableau a diversos orígens de dades:
    - Fitxers, com Microsoft Excel, PDF, dades espacials, etc.
    - Dades allotjades a un servidor, com Tableau Server, Microsoft SQL Server, Google Analytics, etc.
3. **Open** et permet obrir projectes anteriors.
4. **Sample Workbooks** hi ha exemples de projectes.
5. A **Discover** hi ha diversos recursos online com tutorials, vídeos, etc.

Un full de treball té aquesta pinta:

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Drag28.png)

**Element** | **Description**
--- | ---  
Undo | És el botó de deshacer/desfés. També funciona el Ctrl + Z.
Cards i Shelves | _Cartes i Prestatges_. Cards són els contenidors dels diferents contorls de Tableau. Shelves és una manera de controlar Cards. Quan arrastres un camp des del panell Data fins a un prestatge de Columna o Fila, les dades s'afegeixen a l'eix X o Y.  Si arrastres camps del panell de Data fins a la carta Marks, pots controlar propietats com el color, forma, etc.
Data Pane | Et permet veure les dades que hi ha al dataset carregat, com el nom de les columnes.
Show/Hide Cards | Per mostrar o amagar Cartes.  

Alguns altres conceptes sobre Tableau:

**Term** | **Description**
--- | ---  
Aggregation | Row-level data rolled up to a higher category, such as sum of sales or total profit. Tableau does this automatically so you can break data down to the level of detail that you want to work with.  
Dimension vs. Measure | Dimensions són variables/dades categòriques; Measures són dades quantitatives (numèriques). És força típic _agregar_ dades quantitatives segons una o diverses variables categòriques (ex: vendes (Measure) per regió (Dimension).

## 2.3. Llegir dades (Step 1)

_Connectar-se_ a dades és molt fàcil. Només cal apretar Connect i sel·leccionar una font de dades. En aquest cas, ens connectarem a un dataset de mostra que es diu Sample - Superstore.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Connect4.png)

Aquest dataset d'exemple conté informació sobre productes, vendes, beneficis, etc.

## 2.4. Exploraroty Data Analysis (EDA)

### Step 2: Drag and drop to take a first look

El dataset conté 4 anys de dades i començarem amb donar un cop d'ull a les dades de vendes (sales) del 2014 al 2017. Creem un gràfic simple!

Bona part del workflow a Tableau es basa en arrastrar amb el ratolí. 
1. Des de Dimensions, arrastrem **Order Date** al prestatge **Columns**.
2. Des de Measures, arrastrem **Sales** al prestatge **Rows**.

Tableau genera el gràfic amb les vendes agregades com a suma.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Drag23.gif)

_Sempre que creeu un gràfic que inclou temps (en aquest cas, el camp Order Date), Tableau genera un gràfic de línia._

Per canviar el tipus de gràfic, seleccionem el menú drop-down **Marks**. Provem, per exemple, amb **Area**.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Drag2.png)

**Nota:** Abans de continuar, tornem a seleccionar **Automatic**.

Observem que les vendes augmenten anualment, però la informació continua essent força pobra. Explorem una mica més, a veure quins productes estan funcionant millor.

* * *

### Step 3: Refinem el gràfic

Una bona manera serà afegint dades cateegòriques:
    1. Des de Dimensions, arrastra **Category** al prestatge **Columns** a la dreta de YEAR(Order Date). 

El gràfic es converteix automàticament en un gràfic de barres. En afegir una segona variable categòrica, les dades s'organitzen segons aquesta variable i podem veure les dades separades anualment enlloc de forma contínua en el temps.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Drag4.png)

Proveu el botó: **Show Mark Labels**.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Drag6.png)

I també el botó **Swap**:

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Drag7.png)

Retornem a la visualització anterior abans de continuar.

Podem encara filar més prim i mirar els productes per sub-categoria per veure quins ítems són els best-sellers: Arrastrem **Sub-Category** a **Columns**. Com que és una altre variable categòrica, i discreta, apareixen barres per cada sub-categoria, agrupades per categoria i any.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Drag24.gif)

La idea és bona, però potser són masses dades alhora per poder entendre-les.

Es pot fer el mateix, però enlloc d'arrastrar **Sub-Category** al prestatge de columnes, es pot arrastrar **Sub-Category** a **Color** a la carta Marks. Ara tenim un gràfic de barres apilades amb cada color representant una subcategoria.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Drag8.png)

Podem canviar de lloc les barres canviant de lloc els noms a la llegenda.

Tornem a la visualització anterior abans de continuar.

* * *

### Afegim filtres

Els filtres serveixen per incloure o excloure valors del gràfic. En aquest exemple afegim dos filtres per fer més fàcil visualitzar les vendes per subcategoria en un any en concret.

    1. Al panell Data, a Dimensions, right-click **Order Date** i selecciona **Show Filter**.

    2. Fem el mateix amb el camp **Sub-Category**.

Els filtres s'afegeixen a la part dreta del full però es poden moure allà on convingui.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Drag25.gif)

### Afegim color

Podem veure que alguns productes es venen poc, de forma consistent durant els 4 anys. Però potser no és així pel que fa al benefici. Arrastrem **Profit** a **Color** a la carta Marks a veure què passa.

Algun nou insight?

Afegir colors pot millorar el gràfic estèticament, però també pot desvetllar tendències que no s'havien trobat abans. Els colors per defecte es poden canviar clicant a **Color** i després a **Edit Colors**.

Ens cal investigar els productes que no aporten beneficis, a veure si han tingut pèrdues any rere any. Petita pista: utilitzarem filtres!

* * *

Jugant, jugant, hem decidit trencar el gràfic per regió:

    1. Selecciona **All** al filtre **Sub-Category** per mostrar totes les sub-categories altre cop.  

    2. De Dimensions, arrastrem **Region** a **Rows** i ho posem a l'esquerra de Sum(Sales). 

Tableau crea un gràfic amb diversos eixos segons la regió.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/FocusRegions1.png)

Torneu a utilitzar filtres per observar els ítems que tenien pèrdues.

Les màquines del sud encara tenen un benefici més negatiu que les altres regions: un nou insight! 

Aquesta visualització ens agrada prou. Volem guardar-la però sense perdre res del que hem fet anteriorment. Si fem clic dret al nom del full "Sheet1" podem duplicar-lo. I de pas, canviar-li el nom.

    3. L'anomenem _Vendes al Sud_

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Drag27.gif)

Guardem el llibre: **File** &gt; **Save As**. Per defecte, es guardarà a **Documents** &gt; **My Documents** &gt; **My Tableau Repository**.

* * *

### Step 4: Explora les dades sobre el mapa

Hem vist alguns productes amb pèrdues a la regió Sud. Com que la columna **Region** conté dades geogràfiques, podem visualitzar-les sobre un mapa.

En aquest exemple Tableau ha reconegut les dades de Country, State, City, i Postal Code gràcies al nom de les variables. Sempre va bé que els noms de columnes/variables siguin descriptius!

Els valors geogràfics s'indiquen com a ![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Explore16.png). Si Tableau no reconeix les dades com a geogràfiques, es poden assignar manualment.

### Build a map view

Comencem amb un nou worksheet.

  1. Apreta **New worksheet** a sota el worksheet.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/explore17.png)

  2. Un doble-click a **State** l'afegeix a la carta **Detail** (o bé es pot arrastrar).

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Explore3.gif)

Fixeu-vos que a columnes i files hi han aparegut els camps latitud i longitud! Latitud i longitud són essencials quan es treballa amb mapes. 

Centrem-nos en el Sud:

  3. Filtrem només la regió sud.

  4. Afegim **Sales** a una carta i mirem que quedi de la següent manera:
  
![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Explore4.gif)

  5. Canvia una mica el **Color** com hem fet abans.

  6. Seleccionem la paleta que més convingui tenint en compte que volem separar estats que venen molt dels que venen poc.

Això seria un resultat adequat:

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Explore5.png)

Però un moment. Potser millor mirar beneficis que no pas vendes.

  7. Cliquem **Undo**.

  8. I pintem els estats segons beneficis, no pas vendes..

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Explore6.png)

Estats que tenien bones vendes en realitat tene pèrdues!

### Step 5: Drill down into the details

Tennessee, North Carolina, i Florida tenen benefici negatiu. Per conèixer el motiu investigarem més en detall.

  1. Doble-click **Sheet 3** i anomenem el llibre **Profit Map**.

  2. Dupliquem el full i l'anomenem **Negative Profit Bar Chart**.

  3. Apretem **Show Me** a dalt a la dreta de la pantalla i seleccionem **horizontal bars**.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Explore8.png)

I ja tenim altre cop un gràfic de barres.

  4. Seleccionem les barres de **Tennessee**, **North Carolina**, i **Florida** i eliminem la resta, seleccionant **Keep Only**.
  
Ara mirarem les ciutats en aquests estats.

  5.A **Rows**, cliquem el símbol de sumar a **State** per mostrar els camps de Ciutat. 
  
Ens trobem de nou amb massa informació a la pantalla, així que farem un Top N anàlisi.

### Create a Top N Filter

Explicar els valors més alts (o més baixos, en aquest cas), pot ajudar a explicar la tendència observada.

1. Arrastra **City** al prestatge **Filters**.

2. Al diàleg que apareix, apretem la pestanya Top. Després:

    1. Click **By field**.

    2. Volem seleccionar els **Bottom** **5** (els 5 pitjors).

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Explore12.png)

    3. Click **OK**.

En aquest moment podem trobar algunes inconsistències en el gràfic. Això és degut a com Tableau aplica els filtres; ho fa en aquest ordre:

    1. Extract Filters

    2. Data Source Filters

    3. Context Filters

    4. Top N Filters

    5. Dimension Filters

    6. Measure Filters


Per resoldre-ho, cal clicar amb el botó dret a _Inclusions (Country, State) (Country, State)_ i apretar **Add to Context**.

Ara ens trobem, però que hi ha una ciutat amb benefici positiu. Això és perquè Tableau no pot diferenciar entre Jacksonville,
NC, i Jacksonville, FL, perquè ciutat és la vista més detallada que apliquem. Si afegim Postal Code, la ciutat amb benefici desapareix de la visualització.

El resum és aquest:

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Explore13.gif)

* * *

### Identify the troublemakers

Per acabar d'anar en detall, podem filtrar per Sub-Category per identificar els productes que incrementen les pèrdues.

  1. Arrastrem **Sub-Category** al lloc adequat.
  2. Ho pintem de color.
  3. Filtrem per any.

Ara podem explorar quins productes fan disminuir els beneficis cada any.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Explore15.png)

* * *

### Verify your findings

Millorarien els beneficis si eliminem binders, machines, i tables de Florida, North Carolina, i Tennessee? Podem respndre-ho de la manera següent:

  1. Tornem al mapa que hem creat abans.

  2. Mostrem el filtre per a **Sub-category**.
  
  3. Arrastrem **Profit** i **Profit Ratio** a **Label**. 

  4. Right-click **Order Date** i apretem **Show Filter**. 

  5. Eliminem **Binders**, **Machines**, i **Tables** del filtre Sub-Category i observem com afecten els beneficis de cada estat. 

Això és un descobriment!

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/explore21.gif)

* * *

## 2.5. Fer un Dashboard (Step 6)

L'èmfasis el volem en el fet que alguns ítems venuts a determinats llocs no estan funcionant. Un gràfic de barres i el mapa ho demostraran.

  1. Apreta **New dashboard**.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Build1.png)

  2. Arrastra **Sales in the South** al dashboard.

  3. Arrastra **Profit Map** al dashboard, sota l'anterior.

Hauria de quedar així:
![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Build2.png)

Cal millorar el gràfica de barres, que queda molt estret.

* * *

### Arrange your dashboard and add interactivity

Mini-exercici: intenta deixar el Dashboard com el que es mostra:

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Build3.gif)

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Build4.gif)

* * *

## 2.6. Crear una història i compartir-la (Step 7 i 8)


Una història es tracta d'un recorregut més o menys interactiu pels resultats, on se sol recrear les parts més importants del procés d'exploració. 

### Create your first story point

1. Click **New story**. És l'últim botó d'aquest panell, ja estem acabant!

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Story1.png)

Les històries s'assemblen molt als dashboards. El workflow és el mateix. Es poden arrastrar worksheets i dashboards per presentar-los a una **Story**.

Per començar, volem presentar una vista global dels resultats a l'audiència.

2. Arrastrem la worksheet **Sales in the South**  al full en blanc. 

3. La _caption_ descriu una mica aquesta primera pàgina de la story.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Story2_updated.png)

Un cop presentada la foto global, volem posar l'accent a les vendes de màquines a Carolina del Nord. 

### Highlight machine sales

Ara farem la segona pàgina de la història.

  1. Click a **Duplicate** per duplicar aquesta primera pàgina. 

  2. Al filtre Sub-Category, seleccionem només **Machines**.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Story4_updated.png)

  3. Canviem el nom de la caption.

Ara falta posar l'accent en les vendes de màquines en determinats estats (no pas les vendes globals!). Aquí entrarà en joc un mapa.

  4. Apretem **Blank** per crear una nova pàgina, aquest cop blanca.

Recordem que el principal és que les màquines a Carolina del Nord (NC) provoquen pèrdues, ho hem vist mentre fèiem el dashboard. Com dèiem, cal afegir-hi un mapa.

  5. Arrastrem la dashboard que  hem fet abans a la pàgina.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Story6.png)

  6. I canviem la caption per un títol descriptiu.

La idea ara és centrar-nos només en Carolina del Nord. Utilitzant el botó de duplicar i el filtre que ja existeix d'any, crearem diverses pàgines en aquesta història. NC el 2014-17, NC el 2014, NC el 2015, NC el 2016 i NC el 2017.

En aquesta diapositiva/pàgina, que es basa en dades del 2017, podríem avançar una petita conclusió, un petit text que ens porti a la diapositiva final, que serà la del gràfic de barres de pèrdues.

  1. Per fer la mini-conclusió, arrastrem **Drag to add text** a la pàgina, l'editem i ja podem continuar amb la diapositiva final.

  2. Creem una nova diapositiva blanca i hi arrastrem el full **Negative Profit Bar Chart**.

  3. Mostrem només el **2017**. 

Ara s'observa que les pèrdues provenien principalment de Burlington, NC.

  4. Click dret a **Burlington** (la bar) i afegim una anotació amb **Annotate** &gt; **Mark**.

  5. Hi escrivim alguna cosa de l'estil "Les vendes de màquines a Burlington van perdre gairebé 4000$".

  6. Donem nom a la pàgina, donem nom a la història i la podem revisar a **Window** &gt; **Presentation mode**.

Si ens molesta que la presentació sigui massa gran per la pantalla (i que apareguin barres de scroll), podem sortir del mode presentació i canviar la mida del dashboard que presentem durant la història.

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Story10.png)

### Share your findings

A Tableau Public, les visualitzacions són públiques. No l'utilitzeu amb dades confidencials! La versió de pagament és privada i es diu Teblau Server.

  1. Selecciona **Server** &gt; **Tableau Public** &gt; **Save to Tableau Public**.

  2. Fem el login.

  3. Ens demanarà **Create Data Extract**, que vol dir que agafarà les dades que hem utilitzat durant la presentació, les transformarà a un format específic de Tableau i les pujarà online. Això també vol dir que la presentació no s'actualitzarà automàticament quan canvïin les dades! Ho podem fer des de **Data** &gt; **Sample - Superstore** &gt; **Extract Data**.

  4. Tornem a seleccionar **Server** &gt; **Tableau Public** &gt; **Save to Tableau Public**, el procés pot tardar una estona depenent de la connexió.

<br><br>

* * *

# 3. PowerBI

## 3.1. Instal·lació de PowerBI

EL link per instal·lar Power BI el podeu trobar aquí.
- [PowerBI](https://powerbi.microsoft.com/en-us/)

## 3.2. Workflow

* Llegir dades a Power BI Desktop, i crear un report.

* Publicar a Power BI service, per crear visualitzacions i dashboards.

* Compartir les dashboards amb altres

![](https://docs.microsoft.com/ca-es/power-bi/guided-learning/includes/media/0-1-intro-using-power-bi/c0a1_1.png)

Els blocs principals de creació són:

* Visualitzacions

![Visualitzacions](https://docs.microsoft.com/es-es/power-bi/guided-learning/includes/media/0-0b-building-blocks-power-bi/c0a0b_1.png)

* Conjunts de dades

![Conjunts de dades](https://docs.microsoft.com/es-es/power-bi/guided-learning/includes/media/0-0b-building-blocks-power-bi/c0a0b_2.png)

* Informes

![Informes](https://docs.microsoft.com/es-es/power-bi/guided-learning/includes/media/0-0b-building-blocks-power-bi/c0a0b_3.png)

* Dashboards (informes d'una pàgina)

* Icones

![Icones](https://docs.microsoft.com/es-es/power-bi/guided-learning/includes/media/0-0b-building-blocks-power-bi/c0a0b_4.png)


## 3.3. Llegir dades

És molt fàcil llegir dades:

![Load data](https://docs.microsoft.com/en-us/power-bi/guided-learning/includes/media/1-2-connect-to-data-sources-in-power-bi-desktop/1-2_2.gif)

### 3.3.1. Des d'un Excel

Nosaltres descarregarem un .xlsx d'aquest [link](http://download.microsoft.com/download/1/4/E/14EDED28-6C58-4055-A65C-23B4DA81C4DE/Products.xlsx) i en llegirem les dades.

Un cop establerta la connexió, clicarem a editar per sel·leccionar només les columnes d'interès:
![Editar](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_2.png)

En aquest pas eliminarem totes les columnes excepte ProductID, ProductName, UnitsInStock, i QuantityPerUnit.

El que s'obre quan apretes editar és el que es diu Power Query Editor. També s'hi pot accedir apretant a Edit Queries des de la Home. Els següents passos els farem al Power Query Editor.

1. Seleccionem ProductID, ProductName, QuantityPerUnit, i UnitsInStock (Ctrl+Click per sel·leccionar més d'una columna alhora, o Shift+Click per seleccionar columnes que estan una al costat de l'altra).

2. Apretem a Remove Columns > Remove Other Columns, o right-click al nom d'una columna i click a Remove Other Columns.

![Editar](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/anlayzingsalesdata_removeothercolumns.png)

Quan el Power Query Editor es connecta a dades, revisa cada camp (cada columna) per determina el millor tipus de dada (caràcters, números, dates, etc.). Per aquest fitxer d'Excel, els productes en stock serà sempre un camp numèric enter, així que es pot confirmar que UnitsInStock siguin Whole Number.

1. Seleccionar la columna UnitsInStock.
2. Seleccionar el menú Data Type des del menú de la Home.
3. Si no és ja Whole Number, seleccionar-ho.

![Canviar Data Type](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/anlayzingsalesdata_wholenumber.png)

### 3.3.2. Des d'un OData feed

#### Pas 1. Connect to an OData feed
[OData](http://www.odata.org/) vol dir Open Data Protocol, i és un protocol open source que permet la creació i consum de dades a través d'una API [RESTful](https://ca.wikipedia.org/wiki/REST) d'una manera força estàndard.

En aquest cas ens connectarem a dades d'un sistema de vendes. Importarem les dades a Power BI Desktop des del Northwind OData feed a la següent URL: http://services.odata.org/V3/Northwind/Northwind.svc/

Per cert, encara estam al Power Query Editor!
1. Des de la Home seleccionem Get Data, i busquem OData Feed data source. 
2. L'únic que necessitem és copiar la URL i enganxar-la al diàleg que apareix (Basic).
3. Seleccionem la taula Orders i apretem a Ok.

![OData](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/anlayzingsalesdata_odatafeed.png)

#### Pas 2. Expand the Order_Details table

La taula Orders conté una referència a una altra taula que es diu Details, que és la que conté els productes que van ser inclosos a cada comanda (Order). Això pot passar quan ens connectem a una font de dades amb diverses taules (per exemple, una base de dades relacional).

En aquest pas expandim la taula Order_Details que està relacionada amb la taula Orders, per combinar les columnes  ProductID, UnitPrice, i Quantity de la taula Order_Details a la taula Orders. Així es podria representar les dades en aquestes taules:

![DB Relacional](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/orderdetails.png)

La operació "expandir" combina les columnes d'una taula relacionada capa una altra taula. Quan la query és executada, files de la taula relacionada (Order_Details) es combinen amb les de l'altra taula (Orders).

Veurem 3 noves columnes i diverses files a la taula Orders, una per cada fila de la columna relacionada.

1. A Power Query View, scroll cap a la columna Order_Details.
2. A la columna Order_Details, selecciona expand ![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/expand.png).
3. Al drop-down d'Expand:
  - Selecciona Select All Columns per desclicar totes les columnes.
  - Selecciona ProductID, UnitPrice, i Quantity.
  - Click OK. 
  
![Expandir taula](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/7.png)

#### Pas 3. Remove other columns to only display columns of interest

Com a petit exercici, elimineu totes les columnes excepte OrderDate, ShipCity, ShipCountry, Order_Details.ProductID, Order_Details.UnitPrice i Order_Details.Quantity. Per fer-ho, però:
1. Seleccioneu TOTES les columnes.
2. Des-seleccioneu les columnes d'interès.
3. Elimineu les columnes seleccionades.

Així, per practicar!

#### Pas 4. Calculate the line total for each Order_Details row

Power BI et deixa fer càlculs de columnes _que estàs important_. Això farem: una columna nova amb el càlcul _suma_ per cada fila de la taula Order_Details. 

Apretem Add Column > Custom Column.De nom es dirà LineTotal i la seva fórmula serà [Order_Details.UnitPrice] * [Order_Details.Quantity]. LineTotal serà el nom de la columna i el seu valor, el resultat de la multiplicació de les columnes Order_Details.UnitPrice i Order_Details.Quantity.

#### Pas 5. Set the datatype of the LineTotal field

El botó dret ajuda!

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/9.png)

#### Pas 6. Rename and reorder columns in the query

Ara podem canviar el nom de les columnes i canviar-les d'ordre per facilitar l'anàlisi i la creació de reports.

1. A Power Query Editor, arrastrem la columna LineTotal a l'esquerra, després de ShipCountry.

2. Eliminem el prefix _Order_Details._ de les columnes Order_Details.ProductID, Order_Details.UnitPrice i Order_Details.Quantity fent doble-click a cada títol de columna i eliminant el text del nom.

## 3.4. Data Manipulation

Per fer un report no cal que ajuntem les dues bases de dades que hem llegit. Enlloc d'això, Power BI permet crear _relacions_ entre datasets. Això es pot fer sempre i quan hi hagi alguna columna en comú entre els dos origens de dades.

Les dues taules que estem treballant, Orders i Products, tenen la columna ProductID en comú, així que podem relacionar-les. Per fer-ho només cal especificar a PowerBI que les columnes estan relacionades (contenen ela mateixos valors).

Això farem: confirmar que hi ha una relació entre les columnes Products i Total Sales queries.

1. Primer carreguem el model que hem creat al Power Query Editor a PowerBI tot apretant Close & Load.

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_4.png)

2. Pot tardar una mica en carregar les queries.

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/11.png)

3. Cliquem a Manage Relationships.

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_5.png)


4. Apretem New…

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_6.png)

5. En intentar de crear una relació, veiem que n'hi una que ja existeix. Sembla que ja s'ha detectat una relació entre les columnes ProductID de les dues taules. Perfecte!

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/12.png)


6. No cal executar res perquè la relació ja ha estat trobada automàticament. Apretem Cancel, i cliquem a la Relationship un cop a Power BI Desktop.

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_7.png)

Si fem doble clic sobre la fletxa, ens apareix un diàleg de Edit Relationship.

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_8.png)

No cal que canviem res, així que apretem Cancel i ja estem llestos per visualitzar dades!

## 3.5. Creació d'un Report

Una de les gràcies del programa és que permet crear moltes visualitzacions per guanyar _insight_ sobre les dades. Es poden construir reports amb diverses pàgines i cada pàgina pot tenir diferents gràfics. També es pot interactuar amb les visualizacions per analitzar i entendre millor les dades.

El que farem serà un report basat en les dades que hem carregat prèviament. S'utilitza el panell de Fields per seleccionar les columnes que utilitzarem per crear les visualitzacions.

#### Gràfic  1: Quantitat per cada producte

Arrastra **Quantity** des d'Orders del panell Field (a la dreta de la pantalla) fins a un espai buit del full. Fent això es crea un gràfic de barres molt senzill. Després, arrastra la columna **ProductName** a sobre el mateix gràfic. Després seleccionem **Sort By Quantity** apretant a l'extrem superior dret de la visualització.

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/19.png)

#### Gràfic  2: LineTotal vs temps

Arrastrem **LineTotal** a una part blanca del full, fet que crea un altre gràfic de barres. Arrastrem també a sobre **OrderDate**. Podem jugar amb el menú drop down que s'obre apretant la fletxa que hi ha a OrderDate, al camp Axis del panell de  Visualizations: sel·lecciona OrderDate enlloc de Date Hierarchy. També pots transformar el gràfic de barres en un LineChart.

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/20.png)

#### Gràfic  3: Quantitat per país

Ara que això està fet, arrastrem **ShipCountry** a una part blanca del full. Com que la columna conté dades geogràfiques, s'ha creat un mapa automàticament. A més, el mapa conté un punt per a cada país que té **Orders**. Ara podem arrastrar **LineTotal** al camp de Size (o directament sobre el mapa); els cercles del mapa i les seves mides representen el valor de LineTotal per comandes enviades a cada país.

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/21.png)

Ara podem _interactuar_ amb els gràfics.

Per exemple, si cliquem al cercle de dins de Canadà veurem que la resta de gràfics es filtren automàticament per representar la quantitat (Quantity) i el total de comandes (LineTotal) només per Canadà.

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/22.png)

## 3.6. Publicació del Report

Publicar el report és realment fàcil. Cal clicar el botó de Publish:

![](https://docs.microsoft.com/en-us/power-bi/guided-learning/includes/media/4-1-publish-reports/4-1_1.png)

Això sí, caldrà que ens fem un compte a PowerBI online, que és gratuït.

Quan acabem el procés, podem tornar a PowerBI i introduir l'usuari i contrassenya. Tot seguit el report es publica a PowerBI Service. Podem entrar al [compte d'usuari](https://app.powerbi.com/groups/me/contentlist). I ja està online!

![](https://docs.microsoft.com/en-us/power-bi/guided-learning/includes/media/4-1-publish-reports/4-1_4.png)

## 3.7. De Report a Dashboard

Des de PowerBI Service entrem al report que acabem de publicar i _anclem_ les visualitzacions que volem al **Dashboard** apretant el botó ![](https://docs.microsoft.com/en-us/power-bi/media/service-dashboard-create/power-bi-pin-icon.png).

Donem un nom al Dashboard i podem visualitzar-lo o bé afegir-hi més gràfics.

![](https://docs.microsoft.com/en-us/power-bi/media/service-dashboard-create/power-bi-pin-tile.png)

Els gràfics es poden arrastrar des de la web mateix.

### Dashboards vs. reports (anglès)

| **Capability** | **Dashboards** | **Reports** |
| --- | --- | --- |
| Pages |One page |One or more pages |
| Data sources |One or more reports and one or more datasets per dashboard |A single dataset per report |
| Available in Power BI Desktop |No |Yes, can create and view reports in Desktop |
| Pinning |Can pin existing visualizations (tiles) only from current dashboard to your other dashboards |Can pin visualizations (as tiles) to any of your dashboards. Can pin entire report pages to any of your dashboards. |
| Subscribe |Can't subscribe to a dashboard |Can subscribe to report pages |
| Filtering |Can't filter or slice |Many different ways to filter, highlight, and slice |
| Set alerts |Can create alerts to email you when certain conditions are met |No |
| Feature |Can set one dashboard as your "featured" dashboard |Cannot create a featured report |
| Natural language queries |Available from dashboard |Not available from reports |
| Can change visualization type |No. In fact, if a report owner changes the visualization type in the report, the pinned visualization on the dashboard does not update |Yes |
| Can see underlying dataset tables and fields |No. Can export data but can't see tables and fields in the dashboard itself. |Yes. Can see dataset tables and fields and values. |
| Can create visualizations |Limited to adding widgets to dashboard using "Add tile" |Can create many different types of visuals, add custom visuals, edit visuals and more with Editing permissions |
| Customization |Can do things with the visualizations (tiles) like move and arrange, resize, add links, rename, delete, and display full screen. But the data and visualizations themselves are read-only. |In Reading view you can publish, embed, filter,export, download as .pbix, view related content, generate QR codes, analyze in Excel, and more.  In Editing view you can do everything mentioned so far and so much more. |

Els dashboards es poden compartir, però només amb la versió pro (de pagament).

# 4. Següents passos

### [Tableau VS PowerBI](https://www.betterbuys.com/bi/tableau-vs-power-bi/)

Check this out:
- [Tutorial de Tableau: dades de GapMinder](https://www.edupristine.com/blog/animation-in-tableau)
- [Tutorial de Tableau: accidents d'aviació](https://www.edupristine.com/blog/visualizing-air-crashes-history-tableau)
- [Tableau a Coursera](https://www.coursera.org/specializations/data-visualization)
- [Tutorial de PowerBI (I)](https://docs.microsoft.com/es-es/power-bi/guided-learning/gettingstarted)
- [Tutorial de PowerBI (II)](https://docs.microsoft.com/en-us/power-bi/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed)
- [Tutorial de PowerBI (Facebook)](https://docs.microsoft.com/en-us/power-bi/desktop-tutorial-facebook-analytics)
- [Tutorial de PowerBI (Sentiment Analysis)](https://community.powerbi.com/t5/Community-Blog/Text-Analytics-in-Power-BI-Extraction-of-key-phrases-from/ba-p/88483)
- [Tutorial de PowerBI (elTemps)](https://tektuts.com/power-bi-tutorial-create-a-weather-dashboard/)

### D'on puc treure les dades?
- [Gapminder](https://www.gapminder.org/data/)
- [IndexMundi](https://www.indexmundi.com/)
- [data.world](https://data.world/) (hi ha connector per a PowerBI)

<br><br>
<br><br>

_Josep Anton Mir Tutusaus. 2018 ._

<br><br>

-----------------------------------
