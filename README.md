# Dag 6 · CSS Grid

*Modul 4, UI/UX & Frontendutveckling, Lexicon IT-Proffs*

## Vad du ska göra idag

Du bygger menyns rutnät och Om oss-sektionens layout med CSS Grid.

## Bakgrund

Grid ordnar element i **två dimensioner**: rader och kolumner samtidigt. Tumregeln du ska ha i ryggraden: **Grid för helheten, Flexbox inuti.** Idag bygger du ett responsivt rutnät utan en enda media query.

## Så arbetar du (samma som alltid)

1. **Forka** dagens repo på GitHub (*Fork → Create fork*).
2. **Klona din fork:** *Code → HTTPS → kopiera adressen*. I terminalen (Ctrl+ö i VS Code): `git clone <adressen>`. Öppna den nya mappen i VS Code och starta *Live Server*.
3. **Gör uppgiften.** Spara och kontrollera i webbläsaren efter varje steg. Gör en commit efter varje avslutat steg: `git add .` och `git commit -m "Beskriv vad du gjorde"`.
4. **Skicka upp** när du är klar: `git push`.
5. **Lämna in i Microsoft Forms.**

Fastnar du: skriv ner exakt var och vad du försökt, och ta det först i nästa handledda pass.

## Uppgiften steg för steg

### Steg 1. Menyn som rutnät

Gör `.meny-lista` (diven som håller de tre korten) till en gridbehållare. Börja med `grid-template-columns: 1fr 1fr 1fr` och se tre kolumner. Lägg till `gap: 20px`. Ta bort `margin-bottom` på korten inne i rutnätet, `gap` sköter avståndet.

### Steg 2. Gör det flexibelt

Byt kolumnerna mot `repeat(auto-fit, minmax(240px, 1fr))`. Dra i webbläsarfönstret och se hur antalet kolumner anpassar sig själv.

### Steg 3. Om oss i två kolumner

Gör `#om-oss` till en grid. Textstyckena i den ena kolumnen och bilden i den andra. Rubriken ska täcka båda kolumnerna: `grid-column: 1 / -1`.

### Steg 4. Använd grid-visualiseringen

I DevTools: klicka på `grid`-ikonen bredvid elementet. Rader och kolumner ritas ut. Ta en titt på radnumren.

### Steg 5. Explicit placering

Placera bilden i kolumn 2 med `grid-column: 2` och `grid-row`. Experimentera med att byta plats på text och bild.

### Steg 6. Motivera ditt val

I en kommentar för varje layout: skriv "Grid" eller "Flexbox" och varför.

## AI-spåret (nivå 2: Specificera och jämför)

**Be om två lösningar och välj** (cirka 25 minuter, efter att du gjort din egen lösning)

Du beskriver vad som ska byggas, AI föreslår kod, du testar, jämför och förstår. Det finns sällan en enda rätt lösning. Att välja och motivera är arbetet.

Regler: egen lösning först, du ska kunna förklara varje rad, och du loggar i `docs/ai-logg.md` i `mitt-projekt`. Reglerna finns i `AI-REGLER.md` i `mitt-projekt`.

1. Be AI om två olika sätt att bygga menyrutnätet (prompten nedan).
2. Implementera det du väljer. Hoppa inte över att läsa förklaringen.
3. Testa på tre bredder: 360, 768 och 1280 px.
4. Skriv en mening om varför du valde som du gjorde.
5. Logga valet och motiveringen.

Prompt att utgå från:

```
Ge mig två olika sätt att bygga ett
rutnät med tre menykort i CSS Grid.
Förklara kort när man väljer det ena
eller det andra.
```

**Kontrollera med:**

- Testa i DevTools enhetsläge på tre bredder.
- Titta på Grid-markeringen i DevTools.

**I ditt projekt:** Be om två lösningar för sidans övergripande layout. Välj och motivera.

## Kontrollista: så vet du att du är klar

- [ ] Menyn är ett grid som ändrar antal kolumner utan media queries.
- [ ] Rubriken i Om oss sträcker sig över båda kolumnerna.
- [ ] Om oss har en tvåkolumnslayout.
- [ ] Du har använt `gap`.
- [ ] Du har motiverat valet mellan Grid och Flexbox i kommentarer.
- [ ] Du har pushat till din fork och skickat in länken.
- [ ] Du har gjort AI-uppgiften och skrivit en post i `docs/ai-logg.md`.

## Tips om du fastnar

- `fr` är en andel av ledigt utrymme: `1fr 2fr` ger dubbelt så bred andra kolumn.
- Barnet ligger fel? Kolla om det har explicita `grid-column`-värden.
- Skriv ut kolumnerna på papper om du tappar bort dig.

## Ditt projekt: Dagens steg i `mitt-projekt`

Efter övningen här jobbar du vidare i ditt eget projekt (din design från modul 3). Dagens steg står i `PROJEKTSTEG.md` i ditt repo `mitt-projekt`, under **Dag 6**. Det är där ditt riktiga arbete växer. Övningen här är träningsbanan.

## Inlämning

**Deadline: imorgon klockan 09.00.** Allt lämnas in i Microsoft Forms. Du behöver inte redovisa något muntligt.

I formuläret fyller du i:

1. Länk till din fork av det här repot.
2. Länk till ditt `mitt-projekt`.
3. Reflektion: Förklara tumregeln "Grid för helheten, Flexbox inuti" med ett eget exempel från din egen design.

## Vill du mer? (frivilligt)

- Bygg om hela sidan med `grid-template-areas` (header, main, footer).
- Gör en bildgalleri-sektion i Om oss med ett grid i grid.
