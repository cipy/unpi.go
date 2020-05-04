### Alt cuvânt înainte

Vei putea urma prima parte a cursului de programare în Golang și pe un calculator personal cu Windows OS 7, 8.1 sau 10 - **numai dacă** respecți pașii pregătitori de mai jos. Dar pe parcurs, după primul an de studii cu noi, îți va fi din ce în ce mai greu să ne urmărești, dacă nu ai [unPi](https://start.unpi.ro/spec/) al tău.

Dacă folosești deja Linux OS sau Mac OS X pe calculatorul tău personal, vei ști cum să execuți singur pașii preparatori (de mai jos) necesari pentru Windows OS, pe platforma ta preferată. De asemenea, pentru cunoscători, dacă ai Windows 10 Pro licențiat pentru 64-bit, vei putea [instala Debian Linux din Microsoft Store](https://www.microsoft.com/en-us/p/debian/9msvkqc78pk6) ca Windows Subsystem for Linux (WSL) și menține astfel un sistem mult mai rapid decât cel cu VirtualBox 😎

### Cum pregătesc un calculator personal cu Windows OS pentru cursul de Golang

În primul rând trebuie să ai pe calculatorul tău sistemul de operare Windows versiunea 7, 8.1 sau 10. Windows XP **nu** mai este suportat, deci nu te putem ajuta dacă ai acest vechi sistem de operare. Dacă ai în schimb un Windows 8.1 sau 10 fără licență, te poți înscrie în programul de voluntariat al Asociației unPi pentru Școlari și vei primi o licență gratis câtă vreme ești voluntar și ne ajuti în rolul pe care ți-l alegi.

### Pas cu Pas

Pentru a putea învăța și exersa cursul de Golang cu noi, **trebuie** ca tu să execuți **exact** pașii următori:

- creează un director ("folder") la tine pe calculatorul personal, pe Desktop și numește acest director (să zicem) "unpi"

- descarcă [ultima versiune a sistemului de operare Raspbian Desktop pentru PC](https://www.raspberrypi.org/downloads/raspberry-pi-desktop/) ca fișier **ISO** în directorul "unpi"

- dacă versiunea ta de Windows OS este pentru 32-bit, trebuie să descarci în același director "unpi" [programul de virtualizare VirtualBox](https://download.virtualbox.org/virtualbox/5.2.40/VirtualBox-5.2.40-137108-Win.exe) versiunea 5.2

- **doar** dacă versiunea ta de Windows OS este pentru 64-bit, trebuie să descarci în același director "unpi" [programul de virtualizare VirtualBox](https://download.virtualbox.org/virtualbox/6.0.20/VirtualBox-6.0.20-137117-Win.exe) versiunea 6.0

- instalează acum programul VirtualBox din directorul "unpi" (unde l-ai descărcat mai sus)
- pornește programul VirtualBox nou instalat și creează o mașină virtuală nouă de tip Linux/Debian 32-bit
- atașează acum fișierul **ISO** (Raspbian Desktop pentru PC) ca DVD la mașină ta virtuală nou creată
- pornește noua ta mașină virtuală și continuă configurarea ei precum este descris [aici]

### Ești gata? (te poți întoarce acum la [cursul de programare în Golang](https://go.unpi.ro/))
