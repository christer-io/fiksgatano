# Release notes 23. mars 2025

Relativt mye nytt i denne sprinten, inkludert funksjonalitet og ny-utvikling av brukergrensesnitt. Er også mye som er helt fersk funksjonalitet og kode, så jeg regner med at det vil ta litt tid før alt er feilfritt, men det meste av helt grunnleggende funksjonalitet skal nå funke. 

## 1. API documentasjon
En første veldig enkel side med API dokumentasjon for tre nye endepunkter. 

1. Et endepunkt som returnerer alle meldinger
- eller alle meldinger for en kommune
- eller alle meldinger for en kommune innenfor en spesifikk kategori
- eller alle meldinger for et fylke
2. Et endepunkt som returnerer alle kommuner
3. Et endepunkt som returnerer alle fylker
4. Et endepunkt som returnerer alle meldingskategorier som benyttes på plattformen

Merk: Denne første versjonen av API dokumentasjon inneholder kun GET. 

## 2. Re-design av forside for mobil og stor skjerm og side for å utforske nye meldinger
Endret design på forsiden for PC/stor skjerm. Har skiftet til Material UI rammeverket for komponenter og buttons. 

## 3. Brukervilkår og kontakt sider
Har utformet side for brukervilkår og side med bakgrunn for prosjektet. Dette er den første versjonen som dekker det mest grunnleggende knyttet til brukervilkår og datalagring. 
Kontakt siden inkluderer kontakt via e-post, mulighet for å legge til issues på Github, samt peker til Discord kanal. 

## 4. Github prosjekt med back-log og roadmap
Et etablert eget Github-prosjekt med dokumentasjon, backlog og mulighet til å bidra med issues. OBS: selve kildekoden til plattformen er ikke inkludert i denne fasen. Koden blir offentlig senere, etter gjennomgang og kvalitetssikring. 

- [Lenke til prosjekt.](https://github.com/christer-io/fiksgatano) 
- [Lenke til roadmap](https://github.com/users/christer-io/projects/4/views/4)

## 5. Endret design og funksjonalitet på "mine saker"
Har lagt til multiline edit av beskrivelse og gjort redigeringen mer brukervennlig for mobil. 

## 6. Funksjonalitet for å filtrerer på saker per kommune og kategori
Egen side lenket fra forsiden hvor bruker kan filtrere på kommune, løst/ikke løst og kategori.
På denne siden vil det også komme funksjonalitet for å se alle saker per fylke, men det kommer i neste sprint. 

## 7. Integrasjon Statens Vegvesen API
Første versjon av komponent som henter data fra Statens Vegvesen API for å estimere om en sak er i nærheten av en vei og i så fall hvilken vei. 
Ikke implmementer: Neste fase er en enkel beslutnings-algoritme som sender epost til fylke, kommune eller statens vegvesen basert på hvilken vei man melder sak ved.

## 8. Henter data fra Yr.no API
Ikke en veldig sentral komponent men i noen tilfeller vil det være relevant å ha informasjon om nedbør for en gitt lokasjon de neste 6 timene. Jeg har derfor laget en komponent som henter data fra Yr basert på den geolokasjon som er valgt av brukeren. 

## 9.  Her data fra Statens Kartverk 
På samme måte som for Statens Vegvesen er det viktig å ha informasjon om hvilken kommune en feil/sak er meldt i. Henter data fra API hos Kartverket som gir kommune ut som verdi på en gitt lokasjon. 


