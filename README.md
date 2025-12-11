# Sistem Simplu de Ticketing IT

Documentația proiectului pentru o aplicație desktop de ticketing IT. Include cerințele proiectului, diagrame UML și un prototip simplu pentru fluxul unui ticket.

## SRS
Document cu cerințele aplicației:
- Funcționale: creare ticket, vizualizare, actualizare status, închidere ticket.
- Non-funcționale: notificare prin email.

## UML
Diagrame PlantUML incluse:
- Use Case – Utilizator și Tehnician.
- Activity – Rezolvarea unui ticket.

## Prototip
Mini-card realizat în Figma, prezentând stadiul și fluxul unui ticket:
New → In Progress → Resolved.
[Figma Prototype](https://www.figma.com/design/buTQPqP9k0A0zsYs0Yucng/Untitled?node-id=0-1&t=0NNDkDlo6SPOX6N5-1)

## Modulele aplicației

# Business Logic (BL)
Gestionarea regulilor aplicației: validare date, procesarea ticketelor (creare, editare, filtrare, schimbare status), generare ID-uri și legătura dintre UI și Data Layer.

# UI Layer
Interfața vizuală: ferestre, formulare, butoane, liste. Preia acțiunile utilizatorului și afișează datele furnizate de BL. Nu conține logică de business.

# Data Layer (DAL)
Stocarea datelor în SQLite/fișiere. Operații CRUD, încărcare la pornire, salvare la închidere, serializare și gestionarea erorilor. Nu implementează logică de procesare.

# Auxiliary Layer
Funcții utilitare și servicii: logging, configurări, generare ID-uri simple, parsări, excepții personalizate și alte ajutoare folosite de toate modulele.
