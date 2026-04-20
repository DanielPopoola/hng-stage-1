# Tradeoffs & Design Decisions

## SQLite over PostgreSQL

The spec implies a production-grade database but the dataset is 2026 records.
SQLite handles millions of rows efficiently and eliminates operational complexity
(no separate DB service, no connection pooling, no driver differences).
Switched to PostgreSQL only if dataset size or concurrent write requirements grow.