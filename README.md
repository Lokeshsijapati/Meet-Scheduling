# Meet Scheduling

A meeting scheduling backend built with Spring Boot. Handles slot booking, checks for conflicts, syncs with Google Calendar, and sends automated email confirmations via Brevo.

---

<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/fa94e703-704a-4987-863d-ba41e2e4ccff" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/6ecd6f29-13f7-42b1-b05e-ac5b4ade1377" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/6f636880-e150-439d-8fdf-e194782b19f2" />
<img width="1920" height="1080" alt="Image" src="https://github.com/user-attachments/assets/cc8f9907-058e-4361-97f8-6d1392f10b65" />
<img width="720" height="1600" alt="Image" src="https://github.com/user-attachments/assets/d57b8a3d-fa8f-4784-8aa5-604bae80bf64" />

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

