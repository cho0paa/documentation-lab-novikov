GET /api/events

Повертає список усіх подій користувача.

Приклад запиту
GET /api/events

Приклад відповіді
```
{
  "events": [
    {
      "id": 1,
      "title": "Business Meetup 2025",
      "attendees": 120
    },
    {
      "id": 2,
      "title": "UX Workshop",
      "attendees": 45
    }
  ]
}
```
POST /api/events

Створює нову подію.

Приклад запиту
```
POST /api/events
Content-Type: application/json
```
```
{
  "title": "New Tech Conference",
  "date": "2025-06-20",
  "location": "Kyiv",
  "tickets": 150
}
```

Приклад відповіді
```
{
  "status": "success",
  "eventId": 12
}
```

GET /api/events/{id}

Повертає інформацію про конкретну подію.

Приклад запиту
GET /api/events/12

Приклад відповіді
```
{
  "id": 12,
  "title": "New Tech Conference",
  "date": "2025-06-20",
  "attendees": 0
}
```


Коди статусів

200 — Success / OK

201 — Created

400 — Bad Request (неправильні дані)

401 — Unauthorized (потрібно увійти)

404 — Not Found (подію не знайдено)

500 — Server Error
