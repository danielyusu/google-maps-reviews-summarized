# Google Maps Reviews Summarized

## Technische Anforderungen

### Backend

**API-Integration:**
- Zugriff auf Google Maps Places API, um Rezensionen eines Ortes abzurufen.
- Bei Schwierigkeiten oder Begrenzungen: Nutzung von Web-Scraping-Methoden (z.B. Beautiful Soup Library in Python) um Rezensionen zu erreichen.
- Nutzung von ChatGPT API mit einem modifizierten Command oder eines Hugging Face-Modells für Zusammenfassungen.

**Verarbeitungsschritte:**
- Abruf und Zusammenfassung der Rezensionen pro Anfrage.
- Keine komplexe Datenverarbeitung: Rückgabe der von der ChatGPT-API oder dem Hugging Face-Modell ausgegebenen Antwort mit den erforderlichen Anpassungen.

### Frontend

**Benutzeroberfläche:**
- Eingabefeld für Ortssuche (z.B. Eingabe des Namens oder der Adresse). Alternativ kann der gezielte Ort von der Google Maps Karte ausgewählt werden.
- Anzeige der zusammengefassten Rezensionen in einer einfachen Textbox.

**Technologie:**
- Backend: Flask oder FastAPI für einfache API-Endpunkte.
- Frontend: Minimalistisch mit HTML/CSS und optional JavaScript.
- Hosting: Lokales Hosting (z.B. mit Flask-Server) oder Deployment auf Heroku.

## Implementierung

**Schritte:**
1. API-Schlüssel für Google Maps und OpenAI/Hugging Face generieren.
2. Einfacher Flask-Server mit Endpunkt:
    - Anfrage: Ort
    - Antwort: Zusammenfassung
3. Frontend: Einfaches HTML-Formular zur Eingabe und Ausgabe.
4. Integration: Verbindung von Frontend und Backend über Fetch- oder Axios-Anfragen.
5. Tests: Prüfung mit einigen bekannten Orten.