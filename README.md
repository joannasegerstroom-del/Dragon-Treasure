# Dragon-Treasure
*Författare: Valentino Markouch, Oscar Dahl, Joanna Segerström  
Datum: 2025-12-13  
Version: 1.0.0  
Språk: Java*

## Om projektet
**Dragon Treasure** är ett äventyrsspel skrivet i java, där spelaren utforskar en grotta (*Dungeon)* genom olika dörrar och rum.  
Det är ett textbaserat spel med fokus på objektorienterad programmering (OOP).  
Spelet hanterar navigering mellan rum via olika dörrar samt håller koll på spelarens position i grottan.

### Funktioner
* **Navigering:** Genom att välja olika väderstreck (N/S/V/O) kan spelaren förflytta sig från ett rum till ett annat.  
*Vi valde att byta ut bokstaven 'Ö' (öster) till bokstaven 'O'. Detta gjorde vi på grund av vissa problem som uppstod vid användning av 'Ö'*  
* **doNarrative:** Varje rum har en unik beskrivning som skrivs ut när spelaren anländer i rummet. Det skrivs även ut vilka dörrar som finns kopplade till rummet för vidare navigering.  
* **Låsta dörrar:** Samtliga dörrar har ett lås som antingen kan vara *False (dörren är upplåst)* eller *True (dörren är låst)*. Denna funktion är tillagd då en av dörrarna är låsta och kräver en nyckel för att öppnas.  
*Just nu finns det ingen nyckel och därav inget sätt att öppna den låsta dörren, eftersom det inte var nödvändigt enligt uppgiftsbeskrivningen.*  
* **Objektorienterad design:** Tydlig uppdelning mellan spellogik, kart-setup och entiteter.

## Projektstruktur
* **'Main.java'** - Startpunkten som sätter igång spelet. Här finns Main-metoden *(public static void main)* som är nödvändig för att kunna köra spelet.
* **'DragonTreasure.java'** - Uppbyggnaden av spelet. Här skapas alla rum med tillhörande beskrivningar samt ihopkopplingar av dörrarna.
* **'Dungeon.java'** - Hanterar spellogiken och spelarens interaktioner. Här finns en spel-loop som baseras på spelarens input.
* **'Room.java'** - Hantering av rumsbeskrivningar samt närliggande dörrar. Här finns en lista *(ArrayList)* som retunerar vilka dörrar som finns kopplat till rummet samt skriver ut vilket väderstreck och position dörren har. 
* **'Door.java'** - Hantering av dörrens position, destination samt låsstatus.
* **'Player.java'** - Håller information om spelaren. *(som just nu endast består av 'Namn')*

## Så spelar du

### Förutsättningar
* Installation av **Java Development Kit (JDK)** krävs.
* Ladda ned källkoden till en mapp på datorn.
* Öppna en terminal och navigera till mappen.
* Kompilera alla java-filer:
```bash
javac *.java
```
* Starta spelet:
```bash
java Main
```

### Kontroller
När spelet startar skriver du in ditt namn och trycker på [Enter] för att komma till det första rummet.  
Därefter navigerar du igenom grottan genom att skriva in bokstaven för det väderstreck du vill gå mot, följt av [Enter].

* **'N'** - Gå norrut
* **'S'** - Gå söderut
* **'V'** - Gå västerut
* **'O'** - Gå österut
* **'Q'** - Avsluta spelet

*Kommandona fungerar med både stora och små bokstäver*

---
*Skapat av Joanna Segerström*

