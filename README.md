# Hronopis

Enkriptovani dnevnik beleški o učenicima. Radi potpuno offline, direktno iz browsera.

## Kako radi

- **HTML je statična aplikacija** — nikad se ne menja
- **Podaci se čuvaju u zasebnom enkriptovanom JSON fajlu** (`hronopis-podaci-*.json`)
- AES-GCM enkripcija sa PBKDF2 derivacijom ključa (Web Crypto API)
- Zero dependencies, vanilla JS, sve inline u jednom HTML fajlu

## Korišćenje

1. Otvorite `hronopis.html` u browseru (radi i sa `file://` protokolom)
2. **Prvi put:** kliknite "Kreirajte novi dnevnik" → postavite PIN → dodajte razrede i učenike → "Sačuvaj" downloaduje enkriptovan JSON
3. **Sledeći put:** otvorite HTML → učitajte JSON (drag-and-drop ili klik) → unesite PIN → radite → "Sačuvaj"

## Funkcionalnosti

- PIN autentifikacija sa AES-GCM enkripcijom
- CRUD za razrede, učenike i beleške
- Kontrolna tabla sa statistikama
- Globalna pretraga učenika
- Filtriranje beleški po tipu (pozitivna/negativna/info)
- Sortiranje tabele učenika
- Profil učenika sa svim beleškama
- Promena PIN-a
- Izvoz podataka (nekriptovan JSON backup)
- Izvoz izveštaja (Markdown po razredima)
- Upozorenje na nesačuvane promene
