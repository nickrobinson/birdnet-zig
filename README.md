# Ditto DQL CLI

Interactive CLI tool for testing and benchmarking DQL queries against a Ditto database.

## Requirements

- Java 17 or higher
- Maven 3.6+
- Ditto Java SDK 5.0.0-preview.4-dev in local Maven repository

## Build

```bash
mvn clean package
```

## Run

```bash
java -jar target/ditto-dql-cli-1.0.0.jar
```

Or during development:

```bash
mvn exec:java -Dexec.mainClass="com.ditto.cli.DittoDqlCli"
```

## Commands

- `<query>` - Execute a DQL query
- `.bench <query>` - Benchmark query (20 runs)
- `.explain <query>` - Show query execution plan
- `.load <file>` - Import NDJSON file
- `.help` - Display available commands
- `.exit` / `.quit` - Exit CLI

## Example

```
dql> SELECT * FROM movies WHERE year > 2020
dql> .bench SELECT * FROM movies WHERE rating > 8.0
dql> .explain SELECT * FROM movies WHERE year = 2021
```
# birdnet-zig
