# Digital Signature API - Arion banki Fintech Party API documentation version v1
https://arionapi-sandbox.azure-api.net/digitalSignatures/v1

### Um DigitalSignature - Rafrænar undirritanir
Undir þessari þjónustu er að finna möguleika tengda því að undirrita skjöl. Fyrir prófunarumhverfi er það ávallt Arion banki sem kemur fram sem beiðandi undirritunar en raunverulegar kennitölur þurfa að vera gefnar upp fyrir undirritendur. Farið er gegnum [https://prufa.signet.is/](https://prufa.signet.is/ "Signet prófunarumhverfi") til að framkvæma undirritanir.

Virknin er að öðru leiti sambærilegar við þá möguleika sem Signet býður upp á, utan að API viðmótið einfaldar eilítið ákveðna þætti í þessum fyrsta fasa.
      
Hér má skoða mun ítarlegri [html lýsingu](https://rawgit.com/arionbanki/Fintech-Party-2016-06-API/master/DigitalSignature/DigitalSignature.html "sjá DigitalSignature.html") á samningnum í GitHub repo fyrir Fintech partý.

### Öryggi
Köll á þjónustuna þurfa að innihalda API lykil sem samþykkt teymi í Fintech Party munu geta sótt um á gátt API viðmótsins. Þess utan er þjónustan varinn með OAuth 2.0 heimildarveitingu, sem ýmist fylgir authorization_code eða implicit flæði.

Sem stendur er afmörkun heimilda nokkuð gróf, auðkenndur notandi fær aðgang að öllum upplýsingum og aðgerðum undir auðlindinni. Í framtíðinni má sjá fyrir sér að miðla tilteknum upplýsingum sem notandi heimilar, eftir því sem passar þjónustuveitendum.      

---

## Digital signatures

### /digitalSignatures

* **post** *(secured)*: Creates a new digital signature

### /digitalSignatures/{uuid}
Universal unique identifier for signature.

* **get** *(secured)*: 
* **delete** *(secured)*: 

### /digitalSignatures/{uuid}/documentContent
The document that is to be signed by the receiving parties

* **get** *(secured)*: Gets the content.
* **post** *(secured)*: Uploads the file content to be digitally signed. Until this has happened, the signature remains invalid.
After the upload is finished, the processing starts.

