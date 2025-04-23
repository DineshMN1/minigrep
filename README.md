# minigrep 🦀

A simple `grep` clone written in Rust, built as a learning project from **The Rust Programming Language** book.

## Features

- Search for text patterns in files
- Case-sensitive search by default
- Case-insensitive search via environment variable
- Simple error handling
- Modular and testable codebase

## Installation

Clone the repository and build with Cargo:
```bash
git clone https://github.com/DineshMN1/minigrep
cd minigrep
cargo build --release
```

The executable will be available in the target/release directory.

## Usage

To use the tool, run it from the command line with the following syntax:
```bash
cargo run <query> <file_path>
```

Example:

To search for the word "nobody" in the poem.txt file:
```bash
cargo run nobody poem.txt
```

To perform a case-insensitive search, set the IGNORE_CASE environment variable:
```bash
IGNORE_CASE=1 cargo run nobody poem.txt
```

## Environment Variables

- `IGNORE_CASE`: When set to any value, searches will be case-insensitive. Set this variable to perform a case-insensitive search.

## Project Structure

The project is structured as follows:
```
minigrep/
├── src/
│   ├── lib.rs     # Core functionality: configuration structure and search algorithms
│   └── main.rs    # Command-line interface handling
├── poem.txt           # Sample text file for testing
├── output.txt         # sample output file
├── Cargo.toml         # Project metadata and dependencies
└── README.md          # Project documentation
```

## Testing

To run the tests for the search functionality, execute:
```bash
cargo test
```

## Acknowledgments

This project is based on the example in **The Rust Programming Language** book by Steve Klabnik and Carol Nichols.