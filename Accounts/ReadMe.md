# Accounts API - Arion banki Fintech Party API documentation version v1
https://arionapi-sandbox.azure-api.net/accounts/v1

### Um Accounts - Innlánsreikninga
Undir þessari [þjónustu](/ "e. resource, gæti verið þýtt is. auðlind\viðfang") er að finna upplýsingar um bankareikninga sem innskráður notandi hefur aðgang að. Þegar um er að ræða prófananotanda, eru búin til slembigögnin í fyrstu innskráningu sem notuð eru svo áfram.

Upplýsingarnar eru sambærilegar við gögn sem notendur hafa aðgang í gegnum netbanka, smáforrit og B2B lausnir Arion banka. Þannig sér notandi bæði veltureikninga sína sem og sparnaðarreikninga. Grunnupplýsingar um eiginleika reiknings eru á honum sjálfum en undir hverjum reikningi má svo nálgast hreyfingar og stöður.
      
Hér má skoða mun ítarlegri [html lýsingu](https://rawgit.com/kristinnstefansson/intechParty201606Documentation/master/Accounts/Accounts.html "sjá Accounts.html") á samningnum í GitHub repo fyrir Fintech partý.

### Öryggi
Köll á þjónustuna þurfa að innihalda API lykil en sem samþykkt teymi í Fintech Party munu geta sótt um slíka á portal þjónustunnar. Þess utan er þjónustan varinn með OAuth 2.0 heimildarveitingu, sem ýmist fylgir authorization_code eða implicit flæði.

Sem stendur er afmörkun heimilda nokkuð gróf, auðkenndur notandi fær aðgang að öllum upplýsingum og aðgerðum undir auðlindinni. Í framtíðinni má sjá fyrir sér að miðla tilteknum upplýsingum sem notandi heimilar, eftir því sem passar þjónustuveitendum.      

---

## Accounts

### /accounts

* **get** *(secured)*: Retrieves information about available accounts.

### /accounts/{accountId}
A single account identified by account ID.

* **get** *(secured)*: Information about an account.

### /accounts/accountTransactions
Provides an overview of account transactions.It is not permitted to get all transactions at once. Instead you have to define page number and transactions per page.

* **get** *(secured)*: Some requests can be filtered by a date range.

