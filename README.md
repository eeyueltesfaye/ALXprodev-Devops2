# Pokémon API Automation 

A collection of shell scripts that automate data fetching, parsing, summarization, error handling, and parallel processing using the [PokéAPI](https://pokeapi.co/). This project demonstrates real-world automation with `curl`, `jq`, `awk`, `sed`, and Bash process management.

## 📁 Directory: `Advanced_shell`

Each task is implemented as a separate script file.



## ✅ Tasks Breakdown

### 0. API Request Automation
**File:** `apiAutomation-0x00`

- Fetches data for Pikachu from the PokéAPI.
- Saves response to `data.json`.
- Logs errors to `errors.txt` if request fails.



### 1. Extract Pokémon Data
**File:** `data_extraction_automation-0x01`

- Extracts Pikachu's `name`, `type`, `height`, and `weight` from `data.json`.
- Formats output like:  
  `"Pikachu is of type Electric, weighs 6kg, and is 0.4m tall."`



### 2. Batch Pokémon Data Retrieval
**File:** `batchProcessing-0x02`

- Loops through a predefined list of Pokémon.
- Retrieves and stores each Pokémon’s data in a separate `.json` file inside `pokemon_data/`.



### 3. Summarize Pokémon Data
**File:** `summaryData-0x03`

- Reads all JSON files in `pokemon_data/`.
- Extracts `name`, `height`, and `weight`.
- Generates a CSV report: `pokemon_report.csv`.
- Uses `awk` to calculate and display average height and weight.



### 4. Error Handling and Retry Logic
**File:** `batchProcessing-0x02` (updated version)

- Adds robust retry logic (up to 3 attempts).
- Logs failures in `errors.log`.
- Skips to the next Pokémon if all attempts fail.



### 5. Parallel Data Fetching
**File:** `batchProcessing-0x04`

- Uses background processes to fetch multiple Pokémon in parallel.
- Speeds up batch processing.
- Ensures all processes complete using `wait`.



## 🛠️ Requirements

- `bash`
- `curl`
- `jq`
- `awk`
- `sed`

> On Ubuntu/Debian:
> ```bash
> sudo apt update
> sudo apt install jq
> ```

> On Windows (Git Bash):
> - Download `jq` binary: https://stedolan.github.io/jq/download/
> - Add it to your system PATH



## 📂 Folder Structure

```
Advanced_shell/
├── apiAutomation-0x00
├── data_extraction_automation-0x01
├── batchProcessing-0x02
├── batchProcessing-0x04
├── summaryData-0x03
├── pokemon_data/
│   ├── bulbasaur.json
│   ├── ...
├── data.json
├── errors.log
├── pokemon_report.csv
```



## 📜 License

This project is part of the **ALX DevOps curriculum** and is licensed for educational use.



## 🤖 Author

**Eyuel Tesfaye **  


