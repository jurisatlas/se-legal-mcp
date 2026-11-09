# Sweden Legal Research MCP Server (`se-legal-mcp`)

**[Svenska](#lang-sv) | [English Documentation](#english-documentation)**

---

<a id="lang-sv"></a>
## Rättslig MCP-server för lagstiftning och rättspraxis (`se-legal-mcp`) — Svenska

### Om detta arkiv

Detta arkiv innehåller en Model Context Protocol (MCP) server som ansluter din AI-applikation (Claude Desktop, Cursor, Windsurf, VS Code / Copilot, Cline eller Antigravity) direkt till officiella författningssamlingar och rättsfallsdatabaser för **Sweden** (första instans, hovrätter/kammarrätter samt högsta domstolar).

### Installation (Val av AI-applikation)

1. **Ladda ner:** Klicka på **`<> Code` -> `Download ZIP`** uppe till höger och packa upp mappen på din dator.
2. **Starta installationsguiden:** Dubbelklicka på **`Click_Here_To_Install_Windows.bat`** (Windows) eller **`Click_Here_To_Install_Mac.command`** (macOS).
3. **Välj AI-klient:** Markera de AI-program du använder (Claude, Cursor, Windsurf, VS Code, Antigravity), klicka på installera och starta om din AI-applikation.

**Säkerhetsinformation:** Installationsprogrammet arbetar i skrivskyddat läge (read-only) och läser eller ändrar inga personliga filer på din dator.

### Domstolshierarki och officiella källor

| Instans | Domstolar som omfattas |
|:---|:---|
| **1:a instans (Underrätter)** | 48 Tingsrätter (District Courts), 12 Förvaltningsrätter (Administrative Courts) & Mark- och miljödomstolar |
| **2:a instans (Överrätter / Appellationsdomstolar)** | 6 Hovrätter (Svea, Göta, Skåne och Blekinge, Västra Sverige, Nedre Norrland, Övre Norrland) & 4 Kammarrätter (Stockholm, Göteborg, Sundsvall, Jönköping) |
| **Högsta instans (Högsta domstolar)** | Högsta domstolen (HD), Högsta förvaltningsdomstolen (HFD), Arbetsdomstolen & Mark- och miljööverdomstolen |

- **Riksdagen Open Data JSON API (data.riksdagen.se - Svensk författningssamling SFS):** [https://www.riksdagen.se](https://www.riksdagen.se) (`riksdagen.se`, `lagrummet.se`, `regeringen.se`)
- **Domstolsverket Vägledande avgöranden (rattspraxis.etjanst.domstol.se — HD, HFD, Hovrätter & Kammarrätter):** [https://rattspraxis.etjanst.domstol.se](https://rattspraxis.etjanst.domstol.se) (`domstol.se`, `hogstadomstolen.se`, `lagrummet.se`)

---

<a id="english-documentation"></a>
## English Documentation

Model Context Protocol (MCP) server providing live, read-only access to **Sweden (SE)** legislation, official gazettes, multi-tier judicial decisions (First Instance, Regional/Cantonal/Appellate, and Supreme/Constitutional courts, including HTML and PDF full-text extraction), and statutory citation verification across all major AI clients (**ChatGPT Desktop, OpenAI Codex CLI, Claude Desktop, Claude Code CLI, Cursor, Windsurf, VS Code / GitHub Copilot / Cline / Roo Code, Google Antigravity / Gemini CLI, Perplexity, and Continue.dev**).

---

### Interactive Desktop Setup (Select Your AI Assistant)

This package includes a graphical installer for legal practitioners and non-technical users that lets you select which AI application(s) you use:

1. **Download:** Click **`<> Code`** at the top right of this repository, select **`Download ZIP`**, and extract the folder to your computer.
2. **Run the Setup Utility:**
   - **Windows:** Double-click `Click_Here_To_Install_Windows.bat`
   - **macOS:** Double-click `Click_Here_To_Install_Mac.command`
3. **Select Your AI Client(s) & Connect:** Check the box(es) for the AI assistant(s) installed on your computer (**ChatGPT Desktop & OpenAI Codex CLI**, **Claude Desktop & Claude Code CLI**, **Cursor**, **Windsurf**, **VS Code / GitHub Copilot / Cline / Roo Code**, **Google Antigravity / Gemini CLI**, or **Perplexity / Continue.dev**), click **Install to Selected AI Clients**, and restart your selected AI application.

**System Integrity Note:** The setup utility operates strictly in read-only mode with respect to your personal files and documents. It installs an isolated Python runtime inside the extracted folder and registers the server entry only in the AI client configuration files you select.

---

### Multi-Tier Judicial Hierarchy & Live Indexed National Archives

This server performs live queries across the full judicial hierarchy and official legal archives of **Sweden**, extracting full text from both HTML pages and official court/gazette PDF judgments:

| Judicial Tier | Covered Courts & Tribunals |
|:---|:---|
| **Tier 1 — First Instance** | 48 Tingsrätter (District Courts), 12 Förvaltningsrätter (Administrative Courts) & Mark- och miljödomstolar |
| **Tier 2 — Regional / Cantonal / Appellate** | 6 Hovrätter (Svea, Göta, Skåne och Blekinge, Västra Sverige, Nedre Norrland, Övre Norrland) & 4 Kammarrätter (Stockholm, Göteborg, Sundsvall, Jönköping) |
| **Tier 3 — Supreme & Constitutional** | Högsta domstolen (HD), Högsta förvaltningsdomstolen (HFD), Arbetsdomstolen & Mark- och miljööverdomstolen |

#### Official Portals & Live Indexed Domains

- **National Legislation & Official Gazette:** Riksdagen Open Data JSON API (data.riksdagen.se - Svensk författningssamling SFS) — [https://www.riksdagen.se](https://www.riksdagen.se)
  - *Indexed Legislation Domains:* `riksdagen.se`, `lagrummet.se`, `regeringen.se`
- **Court Decisions & Jurisprudence Archives:** Domstolsverket Vägledande avgöranden (rattspraxis.etjanst.domstol.se — HD, HFD, Hovrätter & Kammarrätter) — [https://rattspraxis.etjanst.domstol.se](https://rattspraxis.etjanst.domstol.se)
  - *Indexed Judicial & Open Case Law Domains:* `domstol.se`, `hogstadomstolen.se`, `lagrummet.se`

---

### Available MCP Tools

| Tool | Description |
|:---|:---|
| `search_legislation` | Searches enacted statutes, codes, decrees, and official gazette publications in Sweden. |
| `search_case_law` | Searches national jurisprudence and open judicial archives for Sweden. |
| `search_tiered_court_decisions` | Filters case law specifically by judicial instance (`first_instance`, `appellate_regional`, `supreme_constitutional`) or specific regional/cantonal/district court. |
| `list_court_hierarchy` | Returns the complete 3-tier court structure and supported regional court filters for Sweden. |
| `get_legal_document_markdown` | Retrieves full statutory or judicial texts (both HTML and official `.pdf` court judgments) and converts them into clean Markdown. |
| `verify_citation` | Validates statutory and case law citations against official registries. |

---

<details>
<summary><b>Manual Configuration for Developers (Optional)</b></summary>

```json
{
  "mcpServers": {
    "se-legal-mcp": {
      "command": "uvx",
      "args": [
        "--from",
        "https://github.com/jurisatlas/se-legal-mcp/archive/refs/heads/main.zip",
        "se-legal-mcp"
      ]
    }
  }
}
```
</details>
