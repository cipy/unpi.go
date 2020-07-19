### Alt cuvânt înainte

Vei putea urma prima parte a cursului de programare în Golang și pe un calculator personal cu **Windows OS** - doar dacă urmezi cu **strictețe** pașii pregătitori de mai jos. Dar pe parcurs, după primul an de studii cu noi, îți va fi din ce în ce mai greu să ne urmărești, dacă nu ai [unPi](https://start.unpi.ro/spec/) al tău.

#### înainte de a începe, verifică te rog că Windows OS este **up-to-date** sau instalează **toate** update-urile și repornește-l

### Cum pregătesc un calculator personal cu Windows 10 Pro 64-bit

În primul rând, chiar ai nevoie de un calculator cu sistemul de operare **Windows 10 Pro pe 64 de biți**, licențiat. Acești pași **nu vor funcționa** decât pe varianta de [64 biți](https://support.microsoft.com/en-us/help/15056/windows-32-64-bit-faq). Continuă prin a [instala aplicația Debian Linux din Microsoft Store](https://www.microsoft.com/en-us/p/debian/9msvkqc78pk6). _Nu trebuie neapărat să te autentifici în Microsoft Store, poți chiar închide fereastra de logare._ Odată instalat Debian OS ca Windows Subsystem for Linux (WSL, în termeni tehnici) vei avea un calculator **mult mai rapid** decât cel bazat pe VirtualBox (descris puțin mai jos la Windows OS).

### Pas cu Pas pentru WSL / numai pe Windows 10 Pro 64-bit

- trebuie să activezi WSL(1) în Windows 10,
- pentru asta deschide aplicația PowerShell **ca Administrator** și rulează în ea:

```
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
```

- după ce comanda precedentă se termină de executat, **trebuie** să restartezi Windows 10
- pornește acum [aplicația Debian](https://www.microsoft.com/en-us/p/debian/9msvkqc78pk6) pe care ai instalat-o (mai devreme) din Microsoft Store 
- la pornire aplicația îți va cere un nume de utilizator, folosește: **pi** iar ca parolă, folosește: **raspberry**
- (**nimeni nu se poate conecta** din afara calculatorului tău, chiar dacă știe parola acestui utilizator)
- după ce ai introdus combinația utilizator / parolă, vei vedea un prompt, o linie pe ecran care se termină cu simbolul **$** după care trebuie să tastezi **exact** comenzile de mai jos, apăsand tasta **Enter** după fiecare linie de comandă:

```bash
curl.exe -sL init.unpi.ro -o init.sh
sudo bash init.sh
```

- la ultima comandă (sudo) vei fi întrebat parola pentru utilizatorul **pi**, care este **raspberry**
- așteaptă te rog comenzile de mai sus să-și termine execuția cu textul "spor la studiu" 
- calculatorul tău este acum pregătit pentru [cursul nostru de programare în limbajul Golang](https://go.unpi.ro/)

### Cum pregătesc un calculator personal cu Windows OS 7, 8.1 sau 10

Trebuie să ai pe calculatorul tău personal sistemul de operare Windows versiunea 7, 8.1 sau 10 (**nu** varianta 10 Pro pe 64 biți descrisă mai sus). Windows XP **nu** mai este suportat de Microsoft, deci nu te putem ajuta dacă ai acest vechi sistem de operare. Dacă ai în schimb un Windows 7, 8.1 sau 10 fără licență, te poți înscrie în [programul de voluntariat al Asociației unPi pentru Școlari](https://start.unpi.ro/ong/voluntar/) și vei primi o licență gratis câtă vreme ești voluntar și ne ajuti în rolul pe care ți-l alegi. Atunci când folosești VirtualBox (descris mai jos), calculatorul tău poate funcționa [mult] **mai lent** decât de obicei.

### Pas cu Pas pentru Windows OS

Pentru a putea învăța și exersa cursul de Golang cu noi, **trebuie** ca tu să execuți **exact** pașii următori:

- creează un director ("folder") la tine pe calculatorul personal, pe Desktop și numește acest director (să zicem) "unpi"
- [verifică dacă versiunea ta de Windows OS este pe 32 sau pe 64 biți](https://support.microsoft.com/en-us/help/15056/windows-32-64-bit-faq)
- dacă versiunea ta de Windows OS este pentru 32-bit, trebuie să descarci în același director "unpi" [programul de virtualizare VirtualBox](https://download.virtualbox.org/virtualbox/5.2.44/VirtualBox-5.2.44-139111-Win.exe) versiunea 5.2
- **doar** dacă versiunea ta de Windows OS este pentru 64-bit, trebuie să descarci în același director "unpi" [programul de virtualizare VirtualBox](https://download.virtualbox.org/virtualbox/6.1.12/VirtualBox-6.1.12-139181-Win.exe) versiunea 6.1
- instalează acum programul VirtualBox din directorul "unpi" (unde l-ai descărcat mai sus)

#### [continuă cu: mai dificil, sau sari direct la: mai ușor]
- descarcă [ultima versiune a sistemului de operare Raspbian Desktop pentru PC](https://www.raspberrypi.org/downloads/raspberry-pi-desktop/) ca fișier **ISO** în directorul "unpi"
- pornește programul VirtualBox nou instalat și creează o mașină virtuală nouă de tip Linux/Debian 32-bit
- folosește fișierul **ISO** (Raspbian Desktop pentru PC) ca DVD virtual la mașina ta virtuală nou creată
- pornește noua ta mașină virtuală, bootează de pe DVD-ul virtual și continuă instalarea și configurarea ei
- după instalarea completă, pornește aplicația Terminal 📺 din Raspbian Desktop, și pe linia de pe ecran care se termină cu simbolul **$** trebuie să tastezi **exact** comenzile de mai jos, apăsând tasta **Enter** după fiecare linie de comandă:

```bash
wget init.unpi.ro
bash index.html
```

#### [continuă cu: mai ușor]
- înainte de a începe, **asigură-te că ai cel puțin 10 GB liberi** pe discul PC-ului tău
- descarcă și instalează [ultima versiune a programului 7-Zip](https://www.7-zip.org/download.html) pentru sistemul tău de operare
- descarcă și instalează [ultima versiune a programului uTorrent](https://www.utorrent.com/downloads/complete/track/stable/os/win) pentru sistemul tău de operare
- descarcă fișierul nostru [.torrent](files/Raspbian_Desktop_de_la_unPi.torrent) și deschide-l în aplicația uTorrent
- astfel, aplicația uTorrent îți va aduce din Internet o mașină virtuală de tip VirtualBox 32-bit, deja comprimată cu 7-Zip (arhivă este numită: Raspi4unPi.7z și are aproximativ **2 GB**) pe care noi am configurat-o deja complet precum unPi
- după ce uTorrent îți aduce arhiva .7z, trebuie să o dezarhivezi cu programul 7-Zip dând dublu click pe arhivă; odată dezarhivată, mașina virtuală (din directorul: Raspbian Desktop de la unPi, are aproximativ **8 GB**, dar va mai crește în timp, în functie de utilizare) este vizibilă ca o iconiță de forma unui 'cub albastru'
- dai dublu click pe această iconiță 'cub albastru' și mașina virtuală Raspbian Desktop va porni în VirtualBox
- poți șterge arhiva Raspi4unPi.7z **doar după ce** Raspbian Desktop a pornit complet (la rezoluție 1024x768)

#### Performanța mașinii virtuale Raspbian Desktop va depinde de **cât de rapid** este deja calculatorul tău personal.

### Cum pregătesc un calculator personal cu Linux OS / Mac OS X

Dacă folosești deja Linux OS sau Mac OS X pe calculatorul tău personal, vei ști cum să execuți singur pașii preparatori pe care i-am descris mai sus pentru Windows OS (nu cei din varianta 10 Pro 64-bit), dar folosind programul VirtualBox/VMware/Fusion pentru a instala [sistemului de operare Raspbian Desktop pentru PC](https://www.raspberrypi.org/downloads/raspberry-pi-desktop/) pe platforma ta preferată, ca o nouă mașină virtuală. Pentru a avea un sistem _mult_ mai performant, îți recomandăm să instalezi Raspbian Desktop pentru PC pe un disk separat, sau pe un memory stick și să bootezi direct în el doar pentru lecțiile de programare în Golang. În felul acesta te vei putea izola de distracțiile existente deja pe calculatorul tău și concentra mai bine să înveți programare.

**Doar** dacă folosești deja _Linux Debian OS_ vei putea folosi direct următoarele comenzi în aplicația Terminal 📺

```bash
wget https://infra.unpi.ro/init.sh -O init.sh
sudo bash init.sh
```

### Cum pregătesc un calculator personal generic ("mă descurc [și] singur")
- instalează [versiunea Golang **corectă**](https://golang.org/dl/#stable) pentru sistemul tău de operare (folosind .msi pentru Windows)
- instalează [Visual Studio Code](https://code.visualstudio.com/download) (un editor gratis pentru programatori) pentru sistemul tău de operare
- instalează [extensia Go pentru Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=golang.go) ca să poți programa în limbajul Golang

### Ești gata? (te poți întoarce acum la [cursul de programare în Golang](https://go.unpi.ro/))
