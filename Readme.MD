# minidb

A database I'm building from scratch in C++ to learn how real databases work inside.

No database libraries, no shortcuts. Just C++, the standard library, and a lot of reading.

## Why

Databases are everywhere, but most developers treat them like a black box. I want to understand what happens under the hood: how data is stored on disk, how it survives a crash, how indexes make lookups fast, and how many users can read and write at the same time.

## Status

🚧 Work in progress. I'm building it one stage at a time.

## Roadmap

- [ ] **Stage 1: In-memory key-value store.** A command line with `SET`, `GET`, `DEL`
- [ ] **Stage 2: Persistence.** Save data to a file and load it on startup
- [ ] **Stage 3: Write-ahead log (WAL).** Data survives crashes
- [ ] **Stage 4: B-tree index.** Fast lookups using fixed-size pages on disk
- [ ] **Stage 5: Simple SQL.** `CREATE TABLE`, `INSERT`, `SELECT ... WHERE`
- [ ] **Stage 6: TCP server.** Many clients can connect at once
- [ ] **Stage 7: Transactions.** `BEGIN`, `COMMIT`, `ROLLBACK`
- [ ] **Benchmarks.** Compare performance against SQLite

## Build and run

Requires a C++17 compiler and CMake.

```bash
mkdir build && cd build
cmake ..
make
./minidb
```

## Usage

```
minidb> SET name Lord
OK
minidb> GET name
Lord
minidb> DEL name
1
minidb> GET name
(nil)
```

## What I'm learning

I'll write notes here as I go: problems I hit, design choices I made, and why.

## License

MIT
