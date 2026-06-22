# Meet Scheduling

A meeting scheduling backend built with Spring Boot. Handles slot booking, checks for conflicts, syncs with Google Calendar, and sends automated email confirmations via Brevo.

---

## Tech Stack

- Java, Spring Boot
- MySQL, Spring Data JPA, Hibernate
- Google Calendar API (OAuth 2.0)
- Brevo API (email)
- Maven

---

## Features

- Create, update, delete and fetch meetings
- Conflict detection before booking a slot
- Auto sync with Google Calendar
- Email confirmations and reminders via Brevo
- Clean REST API structure

---

## API Endpoints

| Method | Endpoint | Description |
|--------|----------|-------------|
| POST | `/api/meetings` | Create a meeting |
| GET | `/api/meetings` | Get all meetings |
| GET | `/api/meetings/{id}` | Get meeting by ID |
| PUT | `/api/meetings/{id}` | Update a meeting |
| DELETE | `/api/meetings/{id}` | Delete a meeting |

---

## Project Structure

```
src/
├── controller/     API request handling
├── service/        Business logic + Calendar & Brevo integration
├── repository/     Database layer (JPA)
├── entity/         DB models
└── config/         OAuth and app config
```

---

## Setup

1. Clone the repo
```bash
git clone https://github.com/Lokeshsijapati/Meet-Scheduling.git
cd Meet-Scheduling
```

2. Add your credentials in `application.properties`
```properties
spring.datasource.url=jdbc:mysql://localhost:3306/meet_db
spring.datasource.username=YOUR_USERNAME
spring.datasource.password=YOUR_PASSWORD

google.calendar.client-id=YOUR_CLIENT_ID
google.calendar.client-secret=YOUR_CLIENT_SECRET

brevo.api.key=YOUR_BREVO_API_KEY
```

3. Run
```bash
mvn spring-boot:run
```

