## Go Advent of Code

### Structure

Each year expects a top level directory, e.g. `2025`

Each day's solution for a year expects a child directory, e.g. `2025/Day9`

Each solution's directory requires an `input` directory with two files, `example.txt` and `complete.txt`. 

`.txt` files are ignored due to AoC's preference that puzzle inputs not be shared publicly.

### Fetching AoC Inputs

The script found in `scripts/fetch_aoc_inputs.sh` can fetch and create `complete.txt` files in `input` folders for days defined according to the structure defined above.

This script requires the creation of an `.env` file at the root directory with a `SESSION_TOKEN` variable. You can grab this from the cookie set in your browser after authenticating with the Advent of Code website.

### Running Tests

To run all tests in parallel from the root directory run: `go test -v -parallel 8 ./...`

#### For a Particular Day
- Add the required `inputs` (`example.txt` and `complete.txt`)
- Navigate to that day's directory, e.g. `2021/Day9`
- Run `go test`

#### All Complete Problems
- Add the required `complete.txt` inputs (can use the script for this)
- Run 2023 tests: `go test -v ./2023/... -run 'TestDay[0-9]+Part[AB]2023Complete'`
- Run 2024 tests: `go test -v ./2023/... -run 'TestDay[0-9]+Part[AB]2023Complete'`
- Run 2025 tests: `go test -v ./2023/... -run 'TestDay[0-9]+Part[AB]2023Complete'`
    - Day 5 Part B takes a while to run (~5 mins)

## To-do

- Queue implementation
- Update `ReverseArray` utility to not edit array in place
- Grid implementation
- Refactor 2024 guard problem to use State pattern

Display basins: `go test -timeout 30s -run ^TestDay9PartB2021Complete$ github.com/chrisg07/Advent-of-Code-Go/2021/Day9 -v`
