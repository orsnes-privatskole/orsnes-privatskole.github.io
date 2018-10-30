# Lag spillet "Gjett riktig tall" i Python

Bruk Python til å lage et spill hvor maskinen velger et tilfeldig tall, og så skal spilleren gjette riktig tall på et gitt antall forsøk. Hvis spilleren gjetter feil, skal spillet fortelle om forslaget var for høyt eller lavt.

Oppgaven er delt i flere del-oppgaver som bygger videre på de første delene. Så første versjon blir helt enkel, og så bygger vi på med mer funksjoner etter hvert.

Hver del har et løsningsforslag, men vent med å se på det til du har *prøvd* selv først! Bruk oversikten på [https://orsnes-privatskole.github.io/](https://orsnes-privatskole.github.io/) for å se hvordan man gjør de forskjellige tingene som trengs for å løse hver deloppgave.

## Del A – Start spillet
- Skriv en tittel med hva spillet heter, f.eks. «Guess Number Game v 0.1»
- Be spilleren skrive inn navnet sitt, og lagre det i en variabel
- Skriv en velkomst-tekst som ønsker spilleren velkommen, med bruk av spillerens navn

### Relevante avsnitt fra hjelpeteksten:
- [Skrive ut tekst på skjerm](https://orsnes-privatskole.github.io/#skriv-ut-tekst-p%C3%A5-skjerm)
- [Les inn tekst / tall fra bruker](https://orsnes-privatskole.github.io/#les-inn-tekst--tall-fra-bruker)

<details>
<summary>Løsningsforslag A</summary>

```python
# The guess number game
# Made by: 
# Version A
import time

name = input("What is your name? ")
print(f"Hello {name}, lets play the game Guess number!")

time.sleep(1)
```

</details>

## Del B – Lag et tilfeldig tall
Her skal spillet "tenke på et tilfeldig tall". Vi må bestemme oss for hvor stort tallet maks kan være, jo større jo høyere vanskelighetsgrad vil det være på å gjette riktig. For første versjon velger vi at tallet skal være mellom 1 og 10.

Lagre det tilfeldige tallet i en variabel og skriv det ut på skjermen (bare for testing, vi kan selvsagt ikke skrive det ut når spilleren skal gjette det 🙂, men det kommer senere).

### Relevant avsnitt fra hjelpeteksten:
- [Tilfeldige tall](https://orsnes-privatskole.github.io/#tilfeldige-tall)

<details>
<summary>Løsningsforslag B</summary>

```python
# The guess number game
# Made by: 
# Version B
import time
import random

name = input("What is your name? ")
print(f"Hello {name}, lets play the game Guess number!")

time.sleep(1)

# Pick a random number between 1 and 10
secret_number = random.randint(1, 10)

print(f"The random number is {secret_number}")

```

</details>

## Del C – La spilleren gjette!
- Be spilleren gjette hvilket tall du tenker på
- Skriv ut om svaret er riktig, høyere eller lavere enn det tilfeldige tallet

Her må vi bruke en logisk test for å sjekke om svaret er riktig. Siden vi skal sammenligne med et tilfeldig *tall*, så er det viktig å gjøre om innlest svar fra tekst til tall.

### Relevant avsnitt fra hjelpeteksten:
- [Logiske tester](https://orsnes-privatskole.github.io/#logiske-tester)
- [Gjør om input til tall](https://orsnes-privatskole.github.io/#gj%C3%B8r-om-input-til-tall)

<details>
<summary>Løsningsforslag C</summary>

```python
# The guess number game
# Made by: 
# Version C
import time
import random

name = input("What is your name? ")
print(f"Hello {name}, lets play the game Guess number!")

time.sleep(1)

# Pick a random number between 1 and 10
secret_number = random.randint(1, 10)

# Let the player guess
player_guess = int(input("I am thinking of a number between 1 and 10, can you guess which number? "))

# Check player answer
if player_guess == secret_number:
    print("WOW, you are good! The answer is correct.")
else:
    print(f"Sorry, that was wrong. The number was {secret_number}")

```

</details>

## Del D – La spilleren få flere forsøk
Å gjette riktig på første forsøk kan være litt vel flaks-basert, så vi må la spilleren prøve flere gang. Lag en løkke som lar spilleren gjette helt til riktig svar er gitt.

## Del E – Vanskelighetsgrad
Det er særlig to ting som kan påvirke vanskelighetsgraden i dette spillet: Hvor mange tall det velges fra, og hvor mange forsøk spilleren får på å gjette.
La spilleren velge vanskelighetsgrad i starten av spillet, f.eks.:

1. Lett (tall fra 1 til 20, 10 forsøk)
2. Middels (tall fra 1 til 100, 10 forsøk)
3. Vanskelig (tall fra 1 til 100, 5 forsøk)
4. Svært vanskelig (tall fra 1 til 1000, 10 forsøk)

For hvert forsøk kan det skrives ut hvor mange forsøk som er brukt og hvor mange som er igjen.
