# 1. Základní HTML značky

## Nadpis
`<h1>obsah nadpisu</h1>` - úrovně h1 - h7. Úroveň h1 je nevyšší, h7 nejnižší.

Nepoužívejte úroveň nadpisu čistě ke stylování velikosti, musí dávat smysl.
  
## Odstavec 
`<p>obsah odstavce</p>`

## Seznam
`<ol>...obsah seznamu...</ol>` - seřazený seznam

`<ul>...obsah seznamu...</ul>` - neseřazený seznam

### Prvek seznamu
`<li>obsah prvku sezamu</li>`
uvnitř značky se může nacházet (a zpravidla se tam i nachází) další html značka, případně i další seznam

```
<ol>
  <li><h5>prvek seznamu</h5></li>
  <li><h5>prvek seznamu</h5></li>
</ol>
```

### Vnořený seznam
```
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
`<a href="..." target="...">Obsah odkazu</a>`

`href` - odkaz na cíl, URL nebo cesta

`target` - specifikuje, jak se stránka otevře

## Navigace
`<nav> ... </nav>`

sdružuje dohromady prvky, které slouží jako navigace, typicky jde o nějaké kotvy.


## Obrázek
`<img src="...">`

Pozor na nepárovost značky!

`src` - zdroj obrázku, URL nebo cesta

`alt` - alternativní text. Měl by být dostatečně deskriptivní, využívají ho čtecí zařízení

### Absolutní a relativní cesty
`C:users/pepa/Documents/Mujhtmlprojekt/images/sussybaca.jpg` - absoultní cesta, bude fungovat jen u nás. To nechceme.

`images/sussybaca.jpg` popř. `./images/sussybaca.jpg` - relativní cesta pracuje jen s obsahem aktuální složky, bude fungovat i po jejím přesunutí. To chceme.

# 2. HTML tabulky

## Buňka tabulky
`<td> ... </td>`

Může obsahovat obrázek, text, seznam ...

## Hlavička tabulky
`<th> ... </th>`

Používa se stejně jako buňka, umisťujte je však jen do prvního řádku.

## Řádek tabulky
`<tr> ... </tr>`

Sdružuje dohromady buňky do jednoho řádku. Až na výjimky by mělo platit, že všechny řádky tabulky mají stejný počet buňek.

## Tabulka

`<table> ... </table>`

Sdružuje jednotlivé řadku do celé tabulky. Použití by tedy mohlo vypadat zhruba takto:

```
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