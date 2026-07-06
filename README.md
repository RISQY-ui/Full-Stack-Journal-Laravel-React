# 📚 FULL-STACK JOURNAL: LARAVEL TO REACT

Progress Achievements as of June 15, 2026

---

## PHASE 1: BUILDING THE BACKEND (LARAVEL)

### 1. Creating the Data Structure (Model & Migration)

| Aspect | Description |
|--------|-------------|
| Objective | Create a database table to store website data |
| Command | `php artisan make:model ModelName -m` |
| Result | Generated `ModelName.php` and migration file. Added columns: `model_name` and `status` |
| Execution | `php artisan migrate` — finalize table in the database |

---

### 2. Creating the Application Logic (Controller)

| Aspect | Description |
|--------|-------------|
| Objective | Manage logic for retrieving and sending data from the database |
| Command | `php artisan make:controller ModelController --api` |
| Result | Generated `ModelController.php`. Contains `index()` function that fetches all data (`ModelName::all()`) and converts to JSON (`return response()->json($data)`) |

---

### 3. Creating the Access Bridge (Routing)

| Aspect | Description |
|--------|-------------|
| Objective | Create URL endpoint for browsers or external apps to call the Controller |
| Location | `routes/web.php` file |
| Route Code | `use App\Http\Controllers\ModelController;`<br>`Route::get('/model-name', [ModelController::class, 'index']);` |

---

## PHASE 2: TROUBLESHOOTING JOURNEY

### Issue 1: ParseError - Stray 'p' Character

| Aspect | Description |
|--------|-------------|
| Problem | Laravel threw a syntax error when starting the server |
| Cause | Accidentally typed a 'p' at the end of `Route::get(...);p` |
| Solution | Removed the 'p' character, server ran normally |

---

### Issue 2: 404 Not Found Page

| Aspect | Description |
|--------|-------------|
| Problem | Opening `http://127.0.0.1:8000` showed a blank "Not Found" page |
| Cause | Did not append the endpoint to the URL |
| Solution | Added `/model-name` → `http://127.0.0.1:8000/model-name` — successfully displayed empty JSON data |

---

### Issue 3: Waiting for Cache Lock (Linux)

| Aspect | Description |
|--------|-------------|
| Problem | Terminal froze when installing new packages |
| Cause | Linux system was running background processes |
| Solution | Used `sudo kill -9` to clear the queue and remove lock files |

---

## PHASE 3: PREPARING THE FRONTEND (REACT.JS)

### Key Learning

Node.js and NPM need to be installed — not to replace Laravel, but as essential tools to run React.js.

### Commands Executed

```bash
sudo apt update && sudo apt install -y nodejs npm
