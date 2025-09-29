# ACM Dojo Tools

This repository provides an expanding set of utilities for ACM dojo developers to streamline development and compilation workflows using containerized environments.

## Prerequisites

- Docker must be installed and running on your system.

Though not strictly required, it is recommended that you add the `scripts/` directory to your system PATH for easy access to the tools.

## Available Tools

### `dojo-g++`
A drop-in replacement for the standard `g++` compiler that automatically runs compilation inside a Docker container based on the pwncollege/challenge-simple image.

**Features:**
- Automatically builds the Docker image if it doesn't exist
- Uses a persistent container for faster subsequent compilations
- Automatically starts the container if it's not running
- Mounts the current working directory to `/src` in the container
- Preserves all `g++` command-line arguments and functionality

**Usage:**
```bash
# Use exactly like regular g++
dojo-g++ -o myprogram main.cpp
dojo-g++ -std=c++17 -O2 -o solution solution.cpp
```

## Contributing

This is an expanding set of tools. Future utilities may include:
- Support for other compilers (clang++, etc.)
- Debugging utilities
- Testing frameworks
- Code analysis tools

Feel free to contribute additional tools that help with ACM dojo development workflows.