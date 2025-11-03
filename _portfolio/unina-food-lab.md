---
title: "UninaFoodLab (Gestionale Corsi di Cucina)"
excerpt: "Applicazione gestionale full-stack (Java Swing & PostgreSQL) per un laboratorio di cucina."
date: 2024-06-01
last_modified_at: 2025-01-10
header:
  teaser: "/assets/images/teasers/java-db.png"
tags:
  - Java
  - Java Swing
  - JDBC
  - PostgreSQL
  - SQL
  - Progettazione DB
  - UML
  - Progetto Universitario
toc: true
classes: wide
---

[Codice su GitHub](https://github.com/kiyx/uninafoodlab){: .btn .btn--primary .btn--small }
[Documentazione (PDF)](https://github.com/kiyx/uninafoodlab#readme){: .btn .btn--success .btn--small }

`UninaFoodLab` è un'applicazione gestionale completa sviluppata per il corso di **Basi di Dati e Object Orientation (OOBD)**. Il sistema gestisce le operazioni di un laboratorio di cucina fittizio, dalla gestione dei corsi e degli chef, fino alla creazione di report mensili.

## 1. Il Database (Backend)
È stato progettato e implementato un database relazionale in **PostgreSQL** per gestire tutta la logica di business.
* **Progettazione:** Creazione di diagrammi ER e UML per definire la struttura dei dati e le relazioni.
* **Logica Avanzata:** Utilizzo di trigger, funzioni e procedure (PL/pgSQL) per garantire l'integrità dei dati e automatizzare compiti complessi (es. calcolo dei report).
* **Script:** Creazione di script SQL per la creazione delle tabelle, popolamento e query complesse.

## 2. L'Applicazione Desktop (Frontend)

È stata sviluppata un'applicazione desktop in **Java** per interagire con il database.
* **Interfaccia Grafica:** Utilizzo della libreria **Java Swing** per creare un'interfaccia utente (GUI) intuitiva.
* **Logica Applicativa:** Sviluppo di un'architettura a 3 livelli (Boundary, Controller, DAO) per separare la presentazione, la logica di business e l'accesso ai dati.
* **Connessione:** Utilizzo di **JDBC** (Java Database Connectivity) per far comunicare l'applicazione Java con il database PostgreSQL.

### Funzionalità Principali
* Gestione anagrafica di Chef, Partecipanti e Corsi.
* Iscrizione dei partecipanti ai corsi.
* Gestione delle Ricette e degli Ingredienti.
* Generazione di Report mensili per l'amministrazione.