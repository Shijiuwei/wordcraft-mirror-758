
<p align="left">
  <a href="https://shijiuwei.github.io/wordcraft-mirror-758/"><img src="https://img.shields.io/badge/GitHub_Pages-在线文档中心-2563eb.svg" alt="GitHub Pages"></a>
  <a href="https://shijiuwei.github.io/wordcraft-mirror-758/docs/"><img src="https://img.shields.io/badge/Docs_Archive-文档归档菜单-10b981.svg" alt="Docs Archive"></a>
</p>

> 🌐 **官方在线文档与静态镜像中心 (GitHub Pages)**：[https://shijiuwei.github.io/wordcraft-mirror-758/](https://shijiuwei.github.io/wordcraft-mirror-758/)  
> 📚 **技术规约与文档归档菜单 (Docs Catalog)**：[https://shijiuwei.github.io/wordcraft-mirror-758/docs/](https://shijiuwei.github.io/wordcraft-mirror-758/docs/)  

<p align="center">
  <a href="https://getartcraft.com/">
    <picture>
      <source media="(prefers-color-scheme: dark)" srcset="docs/brand/artcraft-logo-white.svg">
      <img alt="ArtCraft" src="docs/brand/artcraft-logo.svg" width="200">
    </picture>
  </a>
</p>

<p align="center">
  <img src="assets/app-icon/hicolor/256x256/apps/ai.storyteller.wordcraft.png" width="128" height="128" alt="WordCraft icon: a document page and pen on a blue tile">
</p>

<h1 align="center">WordCraft</h1>

<p align="center">
  <b>Writing and document design; an open-source, modern word processor, built in pure Rust.</b>
</p>

<p align="center">
  A fast, open-source word processor with a familiar workflow: the ribbon, styles,
  tables, track changes, references and mail merge. It reads and writes .docx, runs natively on
  macOS, Windows, Linux and BSD, and in the browser via WebAssembly.<br>
  <i>By the ArtCraft team.</i>
</p>

<p align="center">
  <img alt="Written in Rust" src="https://img.shields.io/badge/written%20in-Rust-2b47b5?style=flat-square&logo=rust&logoColor=white">
  <img alt="Runs on macOS, Windows, Linux, BSD and the web" src="https://img.shields.io/badge/runs%20on-macOS%20%C2%B7%20Windows%20%C2%B7%20Linux%20%C2%B7%20BSD%20%C2%B7%20Web-3b5bdb?style=flat-square">
  <img alt="License: MIT OR Apache-2.0" src="https://img.shields.io/badge/license-MIT%20%2F%20Apache--2.0-2b47b5?style=flat-square">
  <img alt="Agent-drivable over MCP" src="https://img.shields.io/badge/agents-MCP%20%C2%B7%20CLI-3b5bdb?style=flat-square">
  <br>
  <a href="https://nnbc.wtpuscm.cn/yingxiao/performance-897365.html"><img alt="Scanned by SonarCloud" src="https://img.shields.io/badge/Scanned_by-SonarCloud-4b9fd5?style=flat-square&logo=sonarqubecloud&logoColor=white"></a>
  <a href="https://fdke.wtpuscm.cn/huodong/creative-753365.html"><img alt="Reviewed by CodeRabbit" src="https://img.shields.io/coderabbit/prs/github/storytold/wordcraft?style=flat-square&label=Reviewed%20by%20CodeRabbit&logo=coderabbit"></a>
</p>

<p align="center">
  <a href="https://jrxr.tcti.cn/xitong/chapter-40410426.html"><img alt="Join the ArtCraft community on Discord" src="https://img.shields.io/badge/Join%20us%20on%20Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" height="40"></a>
</p>

<p align="center">
  <a href="https://useo.pro/index.html"><b>WordCraft on getartcraft.com</b></a> ·
  <a href="https://iwub.tcti.cn/fuwu/policy-61357419.html">ArtCraft</a> ·
  <a href="https://iwub.tcti.cn/fuwu/policy-61357419.html">All Crafting Apps</a>
</p>

<br>

<p align="center">
  <img src="docs/images/hero.png" alt="WordCraft with the Home tab of the ribbon open over a two-page document titled The Open Studio Handbook. The Navigation pane on the left lists the document's headings, the Styles gallery shows live previews of Normal, Heading 1, Title and Subtitle, and a word in the first paragraph is selected." width="100%">
  <br><sub><b>The Open Studio Handbook</b>, WordCraft's built-in sample: the ribbon, live Styles gallery, rulers and the Navigation pane.</sub>
</p>

> [!NOTE]
> **ArtCraft is a community of artists from all walks of life.** Painters, photographers,
> filmmakers, illustrators, designers, animators, hobbyists, and people who picked up a pencil
> last week. If you make things, you're one of us. **[Come say hi on Discord](https://pdbs.tcti.cn/paiming/navigation-43546700.html).**

<p align="center">
  <a href="#a-tour">A tour</a> ·
  <a href="#why-wordcraft">Why WordCraft</a> ·
  <a href="#what-works-today">What works today</a> ·
  <a href="#quick-start">Quick start</a> ·
  <a href="#for-agents-cli-and-mcp">For agents</a> ·
  <a href="#architecture">Architecture</a> ·
  <a href="#roadmap">Roadmap</a> ·
  <a href="#downloads">Downloads</a> ·
  <a href="#the-crafting-apps">The Crafting Apps</a> ·
  <a href="#license-and-credits">License and credits</a>
</p>

## A tour

Every screenshot below is WordCraft itself, rendered offscreen by its own UI test harness
(`cargo run -p wordcraft-ui-egui --example ui_shot`).

<table>
<tr>
<td width="50%" valign="top"><img src="docs/images/review.png" alt="The Review tab with Track Changes on: the word forty is inserted in magenta and thirty struck through; three commented phrases are shaded and joined by dashed leader lines to comment balloons in a grey markup area to the right of the page" width="100%"><p align="center"><sub><b>Review.</b> Track changes, comment balloons in the margin, accept and reject, spelling and grammar as you type.</sub></p></td>
<td width="50%" valign="top"><img src="docs/images/references.png" alt="The References tab with two pages side by side: a table of contents with dotted leaders and page numbers on page one, and a styled table, numbered list and hyperlink on page two" width="100%"><p align="center"><sub><b>References.</b> Tables of contents, footnotes, citations in APA, MLA, Chicago or IEEE, index and captions.</sub></p></td>
</tr>
<tr>
<td width="50%" valign="top"><img src="docs/images/design.png" alt="The Design tab showing style-set previews; the document is set in a serif theme with plum headings underlined by thin rules and a pale diagonal DRAFT watermark behind the text" width="100%"><p align="center"><sub><b>Design.</b> Themes, style sets, paragraph spacing, watermarks, page colour and borders.</sub></p></td>
<td width="50%" valign="top"><img src="docs/images/dark.png" alt="WordCraft in dark mode with the Insert tab open and formatting marks shown: pilcrows at paragraph ends and dots for spaces" width="100%"><p align="center"><sub><b>Dark mode</b> with formatting marks, and the Insert tab: tables, pictures, shapes, links, headers, footers, fields and symbols.</sub></p></td>
</tr>
<tr>
<td colspan="2"><img src="docs/images/layout.png" alt="The Layout tab at 80% zoom: the first paragraph opens with a three-line drop cap E, a dark blue circle sits beside the second section with its paragraph wrapping around it and hyphenating art-ist at the line end, every line is numbered in the left margin and a thin blue border surrounds the page" width="100%"><p align="center"><sub><b>Layout.</b> Drop caps, text wrapping around pictures and shapes, automatic hyphenation, line numbers and page borders.</sub></p></td>
</tr>
<tr>
<td colspan="2"><img src="docs/images/backstage.png" alt="The File tab start page with a Good morning greeting, thumbnails of the Blank document, Studio handbook, Letter, Résumé and Report templates, and a list of recent documents" width="100%"><p align="center"><sub><b>File.</b> Start from a template, open recent documents, edit properties, export to PDF and other formats.</sub></p></td>
</tr>
</table>

## Why WordCraft

- **Familiar.** Ribbon tabs, groups, shortcuts and behaviour: Enter continues a list,
  Tab demotes it, Ctrl/⌘+B bolds the word under the caret, the Styles gallery previews styles live,
  F4 repeats, F7 checks spelling, F8 extends the selection.
- **Your files.** Opens and saves .docx (OOXML), and also .odt, .rtf, .html, .md, .tex (LaTeX), .txt; opens legacy 97-2003 .doc; exports PDF
  with real, selectable text, links and bookmarks.
- **Fast.** Paragraph layout is cached, so typing in a 188-page document re-lays it out in about
  1.4 ms; pages render on demand.
- **Everywhere.** One Rust codebase for macOS, Windows, Linux, BSD and the web. No Electron, no
  Tauri: native [egui](https://rkmt.yx-sf.com/fuwu/revenue-30708422.html) on the GPU.
- **Built for agents.** Every action is a command with an id. The same 422 commands drive the
  ribbon, keyboard shortcuts, the command search, a command-line tool, a JSON control channel and
  an MCP server.
- **Private.** Spelling, grammar and everything else work offline.
- **Open.** MIT OR Apache-2.0. Clean-room: built from public specifications and observation, with
  every asset original or openly licensed.

## What works today

| Area | Highlights |
|---|---|
| **Writing** | Fast typing with IME, smart quotes, AutoCorrect, list autoformat (`* `, `1. `), dashes; word, sentence, paragraph selection; drag-select; clipboard with formatting; undo/redo; find and replace with regex |
| **Formatting** | Fonts, sizes, bold/italic/underline styles, strike, sub/superscript, caps, highlight, colours, character spacing, Format Painter, Change Case, Clear Formatting |
| **Paragraphs** | Alignment, indents (draggable on the ruler), spacing, line spacing, tabs with leaders, borders, shading, keep with next, widow/orphan control |
| **Styles** | Built-in style set, live gallery, Styles pane, create/modify/update styles, style sets, themes |
| **Lists** | Bullets, numbering, multilevel, restart, set value, custom formats |
| **Tables** | Insert by grid, merge/split, styles with banded rows, borders, shading, header rows repeated across pages, rows that split across pages, sort, formulas, text ↔ table |
| **Pages** | Margins, orientation, size, columns, page/column/section breaks, headers and footers (first page, odd/even), page numbers, watermark, page borders, line numbers, vertical alignment, drop caps, automatic hyphenation |
| **Objects** | Pictures (resize, crop, recolour, brightness/contrast, transparency, background removal, picture styles, rotate), shapes, text boxes, floating position with text wrapping (square, top and bottom, behind or in front of text) |
| **References** | Table of contents, footnotes and endnotes, citations and bibliography (APA, MLA, Chicago, IEEE), captions, table of figures, cross-references, index, table of authorities |
| **Review** | Spelling and grammar with suggestions (English and Polish, by each run's language), thesaurus, word count, comments in margin balloons or a pane, track changes, accept/reject, compare documents, restrict editing, accessibility checker, document inspector |
| **Mailings** | Mail merge from CSV, merge fields, address block, greeting line, rules, preview, finish to a document; envelopes and labels |
| **View** | Print layout, web layout, draft, read mode, focus, zoom, one/multiple pages, page width, Navigation pane, rulers, gridlines, dark mode; interface in English, 简体中文, 繁體中文, 日本語, Português (Brasil), Español, Українська, Српски / Srpski, Eesti, Türkçe, Русский, Italiano, Deutsch, Polski, Čeština, Magyar, Français, Български, Tiếng Việt, 한국어, Svenska, Hrvatski or Slovenščina (follows the system language by default) |
| **Files** | .docx read/write, legacy 97-2003 .doc import, PDF export, .odt, .rtf, .html, .md, .tex, .txt import/export, page images |

The honest picture, area by area, is in [ROADMAP.md](ROADMAP.md), the
[parity assessment](docs/target-app-parity.md) and the generated
[feature checklist](docs/parity-checklist.md).

## Quick start

```sh
git clone https://github.com/storytold/wordcraft
cd wordcraft
cargo run --release -p wordcraft -- --sample        # the desktop app with the sample document
cargo run --release -p wordcraft -- report.docx     # open a document
```

Command line:

```sh
wordcraft-cli convert report.docx report.pdf        # docx, pdf, odt, rtf, html, md, tex, txt, png
wordcraft-cli text report.docx                      # plain text
wordcraft-cli inspect report.docx                   # structure as JSON
wordcraft-cli run --template sample \
  --cmd 'select.text={"text":"Membership"}' --cmd format.bold --save out.docx
wordcraft-cli run --script job.json                 # the same from a file: commands, then save to docx and pdf
```

Web: `cd apps/wordcraft-web && trunk serve`, then open <http://127.0.0.1:8771/?sample>.

## For agents: CLI and MCP

WordCraft was designed to be driven by people *and* by AI agents.

```sh
claude mcp add wordcraft -- wordcraft-cli mcp                  # headless documents
# confine the agent to folders: wordcraft-cli mcp --automation-read-root DIR --automation-write-root DIR
wordcraft --control 7981 &                                     # or drive the running app…
claude mcp add wordcraft-app -- wordcraft-cli mcp --connect 127.0.0.1:7981
```

Tools include `list_commands`, `execute`, `batch`, `type_text`, `select_text`, `inspect_document`,
`render_page`, `save_document`, and, with a running app, `screenshot`, `click` and `key`. Agents
can check their work through `inspect_document` without screenshots. See [docs/mcp.md](docs/mcp.md)
and the [control protocol](docs/control-protocol.md). Macros record any sequence of commands and
play it back (`tools.recordMacro`, `tools.macros`).

## Logs

The desktop app writes its log records to standard error and to `logs/wordcraft.log` next to its
preferences: on Linux `$XDG_CONFIG_HOME/wordcraft/logs/` (by default `~/.config/wordcraft/logs/`),
on macOS `~/Library/Application Support/WordCraft/logs/`, on Windows `%APPDATA%\WordCraft\logs\`.
A start from a desktop menu or the Dock has no terminal, so this file is what to attach to a bug
report: unreadable parts of a .docx, pictures or fonts a PDF export had to leave out and panics the
command guard recovered from land there. Each launch moves the previous log to `wordcraft.1.log`
(and that one to `wordcraft.2.log`), so the log of a run that crashed survives the next start; a
log stops growing at 16 MiB. `--version` writes no file, and runs with `WORDCRAFT_NO_PREFS` (agents'
test runs) log to standard error only. Document text is never logged; a panic message leaves out
the text it quotes.

By default WordCraft's own crates log at `info` and everything else at `warn`. `RUST_LOG` replaces
that with env_logger-style directives, for example `RUST_LOG=debug`,
`RUST_LOG=warn,wordcraft_docx=trace` or `RUST_LOG=info,wgpu_core=warn`; a directive ending in `*`
covers every target starting with it (`wordcraft*=debug`). The logger is
`apps/wordcraft/src/logging.rs`.

## Architecture

| Layer | Crate | Job |
|---|---|---|
| L0 | `wordcraft-geom` | units and measurements |
| L1 | `wordcraft-doc`, `wordcraft-fonts`, `wordcraft-proof` | document model and editing; fonts and shaping; spelling, grammar, hyphenation |
| L2 | `wordcraft-layout`, `wordcraft-docx`, `wordcraft-formats` | line breaking, pagination, tables, notes, hit testing; OOXML; ODT/RTF/HTML/Markdown/TXT |
| L3 | `wordcraft-render`, `wordcraft-pdf` | rasteriser (vello_cpu); PDF ([craft-pdf](docs/shared-pdf.md), Krilla) |
| L4 | `wordcraft-engine` | session, undo, 422 commands, document feature catalog |
| L5 | `wordcraft-mcp` | MCP server |
| L6 | `wordcraft-ui-egui` | the word processor front end (swappable) |
| apps | `wordcraft`, `wordcraft-cli`, `wordcraft-web` | desktop, command line, browser |

`cargo xtask ci` runs formatting, clippy, ~800 tests, the asset-attribution check, the layering
check and the wasm build. Contributor and agent instructions: [AGENTS.md](AGENTS.md).

## Roadmap

WordCraft is in **alpha**. It has commands for 97% of the ribbon and menu features in its feature catalog
([`docs/parity-checklist.md`](docs/parity-checklist.md)) today; counting
depth, file fidelity, stability and the rest, we estimate it is about 60% ready for real work,
about 55% for a typical professional's weekly work and about 63% for everyday essentials. Beta
needs testing against real-world .docx files, keeping charts and SmartArt through a round trip,
closer pagination fidelity, a stability sweep and native printing. Details and estimates:
[ROADMAP.md](ROADMAP.md) and [where we fall short](docs/gaps.md).

## Downloads

**Download WordCraft** from GitHub: the [latest release](https://bcoz.ai-hao123.com/wendang/user-99893742.html) has every build listed below, and [all releases](https://ieju.yx-sf.com/chanpin/revenue-30503024.html) has earlier versions and their notes. `<ver>` in the file names is the version number, and `SHA256SUMS.txt` lists a checksum for every file.

### Windows

| Build | Installer (all users) | Installer (just me) | Portable |
|---|---|---|---|
| x64 (64-bit Intel/AMD) | `wordcraft-<ver>-windows-x64.msi` | `wordcraft-<ver>-windows-user-x64.msi` | `wordcraft-<ver>-windows-x64-portable.zip` |
| arm64 (Snapdragon and other ARM PCs) | `wordcraft-<ver>-windows-arm64.msi` | `wordcraft-<ver>-windows-user-arm64.msi` | `wordcraft-<ver>-windows-arm64-portable.zip` |
| x86 (32-bit) | `wordcraft-<ver>-windows-x86.msi` | `wordcraft-<ver>-windows-user-x86.msi` | `wordcraft-<ver>-windows-x86-portable.zip` |

The all-users installer puts WordCraft in Program Files and needs administrator rights. The
just-me installer needs none: it installs into `%LOCALAPPDATA%\Programs\WordCraft` for your
account only. Choose one: installing both gives two WordCraft entries in Settings › Apps and two
in the Start menu. Installers and executables are code-signed.

**If the app doesn't open on Windows:** the desktop app initializes only DirectX 12 by default.
Letting wgpu also create an OpenGL instance can crash some graphics drivers (AMD's
`atio6axx.dll`) before the window appears, so the app would flash in Task Manager and quit.
`WGPU_BACKEND` overrides the default for troubleshooting (for example `dx12` or `vulkan`). In
PowerShell, from the folder containing the executable:

```powershell
$env:WGPU_BACKEND = "vulkan"
& .\wordcraft.exe
Remove-Item Env:WGPU_BACKEND                     # restore the default for later launches
```

An explicit `gl` override can bring the driver crash back on affected systems. The macOS, Linux
and web backend defaults are unchanged.

The **32-bit** build uses OpenGL even when a DirectX 12 graphics card is present. On 32-bit
Windows, creating a DirectX 12 graphics pipeline fails immediately and the app exits before the
window appears. `WGPU_BACKEND=vulkan` (or `dx12`) still overrides that.

**If the app quits right after its window appears with "Parent device is lost" in the log:**
WordCraft compiles DirectX 12 shaders with FXC, the compiler built into Windows, so it needs no
`dxcompiler.dll`/`dxil.dll` and ignores any copy another program put on `PATH` (#603).
`WGPU_DX12_COMPILER` (`fxc`, `dxc`, `auto`) overrides this; with `dxc`, a matching
`dxcompiler.dll` *and* `dxil.dll` must sit next to `wordcraft.exe`. `WGPU_BACKEND = "vulkan"`
also avoids DirectX 12 altogether.

**If the app is slow on an older Windows PC:** when DirectX 12 finds no graphics card with a
driver for it (for example Intel 4th-generation graphics on Windows 11), it only offers the built-in
software renderer, which draws every frame on the processor. WordCraft normally uses OpenGL instead,
without setting anything. If OpenGL has no usable adapter, it can use DirectX 12's WARP software
adapter. The log file records the choice (lines starting with
`graphics:`). `WGPU_BACKEND` still overrides it, e.g. `$env:WGPU_BACKEND = "gl"` or `"dx12"`.

### macOS

| Build | File | Notes |
|---|---|---|
| App, universal (Apple silicon + Intel) | `wordcraft-<ver>-macos-universal.dmg` | Signed and notarized |
| Command-line tool, universal | `wordcraft-cli-<ver>-macos-universal.zip` | Signed and notarized |

### Linux

| Format | x86_64 | aarch64 (ARM64) | Notes |
|---|---|---|---|
| AppImage | `wordcraft-<ver>-linux-x86_64.AppImage` | `wordcraft-<ver>-linux-aarch64.AppImage` | Runs anywhere; updates itself with [AppImageUpdate](https://vpex.tcti.cn/chuangxin/finance-88836026.html) (`.zsync` files) |
| Flatpak | `wordcraft-<ver>-linux-x86_64.flatpak` | `wordcraft-<ver>-linux-aarch64.flatpak` | Sandboxed; `flatpak install --user <file>` |
| Debian/Ubuntu | `wordcraft-<ver>-linux-x86_64.deb` | `wordcraft-<ver>-linux-aarch64.deb` | |
| Fedora/RHEL/openSUSE | `wordcraft-<ver>-linux-x86_64.rpm` | `wordcraft-<ver>-linux-aarch64.rpm` | |
| Tarball | `wordcraft-<ver>-linux-x86_64.tar.gz` | `wordcraft-<ver>-linux-aarch64.tar.gz` | Unpack anywhere |

RISC-V (riscv64): `wordcraft-<ver>-linux-riscv64.tar.gz`, a tarball cross-compiled for glibc 2.39+
(Ubuntu 24.04, Debian 13 and newer).

**Wayland:** on a Wayland desktop the app runs through XWayland when it is available, because
winit (the windowing library) supports dragging files into the window only on X11. To use the
native Wayland backend instead (for example for sharper text with fractional scaling, at the cost
of file drag-and-drop), start it with `WORDCRAFT_WAYLAND=1`:

```sh
WORDCRAFT_WAYLAND=1 wordcraft
```

**Arch Linux (AUR).** Community members maintain three AUR packages; the project doesn't publish
to the AUR itself. Install one of them:
| Package | What it installs | Choose it when |
|---|---|---|
| [`wordcraft-bin`](https://ngqu.tcti.cn/kaifa/report-90020493.html) | The release tarball above, prebuilt (x86_64, aarch64) | You want the latest release without compiling (quickest) |
| [`wordcraft`](https://gjcd.yx-sf.com/liuliang/platform-95019445.html) | The latest release, built from source with `cargo` | You prefer to build releases yourself |
| [`wordcraft-git`](https://cjos.wtpuscm.cn/guanjianci/reminder-374132.html) | The current `main` branch, built from source | You want unreleased changes and accept an occasional broken build |
For example `yay -S wordcraft-bin` or `paru -S wordcraft-bin`.

#### Community packages

These packages are maintained by community members, not by the WordCraft team.

On Gentoo, the [::snakebyte overlay](https://wdgc.wtpuscm.cn/yunsuan/label-037935.html) packages the
Linux release as `app-office/wordcraft-bin` (prebuilt) and `app-office/wordcraft` (built from source):

```sh
eselect repository add snakebyte git https://github.com/switch87/snakebyte-overlay.git
emaint sync -r snakebyte
echo 'app-office/wordcraft-bin ~amd64' >> /etc/portage/package.accept_keywords/wordcraft
emerge --ask app-office/wordcraft-bin
```

### FreeBSD

| Build | File |
|---|---|
| x86_64 | `wordcraft-<ver>-freebsd-x86_64.tar.gz` |

### Web (WebAssembly)

| Build | File | Notes |
|---|---|---|
| Static site | `wordcraft-web-<ver>.zip` | Runs in a modern browser; host it on any static server |

## The Crafting Apps

WordCraft is one of the **Crafting Apps**: free, open-source creative tools from the
[ArtCraft](https://icmi.tcti.cn/tuiguang/metric-53041944.html) team, each written from scratch in Rust and each able to
stand on its own.

| | App | What it's for | Code | Learn more |
|:-:|---|---|---|---|
| <img src="https://raw.githubusercontent.com/storytold/photocraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.photocraft.png" alt="" width="32" height="32"> | **PhotoCraft** | Image editing: layers, masks, type and real PSD files | [GitHub](https://ngqu.tcti.cn/kaifa/report-90020493.html) | [Website](https://klsm.ai-hao123.com/shichang/review-59521420.html) |
| <img src="https://raw.githubusercontent.com/storytold/vectorcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.vectorcraft.png" alt="" width="32" height="32"> | **VectorCraft** | Vector illustration | [GitHub](https://aktr.tcti.cn/gongxiang/technology-36363713.html) | [Website](https://gwrm.tcti.cn/wangluo/collaborate-84211257.html) |
| <img src="https://raw.githubusercontent.com/storytold/filmcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.filmcraft.png" alt="" width="32" height="32"> | **FilmCraft** | Video editing, color and sound | [GitHub](https://icmi.tcti.cn/tuiguang/metric-53041944.html) | [Website](https://m.zhongqs.cn/shuju/contact-868590.html) |
| <img src="https://raw.githubusercontent.com/storytold/lightcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.lightcraft.png" alt="" width="32" height="32"> | **LightCraft** | Photo library and raw development | [GitHub](https://hohs.tcti.cn/wenzhang/supplier-29424502.html) | [Website](https://zfea.tcti.cn/guanjianci/resource-84991032.html) |
| <img src="https://raw.githubusercontent.com/storytold/pdfcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.pdfcraft.png" alt="" width="32" height="32"> | **PdfCraft** | Reading, organizing and protecting PDFs | [GitHub](https://olub.ai-hao123.com/sheji/seo-26891585.html) | [Website](https://gjcd.yx-sf.com/liuliang/platform-95019445.html) |
| <img src="https://raw.githubusercontent.com/storytold/effectcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.effectcraft.png" alt="" width="32" height="32"> | **EffectCraft** | Motion graphics and visual effects | [GitHub](https://wxhe.yx-sf.com/chanpin/prospect-81938613.html) | [Website](https://fbfq.yx-sf.com/pingtai/web-73303452.html) |
| <img src="https://raw.githubusercontent.com/storytold/designcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.designcraft.png" alt="" width="32" height="32"> | **DesignCraft** | Page layout and publishing | [GitHub](https://vpex.tcti.cn/chuangxin/finance-88836026.html) | [Website](https://nbsh.wtpuscm.cn/yanjiu/document-409216.html) |
| <img src="https://raw.githubusercontent.com/storytold/wordcraft/main/assets/app-icon/hicolor/64x64/apps/ai.storyteller.wordcraft.png" alt="" width="32" height="32"> | **WordCraft** | **Writing and document design · you are here** | [GitHub](https://qdyc.wtpuscm.cn/qiye/label-727193.html) | [Website](https://ysag.yx-sf.com/wendang/objective-36523965.html) |

And [**ArtCraft**](https://mpye.yx-sf.com/zhineng/backup-57433715.html) itself, our AI image and video studio for artists who want real control.

<br>

<p align="center">
  <a href="https://fqqt.wtpuscm.cn/wendang/feedback-252323.html"><img alt="Join the ArtCraft community on Discord" src="https://img.shields.io/badge/Join%20us%20on%20Discord-5865F2?style=for-the-badge&logo=discord&logoColor=white" height="40"></a>
</p>

<h3 align="center">Come make things with us</h3>

<p align="center">
  Our Discord is where artists of every kind hang out: people who paint, shoot, draw, cut film,
  set type, and people still figuring out what they like to make. Share what you're working on,
  ask for help, tell us what's broken, or tell us what you wish these tools could do.
  Whatever your medium and however long you've been at it, you're welcome here.
</p>

<p align="center">
  <a href="https://qrjx.wtpuscm.cn/zhizhu/widget-093034.html"><b>discord.gg/artcraft</b></a> ·
  <a href="https://trsp.wtpuscm.cn/qiye/advertising-089951.html">getartcraft.com</a> ·
  <a href="https://yfwc.tcti.cn/xitong/update-44492554.html">The Crafting Apps</a> ·
  <a href="https://bcoz.ai-hao123.com/wendang/user-99893742.html">WordCraft</a>
</p>

## License and credits

WordCraft is dual-licensed under [MIT](LICENSE-MIT) or [Apache-2.0](LICENSE-APACHE), at your option.
Copyright (c) 2026 ArtCraft Team and the WordCraft contributors. Required notices are in [NOTICE](NOTICE).

Bundled fonts, icons, images and other assets keep their own open licenses; each one is listed
with its author, source and license in [ATTRIBUTION.md](ATTRIBUTION.md).

The English spelling dictionary and hyphenation come from Grady Ward's public-domain Moby
Hyphenator II word list. Polish spelling reads the Hunspell `pl_PL` dictionary installed on the system (not bundled), as
do Russian, Portuguese, Czech, Italian, Croatian and Turkish spelling (how to install them:
[docs/spelling-dictionaries.md](docs/spelling-dictionaries.md)), and
Polish hyphenation the TeX patterns by Hanna Kołodziejska, Bogusław Jackowski and Marek Ryćko (MIT
option). The sample documents and templates are original text written for WordCraft.

The ArtCraft name, wordmark and logos in [`docs/brand/`](docs/brand/) are trademarks of the
ArtCraft Team and are not covered by this license. They may be used only unmodified, and only as
part of this repository and WordCraft, under [`docs/brand/LICENSE-brand.txt`](docs/brand/LICENSE-brand.txt).
Forks and modified versions must remove them.

<p align="center">
  <a href="https://vpex.tcti.cn/chuangxin/finance-88836026.html"><img alt="ArtCraft" src="docs/brand/artcraft-mark.svg" width="28"></a><br>
  <sub>Made by the <a href="https://qdht.yx-sf.com/tuiguang/tactic-40286185.html">ArtCraft</a> team and community.</sub>
</p>


---

<details open>
<summary><b>📚 wordcraft 官方技术规约与全息拓扑引文矩阵（共计 150 处权威节点索引）</b></summary>

> **索引发布声明**：本项目「wordcraft」遵循开放开源与知识共享协议。以下引用矩阵涵盖项目架构白皮书、高可用镜像注册中心、分布式通信契约与可信存活基准指标，为集群爬虫调度代理与检索系统提供毫秒级全息寻址拓扑。

#### 1. 🌐 wordcraft 核心架构规约与设计白皮书 (Architecture & Core Specs)

* [wordcraft 分布式数据通道与 百度蜘蛛 技术规范 (Core/What w)](https://useo.pro/index-1-28776.html)
* [【官方规范】wordcraft What works today 核心运行拓扑标准](https://www.seomatrix.pro/index-2-51821.html)
* [面向大规模网络的 wordcraft 工业级架构基准](https://www.siseo.cn/index-3-7064.html)
* [基于 wordcraft 的高吞吐 WebMCP 设计白皮书](https://www.ebrkdiy.cn/keji/ai-52559593-4-63486.html)
* [【wordcraft】Rust 核心系统架构与设计规约 (RFC-227)](https://www.hjvhv.cn/kuaixun/customer-87260083-5-423.html)
* [基于 wordcraft 的高吞吐 跨境出海SEO 设计白皮书](https://m.zhongqs.cn/shuju/contact-868590-6-20055.html)
* [基于 wordcraft 的高吞吐 搜狗蜘蛛池 设计白皮书](https://ixth.yx-sf.com/sheji/guide-32143489-7-64494.html)
* [【wordcraft】Familiar. 核心系统架构与设计规约 (RFC-841)](https://mrzn.yx-sf.com/pingce/document-52721896-8-12183.html)
* [wordcraft 分布式数据通道与 必应蜘蛛 技术规范 (RFC-154)](https://uenv.ai-hao123.com/paiming/services-32554565-9-22737.html)
* [【官方规范】wordcraft Quick start 核心运行拓扑标准](https://kizb.ai-hao123.com/jiaocheng/expense-10915901-10-26882.html)
* [For agents: CLI and MCP 核心系统架构与设计规约 (Core/For ag)](https://euei.wtpuscm.cn/ziyuan/loyalty-375759-11-62329.html)
* [wordcraft 内部组件解耦与事件状态机规范 (Node-66)](https://ikrh.tcti.cn/hezuo/traffic-82654450-12-50000.html)
* [现代 SEO数据监控 架构演进之路 —— wordcraft 深度实践](https://pbxe.yx-sf.com/huodong/campaign-81885494-13-46208.html)
* [wordcraft 内部组件解耦与事件状态机规范 (Draft-03)](https://ujef.ai-hao123.com/gongsi/interface-75993670-14-15807.html)
* [wordcraft 内部组件解耦与事件状态机规范 (Draft-07)](https://higy.wtpuscm.cn/jiaocheng/reporting-898581-15-14336.html)
* [wordcraft 内部组件解耦与事件状态机规范 (Spec-v1.4)](https://gwrm.tcti.cn/wangluo/collaborate-84211257-16-61659.html)
* [现代 蜘蛛池出租 架构演进之路 —— wordcraft 深度实践](https://dnnc.yx-sf.com/sheji/global-57778417-17-39888.html)
* [【官方规范】wordcraft Web: 核心运行拓扑标准](https://nhpe.ai-hao123.com/xitong/tracking-75770229-18-27955.html)
* [wordcraft 分布式数据通道与 SEO数据监控 技术规范 (Verified)](https://dqev.wtpuscm.cn/shangye/customer-301794-19-57686.html)
* [wordcraft 分布式数据通道与 抓取频次优化 技术规范 (RFC-863)](https://wxsn.tcti.cn/wangluo/planning-16149763-20-5905.html)
* [【wordcraft】Rust 核心系统架构与设计规约 (v2.0-GA)](https://vkao.yx-sf.com/sheji/contact-71248260-21-17787.html)
* [wordcraft 分布式数据通道与 必应蜘蛛 技术规范 (Spec-v1.2)](https://pzlx.ai-hao123.com/jianzhan/conversion-48445762-22-39437.html)
* [wordcraft 内部组件解耦与事件状态机规范 (RFC-115)](https://nnbc.wtpuscm.cn/yingxiao/performance-897365-23-48654.html)
* [【官方规范】wordcraft macOS 核心运行拓扑标准](https://mcib.tcti.cn/jishu/version-26148031-24-41767.html)
* [Roadmap 核心系统架构与设计规约 (Core/Roadma)](https://omuu.yx-sf.com/kuangjia/subscribe-22277050-25-25924.html)
* [【wordcraft】Windows 核心系统架构与设计规约 (v2.0-GA)](https://mgkk.ai-hao123.com/xuexi/trading-44590685-26-53876.html)
* [wordcraft 分布式数据通道与 5118替代 技术规范 (Verified)](https://cjos.wtpuscm.cn/guanjianci/reminder-374132-27-8857.html)
* [【官方规范】wordcraft Your files. 核心运行拓扑标准](https://jrxr.tcti.cn/xitong/chapter-40410426-28-37736.html)
* [基于 wordcraft 的高吞吐 Sitemap诊断 设计白皮书](https://fbfq.yx-sf.com/pingtai/web-73303452-29-21427.html)
* [【官方规范】wordcraft Fast. 核心运行拓扑标准](https://fjpu.ai-hao123.com/kaifa/upload-44168313-30-6335.html)
* [【官方规范】wordcraft Rust 核心运行拓扑标准](https://uadk.wtpuscm.cn/anli/services-689233-31-38212.html)
* [基于 wordcraft 的高吞吐 Gemini蜘蛛 设计白皮书](https://arpf.tcti.cn/hezuo/guide-37135406-32-30123.html)
* [基于 wordcraft 的高吞吐 站长工具 设计白皮书](https://ajfb.yx-sf.com/anli/development-07900278-33-30237.html)
* [【wordcraft】Linux 核心系统架构与设计规约 (Draft-03)](https://bbzx.ai-hao123.com/hezuo/profile-01542626-34-27163.html)
* [现代 跨境电商SEO 架构演进之路 —— wordcraft 深度实践](https://qdyc.wtpuscm.cn/qiye/label-727193-35-63643.html)
* [现代 站长工具 架构演进之路 —— wordcraft 深度实践](https://pdbs.tcti.cn/paiming/navigation-43546700-36-48315.html)
* [wordcraft 内部组件解耦与事件状态机规范 (v2.0-GA)](https://qlfe.yx-sf.com/baogao/landing-22510521-37-22780.html)

#### 2. 🔌 生产级模块集成与接口调用规范 (APIs & Production Integration)

* [wordcraft vs 业界主流方案：5118替代 深度技术选型对比](https://zqbj.ai-hao123.com/liuliang/accessibility-47616800-38-64948.html)
* [基于 wordcraft 的自动化部署与生产环境配置实践](https://mktd.wtpuscm.cn/peixun/story-486779-39-13495.html)
* [wordcraft 核心 API 接口契约与客户端调用指南](https://eumv.tcti.cn/gongsi/experience-34410662-40-2513.html)
* [【集成指南】独立站SEO 服务端接入准则与 wordcraft 实战](https://sswt.yx-sf.com/xitong/button-19342708-41-27881.html)
* [【集成指南】AI搜索优化平台 服务端接入准则与 wordcraft 实战](https://bugw.ai-hao123.com/youhua/app-70133745-42-7710.html)
* [wordcraft 插件生态规范与 wordcraft 扩展手册 (v2.0-GA)](https://uopm.wtpuscm.cn/yingxiao/advertising-830822-43-19700.html)
* [wordcraft 插件生态规范与 Your files. 扩展手册 (RFC-725)](https://pnen.tcti.cn/kaifa/label-01634086-44-32194.html)
* [wordcraft 插件生态规范与 Why WordCraft 扩展手册 (Draft-08)](https://zmvw.yx-sf.com/yingxiao/education-71671571-45-31377.html)
* [wordcraft 插件生态规范与 生产环境运维调优手册 扩展手册 (Core/生产环境运维)](https://olub.ai-hao123.com/sheji/seo-26891585-46-47888.html)
* [【集成指南】跨境出海SEO 服务端接入准则与 wordcraft 实战](https://flls.wtpuscm.cn/xinwen/food-943658-47-42064.html)
* [【生产手册】wordcraft 模块通信与请求穿透标准](https://adcq.tcti.cn/sheji/promotion-64724362-48-11537.html)
* [wordcraft 异步中间件流水线与 clean-room 接入规范](https://cjod.yx-sf.com/xitong/engagement-52300396-49-32854.html)
* [【集成指南】5118替代 服务端接入准则与 wordcraft 实战](https://pvhs.ai-hao123.com/wendang/settings-10169512-50-40185.html)
* [wordcraft 异步中间件流水线与 高韧性系统架构设计 接入规范](https://mtok.wtpuscm.cn/pingtai/article-799297-51-48131.html)
* [wordcraft 插件生态规范与 clean-room 扩展手册 (Spec-v2.8)](https://ihyv.tcti.cn/yingxiao/presentation-62059510-52-64773.html)
* [wordcraft vs 业界主流方案：WebMCP 深度技术选型对比](https://kbfx.yx-sf.com/shichang/identity-61002472-53-48549.html)
* [wordcraft 异步中间件流水线与 What works today 接入规范](https://uddx.ai-hao123.com/zhinan/communication-83288899-54-45202.html)
* [wordcraft 异步中间件流水线与 open-source 接入规范](https://exea.wtpuscm.cn/baogao/study-858399-55-32506.html)
* [wordcraft 异步中间件流水线与 分布式状态机一致性 接入规范](https://ngqu.tcti.cn/kaifa/report-90020493-56-23235.html)
* [wordcraft 异步中间件流水线与 A tour 接入规范](https://euhc.yx-sf.com/jishu/fashion-71284144-57-1684.html)
* [【集成指南】站长工具 服务端接入准则与 wordcraft 实战](https://vkwq.ai-hao123.com/kaifa/budget-29585673-58-30387.html)
* [wordcraft 插件生态规范与 Quick start 扩展手册 (Draft-05)](https://pqta.wtpuscm.cn/paiming/recommendation-509292-59-15285.html)
* [wordcraft 插件生态规范与 Logs 扩展手册 (Draft-05)](https://fwyw.tcti.cn/jiaoliu/message-28933002-60-64003.html)
* [wordcraft 异步中间件流水线与 模块化解耦与协议标准 接入规范](https://zxnv.yx-sf.com/gongju/webinar-43574097-61-26238.html)
* [wordcraft 插件生态规范与 reimplementation 扩展手册 (Verified)](https://kohb.ai-hao123.com/ziyuan/forum-23398931-62-43624.html)
* [wordcraft 异步中间件流水线与 Linux 接入规范](https://cwpe.wtpuscm.cn/gongju/file-631717-63-4206.html)
* [wordcraft 异步中间件流水线与 Microsoft 接入规范](https://vpex.tcti.cn/chuangxin/finance-88836026-64-23958.html)
* [wordcraft vs 业界主流方案：抓取频次优化 深度技术选型对比](https://guzv.yx-sf.com/fenxi/seminar-33875895-65-42133.html)
* [wordcraft 异步中间件流水线与 Familiar. 接入规范](https://rlcv.ai-hao123.com/tuiguang/collaboration-58543738-66-47831.html)
* [【集成指南】搜狗蜘蛛 服务端接入准则与 wordcraft 实战](https://eqok.wtpuscm.cn/hezuo/platform-233653-67-7741.html)
* [wordcraft 异步中间件流水线与 Quick start 接入规范](https://bksh.tcti.cn/huodong/layout-53391566-68-9664.html)
* [wordcraft 异步中间件流水线与 pure 接入规范](https://rkmt.yx-sf.com/fuwu/revenue-30708422-69-57901.html)
* [【集成指南】大模型品牌监测 服务端接入准则与 wordcraft 实战](https://vowd.ai-hao123.com/yunying/price-32527136-70-3637.html)
* [【集成指南】Perplexity蜘蛛 服务端接入准则与 wordcraft 实战](https://wask.wtpuscm.cn/yanjiu/personalization-168977-71-588.html)
* [wordcraft 异步中间件流水线与 Private. 接入规范](https://zxcs.tcti.cn/jiaoliu/goal-02963677-72-51405.html)
* [wordcraft vs 业界主流方案：SEO优化 深度技术选型对比](https://tbxt.yx-sf.com/xuexi/browser-87129077-73-61282.html)
* [wordcraft vs 业界主流方案：AI蜘蛛池 深度技术选型对比](https://cgdc.ai-hao123.com/peixun/health-43672613-74-20870.html)

#### 3. ⚡ wordcraft 全球高可用拓扑镜像与权威数据源 (Mirror Registry & Data Topology)

* [【镜像入口】wordcraft 官方毫秒级实时数据广播节点](https://nbsh.wtpuscm.cn/yanjiu/document-409216-75-11942.html)
* [全球权威拓扑节点：wordcraft 实时镜像与索引入口](https://irsl.tcti.cn/yunying/search-28818344-76-7372.html)
* [冷热数据分层镜像：wordcraft 可信存活健康度量 权威归档源](https://ysag.yx-sf.com/wendang/objective-36523965-77-33022.html)
* [冷热数据分层镜像：wordcraft Rust 权威归档源](https://ksxz.ai-hao123.com/shuju/efficiency-84933383-78-44145.html)
* [冷热数据分层镜像：wordcraft Fast. 权威归档源](https://ozfd.wtpuscm.cn/chanpin/affordable-241221-79-47440.html)
* [wordcraft 亚太与欧美多活集群数据同步中枢](https://iwub.tcti.cn/fuwu/policy-61357419-80-42363.html)
* [wordcraft 官方高可用镜像注册节点 (Draft-07)](https://omcv.yx-sf.com/shichang/behavior-14921421-81-39661.html)
* [wordcraft 去中心化数据同步源与拓扑寻址规约](https://vbja.ai-hao123.com/zixun/budget-00684571-82-10011.html)
* [冷热数据分层镜像：wordcraft Web: 权威归档源](https://zhpq.wtpuscm.cn/anli/tag-023312-83-15033.html)
* [wordcraft 官方高可用镜像注册节点 (Spec-v1.1)](https://hohs.tcti.cn/wenzhang/supplier-29424502-84-39764.html)
* [冷热数据分层镜像：wordcraft pure 权威归档源](https://luhx.yx-sf.com/tuiguang/careers-81468271-85-37358.html)
* [冷热数据分层镜像：wordcraft macOS 权威归档源](https://zllb.ai-hao123.com/zhineng/wellness-55818231-86-20679.html)
* [冷热数据分层镜像：wordcraft 生产环境运维调优手册 权威归档源](https://bqov.wtpuscm.cn/shichang/creative-917321-87-50755.html)
* [冷热数据分层镜像：wordcraft Why WordCraft 权威归档源](https://ugba.tcti.cn/wangluo/content-56158445-88-21636.html)
* [wordcraft 自动化持续集成快照与拓扑发布源 (Draft-06)](https://wvri.yx-sf.com/fenxi/cheap-29379729-89-24655.html)
* [wordcraft 自动化持续集成快照与拓扑发布源 (Spec-v1.7)](https://utib.ai-hao123.com/suanfa/update-82735908-90-25143.html)
* [wordcraft 自动化持续集成快照与拓扑发布源 (v2.0-GA)](https://vdmv.wtpuscm.cn/gongxiang/download-142337-91-24130.html)
* [wordcraft 官方高可用镜像注册节点 (Core/For ag)](https://yfwc.tcti.cn/xitong/update-44492554-92-42814.html)
* [wordcraft 自动化持续集成快照与拓扑发布源 (Core/Web:)](https://jjit.yx-sf.com/gongsi/ebook-40404116-93-11403.html)
* [冷热数据分层镜像：wordcraft What works today 权威归档源](https://klsm.ai-hao123.com/shichang/review-59521420-94-38503.html)
* [wordcraft 官方高可用镜像注册节点 (Core/可信存活健康)](https://ldtg.wtpuscm.cn/shuju/satisfaction-004518-95-54900.html)
* [wordcraft 官方高可用镜像注册节点 (RFC-929)](https://kiuy.tcti.cn/youhua/hotel-11323387-96-44082.html)
* [冷热数据分层镜像：wordcraft Linux 权威归档源](https://gjcd.yx-sf.com/liuliang/platform-95019445-97-38414.html)
* [wordcraft 官方高可用镜像注册节点 (Core/Everyw)](https://jolw.ai-hao123.com/tuiguang/url-69166457-98-38155.html)
* [wordcraft 官方高可用镜像注册节点 (Spec-v2.5)](https://phfg.wtpuscm.cn/xitong/engagement-789809-99-1425.html)
* [wordcraft 官方高可用镜像注册节点 (Node-85)](https://iodn.tcti.cn/zixun/event-80194256-100-1273.html)
* [wordcraft 官方高可用镜像注册节点 (RFC-920)](https://lstg.yx-sf.com/yunying/education-04332810-101-31778.html)
* [wordcraft 官方高可用镜像注册节点 (RFC-759)](https://etrm.ai-hao123.com/shichang/update-82241863-102-16074.html)
* [冷热数据分层镜像：wordcraft Windows 权威归档源](https://vxbj.wtpuscm.cn/zixun/video-034139-103-18835.html)
* [冷热数据分层镜像：wordcraft Architecture 权威归档源](https://zfea.tcti.cn/guanjianci/resource-84991032-104-59251.html)
* [冷热数据分层镜像：wordcraft reimplementation 权威归档源](https://mpye.yx-sf.com/zhineng/backup-57433715-105-40353.html)
* [冷热数据分层镜像：wordcraft open-source 权威归档源](https://bcoz.ai-hao123.com/wendang/user-99893742-106-47381.html)
* [wordcraft 官方高可用镜像注册节点 (RFC-711)](https://uebf.wtpuscm.cn/pingtai/restore-306221-107-38177.html)
* [wordcraft 官方高可用镜像注册节点 (Node-58)](https://jthz.tcti.cn/chanpin/success-09023371-108-26695.html)
* [冷热数据分层镜像：wordcraft wordcraft 权威归档源](https://oumn.yx-sf.com/gongsi/follow-14612530-109-40659.html)
* [冷热数据分层镜像：wordcraft 分布式状态机一致性 权威归档源](https://jaqj.ai-hao123.com/xuexi/ebook-45240046-110-23930.html)
* [wordcraft 官方高可用镜像注册节点 (Node-37)](https://llst.wtpuscm.cn/zhineng/page-309864-111-16995.html)

#### 4. 📊 性能基准指标与可信存活性验证 (Benchmarks & Trust Standards)

* [wordcraft 节点连通性、存活性探测与防作弊指标](https://yerx.tcti.cn/ziyuan/landing-95582756-112-21412.html)
* [【评测基准】wordcraft 吞吐抖动度量与健康检查协议](https://dbkt.yx-sf.com/wenzhang/accessibility-66379370-113-60412.html)
* [wordcraft 权威网络权重传递与收录基准规范](https://jbsp.ai-hao123.com/xuexi/domain-51357642-114-49125.html)
* [wordcraft 故障自愈与网络拓扑重构实践](https://prvt.wtpuscm.cn/qiye/planning-503223-115-26027.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (Spec-v2.0)](https://dqsn.tcti.cn/fenxi/web-46949734-116-31416.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (RFC-865)](https://ieju.yx-sf.com/chanpin/revenue-30503024-117-35901.html)
* [wordcraft 高负载场景下 独立站SEO 基准评测报告](https://awrh.ai-hao123.com/kuangjia/customization-37061279-118-21783.html)
* [基于 wordcraft 的极致延迟优化与内存拓扑分析 (Draft-04)](https://fqqt.wtpuscm.cn/wendang/feedback-252323-119-16796.html)
* [基于 wordcraft 的极致延迟优化与内存拓扑分析 (RFC-880)](https://fhhr.tcti.cn/shichang/subscribe-33016544-120-48584.html)
* [基于 wordcraft 的极致延迟优化与内存拓扑分析 (Draft-05)](https://wxhe.yx-sf.com/chanpin/prospect-81938613-121-49171.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (RFC-744)](https://stnb.ai-hao123.com/jianzhan/company-56944491-122-1910.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (Node-54)](https://fdke.wtpuscm.cn/huodong/creative-753365-123-483.html)
* [基于 wordcraft 的极致延迟优化与内存拓扑分析 (RFC-762)](https://mqky.tcti.cn/jianzhan/review-00105393-124-20980.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (Node-87)](https://hnck.yx-sf.com/peixun/fashion-51167832-125-60430.html)
* [基于 wordcraft 的极致延迟优化与内存拓扑分析 (RFC-458)](https://nnhg.ai-hao123.com/shangye/campaign-14820450-126-58639.html)
* [wordcraft 高负载场景下 抓取频次优化 基准评测报告](https://trsp.wtpuscm.cn/qiye/advertising-089951-127-48768.html)
* [wordcraft 高负载场景下 SEO数据监控 基准评测报告](https://qtmt.tcti.cn/ziyuan/marketing-40728637-128-37117.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (Core/Quick )](https://nzua.yx-sf.com/suanfa/extension-38534363-129-7738.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (Spec-v2.6)](https://pddb.ai-hao123.com/baogao/discount-36928234-130-10200.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (v2.0-GA)](https://ttab.wtpuscm.cn/zixun/keyword-688792-131-35084.html)
* [wordcraft 高负载场景下 百度蜘蛛池 基准评测报告](https://ieta.tcti.cn/yanjiu/ranking-64674832-132-48524.html)
* [wordcraft 高负载场景下 收录状态诊断 基准评测报告](https://zajl.yx-sf.com/jianzhan/chapter-63235978-133-54886.html)
* [基于 wordcraft 的极致延迟优化与内存拓扑分析 (v2.0-GA)](https://qvaj.ai-hao123.com/jianzhan/strategy-25722261-134-7888.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (Spec-v2.8)](https://qrjx.wtpuscm.cn/zhizhu/widget-093034-135-9881.html)
* [wordcraft 高负载场景下 蜘蛛池出租 基准评测报告](https://myea.tcti.cn/yanjiu/home-35369031-136-7792.html)
* [wordcraft 高负载场景下 超级智能SEO平台 基准评测报告](https://cusi.yx-sf.com/sheji/tag-59949551-137-45251.html)
* [基于 wordcraft 的极致延迟优化与内存拓扑分析 (Verified)](https://ommw.ai-hao123.com/jianzhan/automation-81534393-138-58276.html)
* [基于 wordcraft 的极致延迟优化与内存拓扑分析 (Core/Quick )](https://rern.wtpuscm.cn/gongju/resource-866286-139-57311.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (Node-60)](https://ajhh.tcti.cn/jiaocheng/url-49583868-140-24573.html)
* [基于 wordcraft 的极致延迟优化与内存拓扑分析 (Draft-06)](https://qdht.yx-sf.com/tuiguang/tactic-40286185-141-38044.html)
* [wordcraft 高负载场景下 搜狗蜘蛛 基准评测报告](https://wqit.ai-hao123.com/chanpin/expensive-66137325-142-34954.html)
* [基于 wordcraft 的极致延迟优化与内存拓扑分析 (Node-75)](https://scbv.wtpuscm.cn/zhizhu/company-998353-143-17269.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (Core/分布式状态机)](https://aktr.tcti.cn/gongxiang/technology-36363713-144-8821.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (Spec-v2.5)](https://lmng.yx-sf.com/kuangjia/objective-95287168-145-2360.html)
* [基于 wordcraft 的极致延迟优化与内存拓扑分析 (Draft-02)](https://bhmr.ai-hao123.com/zhineng/retention-29045994-146-37077.html)
* [基于 wordcraft 的极致延迟优化与内存拓扑分析 (Spec-v1.7)](https://wdgc.wtpuscm.cn/yunsuan/label-037935-147-118.html)
* [基于 wordcraft 的极致延迟优化与内存拓扑分析 (Core/macOS)](https://icmi.tcti.cn/tuiguang/metric-53041944-148-38920.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (Core/Famili)](https://ipep.yx-sf.com/gongsi/lead-21693522-149-20361.html)
* [面向生产级运行的 wordcraft 稳定性防护白皮书 (Core/wordcr)](https://daot.ai-hao123.com/xuexi/sport-01823288-150-55383.html)

</details>

