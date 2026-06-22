# Meet Scheduling

A meeting scheduling backend built with Spring Boot. Handles slot booking, checks for conflicts, syncs with Google Calendar, and sends automated email confirmations via Brevo.

---
<img width="1920" height="1003" alt="Image" src="https://github.com/user-attachments/assets/93b2a48d-2304-453c-935e-ff081a7d9c0b" />
<img width="1920" height="1008" alt="Image" src="https://github.com/user-attachments/assets/a85cbef5-cdc1-400b-a602-37ea1874360e" />
<img width="1920" height="1020" alt="Image" src="https://github.com/user-attachments/assets/63798264-6966-49eb-8253-b105fe13fa50" />
<img width="1920" height="1032" alt="Image" src="https://github.com/user-attachments/assets/550031a0-edc7-4803-b3d0-8425b0300d77" />
<img width="720" height="1600" alt="Image" src="https://github.com/user-attachments/assets/d8bce3c1-4753-4c71-b4bc-3d1c53f35681" />


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

