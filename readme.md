# Python - teori og huskeliste

- [Beregninger og operatorer](#beregninger-og-operatorer)
- [Variabler](#variabler)
- [Skriv ut tekst på skjerm](#skriv-ut-tekst-på-skjerm)
- [Les inn tekst / tall fra bruker](#les-inn-tekst--tall-fra-bruker)
- [Logiske tester](#logiske-tester)
- [Lister](#lister)
- [Funksjoner](#funksjoner)
- [Løkker](#løkker)

## Beregninger og operatorer

Regneoperasjon | Operator
---------------|---------
Addisjon | +
Subtraksjon | -
Multiplikasjon | *
Divisjon | /


### Operator rekkefølge

 - Gange og deling gjøres før minus og pluss
 - Bruk parentes for å styre rekkefølge

Eksempler:
```
    5 + 30 * 20 = 605
    (5 + 30) * 20 = 700
  ```
## Variabler
En variabel er en måte å lagre en verdi med et navn. Som man ser av navnet "variabel" så kan verdien variere, - man tilordner en verdi med å "sette variabelen lik" den verdien man vil den skal ha. Eksempel:
```python
score = 25
player_name = "Player One"
```
Legg merke til at det er brukt ``"`` (anførselstegn) rundt ``Player One``. Dette gjør at Python forstår at variabelen vi har laget skal være en tekst (på engelsk *string*). Mens for ``25``så er det ikke anførselstegn, dermed vil Python behandle det som et heltall ``int`` (forkortelse av engelsk *integer*).

En ``string`` variabel kan også lages med enkel apostrof ``'``, men må man alltid starte og slutte med samme type tegn, så f.eks:
```python
player_name = "Pastor Tim" # OK, bruker bare anførselstegn
player_name = 'Pastor Tim' # OK, bruker bare apostrof
player_name = 'Pastor Tim" # Ikke OK, blander apostof og anførselstegn
```

En variabel kan også inneholde flere elementer, se [liste](#lister)
## Skriv ut tekst på skjerm
```python
print("Tekst som skal skrives ut")
```
### Skriv ut med variable
```python
score = 40
print("Your score is: ", score)
```
### Skriv ut med flere variable
Bruker f-string (format string, legg merke til f før anførselstegn - krever Python versjon 3.6 eller nyere)
```python
score = 40
health = 100
print(f"Your score is {score} and your health is {health}")
```
## Les inn tekst / tall fra bruker
```python
choice = input("Please enter your choice: ")
```
Det brukeren skriver inn blir lagret i variabelen choice
### Gjør om input til tall
Når man bruker ``input`` blir det lagret som "tekst". For å gjøre det om til tall brukes funksjon ``int``
```python
choice = int(input("Please enter your choice: "))
```

## Logiske tester
Sjekk om et logisk uttrykk er sant med kommandoen ``if``. Kan teste på variable av typen Boolean (True eller False), matematiske som uttrykk (større enn >, mindre enn <), eller med logiske operatorer som ``and``og ``or``.
```python
if score > 100:
	print("Congratulations!")

if health == 0:
	print("Sorry, no more health")
```
Legg merke til bruk av to likhetstegn i testen ``health == 0``. Dette gjøres for å sammenligne to verdier: "er health det samme som 0?". I motsetning til når man tilordner en verdi til en variabel, da brukes et likhetstegn, se [variabler](#variabler)
### Flere alternativ, - hvis, ellers hvis, ellers
```python
if health < 10:
	print("Take care, this could be dangerous")
elif health < 50:
	print("You are still going strong")
else
	print("No worries :)")
```
## Lister
Lister er en variabel-type som lar deg lagre flere elementer i en variabel. For å lage en liste brukes hakeparentes [], f.eks.
```python
list_of_numbers = [2, 4, 8, 16]
list_of_tools = ['hammer', 'saw', 'nails', 'drill']
```
### Se innholdet i liste
Hele listen kan skrives ut på samme måte som andre variabler:
```python
print(list_of_tools) # skriver ut alle elementene slik: ['hammer', 'saw', 'nails', 'drill']
```

### Indeksering av liste
Elementene i listen telles fra 0. Så om vi for eksempel skal se hva som er det første elementet i listen med verktøy ovenfor, så kan vi skrive:
```python
print(list_of_tools[0]) # skriver ut hammer
print(list_of_tools[1]) # skriver ut saw
```
### Legg elementer til listen
Bruk funksjonen ``append``:
```python
list_of_tools.append('chainsaw')
```
### Fjern element fra listen
Bruk funksjonen ``del``:
```python
del(list_of_tools[0]) # hammer er nå fjernet fra listen
```

## Funksjoner
Måte å organisere kode på så den blir lettere å lese, og gjør det lettere å gjenbruke deler av koden som skal kjøres flere ganger.
### Lage funksjon
```python
def print_menu()
	print("1. First option")
	print("2. Second option")
```
### Bruke funksjon
Kaller funksjonen med å skrive navnet med parentes bak.
```python
print_menu()
```
### Parameter og returverdi
Lar deg "sende verdier inn" i funksjonen, og returnere verdier tilbake.
```python
def add_numbers(number_a, number_b)
	return number_a + number_b
```
Returverdien kommer "ut" der funksjonen kalles, f.eks.
```python
a = 100
b = 160
result = add_numbers(a, b)
```
Her blir resultatet av operasjonen som gjøres inne i ``add_numbers`` lagret i variabelen result.

## Løkker
Når vi ønsker å få en kode til å gjentas flere ganger kan vi bruke en løkke. Enten et gitt antall ganger, eller basert på et logisk uttrykk: "så lenge at følgende er sant, - gjenta".

Dette gjør det mulig å få gjort mer med færre linjer kode, f.eks for å skrive ut en tekst fem ganger så kan vi gjøre følgende:
```python
print('Hello world')
print('Hello world')
print('Hello world')
print('Hello world')
print('Hello world')
```
Eller vi kan gjøre det slik:
```python
for x in range(0, 5):
	print('Hello world')
```

### for løkke
En ``for`` løkke gjentas et gitt antall ganger basert på hvordan vi setter den opp, for eksempel kan vi bruke den til å gå gjennom en gitt mengde med å bruke ``range`` funksjonen slik som i løkken ovenfor. Eller for for å gå gjennom en liste:
```python
for tool in list_of_tools:
	print(tool)
```
Her blir variabelen ``tool`` satt til hvert element i listen for hver gang løkken går, slik at vi vil skrive ut alle elementene i listen på hver sin linje. 

### while løkke
En ``while`` kjøres så lenge et logisk uttrykk er sant. Det kan for eksempel være:
```python
while health_points > 0:
	print("You are still in the game")
```
En "evig" løkke kan man lage med å gjøre følgende:
```python
while True:
	print("This will go on forever...")
```
Nå er det sjelden at man faktisk *ønsker* en evig løkke, men det kan f.eks. være at man kjører løkken "evig", men hopper ut om en gitt hendelse skjer, f.eks:
```python
while True:
	print("This will go on forever...")
	if user_choose_exit:
		break;
print("Hey, the loop did not go on forever?!")
```                                                                                                                                                                                                                                                                     





