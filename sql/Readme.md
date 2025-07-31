# SQL To-Do List for Course

This directory contains SQL instructions for building a minimal to-do list to track course tasks.

## Table Creation

```sql
CREATE TABLE tasks (
    id SERIAL PRIMARY KEY,
    description TEXT NOT NULL,
    due_date DATE,
    completed BOOLEAN DEFAULT FALSE
);
```

## Example Usage

Insert a new task:

```sql
INSERT INTO tasks (description, due_date)
VALUES ('Finish lesson 1 readings', '2023-08-15');
```

Mark a task as completed:

```sql
UPDATE tasks
SET completed = TRUE
WHERE id = 1;
```

List incomplete tasks:

```sql
SELECT id, description, due_date
FROM tasks
WHERE completed = FALSE
ORDER BY due_date;
```
