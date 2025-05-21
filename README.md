# 💬 chat_vhsky

Embedovaný webový chat pro [VHSky.cz](https://vhsky.cz), postavený na [Hydrogenu](https://hydrogen.element.io/) a nasazený přes [Surfer](https://cloudron.io/store/org.surfer.cloudronapp.html) na [chat.vhsky](https://chat.vhsky.cz).

## ✨ Funkce

- Každá Matrix místnost má vlastní HTML stránku (např. `/chat/stream-xyz.html`)
- Funguje i pro nepřihlášené uživatele (guest access)
- Bez nutnosti JavaScriptové konfigurace – čistý a snadno nasaditelný kód
- Možno snadno vložit do iframe na webu nebo k livestreamu

## 🧱 Struktura repozitáře

```
chat_vhsky/
├── index.html              # volitelná domovská stránka nebo redirect
├── chat/
│   ├── stream-abc.html     # chat pro konkrétní místnost (např. livestream)
│   └── stream-def.html
└── README.md
```

## ➕ Přidání nového chatu

1. Zkopíruj existující soubor v adresáři `chat/`, např. `stream-vzor.html`.
2. Uprav `room` ID v `<iframe>` podle Matrix místnosti.
3. Pushni změnu do repozitáře – bude dostupné na `https://chat.vhsky.cz/chat/novychat.html`.

### Ukázka `iframe` pro Hydrogen:

```html
<iframe
  src="https://hydrogen.element.io/?hs_url=https%3A%2F%2Fmatrix.vhsky.cz&room=!abc123:vhsky.cz"
  width="100%"
  height="500"
  style="border: none;">
</iframe>
```

## 📜 Licence

MIT © VHSky.cz


