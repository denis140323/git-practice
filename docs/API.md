# API Documentation

## Аутентификация

Для доступа к API требуется передача токена в заголовке:
`Authorization: Bearer <token>`

---

## GET /api/tasks

Возвращает список задач.

**Query-параметры:**
- `limit` (integer, по умолчанию 20) — количество задач.
- `status` (string) — фильтр по статусу (`open`, `done`).

**Пример успешного ответа (200 OK):**

```json
{
  "items": [
    {
      "id": 1,
      "title": "Купить хлеб",
      "status": "open"
    }
  ]
}