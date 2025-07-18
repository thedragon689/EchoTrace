# EchoTrace
**EchoTrace** - Scansiona il web con stile TRON! 🚀 

# 🕵️‍♂️ EchoTrace - Web Scanner OSINT

**EchoTrace** è un avanzato scanner web per OSINT (Open Source Intelligence) con interfaccia TRON-themed e capacità di rilevamento vulnerabilità avanzate.

![EchoTrace Logo](https://img.shields.io/badge/EchoTrace-Web%20Scanner-00ffff?style=for-the-badge&logo=security&logoColor=black)

## 📋 Indice

- [Caratteristiche](#-caratteristiche)
- [Tecnologie Utilizzate](#-tecnologie-utilizzate)
- [Installazione](#-installazione)
- [Utilizzo](#-utilizzo)
- [Funzionalità](#-funzionalità)
- [Modifiche Recenti](#-modifiche-recenti)
- [Struttura del Progetto](#-struttura-del-progetto)
- [API Endpoints](#-api-endpoints)
- [Contribuire](#-contribuire)
- [Licenza](#-licenza)

## ✨ Caratteristiche

### 🔍 **Scansione Avanzata**
- **Rilevamento IP e Hostname**: Analisi completa della rete
- **Port Scanning**: Scoperta porte aperte e servizi attivi
- **Vulnerabilità**: Rilevamento XSS, SQL Injection e altre vulnerabilità
- **Security Headers**: Analisi degli header di sicurezza
- **Subdomain Discovery**: Scoperta subdomain in stile Shodan

### 📊 **Visualizzazione Dati**
- **Grafici Interattivi**: Chart.js per visualizzazione dati
- **Dashboard Responsive**: Layout adattivo per tutti i dispositivi
- **TRON Theme**: Interfaccia neon con effetti luminosi
- **Timeline Scansioni**: Storico delle scansioni effettuate

### 🛡️ **Sicurezza**
- **XSS Detection**: Rilevamento Cross-Site Scripting
- **SQL Injection**: Analisi vulnerabilità database
- **Security Headers**: Verifica header di protezione
- **SSL/TLS Analysis**: Analisi certificati di sicurezza

## 🛠️ Tecnologie Utilizzate

### **Backend**
- **Python 3.8+**: Linguaggio principale
- **HTTP Server**: Server web built-in Python
- **Socket Programming**: Per port scanning
- **SSL/TLS**: Analisi certificati
- **Regex**: Pattern matching avanzato

### **Frontend**
- **HTML5**: Struttura semantica
- **CSS3**: Styling avanzato con animazioni
- **JavaScript ES6+**: Logica client-side
- **Chart.js**: Visualizzazione grafici
- **Responsive Design**: Mobile-first approach

### **Librerie Python**
- `urllib`: Richieste HTTP
- `socket`: Network operations
- `ssl`: SSL/TLS analysis
- `re`: Regular expressions
- `json`: Data serialization
- `threading`: Concurrent operations

### **Librerie JavaScript**
- **Chart.js**: Grafici interattivi
- **Custom CSS**: TRON theme styling
- **Vanilla JS**: DOM manipulation

## 🚀 Installazione

### **Prerequisiti**
```bash
# Python 3.8 o superiore
python3 --version

# pip (gestore pacchetti Python)
pip3 --version
```

### **1. Clona il Repository**
```bash
git clone https://github.com/thedragon689/EchoTrace.git
cd echotrace
```

### **2. Crea Ambiente Virtuale**
```bash
# Crea ambiente virtuale
python3 -m venv venv

# Attiva ambiente virtuale
# Linux/macOS:
source venv/bin/activate
# Windows:
venv\Scripts\activate
```

### **3. Installa Dipendenze**
```bash
# Installa dipendenze Python
pip install -r requirements.txt

# Oppure installa manualmente:
pip install requests beautifulsoup4
```

### **4. Configurazione**
```bash
# Crea cartella immagini (se non esiste)
mkdir -p immagini

# Aggiungi immagini di sfondo nella cartella immagini/
# Il file verrà utilizzato come background della dashboard
```

### **5. Avvia l'Applicazione**
```bash
# Avvia il server
python simple_server.py

# Oppure usa lo script di avvio
chmod +x start.sh
./start.sh
```

## 📖 Utilizzo

### **Avvio del Server**
```bash
python simple_server.py
```

Il server sarà disponibile su: **http://localhost:3000**

### **Interfaccia Web**
1. **Apri il browser** e vai su `http://localhost:3000`
2. **Inserisci l'URL** da analizzare nella sidebar
3. **Clicca "SCANSIONA"** per avviare l'analisi
4. **Visualizza i risultati** nella dashboard

### **Esempi di URL da Scansionare**
```bash
# Siti web comuni
https://www.example.com
https://google.com
https://github.com

# Siti con vulnerabilità note (per test)
http://testphp.vulnweb.com
http://testasp.vulnweb.com
```

## 🔧 Funzionalità

### **1. Analisi di Rete**
- **IP Address**: Risoluzione DNS
- **Hostname**: Estrazione dominio
- **Porte**: Scansione porte comuni (21, 22, 23, 25, 53, 80, 443, 8080, 8443)
- **Protocollo**: HTTP/HTTPS detection
- **Response Time**: Tempo di risposta

### **2. Rilevamento Vulnerabilità**
- **XSS (Cross-Site Scripting)**: Pattern matching avanzato
- **SQL Injection**: Analisi parametri e form
- **Security Headers**: Verifica header di protezione
- **SSL/TLS**: Analisi certificati e configurazione

### **3. OSINT e Intelligence**
- **Email Extraction**: Estrazione indirizzi email
- **Domain Discovery**: Scoperta domini correlati
- **Social Media**: Rilevamento profili social
- **Technology Detection**: Identificazione tecnologie utilizzate
- **Image Analysis**: Estrazione e analisi immagini

### **4. Visualizzazione Dati**
- **Grafici Vulnerabilità**: Distribuzione per severità
- **Grafici Porte**: Porte aperte e servizi
- **Grafici Security Headers**: Header presenti/mancanti
- **Grafici Insights**: Distribuzione categorie dati
- **Grafici DNS**: Record DNS e configurazione
- **Grafici Sicurezza DNS**: DNSSEC, SPF, DKIM, DMARC
- **Grafici Domini Correlati**: Domini correlati per TLD
- **Grafici Timeline WHOIS**: Timeline del dominio
- **Dashboard Trasparente**: Sfondo trasparente con effetti sci-fi
- **Responsive Design**: Layout adattivo per tutti i dispositivi

## 🔄 Modifiche Recenti

### **v2.1.0 - Dashboard Trasparente e Grafici Migliorati**
- ✅ **Dashboard Trasparente**: Sfondo completamente trasparente per mostrare effetti di sfondo
- ✅ **Grafici Sempre Visibili**: Tutti gli 8 grafici vengono sempre creati, anche senza dati
- ✅ **Messaggi Informativi**: Grafici vuoti mostrano messaggi informativi invece di non essere visualizzati
- ✅ **Gestione Errori**: Try-catch globale per la creazione dei grafici con messaggi di errore
- ✅ **Logging Migliorato**: Console.log dettagliati per debugging e monitoraggio
- ✅ **Controlli Robusti**: Gestione migliorata di dati null/undefined
- ✅ **Responsive Design**: Layout ottimizzato per dispositivi mobili e desktop

### **Grafici Disponibili**
1. **Vulnerabilità per Severità** - Distribuzione vulnerabilità (Alta/Media/Bassa)
2. **Porte Aperte** - Visualizzazione porte scoperte e servizi
3. **Security Headers** - Stato degli header di sicurezza (Presenti/Mancanti)
4. **Distribuzione Insights** - Categorie di insights trovati
5. **Record DNS** - Distribuzione record DNS (A, MX, NS, CNAME, TXT, SRV)
6. **Sicurezza DNS** - Stato sicurezza DNS (DNSSEC, SPF, DKIM, DMARC)
7. **Domini Correlati** - Domini correlati raggruppati per TLD
8. **Timeline WHOIS** - Timeline del dominio (Creazione/Scadenza/Aggiornamento)

### **Miglioramenti Tecnici**
- **CSS Variables**: Sistema di variabili CSS per personalizzazione
- **Media Queries**: Breakpoint responsive per tutti i dispositivi
- **Animazioni**: Effetti di transizione e animazioni fluide
- **Accessibilità**: Miglioramenti per screen reader e navigazione da tastiera

## 📁 Struttura del Progetto

```
echotrace/
├── 📄 README.md                 # Documentazione
├── 🐍 simple_server.py          # Server principale (OSINT avanzato)
├── 🐍 server.py                 # Server Flask (base)
├── 🎨 styles.css                # Stili CSS TRON theme
├── ⚡ script.js                 # Logica frontend e grafici
├── 🌐 index.html                # Interfaccia principale
├── 📦 package.json              # Dipendenze Node.js
├── 🚀 start.sh                  # Script di avvio
├── 📁 immagini/                 # Immagini di sfondo
│   └── Copilot_20250716_115729.png
├── 📁 components/               # Componenti Vue.js
│   ├── 📁 frontend/
│   └── 📁 views/
├── 📁 frontend/                 # Frontend Vue.js
└── 📁 backend/                  # Backend Node.js
```

## 🔌 API Endpoints

### **GET /api/scan**
Scansiona un URL e restituisce dati OSINT completi.

**Parametri:**
- `url` (string, required): URL da analizzare

**Risposta:**
```json
{
  "url": "https://example.com",
  "hostname": "example.com",
  "ip_address": "93.184.216.34",
  "port": 443,
  "protocol": "https",
  "server_info": "nginx/1.19.0",
  "response_time_ms": 245.67,
  "open_ports": [
    {"port": 80, "service": "HTTP"},
    {"port": 443, "service": "HTTPS"}
  ],
  "vulnerabilities": [
    {
      "type": "XSS",
      "severity": "Alta",
      "description": "Cross-Site Scripting rilevato",
      "recommendation": "Sanitizzare input utente"
    }
  ],
  "security_headers": {
    "X-Frame-Options": "present",
    "X-Content-Type-Options": "missing"
  },
  "subdomains": [
    {
      "subdomain": "www",
      "full_domain": "www.example.com",
      "type": "Standard"
    }
  ],
  "additional_insights": [
    {
      "category": "Email",
      "type": "Email Addresses",
      "value": "contact@example.com",
      "description": "Indirizzo email trovato"
    }
  ],
  "titles": ["Homepage", "About Us"],
  "scan_timestamp": "2025-07-16 12:00:00"
}
```

## 🎨 Personalizzazione

### **Modifica Tema**
```css
/* styles.css - Variabili CSS personalizzabili */
:root {
  --tron-blue: #00ffff;      /* Colore principale */
  --tron-orange: #ff6b35;    /* Colore accent */
  --tron-dark: #0a0a0a;      /* Sfondo scuro */
  --sidebar-width: 320px;    /* Larghezza sidebar */
}
```

### **Aggiungere Nuove Vulnerabilità**
```python
# simple_server.py - Aggiungere pattern di rilevamento
def scan_vulnerabilities(self, hostname, port, protocol, html_content, security_headers):
    vulnerabilities = []
    
    # Aggiungi nuovo pattern qui
    if re.search(r'pattern_vulnerabilita', html_content, re.IGNORECASE):
        vulnerabilities.append({
            'type': 'Nuova Vulnerabilità',
            'severity': 'Alta',
            'description': 'Descrizione vulnerabilità',
            'recommendation': 'Raccomandazione di fix'
        })
    
    return vulnerabilities
```

### **Personalizzare Grafici**
```javascript
// script.js - Modifica configurazione grafici
function createVulnerabilityChart(vulnerabilities) {
    // Personalizza colori, dimensioni, animazioni
    new Chart(ctx, {
        type: 'doughnut',
        options: {
            // Configurazioni personalizzate
        }
    });
}
```

## 🐛 Risoluzione Problemi

### **Porta 3000 Occupata**
```bash
# Trova processo che usa la porta
lsof -i :3000

# Termina processo
kill -9 <PID>

# Oppure usa porta diversa
python simple_server.py --port 3001
```

### **Errori di Connessione**
```bash
# Verifica firewall
sudo ufw status

# Abilita porta se necessario
sudo ufw allow 3000
```

### **Dipendenze Mancanti**
```bash
# Reinstalla dipendenze
pip install --upgrade -r requirements.txt

# Verifica versione Python
python3 --version
```

## 🤝 Contribuire

1. **Fork** il progetto
2. **Crea** un branch per la feature (`git checkout -b feature/AmazingFeature`)
3. **Commit** le modifiche (`git commit -m 'Add AmazingFeature'`)
4. **Push** al branch (`git push origin feature/AmazingFeature`)
5. **Apri** una Pull Request

### **Guidelines per Contributi**
- Segui il coding style esistente
- Aggiungi test per nuove funzionalità
- Aggiorna la documentazione
- Mantieni la compatibilità con Python 3.8+

# Linee guida per i contributi

Grazie per il tuo interesse in EchoTrace! Questo progetto è a scopo studentesco e non è destinato all'uso commerciale o professionale.

## Come contribuire

- Forka il repository
- Crea una branch (`git checkout -b feature-nome`)
- Fai commit chiari e descrittivi
- Apri una pull request

## Note legali

EchoTrace è fornito "così com'è", senza garanzie. Qualsiasi uso improprio, investigativo o legale è a rischio dell'utente. L'autore non è responsabile per eventuali conseguenze derivanti dall'uso del software.

## 📚 Disclaimer

EchoTrace è un progetto a scopo **studentesco e didattico**. Non è destinato all'uso professionale, investigativo o commerciale.  
Qualsiasi utilizzo improprio, legale o operativo è a **proprio rischio**. L'autore declina ogni responsabilità per danni diretti o indiretti derivanti dall'uso del software.

## 📄 Licenza

Questo progetto è rilasciato sotto licenza **GNU GPL v3**. Vedi il file `LICENSE` per i dettagli.

## 🙏 Ringraziamenti

- **Chart.js** per la visualizzazione grafici
- **TRON Legacy** per l'ispirazione del design
- **Shodan** per l'ispirazione delle funzionalità OSINT
- **OWASP** per le linee guida di sicurezza

## 📞 Supporto

- **Issues**: [GitHub Issues](https://github.com/
thedragon689 /echotrace/issues)
- **Email**: webdevel73@.com
- **Documentazione**: [Wiki](https://github.com/
thedragon689 /echotrace/wiki)

---

**EchoTrace** - Scansiona il web con stile TRON! 🚀 
