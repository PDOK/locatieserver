# Locatieserver

Voor het melden van issues, gebruik s.v.p. het Geoforum voor Locatieserver: https://geoforum.nl/c/applicaties-en-diensten/locatieserver.

De huidige versie van Locatieserver is versie 3.1. Deze bevat o.a. versionering van de endpoints, filtering op objecttype (t.b.v. backwards compatibility) en de Digitale Kadastrale Kaart (type:perceel en gekoppeld_perceel bij adressen). De zoekvoorbeelden en API-beschrijving zijn aangepast voor de nieuwe versie.
Zie [hier](https://github.com/PDOK/locatieserver/wiki/Zoekvoorbeelden-Locatieserver) voor een aantal zoekvoorbeelden.  
Zie [hier](https://github.com/PDOK/locatieserver/wiki/API-Locatieserver) voor de API-beschrijving.
Zie [hier](https://github.com/PDOK/locatieserver/wiki/API-Reverse-Geocoder) voor de API-beschrijving van de Reverse Geocoder.

## Changelog 3.1 tov 3.0

1. ‘q’ parameter is nu verplicht (behalve bij /free endpoint)
2. CORS pre-flight is veranderd: “dit werkt alleen wanneer de request volgens de http specificaties gedaan wordt, dus met een Origin en Access-Control-Allow-Methods header.”
3. Het is bij de nieuwe locatieserver niet toegestaan om query parameters op te geven die niet in de OpenAPI specificatie staan.
4. Er zijn nu Open API docs beschikbaar https://api.pdok.nl/bzk/locatieserver/search/v3_1/ui/
5. Twee extra velden, te weten "numFoundExact" in de response envelope en het veld "shards" in de documenten. De laatste wordt alleen getoond als je deze in de fl= parameter opneemt.
6. Het algoritme om de score te berekenen is aangepast. Hierdoor hebben de documenten over het algemeen een lagere score.
