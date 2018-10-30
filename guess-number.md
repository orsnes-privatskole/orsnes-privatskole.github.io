# Lag spillet "Gjett riktig tall" i Python

Bruk Python til å lage et spill hvor maskinen velger et tilfeldig tall, og så skal spilleren gjette riktig tall på et gitt antall forsøk. Hvis spilleren gjetter feil, skal spillet fortelle om forslaget var for høyt eller lavt.

Oppgaven er delt i flere del-oppgaver som bygger videre på de første delene. Så første versjon blir helt enkel, og så bygger vi på med mer funksjoner etter hvert.

## Del A – Start spillet
- Skriv en tittel med hva spillet heter, f.eks. «Guess Number Game v 0.1»
- Be spilleren skrive inn navnet sitt, og lagre det i en variabel
- Skriv en velkomst-tekst som ønsker spilleren velkommen, med bruk av spillerens navn

## Del B – Lag et tilfeldig tall
Her skal spillet "tenke på et tilfeldig tall". Vi må bestemme oss for hvor stort tallet maks kan være, jo større jo høyere vanskelighetsgrad vil det være på å gjette riktig. For første versjon velger vi at tallet skal være mellom 1 og 20.

Tips: Her må vi bruke modulen random. Funksjonen randint(tall-fra, tall-til) gir deg et tilfeldig tall mellom tall-fra og tall-til. F.eks random.randint(1, 20).

Lagre det tilfeldige tallet i en variabel og skriv det ut på skjermen (bare for testing, vi kan selvsagt ikke skrive det ut når spilleren skal gjette det , men det kommer senere).

## Del C – La spilleren gjette!
- Be spilleren gjette hvilket tall du tenker på
- Skriv ut om svaret er riktig, høyere eller lavere enn det tilfeldige tallet

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
