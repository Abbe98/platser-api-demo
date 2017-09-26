# platser-api-demo
En liten webbapplikation som använder sig av Platsers API, samt OAuth via Google för autentisering.

Dokumentation för Platsers API
https://svc.raa.se/platser/


Gör såhär:

Registrera din applikations adress (eller lokalhost om du kör lokalt) som giltig redirect-adress hos google. Skapa även ett klient-id (client-id).
Fyll i dessa i koden, och serva index.html, t.ex med browser-sync.

Applikationen är en enkel prototyp där man kan söka bland berättelser och platser, samt logga in och ändra sin biografi på sitt platser-konto.
För att kunna göra saker som inlggad användare måste du skapa ett användarnamn på platser med ditt OpenId/Google-konto. Detta gör du enklast på platsers hemsida.

När man loggar in i applikationen hamnar man på googles inloggningssida. Sedan skickas man till den registrerade redirect-uri:n, med en token som query-parameter.
Det är den nyckeln/token som används för att autentisera användaren vid de anrop som kräver inloggning.
