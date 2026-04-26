# Vehicle Rental Platform

Šis projektas yra transporto priemonių nuomos sistemos simuliacija, parašyta Python kalba. Projektas sukurtas kaip demonstracinė programa, atspindinti pagrindinius objektinio programavimo (OOP) principus ir gerąsias kodo rašymo praktikas.

## Pagrindinės funkcijos

* **Transporto priemonių valdymas:** Palaikomi skirtingi transporto priemonių tipai (automobiliai ir paspirtukai).
* **Klientų registracija ir nuoma:** Galimybė priskirti klientą, išnuomoti jam transporto priemonę tam tikram dienų skaičiui bei grąžinus – suskaičiuoti kainą.
* **Duomenų išsaugojimas (File I/O):** Visas inventorius ir jo užimtumo būsena gali būti išsaugota į `.csv` failą ir vėliau sėkmingai atkurta.
* **Testavimas (Unit Tests):** Sistemoje integruoti baziniai vienetiniai testai naudojant `unittest` biblioteką, užtikrinantys, kad nuomos ir grąžinimo logika veikia be priekaištų.

## Architektūra ir OOP principai

Projekte pritaikyti šie dizaino ir architektūros sprendimai:
1. **Abstrakcija ir Inkapsuliacija:** Bazinė klasė `Vehicle` apibrėžia privalomus metodus ir slepia vidinę būseną naudodama privačius atributus bei savybes (`@property`).
2. **Paveldėjimas ir Polimorfizmas:** `Car` ir `Scooter` klasės paveldi iš `Vehicle` ir savitai perrašo `get_info()` bei `to_csv_row()` metodus.
3. **Factory Method Šablonas:** `VehicleFactory` klasė atsakinga už dinamišką atitinkamo tipo objektų kūrimą.
4. **Agregacija:** `RentalPlatform` klasė savo viduje kaupia `Vehicle` objektus.

## Kaip paleisti?

1. Įsitikinkite, kad jūsų kompiuteryje įdiegtas [Python 3](https://www.python.org/downloads/).
2. Atsisiųskite `Transport Rent Platform` failą.
3. Atsidarykite terminalą (Command Prompt / Terminal) tame pačiame aplanke.
4. Vykdykite komandą:
   ```bash
   python Transport Rent Platform.py