# google-maps-reviews-summarized

Technische Anforderungen

Backend:
    API-Integration:
    Zugriff auf Google Maps Places API, um Rezensionen eines Ortes abzurufen.
    Wenn damit Schwierigkeiten oder Begrenzungen vorkommt, dann Nutzung von Web-Scraping-Methoden (vllt Beatiful Soup Library in Python) damit Rezensionen erreicht werden. 
    Nutzung von ChatGPT API mit einem modifiziertem Command oder eines Hugging Face-Modells für Zusammenfassungen.

Verarbeitungsschritte:
    Abruf und Zusammenfassung Rezensionen pro Anfrage.
    Keine komplexe Datenverarbeitung: Rückgabe der von der ChatGPT-API oder dem Hugging Face-Modell ausgegebenen Antwort mit den erforderlichen Anpassungen.

Frontend:
    Benutzeroberfläche:
    Eingabefeld für Ortssuche (z. B. Eingabe des Namens oder der Adresse). Man kann auch von Karte von Google Maps den gezielten Ort auswählen.
    Anzeige der zusammengefassten Rezensionen in einer einfachen Textbox.

Technologie:
    Backend: Flask oder FastAPI für einfache API-Endpunkte.
    Frontend: Minimalistisch mit HTML/CSS und optional JavaScript. 
    Hosting: Lokales Hosting (z. B. mit Flask-Server) oder Deployment auf Heroku.

Implementierung
    Schritte:
    API-Schlüssel für Google Maps und OpenAI/Hugging Face generieren.
    Einfacher Flask-Server mit Endpunkt:
        Anfrage: Ort
        Antwort: Zusammenfassung
    Frontend: Einfaches HTML-Formular zur Eingabe und Ausgabe.
    Integration: Verbindung von Frontend und Backend über Fetch- oder Axios-Anfragen.
    Tests: Prüfung mit einigen, bekannten Orten.