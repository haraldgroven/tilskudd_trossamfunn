# Tilskudd trossamfunn i Norge

Membership statistics Norwegian religious organisations 2010-2018

Komplett statistikk over medlemstall i alle 912 organisasjoner som har mottatt tilskudd til tros- og livssynssamfunn fra den norske stat i perioden 2010 til 2018.

# TODO

Analyse og visualisering i R og MySQL, oppdatering av [Wikipedia-artikkelen om temaet](https://no.wikipedia.org/wiki/Tilskudd_til_tros-_og_livssynssamfunn).

# Kilde

regjeringen.no [Antall tilskuddstellende medlemmer i tros- og livssynssamfunn](https://www.regjeringen.no/no/tema/tro-og-livssyn/tros-og-livssynssamfunn/innsiktsartikler/antall-tilskuddsberettigede-medlemmer-i-/id631507/)

Brreg (snart)

## API nå tilgjengelig 

Data nå tilgjengelig via udokumentert API

[trussamfunn.fylkesmannen.no](https://trussamfunn.fylkesmannen.no)

```
curl 'https://trussamfunn.fylkesmannen.no/Tilskudd/TilskuddList' -H 'Content-Type: application/json; charset=UTF-8' --data-raw '{"draw":1,"columns":[{"data":"Navn","name":"","searchable":true,"orderable":true,"search":{"value":"","regex":false}},{"data":"Fylke","name":"","searchable":true,"orderable":true,"search":{"value":"","regex":false}},{"data":"Medlemmer","name":"","searchable":true,"orderable":true,"search":{"value":"","regex":false}},{"data":"Tilskudd","name":"","searchable":true,"orderable":true,"search":{"value":"","regex":false}},{"data":"Status","name":"","searchable":true,"orderable":true,"search":{"value":"","regex":false}}],"order":[{"column":0,"dir":"asc"}],"start":0,"length":100000,"search":{"value":"","regex":false},"Year":"2020"}' --compressed | jq '.' > 2020.json
```
