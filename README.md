# Splitwise Clone

## Setup

Ensure you have Docker and Docker Compose installed.

1. Clone the repo:
   ```bash
   git clone <repo>
   cd splitwise-clone
   ```
2. Start services:
   ```bash
   docker-compose up --build
   ```
3. Backend will be at http://localhost:8000  
   Frontend at http://localhost:3000

## API Endpoints

- `POST /users` { "name": "Alice" } -> create user  
- `GET /users/{user_id}` -> get user  
- `POST /groups` { "name": "Trip", "user_ids": [1,2] } -> create group  
- `GET /groups/{group_id}` -> group details  
- `GET /groups/{group_id}/balances` -> group balances  
- `POST /groups/{group_id}/expenses` { "description":"Lunch","amount":100,"paid_by":1,"split_type":"equal" }  
- `GET /users/{user_id}/balances` -> user balances across groups
