<p align="center">
  <img src="https://i.postimg.cc/BZm16C5S/Nexus-Force-Icon-T.png" alt="NexusForge" width="50"/>
</p>

<h1 align="center">NexusForge</h1>
<p align="center">
  <strong>The intelligent archiver.</strong><br>
  Create <code>.nxs</code> archives that are smaller, safer, and smarter than traditional formats.
</p>

<p align="center">
  <img src="https://i.postimg.cc/FHVvrTcy/Nxs-Forge-Logo-big.png" alt="NexusForge" width="550"/>
</p>



## ✨ Why NexusForge?

Old archivers treat your files like a bag of bytes.  
**NexusForge understands them.**

It analyses every file *before* compressing, applies smart lossless transforms, and packs everything with a modern, multi‑threaded engine. The result? Archives that are **smaller than ZIP**, **faster to extract than 7z**, and come with **self‑repair** built right in.

---

## ⚡ Key advantages

| Feature | NexusForge | WinRAR | 7‑Zip |
|--------|------------|--------|-------|
| **Content‑aware compression** | ✅ Smart pre‑filters for text, code, audio | ❌ | ❌ |
| **Authenticated encryption** | ✅ AES‑256‑GCM (tamper‑proof) | ⚠️ AES without auth | ⚠️ AES without auth |
| **Random access in solid archives** | ✅ Instant single‑file extraction | ❌ | ❌ |
| **In‑place rename** | ✅ Rename without re‑packing | ❌ | ❌ |
| **Extraction cache** | ✅ Open a file once – instant next time | ❌ | ❌ |
| **VirusTotal integration** | ✅ Scan any file inside a forge | ❌ | ❌ |
| **Split & merge** | ✅ Split large forges; merge for free | ✅ | ❌ |
| **Self‑repair records** | ✅ Reed‑Solomon, 0–100% redundancy | ✅ RAR 5.0, 0–100% | ❌ (external PAR) |
| **Modern dark UI** | ✅ Clean, professional interface | ⚠️ dated | ⚠️ minimal |

---

## 🧠 Intelligent compression

NexusForge doesn't just "zip" your data. It **classifies** every file and applies a reversible filter before compression, making patterns more visible to the backend.

- **Text & structured data** – replaces common words, XML/HTML tags, SQL keywords with short tokens
- **Executable code** – transforms x86 relative jumps to absolute offsets, turning code into highly compressible patterns (with automatic self‑verification to avoid corruption on packed installers)
- **Audio (16‑bit PCM WAV)** – second‑order predictor delta encoding turns samples into tiny residuals
- **Already‑compressed media** (MP3, JPEG, MP4, etc.) – automatically detected and stored without re‑compression
- **Large files** (>64 MB) – streamed directly through Zstd with zero memory spikes

The result? Up to **40% smaller archives** on real‑world data compared to plain ZIP or 7‑Zip with default settings. The self‑verifying executable filter guarantees zero hash mismatches, no matter what file type you compress.

---

## 🔐 Strong, tamper‑proof encryption

Encrypt your forge with **AES‑256‑GCM** – the gold standard for authenticated encryption.

- Every entry is encrypted independently with a unique salt and authentication tag
- **Tamper detection** – if even a single byte is modified, extraction fails immediately with a clear error
- **Wrong password?** You get a clean "Wrong password" message, not garbage data
- **Chunked streaming encryption** handles files of **any size** without memory spikes
- **Password caching per session** – enter it once, access all encrypted files instantly
- **Per‑entry encryption** – each file gets its own derived key; one password unlocks all

---

## 🛡️ Self‑repair records

Corrupted archives are a nightmare. NexusForge can **heal itself**.

- Add **recovery records** (Reed‑Solomon error correction) to any forge during creation
- Per‑shard integrity validation detects exactly which parts are damaged
- Repair engine streams recovery data segment‑by‑segment – no full‑file RAM loading
- **Free:** up to 5% redundancy – survives minor damage, bit‑rot, or bad sectors
- **Pro:** up to 100% redundancy – even if half the archive is destroyed, everything can be recovered
- **Live progress** – percentage updates as each segment is processed
- Cancellation support – stop the repair at any time

Unlike WinRAR, which cannot repair archives with encrypted file names without a recovery record, NexusForge's recovery records work reliably regardless of encryption state.

---

## 📂 Modern file management

Browse your archives without extracting a single byte.

- **Folder‑based navigation** – see the directory tree, jump into sub‑folders, and see files
- **Live grid** – file names (short), sizes (human‑readable: KB/MB/GB), compressed sizes, compression method (Store/Deflate/Nexus), xxHash3 checksum
- **In‑place rename** – change file names inside the forge without extracting or re‑compressing it
- **Context menus** – right‑click any file to Open, Extract, Scan (On VirusTotal), or Copy its path
- **Extraction cache** – open a file once, and it's available instantly the next time (even encrypted files, after you enter the password once)
- **VirusTotal scan** – right‑click any file inside a forge to scan its xxHash3 against VirusTotal's database
- **Settings** – preserve folder structure, default compression method/level, cache controls, password preferences

---

## ⚡ Instant extraction, always

- **Random access in solid archives** – extract a single file from a massive solid forge without decompressing the whole thing (not all archive apps can do this)
- **Streaming decompression** – files flow to disk while verifying integrity; no full‑file buffering
- **On‑the‑fly decryption** – encrypted files are decrypted as they're read, not loaded into RAM
- **Real‑time progress** – separate progress bars for extraction and copy phases
- **Cancellation at any time** – cancel mid‑extraction; partially copied files are deleted automatically

---

## ✂️ Split and merge

Split a large forge into smaller parts for easier sharing or uploading.

- **Split** – create `.nxs.1`, `.nxs.2`, … each with your chosen part size (in MB)
- **Manifest file** – `.nxsmanifest` stores the original filename, part count, file size, and xxHash3 for verification
- **Merge** – reassemble the original forge perfectly, with xxHash3 verification
- **Merge is free** – anyone can put the pieces back together without a license
- **Split is Pro** – a power‑user feature for sharing large archives
- **Custom output folder** – choose where parts are saved, or use the default `{FileName} Split Parts` folder
- **Encrypted forges** – split and merge work with password‑protected archives

---

## 🖥️ Clean, dark UI

A modern, professional interface that stays out of your way.

- **Dark theme** – easy on the eyes, designed for long sessions
- **Ribbon‑style main window** – New Forge, Open Forge, Split Forge, Merge Forge, Repair Forge at your fingertips
- **Dedicated compression form** – file‑wise progress with cancel support
- **Dedicated extraction form** – overall + per‑file progress.
- **Multi‑instance extraction** – run multiple extraction jobs simultaneously
- **Alert notifications** – modern, auto‑dismissing completion messages
- **File association** – `.nxs` files show a custom icon and description in Windows Explorer

---

## ⌨️ Command‑line interface (Pro)

Automate everything with the powerful CLI.

```bash
# Create a forge with maximum compression
NexusForge.CLI a myForge C:\MyFolder -method 1000 -level Ultra

# List contents
NexusForge.CLI l myForge.nxs

# Extract a single file
NexusForge.CLI x myForge.nxs readme.txt -out D:\Backup

# Extract with password
NexusForge.CLI x myForge.nxs -out D:\Out -p MySecret123

# Split for upload (100 MB parts)
NexusForge.CLI split myForge.nxs -size 100

# Merge parts back
NexusForge.CLI merge myForge.nxs.nxsmanifest -out merged.nxs

# Repair a damaged forge
NexusForge.CLI r damaged.nxs repaired.nxs
```

### CLI options

Supported compression methods:

| Method | Name |
|----------|----------|
| `0` | Store |
| `1` | Deflate |
| `1000` | Nexus |

Compression presets:

- Store
- Fast
- Balanced *(default)*
- High
- Ultra

Common options:

| Option | Description |
|----------|----------|
| `-rr` | Recovery record percentage |
| `-p` | Archive password |
| `-out` | Output directory |
| `-size` | Split part size in MB |

Additional CLI features:

- Modern colored console output
- Real-time progress bars
- Styled help text
- Detailed operation statistics
- Cancellation support

---

## 🔬 VirusTotal integration

Check any file inside a forge against VirusTotal's database of 70+ antivirus engines.

- Right-click → **Scan with VirusTotal** on any file in the archive browser
- Uses the file's **SHA-256** to query VirusTotal without extracting the file first
- If the hash is unknown, the file can be extracted temporarily and uploaded for analysis
- Results display how many engines flagged the file
- Direct link to the full VirusTotal report
- Requires a free VirusTotal API key configured in Settings

---

## 💾 The .nxs format

The `.nxs` format is purpose-built for NexusForge — a modern, 64-bit clean binary archive format.

- **64-bit sizes everywhere** — no 4 GB file-size wall
- **Per-entry xxHash3 verification** during extraction
- **AES-256-GCM authenticated encryption**
- **Reed-Solomon recovery blocks** with per-shard validation
- **Self-describing signatures** for easy identification in hex editors
- **Extensible metadata fields** for future enhancements
- **Content-aware compression methods** including Nexus mode

### Format highlights

| Feature | .nxs |
|----------|----------|
| Maximum archive size | Practically unlimited |
| Maximum file size | Practically unlimited |
| Integrity verification | xxHash3 |
| Encryption | AES-256-GCM |
| Recovery records | Reed-Solomon |
| Random access | Yes |
| Solid archives | Yes |
| Content-aware compression | Yes |

---

## 🚀 Getting started

1. Download the latest release from the Releases page
2. Install and launch NexusForge
3. Click **Create Forge**
4. Add files or folders
5. Choose compression, encryption, and recovery settings
6. Click **Create Forge**

Your `.nxs` forge is now ready.

To open an existing archive:

1. Click **Open Forge** or double-click an **.nxs** file
2. Select the `.nxs` file
3. Browse, extract, rename, or scan files instantly

---

## 💎 Free vs Pro

| Capability | Free | Pro |
|------------|------|------|
| Create & extract `.nxs` archives | ✅ | ✅ |
| Content-aware compression (Nexus) | ✅ | ✅ |
| AES-256-GCM encryption | ✅ | ✅ |
| Self-repair records | Up to 5% | Up to 100% |
| Command-line interface | ❌ | ✅ |
| Split archives | ❌ | ✅ |
| Merge archives | ✅ | ✅ |
| VirusTotal integration | ✅ | ✅ |
| Extraction cache | ✅ | ✅ |
| Commercial use | ❌ | ✅ |

Upgrade to Pro from the **Application** or visit **https://njac.shop/products/nexusforge**.

---

## 📥 System requirements

- Windows 10 or later
- 64-bit operating system recommended
- .NET 9 Runtime *(included with installer)*
- 4 GB RAM minimum
- 8 GB+ RAM recommended for large archives
- Approximately 200 MB of free disk space

---

## 🧰 Contributing

Found a bug or have a feature suggestion?

- Open an issue
- Submit a pull request
- Share feature requests and feedback

Please read the Contributing Guide before opening a PR.

---

## 📜 License

NexusForge is proprietary software.

- Free for personal, non-commercial use
- Commercial use requires a valid Pro license
- Some advanced features are available only in Pro editions

See the `LICENSE` file for complete licensing terms.

---

<p align="center">
Made with 💖 by the <b>NJAC</b><br>
<a href="https://njac.shop">njac.shop</a> •
<a href="mailto:support@njac.shop">support@njac.shop</a>
  <a href="mailto:njac@tuta.io">njac@tuta.io</a>
</p>
