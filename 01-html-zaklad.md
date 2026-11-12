# Milník 1: HTML základ, tabulky, odkazy a obrázky

**Cíl:** Postavit první verzi webu, tedy několik propojených stránek v čistém HTML (zatím bez CSS).

**Termín:** _doplní vyučující_

**Verze:** `v1`

---

## ✅ Základ (povinný)

### Git a GitHub
> 🚀 Jak na to: [návod krok za krokem](00-navod-github.md)

- [x] Mám účet na GitHubu
- [x] Mám svůj repozitář a umím do něj commitnout a pushnout
- [x] Mám zapnuté GitHub Pages a web se mi zobrazuje online
- [x] Mám alespoň **5 commitů** se srozumitelnou zprávou

### Struktura stránek
- [x] Web má alespoň **3 stránky**, hlavní se jmenuje `index.html`
- [x] Každá stránka má `<!DOCTYPE html>`, `<html lang="cs">`, `<head>` a `<body>`
- [x] Každá stránka má v `<head>` nastavené kódování `<meta charset="UTF-8">`
- [x] Každá stránka má vlastní `<title>`, který odpovídá jejímu obsahu

### Obsah
- [x] Na každé stránce je jeden nadpis `<h1>` a alespoň jeden podnadpis `<h2>`
- [x] Texty jsou rozdělené do odstavců `<p>`
- [x] Na webu je alespoň jeden seznam (`<ul>` nebo `<ol>`)

### Tabulka
- [x] Na webu je alespoň **1 tabulka** s hlavičkou `<th>`
- [x] Tabulka má alespoň **3 sloupce a 4 řádky** s daty
- [x] Tabulka dává smysl, porovnává více položek se stejnými vlastnostmi
- [x] V tabulce je alespoň jednou použitý `rowspan` **nebo** `colspan`

> 💡 Tip: tabulka se hodí na menu s cenami, postavy a jejich vlastnosti, díly seriálu, otevírací dobu… Dlouhý text o jedné věci do tabulky nepatří, ten patří do odstavce.

> 💡 **Kdy sloučit buňky?** Když se ve sloupci nebo řádku opakuje stejná hodnota, nebo když potřebuješ jeden nadpis nad více sloupci.
> - `rowspan` (přes více **řádků**): kategorie jídel v menu (*Polévky*, *Hlavní jídla*), číslo řady u dílů seriálu, typ zbraně, tým nebo frakce u postav
> - `colspan` (přes více **sloupců**): nadpis *Statistiky* nad sloupci síla / rychlost / životy, řádek *Řada 2* přes celou šířku tabulky, poznámka *Zavřeno* přes všechny časy v otevírací době

### Odkazy
- [x] Na každé stránce je **stejná navigace** s odkazy na všechny stránky webu
- [x] Alespoň **2 odkazy na jiné weby**, které se otevřou v nové záložce (`target="_blank"`)
- [x] Alespoň **1 odkaz na e-mail** (`mailto:`)
- [x] Všechny odkazy fungují, žádný nevede „do prázdna“

### Obrázky
- [x] Na webu jsou alespoň **2 obrázky** (`<img>`)
- [x] Každý obrázek má atribut `alt` s krátkým popisem, co na něm je
- [x] Obrázky jsou uložené ve složce `img/` a v kódu na ně vede relativní cesta (`img/logo.png`)
- [x] Obrázky se zobrazují i na GitHub Pages, nejen na tvém počítači

> 💡 Tip: GitHub Pages rozlišuje velká a malá písmena. `Logo.PNG` a `logo.png` jsou pro něj dva různé soubory. Pojmenovávej obrázky malými písmeny bez diakritiky a mezer.

### Validace
Prohlížeč ti zobrazí stránku, i když je v ní chyba. Jiné prohlížeče, vyhledávače nebo čtečky pro nevidomé si s ní ale nemusí poradit. Proto se HTML kontroluje **validátorem**.

- [x] Zkontroluj **všechny stránky** ve validátoru: [validator.w3.org](https://validator.w3.org/#validate_by_upload)
- [x] Oprav všechny chyby (**Error**), aby validátor u každé stránky hlásil, že je v pořádku

---

## 🔍 Challenge (povinná)

Obě věci jsme v hodině neprobírali. Zjisti si sám, jak fungují. Odkazy na dokumentaci máš u každé části.

> 💡 Komentář v HTML napíšeš ve VS Code nejrychleji zkratkou **Ctrl + /** (na Macu **Cmd + /**). Zakomentuje řádek, na kterém stojí kurzor, nebo označený text.

### 1. Video nebo audio

Tagy `<video>` a `<audio>` jsme v hodině neprobírali. Vyber si **jeden z nich**, zjisti si sám, jak se používá, a vlož ho na web (třeba trailer, ukázku písničky, znělku seriálu…).

- [x] Na jedné stránce je vložené video (`<video>`) **nebo** audio (`<audio>`)
- [x] Přehrávač má ovládací prvky (play, pauza, hlasitost)
- [x] Soubor je uložený ve složce `media/` a má **maximálně 25 MB**
- [x] Nad tagem je v kódu **komentář**, ve kterém jednou větou vysvětlíš, co dělá atribut `controls` a co by se stalo bez něj

Příklad:
```html
<!-- Atribut controls zobrazí tlačítka přehrávání, bez něj by video nešlo spustit -->
<video src="media/trailer.mp4" controls></video>
```

> 📖 Kde hledat: [Element `<video>` (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/video), [Element `<audio>` (MDN)](https://developer.mozilla.org/en-US/docs/Web/HTML/Element/audio) nebo [HTML Video (W3Schools)](https://www.w3schools.com/html/html5_video.asp)

> ⚠️ Je soubor moc velký? Zkrať ho nebo zkomprimuj, třeba v programu [HandBrake](https://handbrake.fr/) nebo v online převodníku. Pro web stačí nižší rozlišení (720p).

### 2. Sémantické elementy

Stránku jde rozdělit na části i tagy, které popisují, **co** daná část je.

- [x] Každá stránka je rozdělená na `<header>`, `<nav>`, `<main>` a `<footer>`
- [x] Na `index.html` je nad `<header>` **komentář**, ve kterém 1–2 větami vysvětlíš, k čemu tyto elementy jsou, když stránka vypadá stejně i bez nich

> 📖 Kde hledat: [Struktura dokumentu a webu (MDN)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Structuring_documents) nebo [HTML Semantic Elements (W3Schools)](https://www.w3schools.com/html/html5_semantic_elements.asp)

---

## 🥉🥈🥇 Bonus (nepovinný)

### 🥉 Části tabulky
- [x] Rozděl tabulku na hlavičku `<thead>`, tělo `<tbody>` a patičku `<tfoot>` (do patičky se hodí třeba součet, průměr nebo poznámka)

> 📖 [Struktura tabulky (MDN)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Table_accessibility)

### 🥈 Odkazy v rámci stránky
- [x] Na delší stránce vytvoř obsah s odkazy, které skočí na konkrétní místo stránky (pomocí atributu `id`)
- [x] Na konci stránky přidej odkaz **„Zpět nahoru“**

> 📖 [Odkazy na části dokumentu (MDN)](https://developer.mozilla.org/en-US/docs/Learn_web_development/Core/Structuring_content/Creating_links#linking_to_specific_parts_of_a_document)

### 🥇 Vlastní chybová stránka 404
- [ ] Vytvoř soubor `404.html`, který se zobrazí, když někdo zadá adresu stránky, která na tvém webu neexistuje
- [ ] Stránka má stejnou navigaci jako ostatní a odkaz zpět na úvod
- [ ] Vyzkoušej to na GitHub Pages: za adresu svého webu napiš třeba `/neexistuje.html`

> 📖 [Vlastní stránka 404 pro GitHub Pages (GitHub Docs)](https://docs.github.com/en/pages/getting-started-with-github-pages/creating-a-custom-404-page-for-your-github-pages-site)

---

## 🏁 Odevzdání

- [ ] Všechny body základu a challenge jsou odškrtnuté
- [ ] Vše je commitnuté a pushnuté na GitHub
- [ ] Web běží na GitHub Pages
- [ ] Poslední commit je označený tagem `v1`

Jak vytvořit tag ve VS Code najdeš v [návodu](00-navod-github.md#️-označení-verze-tagem-konec-milníku). V Git Bash:
```bash
git tag v1
git push origin v1
```

---

## Moje poznámky

_Sem můžeš psát poznámky nebo otázky._
