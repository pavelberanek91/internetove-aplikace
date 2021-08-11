# 2. Popis XML

XSD Schema je alternativa k šabloně v DTD formátu. Tento způsob psaní schémat je daleko složitější, ale silnější, než DTD. XSD je název jazyku, který se používá pro popis XML schemat a znamená XML Schema Definiton (je zde trošku terminologický zmatek - někdo používá termín XML Schema, někdo XSD Schema).
- Ukázku XSD Schema naleznete na stránce: [W3Schools XML Schema](https://w3schools.com/xml/xml_schema.asp)
- Porovnání XSD a DTD schémat můžete nalézt na této stránce: [W3Schools XSD How To](https://w3schools.com/xml/schema_howto.asp)

## On-site cvičení
V této lekci se seznamíte s psaním velice komplexních XML Schémat pomocí jazyka XML, který vám umožní psát velice komplexní webové aplikace, využívající XML soubory od klientů.

### Cv2.1 XSD Simple elements (XX minut)

Základní stavební bloky XSD dokumenty jsou:
1. kořen [W3Schools XSD <schema>](https://w3schools.com/xml/schema_schema.asp) - každý XSD potřebuje kořenový element, v něm se mohou nacházet definice jmenných prostorů
2. elementy [W3Schools XSD Elements](https://w3schools.com/xml/schema_simple.asp) - jsou dvou typů a to simple a complex; simple obsahují data v primitivních datových typech jako string, decimal, integer, boolean, date a time; complex obsahují další elementy nebo atributy
3. atributy [W3Schools XSD Attributes](https://w3schools.com/xml/schema_simple_attributes.asp) - obsahují data o stejných typech jako simple elementy a mohou být implicitní (default), pevně dané (fixed) a vyžadované (required) a dělají z elementu komplexní typ
4. restrikce [W3Schools XSD Restrictions](https://w3schools.com/xml/schema_facets.asp) - určují rozsah nebo výčet hodnot, kterých musí data elementů a atributů nabývat
5. data - jsou typu [string](https://w3schools.com/xml/schema_dtypes_string.asp), [date](https://w3schools.com/xml/schema_dtypes_date.asp), [numeric](https://w3schools.com/xml/schema_dtypes_numeric.asp), [misc](https://w3schools.com/xml/schema_dtypes_misc.asp) (boolean, binary, anyURI, double, float, atd.)


### Cv2.2 XSD Complex elements (XX minut)

Komplexní element v XSD představuje element, který obsahuje další elementy, atribut a/nebo restrikce [W3Schools XSD Complex](https://w3schools.com/xml/schema_complex.asp) a dělíme je na:
1. Prázdné elementy [W3Schools XSD Empty](https://w3schools.com/xml/schema_complex_empty.asp) - element bez obsahu, ale může mít atributy (takže může obsahovat data)
2. Pouze s elementy [W3Schools XSD Elementy Only](https://w3schools.com/xml/schema_complex_elements.asp) - element nebo sekvence elementů, která může být pojmenovaná 
3. Pouze s textem [W3Schools XSD Text Only](https://w3schools.com/xml/schema_complex_text.asp) - jednoduchý element s rozšířením nebo restrikcí  
4. Smíšené [W3Schools XSD Mixed](https://w3schools.com/xml/schema_complex_mixed.asp) - kombinace předchozích 

### Cv2.3 XSD Indikátory (XX minut)

Jazyk XSD obsahuje mechanismus indikátorů, které jsou určené k tomu, aby řídily způsob používání XML elementů [W3Schools XSD Indicators](https://w3schools.com/xml/schema_complex_indicators.asp). Dělíme je na indikátory:
1. Řádu - řídí pořadá elementů (all = libovolné pořadí, choice = exkluzivní výběr, sequence = přesně dané pořadí)
2. Výskytu - řídí počet elementů (maxOccurs = maximální počet elementů, minOccurs = minimální počet elementů)
3. Skupiny - řídí uspořádání prvků do pojmenovaných skupin

### Cv2.4 XSD Substituční skupiny(XX minut)

Další užitečným mechanismem je substituční mechanismus, který lze využít např.: pro vícejazyčné XML dokumenty. XSD umožňuje definovat skupinu zaměnitelných elementů (tzv. substituční skupina), ve které jsou elementy vzájemně zaměnitelné [W3Schools XSD Substitution](https://w3schools.com/xml/schema_complex_subst.asp).

### Cv2.5 XSD Libovolné elementy (XX minut)

Pokud chceme ještě větší volnost a umožnit vložit uživateli v XML v nějaké části libovolné elementy, pak můžeme využít v XSD element <any> [W3Schools XSD Any](https://w3schools.com/xml/schema_complex_any.asp). Obdobný mechanismus existuje i pro atributy elementů pomocí <anyAttribute> [W3Schools XSD anyAttribute](https://w3schools.com/xml/schema_complex_anyattribute.asp).

## Domácí cvičení

### U2.1 Lorem

### U2.2 Lorem

### U2.3 Lorem





