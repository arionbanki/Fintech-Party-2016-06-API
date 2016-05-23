# Currency Rates API - Arion banki Fintech Party API documentation version v1
https://arionapi-sandbox.azure-api.net/currency/v1

### Um CurrencyRates - Gengisupplýsingar
Undir þessari [þjónustu](/ "e. resource, gæti verið þýtt is. auðlind\viðfang") er að finna upplýsingar um skráð gengi eftir tímabilum. Gögn þjónustunnar eiga að endurspegla uppfærða stöðu gengist sem sýnilegt er á heimasíðu Arion banka.

Hér má skoða [html lýsingu](https://rawgit.com/arionbanki/Fintech-Party-2016-06-API/master/Currency/Currency.html "sjá Currency.html") á samningnum í GitHub repo fyrir Fintech partý.

### Öryggi
Köll á þjónustuna þurfa að innihalda API lykil sem samþykkt teymi í Fintech Party munu geta sótt um á gátt API viðmótsins. Að öðru leiti er þjónustan ekki varin auðkenningu eða kallar á frekari heimildir.

---

## Currencies

### /currencyRates

* **get**: Returns information about available currency exhange rates

### /currencyRates/{currencyTypeName}

* **get**: Returns information about a particular exchange rate

