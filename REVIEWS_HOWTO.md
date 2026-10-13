# Как добавить одобренный отзыв

1. Отзыв приходит на neorixinbox.ru@yandex.ru (Formspree, форма /otzyv.html — ссылку даём только клиентам). Фото клиенты присылают в Telegram t.me/neorix_su.
2. Фото (необязательно): сжать в WebP (~1200px, `cwebp -q 80 in.jpg -o images/reviews/имя.webp`), положить в `images/reviews/`.
3. Добавить объект в `reviews.json` (массив; пустой `[]` = блок скрыт):
```json
[
  {"name": "Иван", "object": "Склад, Подольск", "rating": 5,
   "text": "Текст отзыва", "date": "2026-10-13",
   "photo": "images/reviews/sklad-podolsk.webp"}
]
```
   `photo` и `date` можно не указывать. Поле `example` не использовать.
4. `git commit -am "Отзыв: ..." && git push` — блок #reviews появится на главной сам.
