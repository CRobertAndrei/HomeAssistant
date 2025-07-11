# Casă Inteligentă cu Home Assistant  

## Descriere generală  
Acest proiect reprezintă configurarea unei case inteligente folosind **Home Assistant OS** pe un Raspberry Pi, integrarea de senzori și dispozitive smart, automatizări și asistenți vocali AI personalizați.  

---  

## 1. Instalare și configurare Home Assistant  
- Descărcat imaginea HAOS oficială de pe [home-assistant.io](https://www.home-assistant.io/installation/raspberrypi/)  
- Scris imaginea pe microSD cu **Raspberry Pi Imager**  
- Pornit Raspberry Pi cu cardul introdus  
- Accesat interfața web la `http://homeassistant.local:8123`  
- Setări inițiale:  
  - Creare cont  
  - Locație și fus orar  
  - Conectare la rețea  
  - Activare **Supervisor** pentru Add-on-uri  

---  

## 2. Adăugare dispozitive inteligente  

### Bec RGB Wi-Fi (Philips)  
- Integrat prin **Wiz**  
- Automatizări: aprindere la apus, schimbare culoare, etc.  

### Aer condiționat Wi-Fi  
- Control complet: ON/OFF, temperatură  
- Control prin apeluri folosind **Google Assistant SDK**, folosind dispozitivul din Google Home  

### Senzor temperatură și umiditate 
- Integrare via **Tuya** 
- Date afișate în dashboard  
- Folosit pentru declanșarea automatizărilor  

### Senzor de prezență Aqara FP2  
- Integrare via **Tuya** 
- Automatizare: dacă e mișcare după apus → aprinde becul  
- Comandă vocală: *„Este cineva în cameră?”*  

### Smart Meter Tongou TO-Q-SYS  
- Monitorizează consumul  
- Integrare via **Tuya**  

### Releu TRI160 5V + motor DC  
- Conectat la pini GPIO pe Raspberry Pi  
- Pornire/stingere prin Home Assistant  
- Control vocal și prin automatizări  

### Wake-on-LAN (WOL)  
- Pornirea/oprirea unui PC pe baza MAC address  

---  

## 3. Voice Assistant AI  

### Google Gemini AI (Google Assistant SDK)  
- Configurat cu **Google Cloud Project** + API Key  
- Control complet vocal al casei  
- Integrare cu ElevenLabs pentru voce naturală  

### DeepSeek AI + ElevenLabs  
- Integrare cu **OpenAI** + **Extended OpenAI Conversation**  
- Integrare cu ElevenLabs pentru voce naturală  
- Control complet vocal al casei  

---  

## 4. Add-ons  

### Add-ons oficiale  

- **n8n**  
  - Instalare și configurare pentru automatizări avansate  
  - Permite crearea flow-urilor de automatizare vizuală direct din Home Assistant  
  - Integrare cu servicii externe prin webhook-uri, API-uri și notificări  

- **File Editor**  
  - Editor de fișiere YAML și alte fișiere de configurare direct în interfața Home Assistant  

- **ESPHome**  
  - Platformă pentru configurarea și programarea dispozitivelor ESP8266/ESP32  
  - Integrare simplă cu Home Assistant pentru senzori și actuatori custom  

### Add-ons prin HACS  

- **HACS (Home Assistant Community Store)**  
  - Manager de pachete pentru componente custom, teme și integrări comunitare  

- **Environment Variables**  
  - Gestionare variabile de mediu pentru configurații personalizate  

- **Extended OpenAI Conversation**  
  - Add-on pentru extinderea conversațiilor AI integrate în Home Assistant  

- **Raspberry Pi GPIO**  
  - Control și monitorizare a pinilor GPIO direct din Home Assistant  

---  

## 5. Automatizări  

### Automatizări implementate:  
- Control automat pentru aparatul de aer condiționat în funcție de temperatura ambientală  
- Aprinderea luminii pe baza senzorului de prezență și a apusului  
- Pornirea motorului DC la o anumită oră dacă temperatura este peste un prag  
- Automatizare avansată: pornirea motorului la intervale, cu timp de cooldown  
- Notificări și acțiuni bazate pe consumul energetic monitorizat  

> Exemplele YAML sunt incluse separat în fișierul [automations.yaml](./homeassistant/automations.yaml) din acest repository.


---  

## 6. Automatizări avansate cu n8n  
- Instalare și configurare Add-on `n8n` în Home Assistant  
- Creare flow-uri de automatizare prin interfață vizuală  
- Conectare la servicii externe (webhook-uri, API-uri, notificări)  

---  

## 7. Concluzii  
Home Assistant îți oferă libertatea să-ți configurezi casa exact așa cum vrei, cu automatizări personalizate. Cu AI-uri ca Google Gemini sau DeepSeek, controlul vocal devine mai simplu. Automatizările pot fi cât de simple sau complexe vrei tu. Comunitatea este una open-source - găsești soluții la aproape orice. 

---

## Practică de vară - 2025 - Facultatea de Automatică, Calculatoare și Electronică, Craiova

## Proiect realizat de student: Călinoiu Robert-Andrei
