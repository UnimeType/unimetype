# Security Policy

## Architecture & Data Handling

- **No background keystroke logging**: UnimeType never transmits raw keystrokes while you type normally. Text is processed only when you explicitly invoke an action (**Convert**, **Polish**, or **Explain**).
- **100% offline local option**: Desktop clients (`macOS`, `Windows`, `Linux`) can connect directly to loopback inference servers (`127.0.0.1`) powered by open-weight [`UnimeType/Transliteration-2.0`](https://huggingface.co/UnimeType) models (`LM Studio`, `Ollama`, `mlx-lm`, or `llama.cpp`) with zero external network traffic.
- **Signed release artifacts**: Always download installers from [`unimetype.com/download`](https://unimetype.com/download) or official app stores.

## Reporting a Vulnerability

Please **do not** open a public GitHub issue for security vulnerabilities.

Email **[security@unimetype.com](mailto:security@unimetype.com)** with:

1. Affected platform (`macOS`, `Windows`, `Linux`, `iOS`, `Android`, `ChromeOS`, or `Web`) and build/version number.
2. Clear reproduction steps or proof-of-concept details.
3. Potential impact assessment.

We acknowledge vulnerability reports within **48 hours** and coordinate remediation before public disclosure.
