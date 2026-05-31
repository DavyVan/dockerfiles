# claude-code Docker Image

This image provides a basic environment for multi-language development and Claude-related projects.

This Docker image is based on `rockylinux:9` and includes the following programming languages and tools:

- `C/C++ 11.5`: `gcc/g++`, `CMake`, `make`
- `Python`: `miniconda (base 3.13)`
- `Node.js`: `nvm`, `Node 24 pre-installed`, `yarn`
- Essential development tools: `wget`, `git`, `vim`
- HTTP/HTTPS proxy set to host.docker.internal:7890
- `Claude Code`
