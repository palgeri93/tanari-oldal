# Pálfi Gergő tanári oldala

Élő oldal: https://palgeri93.github.io/tanari-oldal/

Tantárgyanként és tanári feladat szerint rendezett, kereshető honlap. A Symbaloo-gyűjteményt földrajzi modellekkel, a Magyarország története 46 részének jegyzékével és 14 általános iskolai könyvvel bővítettük: 111 tétel, 8 csoport. A sorozatból 45 YouTube-videó beágyazható; a 45. rész a hivatalos műsoroldalra mutat. A könyvek kódjait és a videók forrásait a [LIBRARY-SOURCES.md](LIBRARY-SOURCES.md) dokumentálja.

## Bővítés

A `resources.json` fájl `resources` listájához adj új objektumot:

```json
{
  "id": "egyedi-tananyag",
  "title": "A tananyag címe",
  "category": "foldrajz",
  "description": "Rövid, tényszerű magyar ismertető.",
  "url": "https://pelda.hu/tananyag/",
  "embed": false,
  "kind": "Gyakorló",
  "source": "Saját hozzáadás"
}
```

A `category` a `categories` lista egyik azonosítója. A kategóriák is bővíthetők. Egyedi `id` szükséges, szóköz nélkül. A `featured: true` a kezdőlap gyorslinkjei közé emeli az anyagot.

A saját, beágyazható GitHub Pages alkalmazások `embed: true` értékkel az oldalon belül jelennek meg. Csak a beágyazást engedélyező és ellenőrzött oldalakat állítsd erre. A többi link ugyanabban a böngészőlapon nyílik meg. Az oldal nem módosítja a célszolgáltatások hozzáférési jogosultságait.

## Forrás és ellenőrizhetőség

Eredeti gyűjtemény: https://palfigergo93.symbaloo.com/

A `symbaloo-import.json` az eredeti címeket, célhivatkozásokat és csoportútvonalakat őrzi. A honlapon olvasható címekből kijavítottuk a nyilvánvaló elírásokat és HTML-entitásokat. A Google-, NotebookLM- és egyéb megosztási linkek célját megtartottuk. A YouTube-lejátszó beágyazási URL-jeiből közvetlen videólinkeket készítettünk.

A „Matematika tankönyv” csempe az `OH-FOL78MA` jelű földrajz-munkafüzetre mutatott. A célhivatkozás megmaradt, a megjelenített cím Földrajz 7–8. munkafüzet. Az azonosítót a hivatalos [tankönyvjegyzék](https://cdn.kormany.hu/uploads/document/f/ff/ff5/ff5a4e3a42df1367bf328cb79266facc847c493b.pdf) is megerősíti.

A JAKUCSVERSENY és a külön „Magyarország története” csoportokból az import idején nem jelent meg célhivatkozás; nem készítettünk hozzájuk kitalált URL-t. A másik történelmi csoport két tényleges videója átkerült. Az eredeti Symbaloo a menüből bármikor elérhető. Az import pillanatfelvétel; a későbbi Symbaloo-módosításokat a honlap nem szinkronizálja automatikusan.

## Előnézet és közzététel

Nincs buildlépés vagy csomagfüggőség. Helyi előnézet a szülőmappából: `python -m http.server 8767 --directory tanari-oldal`.

A `main` ágra feltöltött módosításokat a GitHub Actions Pages munkafolyamat publikálja. A Google Fonts betűkészletei hálózat nélkül rendszerbetűvel helyettesítődnek. Nem használunk analitikai kódot vagy helyi adattárolást; külső alkalmazás betöltésekor annak saját szabályai érvényesek.
