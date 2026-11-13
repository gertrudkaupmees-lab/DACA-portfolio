# Nädal 1: SQL Basics
## Grupitöö - Customers (B)
Grupitöö raames analüüsisin detailsemalt klienditabeli (customers) infot ja väljavõtte kvaliteeti.  
Eesmärk oli tuvastada ebakõlad ja puudused andmetes kasutades omandatud teadmisi SQL andmepäringute teostamiseks. Peamiselt kasutatud päringud SELECT, COUNT; ORDER BY, FROM, WHERE, LIMIT ja AS. 

**Põhiandmed**- 3150 rida, 9 veergu, peamine leid duplikaadist klientide read emailide alusel 130 tk. Puudulike andmeid emailide ja loyalty tasemete osas. 

**Analüüsi tulemused:**
Klientide arv (2): kokku 3150, kuid sealhlgas potensiaalseid duplikaate 130
Linnad (4): Haapsalu, Jõhvi, Kuressaare, Narva, Paide, Pärnu, Rakvere, Tallinn, Tartu, Valga, Viljandi, Võru.
Registreerimise vahemik (6): Vanim 2.01.2020, uusim 27.02.2025
Puudulikud sisendid: emailid – 380, klientide tasemed 1260
Peamine leid: Andmetes leidub nii puudulike sisendeid, kui ka duplikaate – seega ei ole andmete koguminsel süsteemis kontrole, mis takistaksid nende tekkimist.

Vastav töö on koodi näol nähtav failis (https://github.com/gertrudkaupmees-lab/DACA-portfolio/blob/main/week-1/GT%20week%201%20customers%20tabel.sql)

**Äriline mõju ja edasine soovitus: 
Teostada detailsem süvaanalüüs ja andmete korrastamine, et vältida topelt infot ja mõelda läbi milline on reaalselt vaja minev info raportite raames. Andmed on sisendina ilma ühtse standardita loodud ning on olnud võimalik sisestada duplikaate või jätta sisend täitmata, seega andmete kogumise protsess vajaks täiendamist. 

Olemasolevad andmed vajavad oluliselt korrastamist, enne nende kasutusele võttu. Ärilisi otsusi antud andmete põhjal ei ole soovitatav teha, kuna tulemused oleksid moonutatud ja ei oleks tõesed.

Kogu grupitöö kokkuvõte nähtav xxx

## Iseseisev töö

