# Creditcards API - Arion banki Fintech Party API documentation version v1
https://arionapi-sandbox.azure-api.net/creditcards/v1

### Um CreditCards - Greiðslukort
Undir þessari [þjónustu](/ "e. resource, gæti verið þýtt is. auðlind\viðfang") er að finna upplýsingar um greiðslukort sem innskráður notandi hefur aðgang að. Þegar um er að ræða prófananotanda, eru búin til slembigögnin í fyrstu innskráningu sem notuð eru svo áfram.

Upplýsingarnar eru sambærilegar við gögn sem notendur hafa aðgang í gegnum netbanka, smáforrit og B2B lausnir Arion banka. Grunnupplýsingar um eiginleika greiðslukorts má skoða en undir hverjum korti má svo nálgast hreyfingar eftir tímabilum.
      
Hér má skoða mun ítarlegri [html lýsingu](https://rawgit.com/arionbanki/Fintech-Party-2016-06-API/master/CreditCards/CreditCards.html "sjá CreditCards.html") á samningnum í GitHub repo fyrir Fintech partý.

### Öryggi
Köll á þjónustuna þurfa að innihalda API lykil sem samþykkt teymi í Fintech Party munu geta sótt um á gátt API viðmótsins. Þess utan er þjónustan varinn með OAuth 2.0 heimildarveitingu, sem ýmist fylgir authorization_code eða implicit flæði.
      
Sem stendur er afmörkun heimilda nokkuð gróf, auðkenndur notandi fær aðgang að öllum upplýsingum og aðgerðum undir auðlindinni. Í framtíðinni má sjá fyrir sér að miðla tilteknum upplýsingum sem notandi heimilar og sleppa eða jafnvel maska svæði eftir því hvað passar tengt þjónustuveitendum.

---

## CreditCards
Provides an overview of credit cards

### /creditCards

* **get** *(secured)*: Provides an overview of credit cards. It provides information on cards where the logged-in user is a cardholder or owner of a card, provided that user is entitled to see the credit card. It shows information on cards in active use and cards in the legal collection process. It does not show amounts on cards in the legal collection process as collection costs are not included in the balance. In such cases null is returned in the field for amounts

### /creditCards/{cardId}
Provides detailed information on individual cards.

* **get** *(secured)*: Provides detailed information on individual cards. The logged in user has to be a cardholder or the owner of a card and also have permission to see the card. It does not show amounts on cards in the legal collection process as collection costs are not included in the balance. In such cases null is returned in the field for amounts.

### /creditCards/{cardId}/creditCardTransactions
Provides an overview of credit card transactions.It is not permitted to get all transactions at once. Instead you have to define page number and transactions per page.

* **get** *(secured)*: Allows the user to view the transactions on a card performed during a specific period. The logged-in user has to be a cardholder or the owner of a card and also have permission to see the card. It is possible to get the data by defining page number and page size.

