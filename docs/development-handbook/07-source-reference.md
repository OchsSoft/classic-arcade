# Source reference

This handbook describes committed source in OchsSoft/classic-arcade at `21cf8599dd68875ebd2042cf8e5e0f88c418cdac`. Paths below are relative to this repository. Source-defined behavior is distinguished from a fresh runtime verification; no application or game was launched to author these chapters. The existing quick operating guide remains available separately.

## Reading the evidence

A source file explains what the program is designed to do. A test states an expectation and may exercise only one layer. A README describes an intended workflow and can lag implementation. When these disagree, inspect the exact revision and the executable code, reproduce the disagreement in a safe local test, and correct the relevant documentation with the change. Do not treat a passing unit test as proof of rendering, sound, external connectivity, deployment, or save recovery.

## File and symbol index

| File | Responsibility | Entry points and locations |
|---|---|---|
| [README.md](https://github.com/OchsSoft/classic-arcade/blob/21cf8599dd68875ebd2042cf8e5e0f88c418cdac/README.md) | Public product boundary, asset names, launch commands, platform and data assertions | L1 to L49 |
