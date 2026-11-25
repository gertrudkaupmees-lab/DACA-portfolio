# Nädal 3: SQL JOINs 


GT W3 A 

TOP 10 klienti kogumüügi järgi
| klient       | city     | ostude_arv | kogumüük |
| ------------ | -------- | ---------- | -------- |
| Tiina Pärn   | Tartu    | 73         | 27668.02 |
| Priit Rand   | Pärnu    | 76         | 26286.10 |
| Kevin Org    | Tallinn  | 78         | 23467.13 |
| Laura Tammik | Pärnu    | 74         | 23385.82 |
| Erkki Ilves  | Tartu    | 72         | 22942.42 |
| Anu Kuusik   | Tallinn  | 77         | 21626.10 |
| Kersti Lill  | Tallinn  | 71         | 21137.47 |
| Riina Lill   | Pärnu    | 67         | 20972.33 |
| Annika Saar  | Viljandi | 66         | 20726.79 |
| Ago Kull     | Pärnu    | 64         | 20124.61 |

Müük linnade kaupa 
| city       | kliente | oste | kogumüük   |
| ---------- | ------- | ---- | ---------- |
| Tallinn    | 1007    | 3601 | 1006252.88 |
| Tartu      | 525     | 1764 | 523286.64  |
| Pärnu      | 276     | 1231 | 374005.86  |
| Narva      | 145     | 438  | 122226.14  |
| Viljandi   | 94      | 359  | 102314.94  |
| Rakvere    | 90      | 338  | 93379.03   |
| Jõhvi      | 71      | 290  | 77601.15   |
| Kuressaare | 80      | 256  | 76509.61   |
| Haapsalu   | 73      | 252  | 73492.83   |
| Võru       | 66      | 216  | 60983.07   |
| Valga      | 69      | 216  | 59530.76   |
| Paide      | 55      | 169  | 53148.87   |


 loyalty_tier jaotust
| loyalty_tier | kliente | kogumüük   |
| ------------ | ------- | ---------- |
| null         | 1024    | 1071805.32 |
| silver       | 560     | 593470.07  |
| gold         | 491     | 533601.64  |
| bronze       | 476     | 423854.75  |

kokkuvõte Annale:
Parimad kliendid kogumüügi järgi on Tiina Pärn Tartust (27 668 €, 73 ostu), Priit Rand Pärnust (26 286 €) ja Kevin Org Tallinnast (23 467 €), kusjuures TOP 10 klientidest 4 on Pärnust ja 3 Tallinnast. 

Kõige rohkem müüki tuleb Tallinnast (1,01 mln, 3601 ostu), millele järgnevad Tartu (523 tuhat) ja Pärnu (374 tuhat); need kolm linna annavad kokku suurema osa kogumüügist.

Kogumüügi poolest on kõige tulusam tase silver (593 tuhat), seejärel gold (534 tuhat) ja bronze (424 tuhat), kuid kliendi kohta on tugevaim gold (~1087 €, silveril ~1060 € ja bronzel ~890 €). 

Märkimisväärne on, et 1024 kliendil (suurim grupp) loyalty_tier puudub, ja nad toovad 1,07 mln müüki, mistõttu tasuks nende tase üle vaadata või lojaalsusprogrammi kaasata. Soovitan koondada lojaalsusprogrammi tähelepanu goldile ja silverile ning täita puuduvad tasemed andmetes.

Lisaanalüüs:
Üle keskmise müügid arvestamata tundmatuid kliente
| ostnud_kliente | keskmine_joinitud | keskmine_sales_ainult | ule_keskmise |
| -------------- | ----------------- | --------------------- | ------------ |
| 2551           | 1028.12           | 1139.96               | 900          |

Tundmatute klientide müük:
| tundmatu_muuk | kogumuuk   | tundmatu_protsent |
| ------------- | ---------- | ----------------- |
| 286446.20     | 2909177.98 | 9.8               |

Tuvastatud klientidest (2551 ostnud klienti) kulutab üle keskmise 900 ehk ligikaudu 35,3%; keskmine müük kliendi kohta on 1028,12 €. Müügid ilma kliendikirjeta (286 446 €) moodustavad 9,8% kogumüügist (2 909 178 €) ja on keskmise arvutusest välja jäetud, et see ei moonduks. Soovitan puuduvad customer_id väärtused müügitabelis üle vaadata, sest ligi kümnendikku käibest ei saa praegu kliendi tasemel analüüsida.

