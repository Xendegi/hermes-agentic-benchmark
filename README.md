# Hermes Agentic Benchmark

Adversarial benchmark framework for evaluating local LLMs on agentic tasks. Uses two agents: Agent A (testee) solves problems, Agent B (evaluator) grades the solutions. Ground truth scoring ensures objective results.

## Architecture

```
run_benchmark.py  →  spawns Agent A (solves tests)
                  →  spawns Agent B (evaluates solutions)
                  →  compares against ground truth
                  →  generates reports
```

## Test Categories

- **Math & Logic** — arithmetic, reasoning, word problems
- **Code Execution** — Python debugging, output prediction, API design
- **System Administration** — shell commands, file operations, networking

## Usage

```bash
python run_benchmark.py
```

Reports are saved to `reports/` as JSON and Markdown.

## Requirements

- Python 3.10+
- LM Studio running with a loaded model
- `httpx` (optional, for async)

## License

MIT
