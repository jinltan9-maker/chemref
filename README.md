# ChemRef — Compound Tracker for Microsoft Word

ChemRef is a free Microsoft Word add-in designed for authors of manuscripts that contain chemical structures. It acts as a compound dictionary within your document, letting you register compounds with a structure image, compound code, IUPAC name, and optional alternate identifier. Insert tracked references anywhere in your manuscript — when you update a compound in the dictionary, every reference in the document updates automatically.

**Features:**
- **Compound dictionary** — register compounds with a structure image (upload or paste from clipboard), compound code, IUPAC name, Other Identifier, and optional structure file attachments (.cdx, .mol, .sdf)
- **Dynamic references** — insert tracked compound codes or names into your manuscript that update automatically when the dictionary changes
- **Uniqueness enforcement** — prevents duplicate codes, names, or other identifiers across compounds
- **Batch renumbering** — freely re-assign all compound codes at once (e.g. after a reviewer request) with collision-free validation on apply
- **Consistency checking** — automatically detects when a collaborator has edited a reference directly in the document without the add-in
- **Unlinked reference scanning** — finds plain text in the document that matches a compound code or name but is not tracked by ChemRef
- **Reference type switching** — change what a reference displays (code, name, or Other ID) without deleting and reinserting
- **Flatten for submission** — strip all ChemRef metadata and convert references to plain text before submitting to a journal
- **Collaborator compatible** — all data is stored inside the .docx file; collaborators without ChemRef see references as normal text
- **Cross-platform** — works on Word for Windows, Mac, and Web

No external servers, no accounts, no data collection. Everything stays in your document.

---

## Setup

### Word on the Web

1. Download `manifest.xml` from this repository (click the file, then click the download button)
2. Open a Word document at [word.new](https://word.new) or in OneDrive
3. In the top search bar, search **Add-ins**
4. Click **More Add-ins**
5. Select **Manage My Add-ins** → **Upload**
6. Upload `manifest.xml` from your computer

### Word for Windows (Desktop)

#### Part A — One-time folder and Windows sharing

1. Create a folder, for example: `C:\OfficeAddins`
2. Copy `manifest.xml` into that folder
3. Right-click the folder → **Properties** → **Sharing** tab → **Share** (or Advanced Sharing)
4. Share with your own account (Read access is sufficient)
5. Copy the network path shown by Windows, for example: `\\YOUR-PC-NAME\OfficeAddins`

#### Part B — Trust the catalog in Word (one-time)

1. Close Word completely
2. Open Word → **File** → **Options** → **Trust Center** → **Trust Center Settings**
3. Select **Trusted Add-in Catalogs** on the left
4. In **Catalog Url**, paste your UNC path: `\\YOUR-PC-NAME\OfficeAddins` (must be `\\computer\share` format, not `C:\...`)
5. Check **Show in Menu**
6. Click **OK** → **OK**
7. Restart Word

#### Part C — Install ChemRef

1. Open Word
2. Find the **Add-ins** button in the ribbon (Home or Insert tab)
3. Click **Advanced...**
4. Select **ChemRef** → **Add** (or Install)

---

## Usage

Click the **ⓘ About** icon in the ChemRef panel for a built-in guide covering all features.

**Quick start:**
1. Open ChemRef from the ribbon
2. Click **+ Add New** to register a compound with a structure image, code, and IUPAC name
3. Place your cursor in the document and click **Insert** on any compound card
4. Choose whether to insert the compound code, IUPAC name, or Other Identifier
5. Edit a compound in the dictionary — all references in the document update automatically

---

## License

Licensed under the [MIT License with Commons Clause](LICENSE) — free to use, modify, and share, but may not be sold.

Developed by Jinlong Tan. Built with Claude (Opus 4.6) by Anthropic.
