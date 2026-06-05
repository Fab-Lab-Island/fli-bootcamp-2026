# Landslagsmódel með landmælingum Íslands, Qgis og Blender

Þetta verkefni snérist um að taka landmælingargögn frá náttúrufræðistofnun [Hlekkur](https://www.natt.is/is)

## Vefsíða náttúrufræðistofnunar

![Vefsíðan](img/landslags_fraes/vefsidanatt.png)

## Velja hæðalíkan.

Hægt er að fara inn í Kortasjá til þess að fá upp lista af mismunandi kortasjám nátt.
Velja "Hæðalíkan" kortasjá.

Þegar við erum inn í Hæðalíkan þá þarf að haka í "Sækja gögn, smelltu á reit"
Þá mun vinnuglugginn vinstra megin breytast þegar við smellum á reitinn sem við viljum sækja.

![Hæðalíkan](img/landslags_fraes/vefsidahaedalikan.png)

## Velja Reit.

![Velja Reit á korti](img/landslags_fraes/saekjahaedalikan.png)

Inn í Hæðalíka getum við valið okkur svæði í þessu tilfelli þá er ég að velja reit NR. 15
Sem að er Skagafjarðarsvæði. Það er hægt að sækja fleiri reiti og samtengja það seinna meir.

Þegar við höfum smellt á 15 í vinnuglugganum þá fáum við upp marga möguleika að sækja mismunandi gögn tengt þessu.
Smelltu á "Sækja" hliðin á "Hæðalíkan ISN2016"

Nú ættum við að hafa tif skjal með reitinum sem við völdum.

# QGIS

Qgis er korta forrit sem hægt er að nota til að setja DEM (digital elevation map) upplýsingar. 
DEM skjöl sem t.d. Tif skjalið sem þú sóttir inniheldur hæðarupplýsingar. 

## Setja .tif skjalið inn í Qgis

![sækjaskjal](img/landslags_fraes/Qgissaekjaskjal.png)

Hérna getur þú dregið .tif skjalið beint inn í Layers

![error](img/landslags_fraes/lokaerrorglugga.png)

Ef þessi error gluggi kemur upp þá má loka honum með því að ýta á X upp í hægra horninu. 
Best er að búa til ferhyrning með sirka jafn langar hliðar. 

![Exportimage](exportimage.png)

Nú getum við valið svæði sem við viljum af þessum reit og vistum út png mynd.
Við förum í Export map to image inn í Project - Export/import - Export map to image

MIKILVÆGT: dpi eða pát eru pixlafjöldi á myndinni sem þú ert að fara að vista. Þú vilt fá mikla nákvæmni og fjölda af 
pixlum svo að módelið sem þú erum að fara að búa til sé eins nákvæmt og hægt er. Ef þú hækkar ekki pixlafjöldan þá verður 
3d modelið mjög gróft. 1000 dpi ætti að virka vel en það sakar ekki að prófa sig áfram með þetta og byrja neðar meðan þú
ert að prófa þessa aðferð. Því hærri sem dpi fjöldinn er því þyngra verður það fyrir tölvuna að vinna með hana í Blender. 

![drawoncanvas](img/landslags_fraes/drawoncanvas.png)

Þegar þú ýtir á skref nr.3 að ofan þá hverfur glugginn og þú færð plús merki sem bendil. 
Þetta virkar eins og Snipping tool eða klippiverfærið í windows þar sem við teiknum yfir það svæði sem við viljum
með því að halda inni músinni og búa til kassa á það svæði sem við viljum. 

Hérna er tækifæri að gera vinnusvæðið okkar ferning með því að breyta 
Output width og Output height sé það sama. Þá fáum við ferning. (þetta einfaldar vinnuna í Blender)
Ef við viljum ójafna stærð á lengd og breidd þá þurfum við að skrifa niður stærðirnar sem eru í þessum Output glugga. 

![saveimage](img/landslags_fraes/saveimage.png)

Nú máttu vista myndina með því að smella á "save" og velja staðsetningu í tölvunni sem þú veist hvar er. (gott er að búa til möppu fyrir öll skjölin á einum stað)

## Laga skjalið í GIMP eða myndvinnsluforriti

ATH!! MÁ SLEPPA EF það er ekkert svæði undir sjávarmáli. svæðið sem ég valdi er með mikinn sjó þannig að ég þarf að laga það. 

![GIMP](img/landslags_fraes/paintbucket.png)

Opnaðu GIMP eða annað myndvinnslu forrit. 
Nú þarftu fylla inn í allt sem er alvítt. Það er undir sjávarmáli en þarf að vera svart svo það fari neðar en strandlengjur.
Einfaldasta aðferðin í Gimp er að velja Paint Bucket og passa að svartur sé í forgrunni. Svo smella á hvíta svæðið.

Svo er hægt að vista yfir upprunalega png skjalið með því að gera file-override "nafnáskjali.png". 

![finalpng](img/landslags_fraes/paintbucket2.png)

Myndin ætti núna að líta svona út.

## BLENDER

![blenderaddplane](img/landslags_fraes/blenderaddplane.png)

Nú getum við opnað blender. Best er að vera með 5.0 eða nýrri útgáfu af blender.
Þú mátt eyða "cube" hlutinum sem er alltaf default þegar við opnum vinnusvæðið. Einnig er í lagi að eyða myndavélinni og ljósi en mér finnst fínt að skilja ljósið eftir ef þú skildir vilja rendera myndina seinna. (en það er annað)
Veldu "ADD" og búðu til "PLANE"


![subdivide](img/landslags_fraes/subdivide.png)

Nú þurfum við að bæta við polygonum á flötinn. Þvi hann er einugis einn polygon með 4 punktum. 
Farðu í "EDIT MODE" og hægrismelltu á flötinn. Þar efst ætti að vera "subdivide" möguleikinn. 

![subdivide2](img/landslags_fraes/subdivide2.png)

Það ætti að birtast subdivide gluggi niðri í vinstra horni og byrjum á því að setja 60 subdivide til að byrja með (alltaf hægt að bæta við seinna meir. 
Þarna er komið nóg af polygonum til þess að byrja að fikta með modifier

Farðu núna í "OBJECT MODE" fyrir næsta skref

![subdivide2](img/landslags_fraes/addmodifier.png)

Hægra megin ættir þú að sjá "Add modifier" takkann. 

![subdivide2](img/landslags_fraes/displace.png)

Nú getur þú valið "Search" og fundið "Displace" modifier

![modifytexture](img/landslags_fraes/modifiertexture.png)

Inn í "Displace" modifier þá notar þú bara tvo glugga. "Modifier" og "Texture"

![subdivide2](img/landslags_fraes/opentexture.png)

Farðu inn í "Texture" gluggan og smelltu á "OPEN"
Finndu .png myndina sem þú ætlar að nota fyrir landslagið. Annað hvort beint úr Qgis eða GIMP fyrir landslag undir sjávarmáli. 

![subdivide2](img/landslags_fraes/strength.png)

Nú sérðu að flöturinn er farinn að afmyndast útfrá png ljósmyndinni. Ef þú vilt ýkja eða minnka styrkleikann á afmynduninni þá breytir þú "STRENGTH" inn í "Modifier"
ég endaði á því að nota "0.15" til þess að það væri ekki of ýkt. 

![subdivide2](img/landslags_fraes/subdivide3.png)

Flöturinn er ennþá mjög pixlaður. Þú getur farið aftur í "EDIT MODE" - Valið flötinn og hægri smellt til þess að fá upp "subdivide" aftur. 

![subdivide2](img/landslags_fraes/subdivide31.png)

ATH!!!!
Hafðu í huga að setja ekki of háa tölu núna því þá frýs forritið. Nú vantar bara 3-4 margafaldanir í viðbót til að fá fleiri polygona.
Því sterkari sem tölvan er því nákvæmara er hægt að búa til módelið. 

Farðu nú aftur yfir í "OBJECT MODE"

![subdivide2](img/landslags_fraes/subdividemodifier.png)

Nú getur þú gert módelið ennþá mýkra með því að bæta við "Subdivide surface" modifier. 
Hann mýkir módelið frekar. 

Ef þú ert að hugsa 
"af hverju að nota ekki bara modifier fyrir alltsaman?" 
Því að "Displace" vinnur úr hversu margir polygonar eru í modelinu. 
"Subdivide surface" mýkir módelið frekar. Eins og sést hér fyrir neðan

![subdivide2](img/landslags_fraes/final1.png)

Hérna sérðu nærmynd af módelinu og "Displace" og "Subdivide surface" modifiers til hliðar.
Þú getur fiktað með "levels viewport" töluna (ekki of háa tölu) og "Strength" til þess að fá módelið sem þig langar að búa til. 

![subdivide2](img/landslags_fraes/final2.png)

Nú getur þú vistað módelið með því að fara í File - Export - STL

EASYPEASY! ;)



