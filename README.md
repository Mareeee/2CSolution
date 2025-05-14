# GraphQL API za upravljanje korisnicima

Ovaj projekat predstavlja jednostavan **GraphQL API** razvijen pomoću **Apollo Server-a** i **Node.js-a**, sa povezivanjem na **PostgreSQL** bazu podataka.

## Opis projekta

API omogućava:

-   Registraciju novih korisnika (name, email)
-   Dohvatanje svih korisnika
-   Filtriranje korisnika po imenu ili email adresi
-   Brisanje korisnika
-   Validaciju email adrese pre dodavanja korisnika

Ovaj projekat je deo zadatka: **Razvoj GraphQL API-ja za upravljanje korisnicima**.

-   [Primer pokretanja](https://youtu.be/OvefBT4muG4)

---

## Pokretanje projekta

### Preduslovi

Pre nego što pokreneš aplikaciju, potrebno je da imaš instalirano:

-   [Node.js](https://nodejs.org/)
-   [PostgreSQL](https://www.postgresql.org/)

### Podesi bazu

Projekat koristi sledeće parametre za konekciju sa PostgreSQL bazom (nalaze se u `index.js`):

```bash
user: 'postgres',
host: 'localhost',
database: 'postgres',
password: 'password',
port: 5432
```

1. Kloniranje projekta:

```bash
git clone https://github.com/Mareeee/2CSolution.git
cd 2CSolution
```

2. Instaliranje Node.js paketa

```bash
node index.js
```

3. Pokretanje aplikacije

```bash
node index.js
```

4. Nakon pokretanja, pristupiti linku na localhost:4000 i pomoću alata kao što je apollo postavljati upite

## Primeri upita:

```bash
mutation {
  addUser(name: "Petar Petrovic", email: "petar@example.com") {
    id
    name
    email
  }
}

query {
  users {
    id
    name
    email
  }
}

mutation {
  deleteUser(id: 1) {
    id
    name
    email
  }
}
```
