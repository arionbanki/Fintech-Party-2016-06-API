# Claims API - Arion banki Fintech Party API documentation version v1
https://arionapi-sandbox.azure-api.net/claims/v1

### Um Claims - Innheimtukröfur
Undir þessari [þjónustu](/ "e. resource, gæti verið þýtt is. auðlind\viðfang") er að vinna með innheimtukröfur innskráður notandi sem kröfuhafi hefur aðgang að. Þegar um er að ræða prófananotanda, eru búin til slembigögnin í fyrstu innskráningu sem notuð eru svo áfram. Þess utan uppfærir notandi gögnin með eigin aðgerðum og halda þau sér milli innskráninga.

Upplýsingarnar eru sambærilegar við gögn sem notendur hafa aðgang í gegnum netbanka og B2B lausnir Arion banka og er því ekki  í boðið að vinna með auðkenni, kröfustofna eða aðgerðir félagaþjónustu sem stendur.
      
Hér má skoða mun ítarlegri [html lýsingu](https://rawgit.com/arionbanki/Fintech-Party-2016-06-API/master/Claims/Claims.html "sjá Claims.html") á samningnum í GitHub repo fyrir Fintech partý.

### Öryggi
Köll á þjónustuna þurfa að innihalda API lykil sem samþykkt teymi í Fintech Party munu geta sótt um á gátt API viðmótsins. Þess utan er þjónustan varinn með OAuth 2.0 heimildarveitingu, sem ýmist fylgir authorization_code eða implicit flæði.
      
Sem stendur er afmörkun heimilda nokkuð gróf, auðkenndur notandi fær aðgang að öllum upplýsingum og aðgerðum undir auðlindinni. Í framtíðinni má sjá fyrir sér að miðla tilteknum upplýsingum sem notandi heimilar og sleppa eða jafnvel maska svæði eftir því hvað passar tengt þjónustuveitendum.

---

## Claims

### /claims

* **get** *(secured)*: Returnes a list of claims belonging to the claimant used to make the API request.
* **post** *(secured)*: Create a new claim.

### /claims/{claimId}

* **get** *(secured)*: Returns a representation of a claim.
* **patch** *(secured)*: Allows you to modify the properties of a claim. For example to cancel a claim.

### /claims/{claimId}/claimTransactions

* **get** *(secured)*: Returnes a list of transactions that encapsulate information about the status of a claim associated with a particular event in its lifetime.

