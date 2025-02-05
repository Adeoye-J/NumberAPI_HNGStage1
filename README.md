# Number Classification API

This is an Express.js API that classifies a given number based on mathematical properties and returns a fun fact about it.

## Features
- Checks if a number is **prime**.
- Checks if a number is **perfect**.
- Checks if a number is an **Armstrong number**.
- Identifies if a number is **odd or even**.
- Calculates the **sum of digits**.
- Fetches a **fun fact** about the number from the [Numbers API](http://numbersapi.com/).
- Handles **CORS** and returns responses in **JSON format**.

## Technologies Used
- Node.js
- Express.js
- Axios (for external API calls)
- CORS (for cross-origin support)

## Installation & Setup
### Prerequisites
Ensure you have **Node.js** installed on your machine.

### Steps
1. Clone the repository:
   ```sh
   git clone https://github.com/Adeoye-J/NumberAPI_HNGStage1
   cd NumberAPI_HNGStage1
   ```
2. Install dependencies:
   ```sh
   npm install
   ```
3. Start the server:
   ```sh
   node server.js
   ```
4. The API will be running on:
   ```sh
   http://localhost:5000
   ```

## API Usage
### Endpoint:
```
GET /api/classify-number?number=<integer>
```

### Request Example:
```
GET http://localhost:5000/api/classify-number?number=371
```

### Success Response (200 OK):
```json
{
    "number": 371,
    "is_prime": false,
    "is_perfect": false,
    "properties": ["armstrong", "odd"],
    "digit_sum": 11,
    "fun_fact": "371 is an Armstrong number because 3^3 + 7^3 + 1^3 = 371"
}
```

### Error Response (400 Bad Request):
```json
{
    "number": "alphabet",
    "error": true
}
```

## Notes
- Only integer values are accepted as valid input.
- If an invalid input is provided, the API will return a `400 Bad Request`.
- The API should have a response time of **less than 500ms**.

## License
This project is open-source and available under the **MIT License**.

## Author
Developed by **Jeremiah Bankole** for HNG12 Stage 1 Backend Task.
