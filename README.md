# newman-wrapper
CLI wrapper for Newman

### Dit is even een eerste proof of concept. Er is ongetwijfeld een handigere methode, maar ik leer meer als ik zelf ga prutsen.

Wat ik wou is een command line interface voor Wordpress zodat ik andere programma's makkelijk de mogelijkheid om blogberichten te posten kon bieden. Omdat ik vrij grote hoeveelheden berichten wil posten en het van buitenaf bereikbaar moet zijn wil ik het niet zelf hosten maar op andermans servers zetten, bijvoorbeeld Blogger.com. 
 
De meest gebruikte manier om een CLI voor WP te hebben is WP CLI (https://wp-cli.org/) maar ik kan Blogger.com niet even bellen om te vragen of ze dat voor mij willen installeren en ik kan het niet zelf op hun servers installeren.

Toen ging ik klooien met Postman en zag ik dat de functionaliteit daarvan via Newman ook beschikbaar is in de CLI.

https://learning.postman.com/docs/postman/collection-runs/command-line-integration-with-newman/

Helaas kan je weliswaar met Postman gemaakte configuraties uitvoeren, maar je kan niet zelf in de commandline specificeren dat je settings in die configuratie wil wijzigen/overrulen. 

https://github.com/postmanlabs/newman/issues/2192

Je kan dus bijv. wel telkens hetzelfde bericht naar hetzelfde blog posten, maar als je dat bericht wil veranderen moet je Postman weer openen, daar de wijziging in maken, JSONs exporteren, en die dan in Netman uitvoeren.

Daarom dacht ik: als ik nou een wrapper maakt die command line arguments accepteert, een JSON uitpoept die Netman configureert, en dan Netman draait...



Nota bene:
----------
* De eerste parameter is momenteel het bestand met de configuratie.

* Ik maak gebruik van een Application Password (mbv Basic Auth in Postman)  https://nl.wordpress.org/plugins/application-passwords/



Todo: 
-----
* autoit JSON generator gebruiken ipv het er hardcoded inzetten

JSON (by Gabriel13) - RFC4627 compliant JSON encode/decode.
JSON (by Ward) - JSMN - A Non-Strict JSON UDF.
JSON (by ozmike) - Bridge to Native Windows JSON plus OO extension for AutoIt.
JSONgen: JSON generator (by Jefrey) - UDF to generate JSON.

* key=value pairs als command line argument accepteren zodat de command line arguments niet in een specifieke volgorde hoeven te staan
* switches accepteren zoals /s 
