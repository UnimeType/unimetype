<p align="center">
  <a href="https://unimetype.com">
    <img src="https://raw.githubusercontent.com/UnimeType/transliteration/main/assets/hero-editorial.png" alt="UnimeType — One keyboard for all your languages, zero keyboard switching across apps or mid-sentence" width="100%" />
  </a>
</p>

<h1 align="center">UnimeType</h1>

<p align="center">
  <strong>One keyboard for all your languages — no switching keyboards across apps or mid-sentence.</strong><br/>
  Official release notes, binary checksums, package manager channels, and public issue tracker for UnimeType across macOS, Windows, Linux, iOS, Android, and ChromeOS.
</p>

<p align="center">
  <a href="./README.zh-CN.md">简体中文</a> ·
  <a href="https://unimetype.com/download">Download</a> ·
  <a href="https://unimetype.com/docs">Documentation</a> ·
  <a href="https://github.com/UnimeType/transliteration">Offline Model Toolkit</a> ·
  <a href="https://huggingface.co/UnimeType">Hugging Face Weights</a> ·
  <a href="https://github.com/UnimeType/unimetype/issues">Report an Issue</a>
</p>

---

## Why UnimeType Exists

Most bilingual people use **one native language alongside English** every day, yet traditional input methods force a hidden state machine onto every app switch and every mixed sentence:

- **Design (`Figma` / `Photoshop` / `Blender`)** — Single-key shortcuts (`V`, `R`, `T`, `Space`) get swallowed by floating candidate bars the moment you return from replying to a message.
- **Research (`Overleaf` / `LaTeX` / `Markdown`)** — Commands like `\cite{}`, `\begin{align}`, and half-width math punctuation turn into full-width brackets or phonetic candidates mid-draft.
- **Global Trade & Cross-App Messaging** — Moving between English quotes in `WhatsApp`, `Mail`, or `Excel` and native-script chats in `WeChat`, `LINE`, or `Slack` means guessing which keyboard layout is active before every first keystroke.
- **Gaming (`WASD` / `Shift`)** — Pressing `Shift` to sprint accidentally wakes up an IME candidate window and freezes movement.
- **Engineering (`VS Code` / `Terminal` / `Vim`)** — `Esc` and normal-mode navigation break whenever the OS remembers the wrong per-window input source.

UnimeType separates **typing** from **converting**: your keyboard stays in clean, predictable ASCII at all times, and pressing **Caps Lock** (or tapping **Convert** on mobile) converts phonetic drafts into native script in-place while keeping English terms, `@handles`, URLs, file paths, and code untouched.

---

## Download & Package Managers

Always verify or download the latest signed installers from **[unimetype.com/download](https://unimetype.com/download)** or install via your platform's package manager:

| Platform | Direct Download / Store | Package Manager / Channel |
| --- | --- | --- |
| **macOS** (`14.0+`, Apple Silicon & Intel) | [Download Universal `.dmg`](https://unimetype.com/download#macos) · [Releases](https://github.com/UnimeType/unimetype/releases) | `brew install --cask losdwind/tap/unimetype` |
| **Windows** (`10 / 11`, `x64` & `ARM64`) | [Download Signed `.exe`](https://unimetype.com/download#windows) · [Releases](https://github.com/UnimeType/unimetype/releases) | `winget install UnimeType.UnimeType` |
| **Linux** (`X11` & `Wayland`) | [Download `.deb` / `.rpm`](https://unimetype.com/download#linux) · [Releases](https://github.com/UnimeType/unimetype/releases) | Arch AUR: `yay -S unimetype-bin` |
| **iOS & iPadOS** (`17.0+`) | [Download on the App Store](https://apps.apple.com/app/id6478013435) | App Store auto-update |
| **Android** (`9.0+`) | [Google Play](https://play.google.com/store/apps/details?id=com.figurich.unimetype.android) · [Signed `.apk`](https://unimetype.com/download#android) | Play Store / Direct signed APK |
| **ChromeOS** (`ChromeOS` & `Crostini`) | [Download IME Extension `.zip`](https://unimetype.com/download#chromeos) · [Releases](https://github.com/UnimeType/unimetype/releases) | Unpacked ChromeOS IME extension |

---

## Open-Weight Offline Models (`Transliteration 2.0` · `v2.6`)

Desktop clients (`macOS`, `Windows`, `Linux`) support **100% offline on-device conversion** through any local OpenAI-compatible runtime (`LM Studio`, `Ollama`, `mlx_lm.server`, or `llama-server`) with zero network requests.

- **Local Inference Toolkit & Protocol Spec**: **[`UnimeType/transliteration`](https://github.com/UnimeType/transliteration)** — Official `unimetype-convert-short-v3` compact JSON protocol, protected-span restoration, one-command `Ollama` / `LM Studio` / Apple Silicon `MLX` / `llama.cpp` launchers, and the reproducible 60-case `Smoke-60` benchmark.
- **Apache-2.0 Weights on Hugging Face (`12` Languages / `13` Modes)**:
  - [`UnimeType/Transliteration-2.0-0.8B`](https://huggingface.co/UnimeType/Transliteration-2.0-0.8B) · [`Safetensors`](https://huggingface.co/UnimeType/Transliteration-2.0-0.8B-Safetensors) · [`GGUF`](https://huggingface.co/UnimeType/Transliteration-2.0-0.8B-GGUF)
  - [`UnimeType/Transliteration-2.0-4B`](https://huggingface.co/UnimeType/Transliteration-2.0-4B) · [`Safetensors`](https://huggingface.co/UnimeType/Transliteration-2.0-4B-Safetensors) · [`GGUF`](https://huggingface.co/UnimeType/Transliteration-2.0-4B-GGUF)
  - [`UnimeType/Transliteration-2.0-9B`](https://huggingface.co/UnimeType/Transliteration-2.0-9B) · [`Safetensors`](https://huggingface.co/UnimeType/Transliteration-2.0-9B-Safetensors) · [`GGUF`](https://huggingface.co/UnimeType/Transliteration-2.0-9B-GGUF)
- **Interactive Browser Playground**: **[`UnimeType/Transliteration-Playground`](https://huggingface.co/spaces/UnimeType/Transliteration-Playground)**

Supported transliteration languages in `v2.6`: **Chinese Pinyin**, **Japanese Romaji** (`natural` & `kana`), **Hindi Hinglish**, **Arabic Arabizi**, **Russian**, **Greek**, **Vietnamese**, **Spanish**, **French**, **Portuguese**, **German**, and **Italian** — each paired seamlessly with inline **English**.

---

## Issue Tracker & Host Compatibility Reports

This repository serves as the public issue tracker and release ledger for UnimeType clients:

- **[Bug Report](https://github.com/UnimeType/unimetype/issues/new?template=bug_report.yml)** — Crashes, UI glitches, conversion errors, or installer issues.
- **[App / Editor / Game Compatibility Report](https://github.com/UnimeType/unimetype/issues/new?template=app_compatibility.yml)** — Report any desktop app, web editor, terminal, or game where in-place selection replacement, cursor positioning, or shortcut passthrough misbehaves.
- **[Feature or Language Request](https://github.com/UnimeType/unimetype/issues/new?template=feature_request.yml)** — Suggest workflow improvements, shortcuts, or phonetic schemes.

---

## Privacy & Security

- **Normal typing never leaves your device.** Keystrokes stay local until you explicitly trigger **Convert**, **Polish**, or **Explain**.
- **Zero-network offline mode.** Point UnimeType Desktop at `http://127.0.0.1:1234/v1` (`LM Studio`) or `http://127.0.0.1:11434/v1` (`Ollama`) to run every conversion locally on your own hardware.
- To report a security vulnerability privately, see **[`SECURITY.md`](./SECURITY.md)** or email **[security@unimetype.com](mailto:security@unimetype.com)**.
