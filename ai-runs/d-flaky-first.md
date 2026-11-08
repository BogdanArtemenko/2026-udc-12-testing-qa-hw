Виправлено нестабільний тест у [receipt.test.js](C:/Users/bogar/ws12-d-flaky/app/test/integration/receipt.test.js:15).

Причина: тест використовував `floor(minutes / 30) + 1`, що помилково завищувало суму для рівно 30/60 хвилин. Замінено на правильне `ceil(minutes / 30)`.

Перевірки пройшли:

- `npm run test:repeat -- 30` — 30/30 успішних прогонів
- `npm test` — 52/52 тести успішні