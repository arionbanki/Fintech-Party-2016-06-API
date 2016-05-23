# National Registry API - Arion banki Fintech Party API documentation version v1
https://arionapi-sandbox.azure-api.net/nationalregistry/v1

### Um NationalRegistry - Þjóðskrá
Undir þessari [þjónustu](/ "e. resource, gæti verið þýtt is. auðlind\viðfang") má fletta upp í þjóðskrá, ef innskráður notandi hefur aðgang að henni. Virknin er sambærileg við uppflettingar sem notendur hafa aðgang í gegnum netbanka Arion banka. Ákveðið þýði af kennitölum er til staðar sem nota má fyrir aðgang að prófunargögnum.
            
Hér má skoða [html lýsingu](https://rawgit.com/arionbanki/Fintech-Party-2016-06-API/master/NationalRegistry/NationalRegistry.html "sjá NationalRegistry.html") á samningnum í GitHub repo fyrir Fintech partý.

### Öryggi
Köll á þjónustuna þurfa að innihalda API lykil sem samþykkt teymi í Fintech Party munu geta sótt um á gátt API viðmótsins. Þess utan er þjónustan varinn með OAuth 2.0 heimildarveitingu, sem ýmist fylgir authorization_code eða implicit flæði.

Sem stendur er afmörkun heimilda nokkuð gróf, auðkenndur notandi fær aðgang að öllum upplýsingum undir auðlindinni.      

---

## National Registry Parties

### /nationalRegistryParties

* **get** *(secured)*: Returns information about parties from the Icelandic National Registry, both individuals and corporations.

### /nationalRegistryParties/{kennitala}
A valid kennitala.

* **get** *(secured)*: A uniquely identifiable party, by kennitala.

