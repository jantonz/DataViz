## Benvinguts/des a la pàgina del curs _Business Intelligence i Data Viz amb Teableau i Power BI_

Des d'aquí podreu seguir el curs sencer. És un bon lloc per començar a aprendre BI!

Aquesta web utilitza [Markdown](https://daringfireball.net/projects/markdown/) i està penjada a [GitHub](https://github.com/jantonz/DataViz). Un cop completat el curs podreu proposar canvis a la web i podran ser implementats a la següent edició. En llenguatge GitHub, els vostres _commits_ podran ser _pushed_ a la _branch_ principal.

# 1. Introducció al Business Intelligence

>Business Intelligence (BI) is a way of structuring, analyzing, and leveraging data. Organizations use BI to better understand their own >business and to connect that understanding with their strategic decision-making.
>
>BI systems are built using specialized databases and software, but successful BI goes further than technology alone. When implemented >well, BI supports an analytic culture in an organization. BI gives decision-makers the tools and methods to turn flat information into >deeper understanding and informed action.
>
> -- <cite>McGill University</cite>

![](https://cdn.business2community.com/wp-content/uploads/2014/02/BI-infographic1.jpg)

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

## 2.3. Llegir dades


In the Connect pane, under Saved Data Sources, click on Sample - Superstore to connect to the sample data set. Your screen will look something like this:

![](http://onlinehelp.tableau.com/current/guides/get-started-tutorial/en-us/Img/Connect4.png)

The Sample - Superstore data set comes with Tableau. It contains information about products, sales, profits, and so on that you can use to identify key areas for improvement within this fictitious company.



























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

### 3.3.1. Des d'un OData feed

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

Si cliquem sobre la fletxa, ens apareix un diàleg de Edit Relationship.

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/t_excelodata_9.png)

No cal que canviem res, així que apretem Cancel i ja estem llestos per visualitzar dades!

## 3.5. Creació d'un Report

Una de les gràcies del programa és que permet crear moltes visualitzacions per guanyar _insight_ sobre les dades. Es poden construir reports amb diverses pàgines i cada pàgina pot tenir diferents gràfics. També es pot interactuar amb les visualizacions per analitzar i entendre millor les dades.

El que farem serà un report basat en les dades que hem carregat prèviament. S'utilitza el panell de Fields per seleccionar les columnes que utilitzarem per crear les visualitzacions.

#### Gràfic  1: Units en Stock per Product i Total Sales per Year

Arrastra **UnitsInStock** des del panell Field (a la dreta de la pantalla) fins a un espai buit del full. Fent això es crea una taula de visualització. Després, arrastra la columna ProductName a la caixa d'Axis (que vol dir _eix_). Després seleccionem **Sort By > UnitsInStock** apretant a l'extrem superior dret de la visualització.

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/14.png)

Arrastrem **OrderDate** a una part blanca del full, i arrastrem també **LineTotal** i seleccionem Line Chart. 

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/15.png)

Ara que això està fet, arrastrem **ShipCountry** a una part blanca del full. Com que la columna conté dades geogràfiques, s'ha creat un mapa automàticament. Ara podem arrastrar **LineTotal** al camp de Values; els cercles apareixen al mapa i les seves mides representen el valor de LineTotal per comandes enviades a cada país.

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/17.png)

Ara podem _interactuar_ amb els gràfics.

Per exemple, si cliquem al cercle de dins de Canadà veurem que la resta de gràfics es filtren automàticament per representar l'stock (ShipCountry) i el total de comandes (LineTotal) només per Canadà.

![](https://docs.microsoft.com/en-us/power-bi/media/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed/18.png)

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

Check this out:
- [Tutorial de PowerBI](https://docs.microsoft.com/es-es/power-bi/guided-learning/gettingstarted)
- [Tutorial de PowerBI (Facebook)](https://docs.microsoft.com/en-us/power-bi/desktop-tutorial-facebook-analytics)
- [Tutorial de PowerBI (II)](https://docs.microsoft.com/en-us/power-bi/desktop-tutorial-analyzing-sales-data-from-excel-and-an-odata-feed)
- [Tableau a Coursera](https://www.coursera.org/specializations/data-visualization)


<br><br>
<br><br>

_Josep Anton Mir Tutusaus. 2018 ._

<br><br>

-----------------------------------

<div class="foundation-wrap off-canvas-wrapper">

<div class="off-canvas-wrapper-inner" data-off-canvas-wrapper="">

<aside class="off-canvas position-left" id="offCanvas" data-off-canvas="" data-position="left" data-mc-ignore="true"></aside>

<div class="off-canvas-content inner-wrap" data-off-canvas-content="">

<div>

<nav class="title-bar tab-bar" data-mc-ignore="true">

<div class="middle title-bar-section outer-row clearfix">

<div class="relative clearfix">[](get-started-tutorial-home.html)

<div class="navigation-wrapper nocontent">

*   <a>placeholder</a>

</div>

<button class="menu-icon" data-toggle="offCanvas"><span></span></button></div>

</div>

<div class="nav-search row outer-row">

<form class="search" action="#">

<div class="search-bar search-bar-container needs-pie"><input class="search-field needs-pie" type="search" placeholder="Search">

<div class="search-filter-wrapper">

<div class="search-filter">

<div class="search-filter-content">

*   All Files

</div>

</div>

</div>

</div>

</form>

</div>

</nav>

</div>

<section class="main-section">

<div class="row outer-row" data-mc-content-body="True">

<div id="form-container">

<form style="width:90%; float:left;" id="first-form"><span class="form-helpful-text form-visible">Was this page helpful?</span>

<div class="form-helpful-radio form-visible"><input type="radio" name="form-helpful-radio" id="helpful-yes" value="1" onclick="submitRating();">Yes <input type="radio" name="form-helpful-radio" id="helpful-no" value="2" onclick="submitRating();">No</div>

</form>

<span id="frame-caption" class="feedback-hidden">Have a comment? Please leave it here.</span><span id="post-submit-msg" class="feedback-hidden">**Thanks for your feedback!**</span></div>

# Step 2: Drag and drop to take a first look

<div class="MCDropDown MCDropDown_Open dropDown"><span class="MCDropDownHead dropDownHead">[![Closed](Skins/Default/Stylesheets/Images/transparent.gif) This multi-step tutorial introduces Tableau Desktop. You are on **Step 2** of 8.](javascript:void(0);)</span>

<div class="MCDropDownBody dropDownBody">

*   [Step 1: Connect to your data](get-started-tutorial-connect.html)
*   **Step 2: Drag and drop to take a first look** (you are here)
*   [Step 3: Focus your results](get-started-tutorial-focus.html)
*   [Step 4: Explore your data geographically](get-started-tutorial-explore.html)
*   [Step 5: Drill down into the details](get-started-tutorial-drilldown.html)
*   [Step 6: Build a dashboard to show your insights](get-started-tutorial-build.html)
*   [Step 7: Build a story to present](get-started-tutorial-story.html)
*   [Step 8: Share your findings](get-started-tutorial-share.html)

Want an overview? Head back to the [Introduction](get-started-tutorial-home.html).

</div>

</div>

## Create a view

You set out to identify key areas for improvement, but where to start? With four years' worth of data, you decide to drill into the overall sales data between 2014 and 2017 to see what you find. Start by creating a simple chart.

<div class="MCDropDown MCDropDown_Open dropDown"><span class="MCDropDownHead dropDownHead">[![Closed](Skins/Default/Stylesheets/Images/transparent.gif)**Learn more:** Terms in this section.](javascript:void(0);)</span>

<div class="MCDropDownBody dropDownBody">

<table style="width: 100%;mc-table-style: url('Resources/TableStyles/Shaded-NoBorder.css');" class="TableStyle-Shaded-NoBorder" cellspacing="0"><colgroup><col class="Column-Column1" style="width: 247px;"> <col class="Column-Column1"></colgroup>

<tbody>

<tr class="Body-Body1">

<td class="BodyE-Column1-Body1">**Term**</td>

<td class="BodyD-Column1-Body1">**Description**</td>

</tr>

<tr class="Body-Body2">

<td class="BodyE-Column1-Body2">Aggregation</td>

<td class="BodyD-Column1-Body2">

Row-level data rolled up to a higher category, such as sum of sales or total profit. Tableau does this automatically so you can break data down to the level of detail that you want to work with.

</td>

</tr>

<tr class="Body-Body1">

<td class="BodyE-Column1-Body1">Dimension vs Measure</td>

<td class="BodyD-Column1-Body1">

Dimensions are qualitative data, such as a name or date. By default, Tableau automatically classifies data that contains qualitative or categorical information as a dimension, for example, any field with text or date values. These fields generally appear as column headers for rows of data, such as Customer Name or Order Date, and also define the level of granularity that shows in the view.

Measures are quantitative numerical data. By default, Tableau treats any field containing this kind of data as a measure, for example, sales transactions or profit. Data that is classified as a measure can be aggregated based on a given dimension, for example, total sales (Measure) by region (Dimension).

</td>

</tr>

<tr class="Body-Body2">

<td class="BodyB-Column1-Body2">Continuous vs. Discrete</td>

<td class="BodyA-Column1-Body2">

Continuous fields can contain an infinite number of values. This can be a range of values such as sales within a specific date range or quantities. Continuous fields are colored green in Tableau.

Discrete fields contain a finite number of values such as country, state, or customer name. Discrete fields are colored blue in Tableau.

</td>

</tr>

</tbody>

</table>

**More on Dimensions and Measures** in the Learning Library (in the top menu).

</div>

</div>

<div class="MCDropDown MCDropDown_Open dropDown"><span class="MCDropDownHead dropDownHead">[![Closed](Skins/Default/Stylesheets/Images/transparent.gif)**Learn more:** Tableau workspace controls and elements.](javascript:void(0);)</span>

<div class="MCDropDownBody dropDownBody">

In this section, you'll drag fields to the Columns and Rows shelves, and you'll also work with the Marks card. The image below identifies some of the workspace controls and elements that you'll use.

![](Img/Drag28.png)

<table style="width: 100%;mc-table-style: url('Resources/TableStyles/Shaded-NoBorder.css');" class="TableStyle-Shaded-NoBorder" cellspacing="0"><colgroup><col class="Column-Column1" style="width: 247px;"> <col class="Column-Column1"></colgroup>

<tbody>

<tr class="Body-Body1">

<td class="BodyE-Column1-Body1">**Element**</td>

<td class="BodyD-Column1-Body1">**Description**</td>

</tr>

<tr class="Body-Body2">

<td class="BodyE-Column1-Body2">Undo</td>

<td class="BodyD-Column1-Body2">

With Tableau, feel free to experiment with your data. You can always get back to where you started with the <span class="uicontrol">Undo</span> button. Use this button to reverse the last action you performed in your workbook.

You can undo an unlimited number of times, back to the last time you opened the workbook, even after you saved your work.

</td>

</tr>

<tr class="Body-Body1">

<td class="BodyE-Column1-Body1">Show/Hide Cards</td>

<td class="BodyD-Column1-Body1">

Did you accidentally hide a card that you now need? No problem! Just about everything on the Tableau workspace can be turned on or off to provide the maximum amount of room for you to create your visualizations.

To show or hide cards like <span class="uicontrol">Pages</span>, <span class="uicontrol">Filters</span> or <span class="uicontrol">Legends</span>, click the drop-down arrow on the <span class="uicontrol">Show/Hide Cards</span> ![](Img/Drag30.png) button on the toolbar and clear or enable the check mark for the card.

You can even collapse the Data and Analytics pane to the lower left corner of the workspace by clicking the <span class="uicontrol">Minimize</span> ![](Img/Drag29.png) button at the top-right corner of the pane. Click the button again to restore the pane like it was.

</td>

</tr>

<tr class="Body-Body2">

<td class="BodyE-Column1-Body2">Data Pane</td>

<td class="BodyD-Column1-Body2">

Displays the name of the data set that is included in the view and the fields in the data set classified as either dimensions or measures.

**More on the Data Pane** in the Learning Library (in the top menu).

</td>

</tr>

<tr class="Body-Body1">

<td class="BodyB-Column1-Body1">Cards and Shelves</td>

<td class="BodyA-Column1-Body1">

Cards are containers for the different controls that are available in Tableau. Shelves are a type of card control. When you drag fields from the Data pane to the Columns or Rows shelves, the data is added as a column or a row on the axes in your view.

When you drag fields from the Data pane to the Marks card, you can control visual properties like type, color, size, shape, and more. Only the marks in your view are impacted by this action; axes do not change.

**More on Cards and Shelves** in the Learning Library (in the top menu).

</td>

</tr>

</tbody>

</table>

</div>

</div>

1.  From Dimensions in the Data pane, drag **Order Date** to the **Columns** shelf.

    **Note:** When you drag <span class="uicontrol">Order Date</span> to the columns shelf, Tableau creates a column for each year in your data set. Under each column is an <span class="uicontrol">Abc</span> indicator. This indicates that you can drag text or numerical data here, like what you might see in an Excel spreadsheet. If you were to drag <span class="uicontrol">Sales</span> to this area, Tableau creates a crosstab (like a spreadsheet) and displays the sales totals for each year.

2.  From Measures, drag **Sales** to the **Rows** shelf.

    Tableau generates the following chart with sales rolled up as a sum (aggregated). You can see total aggregated sales for each year by order date.

![](Img/Drag1.png)

_Any time you create a view that includes time (in this case Order Date), Tableau generates a line chart._

This line chart shows that sales look pretty good and seem to be increasing over time. This is good information, but it doesn't really tell you much about which products have the strongest sales and if there are some products that might be performing better than others. Since you just got started, you decide to explore further and see what else you can find out.

<div class="MCDropDown MCDropDown_Open dropDown"><span class="MCDropDownHead dropDownHead">[![Closed](Skins/Default/Stylesheets/Images/transparent.gif)**Learn more:** Explore your options.](javascript:void(0);)</span>

<div class="MCDropDownBody dropDownBody">

To quickly change the chart type, select the drop-down menu on the **Marks** card.

For example, for an area chart, you can select **Area**.

![](Img/Drag2.png)

Tableau supports many different chart types, referred to as Mark types. **More on Mark types** in the Learning Library (in the top menu).

**Note:** Before you continue the tutorial, make sure your chart type is set back to **Automatic**.

</div>

</div>

### Check your work! Watch "Create a view" in action.

_Click the image to replay it._  
![](Img/Drag23.gif)

**[Top ^](#top)**

* * *

## Refine your view

To gain more insight into which products drive overall sales, try adding more data. Start by adding the product categories to look at sales totals in a different way.

1.  From Dimensions, drag **Category** to the **Columns** shelf and place it to the right of YEAR(Order Date).

    Your view updates to a bar chart. By adding a second discrete dimension to the view you can categorize your data into discrete chunks instead of looking at your data continuously over time. This creates a bar chart and shows you overall sales for each product category by year.

    ![](Img/Drag4.png)

<div class="MCDropDown MCDropDown_Open dropDown"><span class="MCDropDownHead dropDownHead">[![Closed](Skins/Default/Stylesheets/Images/transparent.gif)**Learn more**: Show me the numbers.](javascript:void(0);)</span>

<div class="MCDropDownBody dropDownBody">

You can view or add data point information to your view. In this example, this information shows exact sales totals by category.

To view information about each data point (that is, mark) in your view, hover over one of the bars to reveal a tooltip. The tooltip displays total sales for that category. Here is the tooltip for the Office Suplies category for 2017:

![](Img/Drag5.png)

To add data point information as labels to your view, click **Show Mark Labels** on the toolbar. Below, we show the total sales for each category and year.

**Note:** In the Get Started tutorial, text labels are not added to the view.

![](Img/Drag6.png)

</div>

</div>

<div class="MCDropDown MCDropDown_Open dropDown"><span class="MCDropDownHead dropDownHead">[![Closed](Skins/Default/Stylesheets/Images/transparent.gif)**Learn more:** Change your perspective.](javascript:void(0);)</span>

<div class="MCDropDownBody dropDownBody">

To display the bar chart horizontally instead of vertically, click **Swap** on the toolbar.

**Note:** Undo this action before continuing the Get Started tutorial.

![](Img/Drag7.png)

</div>

</div>

Your view is doing a great job showing sales by category—furniture, office supplies, and technology. An interesting insight is revealed!

From this view, you can see that sales for furniture is growing faster than sales for office supplies, even though Office Supplies had a really good year in 2017\. Perhaps you can recommend that your company focus sales efforts on furniture instead of office supplies? Your company sells a lot of different products in those categories, so you'll need more information before you can make a recommendation.

To help answer that question, you decide to look at products by sub-category to see which items are the big sellers. For example, for the Furniture category, you want to see details about bookcases, chairs, furnishings, and tables. Looking at this data might help you gain insights into sales and later on, overall profitability, so add sub-categories to your bar chart.

1.  Double-click or drag the **Sub-Category** dimension to the **Columns** shelf.

**Note:** You can drag and drop or double-click a field to add it to your view, but be careful. Tableau makes assumptions about where to add that data and it might not be placed where you expect. You can always click <span class="uicontrol">Undo</span> to remove the field, or drag it off the area where Tableau placed it to start over.

Sub-Category is another discrete field. It creates another header at the bottom of the view, and shows a bar for each sub-category (68 marks) broken down by category and year.

![](Img/Drag9.png)

Now you are getting somewhere, but this is a lot of data to visually sort through. In the next section you will learn how you can add color, filters, and more to focus on specific results.

<div class="MCDropDown MCDropDown_Open dropDown"><span class="MCDropDownHead dropDownHead">[![Closed](Skins/Default/Stylesheets/Images/transparent.gif)**Learn more:** Use a different view to compare product sales.](javascript:void(0);)</span>

<div class="MCDropDownBody dropDownBody">

If you want to see how your products contribute to overall sales by category, Tableau gives you another option.

If you drag the **Sub-Category** dimension to **Color** on the Marks card, you create a stacked bar chart with additional marks for each sub-category identified by a unique color.

**Note:** Undo this action before continuing the Get Started tutorial.

![](Img/Drag8.png)

This quickly shows you the amount of sales that each product contributes to the overall total for each category and year, and immediately shows the large and small contributors at a glance.

Sub-categories are displayed as stacked bars in the order that they are listed in the legend, not according to where they fall on the Sales axis.

For example, the above view shows you that bookcases contributed 38,544 USD in sales to the overall total of 170,518 USD for Furniture in 2015\. The mark is displayed at the top of the bar because Bookcases is listed above Chairs, Furnishings, and Tables in the legend. The sub-categories are displayed in the legend so that you can move them around and examine your data in a way that makes sense to you.

Depending on the kind of analysis you want to do, the stacked bar chart might or might not be the chart for you.

</div>

</div>

### Check your work! Watch "Refine your view" in action.

_Click the image to replay it_  
![](Img/Drag24.gif)

**[Top ^](#top)**

* * *

## Step summary

This step was all about getting to know your data and starting to ask questions about your data to gain insights. You learned how to:

*   Create a chart in a view that works for you.

*   Add fields to get the right level of detail in your view.

Now you are ready to begin focusing on your results to identify more specific areas of concern. In the next section, you will learn how to use filters and colors to help you explore your data visually.

Continue to [Step 3: Focus your results](get-started-tutorial-focus.html).

**[Top ^](#top)**

* * *

![](Resources/Code/onLoad.png)</div>

</section>

<a data-close="true"></a></div>

</div>

<script>/* <![CDATA[ */$(document).foundation();/* ]]> */</script></div>
