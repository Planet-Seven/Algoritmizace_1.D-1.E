# 1. Základní HTML značky

  ## Nadpis

  ```html
  <h1>obsah nadpisu</h1>
  ``` 
  
  Úrovně h1 - h7. Úroveň h1 je nevyšší, h7 nejnižší.

  Nepoužívejte úroveň nadpisu čistě ke stylování velikosti, musí dávat smysl.
    
  ## Odstavec 

  ```html
  <p>obsah odstavce</p>
  ```

  ## Seznam

  ### seřazený seznam

  ```html
  <ol>...obsah seznamu...</ol>`
  ```
   
  ### neseřazený seznam

  ```html
  <ul>...obsah seznamu...</ul>
  ```   

  ### Prvek seznamu

  ```html
  <li>obsah prvku sezamu</li>
  ```

  uvnitř značky se může nacházet (a zpravidla se tam i nachází) další html značka, případně i další seznam

  ```html
  <ol>
    <li><h5>prvek seznamu</h5></li>
    <li><h5>prvek seznamu</h5></li>
  </ol>
  ```

  ### Vnořený seznam
  ```html
  <ol>
    <li>
      <ol>
        <li>prvek vnořeného seznamu 1</li>
        <li>prvek vnořeného seznamu 1</li>
      </ol>
    </li>
    <li>
      <ol>
        <li>prvek vnořeného seznamu 2</li>
        <li>prvek vnořeného seznamu 2</li>
      </ol>
    </li>
  </ol>
  ```

  ## Kotva (odkaz)
  ```html
  <a href="..." target="...">Obsah odkazu</a>
  ```

  `href` - odkaz na cíl, URL nebo cesta

  `target` - specifikuje, jak se stránka otevře

  ## Navigace
  ```html
  <nav> ... </nav>
  ```

  sdružuje dohromady prvky, které slouží jako navigace, typicky jde o nějaké kotvy.


  ## Obrázek
  ```html
  <img src="...">
  ```

  Pozor na nepárovost značky!

  `src` - zdroj obrázku, URL nebo cesta

  `alt` - alternativní text. Měl by být dostatečně deskriptivní, využívají ho čtecí zařízení

  ### Absolutní a relativní cesty
  `C:users/pepa/Documents/Mujhtmlprojekt/images/sussybaca.jpg` - absoultní cesta, bude fungovat jen u nás. To nechceme.

  `images/sussybaca.jpg` popř. `./images/sussybaca.jpg` - relativní cesta pracuje jen s obsahem aktuální složky, bude fungovat i po jejím přesunutí. To chceme.

# 2. HTML tabulky

## Buňka tabulky
```html
<td> ... </td>
```

Může obsahovat obrázek, text, seznam ...

## Hlavička tabulky
```html
<th> ... </th>
```

Používa se stejně jako buňka, umisťujte je však jen do prvního řádku.

## Řádek tabulky
```html
<tr> ... </tr>
```

Sdružuje dohromady buňky do jednoho řádku. Až na výjimky by mělo platit, že všechny řádky tabulky mají stejný počet buňek.

## Tabulka

```html
<table> ... </table>
```

Sdružuje jednotlivé řadku do celé tabulky. Použití by tedy mohlo vypadat zhruba takto:

```html
<table>
  <tr>
    <th>Company</th>
    <th>Contact</th>
    <th>Country</th>
  </tr>
  <tr>
    <td>Alfreds Futterkiste</td>
    <td>Maria Anders</td>
    <td>Germany</td>
  </tr>
  <tr>
    <td>Centro comercial Moctezuma</td>
    <td>Francisco Chang</td>
    <td>Mexico</td>
  </tr>
</table>
```

## Formuláře a input

### Formulář

```html
<form> ... </form>
```

Ohraničuje jednotlivé položky formuláře.

### Input

```html
<input type="..." id="..." name="..." value="..." />
```

Umožňuje sbírat vstup od uživatele.

`type` - říká, o jaký vstup se jedná. Může mít hodnoty "text" (textové pole), "radio" (výběr z jednoho), "checkbox" (výběr více možností), "button" (tlačítko), "submit" (tlačítko pro odeslání)

`id` - identifikuje prvek v html dokumentu. Budeme ho používat pro popisek (label).

`name` - V HTML dokumentu nehraje roli. Projeví se v odeslaném formuláři.

`value` - to samé jako name, ale říká, jakou hodnotu uvidíme v odeslaných datech. Data se odešlou ve formátu name=value.

### Popisek

```html
<label for="..." ></label>
```

`for` - id prvku, pro který popisek píšeme.

# 3. Základy CSS

  ### Co je CSS?

  CSS (Cascading Style Sheets) je jazyk, který umožňuje upravovat vzhled a rozvržení HTML dokumentu. Slouží k oddělení obsahu (HTML) od stylu (CSS).

  ## Způsoby přidání CSS

  ### Inline CSS

  Styl je přímo v HTML prvku. Používá se pouze výjimečně.

  ```html
  <p style="color: red;">Toto je červený text.</p>
  ```
    
  ### Interní CSS

  Styl je napsán v `<style>` tagu v `<head>` sekci HTML dokumentu.

  ```html
  <style>
    p {
      color: blue;
    }
  </style>
  ```

  ### Externí CSS

  Styl je uložen v samostatném souboru (např. style.css) a připojen pomocí `<link>`:

  ```html
  <link rel="stylesheet" href="style.css">
  ```

  ## Selektory a základní vlastnosti

  ### Typový selektor

  Cílí na všechny prvky daného typu (např. všechny `<p>`).

  ```css
  p {
  color: green;
  }
  ```

  ### Třídový selektor

  Cílí na prvky s konkrétní třídou (class). V tomhle případě stylujeme třídu "highlight".

  ```css
  .highlight {
  background-color: yellow;
  }
  ```

  ### ID selektor

  Cílí na konkrétní prvek identifikovaný pomocí atributu id. V tomto případě id "special".

  ```css
  #special {
  font-size: 24px;
  }
  ```

  ## Barvy a jednotky

  ### Barvy

  Barvy lze specifikovat několika způsoby:

  *	Pojmenované barvy: např. red, blue, green.
  *	HEX kódy: např. #ff0000 (červená).
  *	RGB a RGBA: např. rgb(255, 0, 0) nebo rgba(255, 0, 0, 0.5) (poloprůhledná červená).
  *	HSL a HSLA: např. hsl(0, 100%, 50%) nebo hsla(0, 100%, 50%, 0.5).

  ### Jednotky
  *	Absolutní: px (pixely), cm (centimetry).
  *	Relativní: % (relativní k rodičovskému prvku), em a rem (relativní k velikosti písma), vh a vw (relativní k setině rozměru okna)

  ## Box model

  Box model popisuje, jak je každý HTML prvek obalen “krabicí”, kterou tvoří následující vrstvy:
	1.	Obsah (content): Text nebo jiné prvky uvnitř.
	2.	Výplň (padding): Prostor mezi obsahem a okrajem.
	3.	Okraj (border): Ohraničení kolem prvku.
	4.	Okrajový prostor (margin): Prostor mezi prvkem a ostatními prvky.

  ```css
  div {
  width: 300px;
  padding: 20px;
  border: 5px solid black;
  margin: 10px;
  }
  ```

  ## Stylování textu

  ### Barva textu

  ```css
  color: red;
  ```

  ### Velikost písma

  ```css
  font-size: 16px;
  ```

  ### Zarovnání textu

  ```css
  text-align: center;
  ```

  ## Pozicování

  ### Display

  `display` určuje, jak se elementy vykreslují na stránce.

  - `block` - element zabírá celou šířku řádku (např. `<div>`, `<p>`)
  - `inline` - element zabírá pouze tolik místa, kolik potřebuje (např. `<span>`, `<a>`)
  - `inline-block` - chová se jako `inline`, ale umožňuje nastavovat rozměry (`width`, `height`)
  - `none` - element je skrytý a nezabírá žádné místo

  Příklad:
  ```css
  .block-element {
    display: block;
  }
  .inline-element {
    display: inline;
  }
  .inline-block-element {
    display: inline-block;
    width: 100px;
    height: 50px;
  }
  ```

### Position

position určuje, jak je element umístěn na stránce.
-	static - výchozí hodnota, element je umístěn v běžném toku dokumentu
-	relative - element je posunut relativně vůči své původní pozici
-	absolute - element je umístěn relativně k nejbližšímu rodiči s position: relative;, jinak vůči <html>
-	fixed - element je umístěn vůči oknu prohlížeče a nemění pozici při scrollování
-	sticky - element se chová jako relative, dokud nedosáhne určité pozice, kde se „přilepí“

Příklad:
```css
.relative-box {
  position: relative;
  top: 20px;
  left: 10px;
}

.absolute-box {
  position: absolute;
  top: 10px;
  right: 10px;
}

.fixed-box {
  position: fixed;
  bottom: 10px;
  right: 10px;
}

.sticky-box {
  position: sticky;
  top: 0;
}
```

### Float

float umožňuje umístit element na stranu (doprava nebo doleva) a obtečení textem.
-	left - element bude zarovnán doleva, text jej bude obtékat zprava
-	right - element bude zarovnán doprava, text jej bude obtékat zleva
-	none - žádné obtékání

Příklad:
```css
.float-left {
  float: left;
  width: 50%;
}

.float-right {
  float: right;
  width: 50%;
}
```

### Clear

clear se používá k odstranění efektu float.
-	left - zabrání obtékání levých elementů
-	right - zabrání obtékání pravých elementů
-	both - zabrání obtékání z obou stran

## Pseudoselektory

CSS pseudoselektory umožňují stylovat prvky na základě jejich stavu, pozice nebo interakce s uživatelem, aniž bychom museli přidávat třídy nebo upravovat HTML.

### Stavové pseudoselektory

Tyto selektory reagují na interakci uživatele.

- `:hover` – když je prvek pod kurzorem myši
- `:active` – když je prvek aktivní (např. držíte tlačítko myší)
- `:focus` – když má prvek fokus (např. aktivní textové pole)

```css
button:hover {
  background-color: lightblue;
}

input:focus {
  border-color: green;
}
```

### Strukturální pseudoselektory

Slouží pro výběr prvků podle jejich pozice mezi sourozenci.

-	`:first-child` – první potomek
- `:last-child` – poslední potomek
- `:nth-child(n)` – n-tý potomek (číslování začíná od 1)
- `:nth-of-type(n)` – n-tý potomek daného typu (např. druhý `<li>`)

```css
li:first-child {
  font-weight: bold;
}

li:nth-child(3) {
  color: red;
}
```

### Ostatní zajímavé pseudoselektory
- `::before a ::after` – přidání obsahu před nebo za obsah prvku
- `:not(selector)` – vybere prvky, které neodpovídají selektoru

```css
p::before {
  content: "tento obsah bude přidán ";
}

a:not(.button) {
  color: red;
}
```