# Speed-test iperf3
Am creat o aplicație completă de testare a vitezei I/O pe rețea și disc, care imită funcționalitatea iperf3 și fio. Iată caracteristicile cheie:

## Testarea rețelei (caracteristici similare iperf3):
- **Moduri client/server** - Poate acționa fie ca client, fie ca server
- **Protocoale multiple** - Suport TCP, UDP și SCTP
- **Tipuri de testare** - Normal (încărcare), Invers (descărcare) și Bidirecțional
- **Fluxuri paralele** - Suport pentru conexiuni simultane multiple
- **Opțiuni avansate**:
   - Configurarea dimensiunii bufferului
   - Reglarea dimensiunii ferestrei
   - Setări MSS (Dimensiunea maximă a segmentului)
   - Limitarea lățimii de bandă
   - Opțiune fără întârziere (algoritmul lui Nagle)
   - Mod zero-copy

## Testarea I/O pe disc (caracteristici similare fio):
- **Modele de testare**:
   - Citire/Scriere secvențială
   - Citire/Scriere aleatorie
   - Citire/Scriere aleatorie mixtă
- **Parametri configurabili**:
   - Dimensiunea fișierului
   - Dimensiunea blocului (4KB până la 1MB)
   - Adâncimea I/O (adâncimea cozii)
   - Numărul de joburi paralele
- **Opțiuni avansate**:
   - Motoare I/O diferite (sincronizare, asincronizare, libaio, posixaio)
   - Mod I/O direct (ocolind memoria cache)
   - Verificare a integrității datelor
   - Durată de execuție personalizată

 ## Caracteristici suplimentare:
- **Afișarea rezultatelor în timp real** cu bare de progres animate
- **Urmărirea istoricului testelor** cu informații detaliate despre sesiune
- **Analiză a performanței** cu diagrame vizuale
- **Funcționalitate de export** pentru a salva rezultatele ca JSON
- **Interfață de utilizator modernă, responsivă** cu design glassmorphic
- **Temă întunecată** cu accente neon pentru o vizibilitate mai bună

 ## Note importante:
1. Aceasta este o **simulare frontend** care demonstrează interfața de utilizator și fluxul de lucru. Testarea reală a rețelei și a discului ar necesita implementare backend cu acces la nivel de sistem.

2. Rezultatele simulate prezintă intervale realiste:

- Debit de rețea: 100-1000 Mbps

- Viteze secvențiale pe disc: 400-1000 MB/s

- Viteze aleatorii pe disc: 50-300 MB/s

- Calcule de latență și IOPS bazate pe parametrii de testare

3. Pentru a implementa funcționalități reale, veți avea nevoie de:

- Server backend (Node.js, Python etc.) cu permisiuni de sistem

- Conexiuni WebSocket pentru streaming de date în timp real

- Legături native sau apeluri de sistem pentru operațiuni reale pe rețea și disc

- Considerații de securitate pentru operațiunile în modul server

Aplicația oferă un flux de lucru complet de testare similar cu iperf3 și fio, cu o interfață intuitivă pentru configurarea și rularea testelor de performanță.
