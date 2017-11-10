# Python - teori og huskeliste

- [Beregninger og operatorer](#beregninger-og-operatorer)
- [Skriv ut tekst på skjerm](#skriv-ut-tekst-på-skjerm)
- [Les inn tekst / tall fra bruker](#les-inn-tekst--tall-fra-bruker)
- [Tester (if)](#tester-if)
- [Funksjoner](#funksjoner)

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
    ((5 + 30) * 20) / 10 = 70.0
  ```

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
Når man bruker input blir det lagret som "tekst". For å gjøre det om til tall brukes funksjon ``int``
```python
choice = int(input("Please enter your choice: "))
```

## Tester (if)
Sjekk om et uttrykk er sant
```python
if score > 100:
	print("Congratulations!")
```
### Flere alternativ, - hvis, ellers hvis, ellers
```python
if health < 10:
	print("Take care, this could be dangerous")
elif health < 50:
	print("You are still going strong")
else
	print("No worries :)")
```
## Funksjoner
Måte å organisere kode på så den blir lettere å lese, og gjør det lettere å gjenbruke deler av koden som skal kjøres flere ganger.
### Lage funksjon
```python
def my_cool_function()
	print("Hey I am a cool function!")
```
### Bruke funskjon
Kaller funksjonen med å skrive navnet med parentes bak.
```python
my_cool_function()
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

