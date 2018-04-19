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

Per començar amb el BI i Data Viz ens descarregarem:
- [Tableau](https://www.tableau.com/)



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

## 3.5. Creació d'un Dashboard

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

## 3.6. Publicació del dashboard


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
