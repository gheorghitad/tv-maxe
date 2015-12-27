# Introducere #

Programul TV-MAXE oferă o interfaţă grafică pentru configurarea acestuia. Aceasta poate fi accesată prin meniul TV-MAXE `->` Preferinţe. Setările de configurare sunt stocate în fişierul `~/.tvmaxe`

# Fereastra de configurare TV-MAXE #

## Tab-ul General ##
![http://i.imgur.com/8XmDR.jpg](http://i.imgur.com/8XmDR.jpg)

Tab-ul "General" include setările privind player-ul video folosit pentru redarea stream-urilor şi setările pentru porturile folosite de SopCast.

Puteţi utiliza un player intern sau unul extern pentru redarea clipurilor video. Utilizarea unui player intern presupune faptul că imaginea video va fi afişată în cadrul aplicaţiei TV-MAXE care va putea, de asemenea, să controleze redarea fluxului. Momentan TV-MAXE suportă două playere ca backend: VLC şi MPlayer. Pentru utilizatorul obişnuit ar trebui să nu existe nicio diferenţă în utilizarea oricărui din cele două playere, cu excepţia faptului că metadatele transmise de posturile de radio nu pot fi afişate atunci când este utilizat MPlayer.
Definirea unui player extern pentru redarea stream-urilor se face bifând opţiunea corespunzătoare şi setând calea spre executabilul acestuia. Avantajele utilizării unui player extern sunt diversitatea opţiunilor puse la dispoziţia utilizatorului de către acesta, spre deosebire de TV-MAXE care dispune de un set limitat de opţiuni. Ţineţi cont că TV-MAXE va adăuga tot timpul adresa stream-ului după şirul de caractere oferit ca setare pentru executabilul player-ului video; în concluzie, dacă player-ul dumneavoastră video necesită adăugarea unui flag pentru a-i transmite să redea un URL, puteţi să îl adăugaţi în căsuţa de editare a comenzii de iniţializare a player-ului. De exemplu, presupunând că player-ul dumneavoastră necesită parametrul -u pentru a anunţa că urmează un URL, în căsuţa de editare veţi adăuga:
```
/usr/bin/player -u
```
TV-MAXE va adăuga automat URL-ul după acest şir de caractere.

La conectarea prin SopCast TV-MAXE va alege aleatoriu două porturi prin care se vor creea conexiuni, unul de intrare şi altul de ieşire. Deşi majoritatea utilizatorilor nu vor fi nevoiţi să modifice această setare, cei ce folosesc un firewall ar trebui să activeze alocarea statică a porturilor şi să completeze cu două porturi pe care să le deblocheze apoi din setările firewall-ului pe care îl folosesc. Numărul porturilor poate fi cuprins între 3000 şi 65535. Portul de intrare va fi folosit pentru comunicarea prin protocolul SopCast, iar pe portul de ieşire va fi pornit un server HTTP care va oferi stream-ul video preluat de pe internet. Adresa stream-ului este http://localhost:port/tv.asf, unde **port** este portul de ieşire setat în configurări.

## Tab-ul Telecomandă ##
![http://i.imgur.com/bc3EV.jpg](http://i.imgur.com/bc3EV.jpg)

Dacă aveţi o telecomandă compatibilă LIRC şi programul _irw_ puteţi să o folosiţi pentru controlul aplicaţiei TV-MAXE. TV-MAXE este configurat implicit să funcţioneze cu telecomenzile Compro VideoMate PVR (deoarece e singura telecomandă avută la dispoziţie pentru teste) însă, cu condiţia remapării butoanelor din setările TV-MAXE, ar trebui ca să funcţioneze cu orice altă telecomandă. Pentru a remapa un buton, apăsaţi pe butonul din dreptul acţiunii căreia vreţi să îi atribuiţi un buton de pe telecomandă iar, când apare fereastra ce vă cere să alocaţi o tastă acţiunii respective, apăsaţi butonul de pe telecomandă dorit.

## Tab-ul Abonamente ##
![http://i.imgur.com/31ngE.jpg](http://i.imgur.com/31ngE.jpg)

_Această funcţie este disponibilă începând cu versiunea 0.5 a aplicaţiei_

Dacă doriţi să vă extindeţi lista de canale, puteţi să vă abonaţi la diverse liste creeate de persoane terţe. Pentru acest lucru accesaţi fereastra de configurare a programului, tab-ul Abonamente. Apăsaţi pe "Adăugare" pentru a adăuga o listă nouă după care introduceţi numele cu care aceasta va apare în program şi adresa către fişierul-listă. Asiguraţi-vă că abonamentul este activ (bifând căsuţa din partea stângă a denumirii abonamentului) după care închideţi fereastra de configurare, moment în care lista se va actualiza şi vor apare noile canale TV.