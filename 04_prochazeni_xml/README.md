# 4. Zobrazeni XML

Pokud XML představují jen holá data s významem, splňující schéma XSD, pak otázkou zůstává, jak tato holá validní data předat uživateli. Možností je napsat si aplikaci, která XML parsuje pomocí nějaké knihovny (případně si napsat vlastní parser) a vizualizovat je pomocí nějaké GUI knihovny. Chytřejší možností transformovat data na jiná, které rozumíme běžně používané aplikace (PDF čtečky, webové prohlížeče). K takové transformaci slouží jazyk XSLT (eXtensible Stylesheet Language Transformations), který představuje obdobu kaskádových stylů, ale XSLT je daleko mocnější stylový jazyk. Příklad XSLT naleznete na [W3Schools XML XSLT](https://w3schools.com/xml/xml_xslt.asp).

Pro potřeby transformace je nutné procházet řízeným způsobem XML dokumentem. K tomu nám slouží jazyk XPath, který přebírá navigační výrazy a nalezá příslušné prvky, splňující cestu definovanou navigačním výrazem. Tato technologie je důležitá nejen pro XSLT, ale i pro XQuery, umožňující dotazovat se nad XML dokumenty.Příklad XPath naleznete na [W3Schools XML XPath](http://w3schools.com/xml/xml_xpath.asp).

Tyto XML technologie obecně označujeme jako XSL jazyk (eXtensible Stylesheet Language - obdoba css ale silnější)[W3Schools XSL Language](https://w3schools.com/xml/xsl_languages.asp):
1. XSLT - jazyk pro transformaci
2. XPath - jazyk pro navigaci
3. XSL-FO - jazyk pro vizualizaci (již se nepoužáví, nahrazen CSS3)
4. XQuery - jazyk pro dotazování

## On-site cvičení
V této lekci se seznamíte s navigací v XML dokumentu pomocí navigačního jazyka XPath a transformaci vyhledaných elementů do jiných jazyků pomocí jazyka XSLT. Tím si ušetříte velké množství práce, kterou byste museli jinak věnovat učením se knihoven pro práci s XML a GUI knihoven pro vizualizaci ve vybraném programovacím jazyce.

### Cv3.1 Převod XML do HTML pomocí XSLT (XX minut)

Ukázku transformace z XML na HTML (konkrétně xhtml) naleznete na stránce [W3Schools XSLT Transform](https://w3schools.com/xml/xsl_transformation.asp). Transformace se provádí pomocí XSLT elementů:
1. <template> [W3Schools XSLT Template](https://w3schools.com/xml/xsl_templates.asp) - sada transformačních pravidel, aplikujících se na vyhledané uzly výrazem jazyka XPath v atributu match
2. <apply-templates> [W3Schools XSLT Apply](https://w3schools.com/xsl_apply_templates.asp) - aplikace XSLT pravidel (templates) na element nebo jeho děti

### Cv3.2 Podmínky a cykly v XSLT (XX minut)

V jazyce XSLT lze využívat podmínky a cykly, kterými dále řídíme, na které uzly a jak aplikovat pravidla v templates. Tyto příkazy provádíme pomocí následujících elementů:
1. <value-of> [W3Schools XSLT ValueOf](https://w3schools.com/xml/xsl_value_of.asp) - získá data z jednoho uzlu a může je využít při transformaci
2. <for-each> [W3Schools XSLT ForEach](https://w3schools.com/xml/xsl_for_each.asp) - realizace cyklu v XSLT z vyfiltrovaného výběru XML uzlů
3. <sort> [W3Schools XSLT Sort](https://w3schools.com/xml/xsl_sort.asp) - slouží pro seřazení uzlů
4. <if> [W3Schools XSLT If](https://w3schools.com/xml/xsl_if.asp) - slouží jako realizace podmínky v XSLT
5. <choose> [W3Schools XSLT Choose](https://w3schools.com/xml/xsl_choose.asp) - realizace přepínače v XSLT (switch=<choose>, case=<when>, default=<otherwise>)

### Cv3.3 Využití XPath v XSLT (XX minut)

Jazyk XPath [W3Schools XPath Introduction](https://w3schools.com/xml/xpath_intro.asp) používá výrazy pro cesty ve tvaru osa::uzel[predikát] [W3Schools XPath Nodes](https://w3schools.com/xml/xpath_nodes.asp):
1. Uzel - XML je brán jako strom uzlů, kde uzel může být větev (element, atribut, data, atd.) nebo list (atomická hodnota - samotná data)
2. Osa [W3Schools XPath Axes](https://w3schools.com/xml/xpath_axes.asp) - relativní vztah k vybranému uzlu pro nalezení jeho příbuzných (rodič, dítě, sourozenec, předek, potomek, následný uzel, atd.)
3. Predikát - dodatečné nepovinné filtrování, viz cvičení Cv.3.4

### Cv3.4 Predikáty a operátory v XPath (XX minut)

Nad nalezenými uzly z XPath výrazu lze provádět dodatečnou filtraci predikáty nebo agregaci operátory. Díky predikátům a operátorům může být výsledek cesty množina uzlů, řetězec, boolean nebo číslo. Pokud budeme aplikovat XSLT, tak potřebujeme získat množinu uzlů. Bližší popis mechanismů predikátů a operátorů:
1. Predikát [W3Schools XPath Syntax](https://w3schools.com/xml/xpath_syntax.asp) - filtrují nalezený výsledek (první element, poslední, s atributem větším než, s atributem rovno, atd.), ale je možnost využít v nich i divokých karet (wildcards)
2. Operátor [W3Schools XPath Operators](https://w3schools.com/xml/xpath_operators.asp)- aritmetické (+,-,*,/,div,mod) a logické operace (=,!=,<,<=,>,>=,and,or), které je možné využít pro zpracování výsledku cesty

### Cv3.5 Kaskádové styly

Jelikož jazyk XSL-FO je již obsolete (ten je bohužel zapotřebí pro konverzi XML do PDF), tak se využívá pro vizualizaci dat CSS3. Kaskádové styly nejsou součástí našeho kurzu, avšak měli byste mít alespoň základní ponětí o nich. V tomto cvičení si vyzkoušíte naformátovat přetransformovaný XML dokument pomocí kaskádových stylů.

## Domácí cvičení

### U3.1 XSLT ve webových aplikacích (XX minut)

Nejčastější využití XML je u webových aplikací, takže otázkou zůstává, kde se vlastně transformace provádí u vztahu klient-server. K transformaci může docházet na straně klienta, kterému je do aplikace zaslán XML dokument, nejčastěji jazykem Javascript [W3Schools XSLT on the Client](https://w3schools.com/xml/xsl_client.asp), nebo na straně serveru, který XML transformuje pro klienta a zašle mu již transformovaný dokument [W3Schools XSLT on the Server](https://w3schools.com/xml/xsl_server.asp), např.: jazykem PHP.


### U3.2 Lorem

### U3.3 Lorem





