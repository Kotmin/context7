# Context7 MCP - Aktualna dokumentacja kodu dla każdego promptu

[![Website](https://img.shields.io/badge/Website-context7.com-blue)](https://context7.com) [![smithery badge](https://smithery.ai/badge/@upstash/context7-mcp)](https://smithery.ai/server/@upstash/context7-mcp) [![NPM Version](https://img.shields.io/npm/v/%40upstash%2Fcontext7-mcp?color=red)](https://www.npmjs.com/package/@upstash/context7-mcp) [![MIT licensed](https://img.shields.io/npm/l/%40upstash%2Fcontext7-mcp)](./LICENSE)

[![Install MCP Server](https://cursor.com/deeplink/mcp-install-dark.svg)](https://cursor.com/en/install-mcp?name=context7&config=eyJ1cmwiOiJodHRwczovL21jcC5jb250ZXh0Ny5jb20vbWNwIn0%3D) [<img alt="Install in VS Code (npx)" src="https://img.shields.io/badge/Install%20in%20VS%20Code-0098FF?style=for-the-badge&logo=visualstudiocode&logoColor=white">](https://insiders.vscode.dev/redirect?url=vscode%3Amcp%2Finstall%3F%7B%22name%22%3A%22context7%22%2C%22command%22%3A%22npx%22%2C%22args%22%3A%5B%22-y%22%2C%22%40upstash%2Fcontext7-mcp%40latest%22%5D%7D)

[![繁體中文](https://img.shields.io/badge/docs-繁體中文-yellow)](./docs/README.zh-TW.md) [![简体中文](https://img.shields.io/badge/docs-简体中文-yellow)](./docs/README.zh-CN.md) [![日本語](https://img.shields.io/badge/docs-日本語-b7003a)](./docs/README.ja.md) [![한국어 문서](https://img.shields.io/badge/docs-한국어-green)](./docs/README.ko.md) [![Documentación en Español](https://img.shields.io/badge/docs-Español-orange)](./docs/README.es.md) [![Documentation en Français](https://img.shields.io/badge/docs-Français-blue)](./docs/README.fr.md) [![Documentação em Português (Brasil)](<https://img.shields.io/badge/docs-Português%20(Brasil)-purple>)](./docs/README.pt-BR.md) [![Documentazione in italiano](https://img.shields.io/badge/docs-Italian-red)](./docs/README.it.md) [![Dokumentasi Bahasa Indonesia](https://img.shields.io/badge/docs-Bahasa%20Indonesia-pink)](./docs/README.id-ID.md) [![Dokumentation auf Deutsch](https://img.shields.io/badge/docs-Deutsch-darkgreen)](./docs/README.de.md) [![Документация на русском языке](https://img.shields.io/badge/docs-Русский-darkblue)](./docs/README.ru.md) [![Українська документація](https://img.shields.io/badge/docs-Українська-lightblue)](./docs/README.uk.md) [![Türkçe Doküman](https://img.shields.io/badge/docs-Türkçe-blue)](./docs/README.tr.md) [![Arabic Documentation](https://img.shields.io/badge/docs-Arabic-white)](./docs/README.ar.md) [![Tiếng Việt](https://img.shields.io/badge/docs-Tiếng%20Việt-red)](./docs/README.vi.md)[![Türkçe Doküman](https://img.shields.io/badge/docs-Türkçe-blue)](./docs/README.tr.md) [![Tiếng Việt](https://img.shields.io/badge/docs-Tiếng%20Việt-red)](./docs/README.vi.md) [![Polish Documentation](https://img.shields.io/badge/docs-Polish-green)](./docs/README.pl.md) 

## ❌ Bez Context7

LLM-y polegają na nieaktualnych lub ogólnych informacjach o używanych przez Ciebie bibliotekach. Jakie to ma skutki:

- ❌ Przykłady kodu są nieaktualne i oparte na wieloletnich danych treningowych
- ❌ Halucynujące API, które w ogóle nie istnieją
- ❌ Ogólne odpowiedzi dla starych wersji pakietów

## ✅ Z Context7

Context7 MCP pobiera aktualną, sprecyzowaną dla wersji dokumentację i przykłady kodu prosto ze źródła — i umieszcza je bezpośrednio w Twoim promcie.

Dodaj `use context7` do swojego promptu w Cursor:

```txt
Stwórz Next.js middleware, który sprawdzi poprawność ważność tokenu JWT w ciasteczkach i przekieruje nie zautoryzowanych użytkowników do `/login`. Używajmy context7
```

```txt
Skonfiguruj Cloudflare Worker script do tworzenia cache odpowiedzi JSON API przez 5 minut. Używajmy context7
```

Context7 pobiera aktualne przykłady kodu i dokumentację bezpośrednio do kontekstu Twojego LLM-a.

- 1️⃣ Napisz swój prompt naturalnie
- 2️⃣ Powiedz LLM-owi, aby użył `use context7`
- 3️⃣ Otrzymaj poprawny kod w odpowiedzi

Bez skakania po kartach przeglądarki, bez halucynajcji API, bez generowania przestarzałego kodu.

## 📚 Dodawanie projektów

Zobacz nasz [przewodnik dodawania projektów](./docs/adding-projects.md), aby dowiedzieć się, jak dodać (lub zaktualizować) swoje ulubione biblioteki w Context7.

## 🛠️ Instalacja

### Wymagania

- Node.js >= v18.0.0
- Cursor, Claude Code, VSCode, Windsurf lub inny klient MCP
- Klucz API Context7 (opcjonalny dla wyższych limitów zapytań) (Zdobądź swój, tworząc konto na [context7.com/dashboard](https://context7.com/dashboard))

> [!WARNING]
> **Komunikat o wycofaniu protokołu SSE**
>
> Protokół transportowy Server-Sent Events (SSE) jest wycofywany i jego endpoint zostanie usunięty w nadchodzących wydaniach. Zamiast tego używaj metod transportu HTTP lub stdio.

<details>
<summary><b>Instalacja przez Smithery</b></summary>

Aby automatycznie zainstalować Context7 MCP Server dla dowolnego klienta za pomocą [Smithery](https://smithery.ai/server/@upstash/context7-mcp):

```bash
npx -y @smithery/cli@latest install @upstash/context7-mcp --client <CLIENT_NAME> --key <YOUR_SMITHERY_KEY>
```

Swój klucz Smithery znajdziesz na [stronie Smithery.ai](https://smithery.ai/server/@upstash/context7-mcp).

</details>

<details>
<summary><b>Instalacja w Cursor</b></summary>

Przejdź do: `Settings` -> `Cursor Settings` -> `MCP` -> `Add new global MCP server`

Zalecane podejście to wklejenie poniższej konfiguracji do pliku `~/.cursor/mcp.json` w Cursor. Można też zainstalować c7 w konkretnym projekcie, tworząc `.cursor/mcp.json` w katalogu projektu. Zobacz [dokumentację Cursor MCP](https://docs.cursor.com/context/model-context-protocol), aby uzyskać więcej informacji.

> Od Cursor 1.0 możesz kliknąć przycisk instalacji poniżej, aby skorzystać z instalacji jednym kliknięciem.

#### Cursor – połączenie zdalne z serwerem

[![Install MCP Server](https://cursor.com/deeplink/mcp-install-dark.svg)](https://cursor.com/en/install-mcp?name=context7&config=eyJ1cmwiOiJodHRwczovL21jcC5jb250ZXh0Ny5jb20vbWNwIn0%3D)

```json
{
  "mcpServers": {
    "context7": {
      "url": "https://mcp.context7.com/mcp",
      "headers": {
        "CONTEXT7_API_KEY": "YOUR_API_KEY"
      }
    }
  }
}
```

#### Cursor – połączenie lokalne z serwerem

[![Install MCP Server](https://cursor.com/deeplink/mcp-install-dark.svg)](https://cursor.com/en/install-mcp?name=context7&config=eyJjb21tYW5kIjoibnB4IC15IEB1cHN0YXNoL2NvbnRleHQ3LW1jcCJ9)

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

</details>

<details>
<summary><b>Instalacja w Claude Code</b></summary>

Uruchom to polecenie. Zobacz [Claude Code MCP docs](https://docs.anthropic.com/en/docs/claude-code/mcp), aby uzyskać więcej informacji.

#### Claude Code – połączenie zdalne

```sh
claude mcp add --transport http context7 https://mcp.context7.com/mcp --header "CONTEXT7_API_KEY: YOUR_API_KEY"
```

#### Claude Code – połączenie lokalne

```sh
claude mcp add context7 -- npx -y @upstash/context7-mcp --api-key YOUR_API_KEY
```

</details>

<details>
<summary><b>Instalacja w Windsurf</b></summary>

Dodaj to do pliku konfiguracyjnego MCP Windsurf. Zobacz [Windsurf MCP docs](https://docs.windsurf.com/windsurf/cascade/mcp), aby uzyskać więcej informacji.

#### Windsurf – połączenie zdalne

```json
{
  "mcpServers": {
    "context7": {
      "serverUrl": "https://mcp.context7.com/mcp",
      "headers": {
        "CONTEXT7_API_KEY": "YOUR_API_KEY"
      }
    }
  }
}
```

#### Windsurf – połączenie lokalne

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

</details>

<details>
<summary><b>Instalacja w VS Code</b></summary>

[<img alt="Install in VS Code (npx)" src="https://img.shields.io/badge/VS_Code-VS_Code?style=flat-square&label=Install%20Context7%20MCP&color=0098FF">](https://insiders.vscode.dev/redirect?url=vscode%3Amcp%2Finstall%3F%7B%22name%22%3A%22context7%22%2C%22command%22%3A%22npx%22%2C%22args%22%3A%5B%22-y%22%2C%22%40upstash%2Fcontext7-mcp%40latest%22%5D%7D)
[<img alt="Install in VS Code Insiders (npx)" src="https://img.shields.io/badge/VS_Code_Insiders-VS_Code_Insiders?style=flat-square&label=Install%20Context7%20MCP&color=24bfa5">](https://insiders.vscode.dev/redirect?url=vscode-insiders%3Amcp%2Finstall%3F%7B%22name%22%3A%22context7%22%2C%22command%22%3A%22npx%22%2C%22args%22%3A%5B%22-y%22%2C%22%40upstash%2Fcontext7-mcp%40latest%22%5D%7D)

Dodaj to do pliku konfiguracyjnego MCP w VS Code. Zobacz [VS Code MCP docs](https://code.visualstudio.com/docs/copilot/chat/mcp-servers), aby uzyskać więcej informacji.

#### VS Code – połączenie zdalne

```json
"mcp": {
  "servers": {
    "context7": {
      "type": "http",
      "url": "https://mcp.context7.com/mcp",
      "headers": {
        "CONTEXT7_API_KEY": "YOUR_API_KEY"
      }
    }
  }
}
```

#### VS Code – połączenie lokalne

```json
"mcp": {
  "servers": {
    "context7": {
      "type": "stdio",
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

</details>

<details>
<summary>
<b>Instalacja w Cline</b>
</summary>

Możesz łatwo zainstalować Context7 poprzez [Cline MCP Server Marketplace](https://cline.bot/mcp-marketplace), postępując zgodnie z tymi instrukcjami:

1. Otwórz **Cline**.
2. Kliknij ikonę hamburgera (☰), aby przejść do sekcji **MCP Servers**.
3. Użyj paska wyszukiwania w zakładce **Marketplace**, aby znaleźć _Context7_.
4. Kliknij przycisk **Install**.

Lub możesz bezpośrednio edytować konfigurację serwerów MCP:

1. Otwórz **Cline**.
2. Kliknij ikonę hamburgera (☰), aby wejść do sekcji **MCP Servers**.
3. Wybierz zakładkę **Remote Servers**.
4. Kliknij **Edit Configuration**.
5. Dodaj context7 do `mcpServers`:

```json
{
  "mcpServers": {
    "context7": {
      "url": "https://mcp.context7.com/mcp",
      "type": "streamableHttp",
      "headers": {
        "Authorization": "Bearer YOUR_API_KEY"
      }
    }
  }
}
```

</details>

<details>
<summary><b>Instalacja w Zed</b></summary>

Można zainstalować przez [Zed Extensions](https://zed.dev/extensions?query=Context7) lub dodać do `settings.json` w Zed. Zobacz [Zed Context Server docs](https://zed.dev/docs/assistant/context-servers), aby uzyskać więcej informacji.

```json
{
  "context_servers": {
    "Context7": {
      "command": {
        "path": "npx",
        "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
      },
      "settings": {}
    }
  }
}
```

</details>

<details>
<summary><b>Instalacja w Augment Code</b></summary>

Aby skonfigurować Context7 MCP w Augment Code, możesz użyć interfejsu graficznego albo konfiguracji ręcznej.

### **A. Użycie interfejsu Augment Code**

1. Kliknij ikonę hamburgera.
2. Wybierz **Settings**.
3. Przejdź do sekcji **Tools**.
4. Kliknij **+ Add MCP**.
5. Wprowadź następujące polecenie:

   ```
   npx -y @upstash/context7-mcp@latest
   ```

6. Nazwij MCP: **Context7**.
7. Kliknij **Add**.

Po dodaniu serwera MCP możesz korzystać z aktualnej dokumentacji kodu Context7 bezpośrednio w Augment Code.

---

### **B. Konfiguracja ręczna**

1. Wciśnij Cmd/Ctrl Shift P lub przejdź do menu hamburgera w panelu Augment
2. Wybierz Edit Settings
3. W sekcji Advanced kliknij Edit w settings.json
4. Dodaj konfigurację serwera do tablicy `mcpServers` w obiekcie `augment.advanced`

```json
"augment.advanced": {
  "mcpServers": [
    {
      "name": "context7",
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  ]
}
```

Po dodaniu serwera MCP uruchom ponownie edytor. Jeśli pojawią się błędy, sprawdź składnię, czy nie brakuje nawiasów zamykających lub przecinków.

</details>

<details>
<summary><b>Instalacja w Roo Code</b></summary>

Dodaj to do pliku konfiguracyjnego MCP Roo Code. Zobacz [Roo Code MCP docs](https://docs.roocode.com/features/mcp/using-mcp-in-roo), aby uzyskać więcej informacji.

#### Roo Code – połączenie zdalne

```json
{
  "mcpServers": {
    "context7": {
      "type": "streamable-http",
      "url": "https://mcp.context7.com/mcp",
      "headers": {
        "CONTEXT7_API_KEY": "YOUR_API_KEY"
      }
    }
  }
}
```

#### Roo Code – połączenie lokalne

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

</details>

<details>
<summary><b>Instalacja w Gemini CLI</b></summary>

Zobacz [Gemini CLI Configuration](https://google-gemini.github.io/gemini-cli/docs/tools/mcp-server.html), aby uzyskać szczegóły.

1.  Otwórz plik ustawień Gemini CLI. Lokalizacja: `~/.gemini/settings.json` (gdzie `~` to katalog domowy).
2.  Dodaj poniższe do obiektu `mcpServers` w pliku `settings.json`:

```json
{
  "mcpServers": {
    "context7": {
      "httpUrl": "https://mcp.context7.com/mcp",
      "headers": {
        "CONTEXT7_API_KEY": "YOUR_API_KEY",
        "Accept": "application/json, text/event-stream"
      }
    }
  }
}
```

Lub dla serwera lokalnego:

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

Jeśli obiekt `mcpServers` nie istnieje, utwórz go.

</details>

<details>
<summary><b>Instalacja w Claude Desktop</b></summary>

#### Połączenie zdalne

Otwórz Claude Desktop i przejdź do Settings > Connectors > Add Custom Connector. Wprowadź nazwę `Context7` oraz zdalny adres URL serwera MCP: `https://mcp.context7.com/mcp`.

#### Połączenie lokalne

Otwórz ustawienia deweloperskie Claude Desktop i edytuj plik `claude_desktop_config.json`, dodając poniższą konfigurację. Zobacz [Claude Desktop MCP docs](https://modelcontextprotocol.io/quickstart/user), aby uzyskać więcej informacji.

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

</details>

<details>
  
<summary><b>Instalacja w Kiro</b></summary>

Zobacz [Kiro Model Context Protocol Documentation](https://kiro.dev/docs/mcp/configuration/), aby uzyskać szczegóły.

1. Przejdź do `Kiro` > `MCP Servers`
2. Dodaj nowy serwer MCP, klikając przycisk `+ Add`.
3. Wklej poniższą konfigurację:

```json
{
  "mcpServers": {
    "Context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"],
      "env": {},
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

4. Kliknij `Save`, aby zapisać zmiany.

</details>

<details>
<summary><b>Instalacja w Trae</bsummary>

Użyj funkcji Add manually i wprowadź informacje JSON konfiguracyjne dla tego serwera MCP.
Więcej szczegółów znajdziesz w [dokumentacji Trae](https://docs.trae.ai/ide/model-context-protocol?_lang=en).

#### Trae – połączenie zdalne (Remote)

```json
{
  "mcpServers": {
    "context7": {
      "url": "https://mcp.context7.com/mcp"
    }
  }
}
```

#### Trae – połączenie lokalne

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

</details>

<details>
<summary><b>Użycie Bun lub Deno</b></summary>

Użyj tych alternatyw, aby uruchomić lokalny serwer Context7 MCP z innymi runtime’ami. Te przykłady działają dla każdego klienta, który wspiera uruchamianie lokalnego serwera MCP przez `command + args`.

#### Bun

```json
{
  "mcpServers": {
    "context7": {
      "command": "bunx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

#### Deno

```json
{
  "mcpServers": {
    "context7": {
      "command": "deno",
      "args": [
        "run",
        "--allow-env=NO_DEPRECATION,TRACE_DEPRECATION",
        "--allow-net",
        "npm:@upstash/context7-mcp"
      ]
    }
  }
}
```

</details>

<details>
<summary><b>Użycie Dockera</b></summary>

Jeśli wolisz uruchomić serwer MCP w kontenerze Docker:

1. **Zbuduj obraz Dockera:**

   Najpierw utwórz plik `Dockerfile` w katalogu głównym projektu (lub gdziekolwiek wolisz):

   <details>
   <summary>Kliknij, aby zobaczyć zawartość Dockerfile</summary>

   ```Dockerfile
   FROM node:18-alpine

   WORKDIR /app

   # Install the latest version globally
   RUN npm install -g @upstash/context7-mcp

   # Expose default port if needed (optional, depends on MCP client interaction)
   # EXPOSE 3000

   # Default command to run the server
   CMD ["context7-mcp"]
   ```

   </details>

   Następnie zbuduj obraz, używając tagu (np. `context7-mcp`). **Upewnij się, że Docker Desktop (lub demon Dockera) działa.** Uruchom poniższe polecenie w tym samym katalogu, w którym zapisałeś `Dockerfile`:

   ```bash
   docker build -t context7-mcp .
   ```

2. **Skonfiguruj klienta MCP:**

   Zaktualizuj konfigurację klienta MCP, aby używać polecenia Dockera.

   _Przykład dla cline_mcp_settings.json:_

   ```json
   {
     "mcpServers": {
       "Сontext7": {
         "autoApprove": [],
         "disabled": false,
         "timeout": 60,
         "command": "docker",
         "args": ["run", "-i", "--rm", "context7-mcp"],
         "transportType": "stdio"
       }
     }
   }
   ```

   _Uwaga: To jest przykład konfiguracji. Odnieś się do konkretnych przykładów dla swojego klienta MCP (jak Cursor, VS Code itp.) wcześniej w tym README, aby dopasować strukturę (np. `mcpServers` vs `servers`). Upewnij się też, że nazwa obrazu w `args` odpowiada tagowi użytemu podczas komendy `docker build`._

</details>

<details>
<summary><b>Instalacja przy użyciu rozszerzenia Desktop</b></summary>

Zainstaluj plik [context7.mcpb](mcpb/context7.mcpb) z folderu mcpb i dodaj go do swojego klienta. Aby uzyskać więcej informacji, sprawdź [dokumentację paczek MCP](https://github.com/anthropics/mcpb#mcp-bundles-mcpb).

</details>

<details>
<summary><b>Instalacja w Windows</b></summary>

Konfiguracja w Windows różni się nieco od Linux lub macOS (_w przykładzie użyto `Cline`_). Ta sama zasada dotyczy innych edytorów; zwróć uwagę na konfigurację `command` i `args`.

```json
{
  "mcpServers": {
    "github.com/upstash/context7-mcp": {
      "command": "cmd",
      "args": ["/c", "npx", "-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"],
      "disabled": false,
      "autoApprove": []
    }
  }
}
```

</details>

<details>
<summary><b>Instalacja w Amazon Q Developer CLI</b></summary>

Dodaj to do pliku konfiguracyjnego Amazon Q Developer CLI. Zobacz [Amazon Q Developer CLI docs](https://docs.aws.amazon.com/amazonq/latest/qdeveloper-ug/command-line-mcp-configuration.html), aby uzyskać więcej informacji.

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

</details>

<details>
<summary><b>Instalacja w Warp</b></summary>

Zobacz [Warp Model Context Protocol Documentation](https://docs.warp.dev/knowledge-and-collaboration/mcp#adding-an-mcp-server), aby uzyskać szczegóły.

1. Przejdź do `Settings` > `AI` > `Manage MCP servers`.
2. Dodaj nowy serwer MCP, klikając przycisk `+ Add`.
3. Wklej poniższą konfigurację:

```json
{
  "Context7": {
    "command": "npx",
    "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"],
    "env": {},
    "working_directory": null,
    "start_on_launch": true
  }
}
```

4. Kliknij `Save`, aby zapisać zmiany.

</details>

<details>

<summary><b>Instalacja w Copilot Coding Agent</b></summary>

## Używanie Context7 z Copilot Coding Agent

Dodaj poniższą konfigurację do sekcji `mcp` w pliku konfiguracyjnym Copilot Coding Agent Repository->Settings->Copilot->Coding agent->MCP configuration:

```json
{
  "mcpServers": {
    "context7": {
      "type": "http",
      "url": "https://mcp.context7.com/mcp",
      "headers": {
        "CONTEXT7_API_KEY": "YOUR_API_KEY"
      },
      "tools": ["get-library-docs", "resolve-library-id"]
    }
  }
}
```

Więcej informacji znajdziesz w [oficjalnej dokumentacji GitHub](https://docs.github.com/en/enterprise-cloud@latest/copilot/how-tos/agents/copilot-coding-agent/extending-copilot-coding-agent-with-mcp).

</details>

<details>
<summary><b>Instalacja w LM Studio</b></summary>

Zobacz [LM Studio MCP Support](https://lmstudio.ai/blog/lmstudio-v0.3.17), aby uzyskać więcej informacji.

#### Instalacja jednym kliknięciem:

[![Add MCP Server context7 to LM Studio](https://files.lmstudio.ai/deeplink/mcp-install-light.svg)](https://lmstudio.ai/install-mcp?name=context7&config=eyJjb21tYW5kIjoibnB4IiwiYXJncyI6WyIteSIsIkB1cHN0YXNoL2NvbnRleHQ3LW1jcCJdfQ%3D%3D)

#### Konfiguracja ręczna:

1. Przejdź do `Program` (prawa strona) > `Install` > `Edit mcp.json`.
2. Wklej poniższą konfigurację:

```json
{
  "mcpServers": {
    "Context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

3. Kliknij `Save`, aby zapisać zmiany.
4. Przełącz serwer MCP włącz/wyłącz po prawej stronie, w sekcji `Program`, lub klikając ikonę wtyczki na dole okna czatu.

</details>

<details>
<summary><b>Instalacja w Visual Studio 2022</b></summary>

Możesz skonfigurować Context7 MCP w Visual Studio 2022, postępując zgodnie z [dokumentacją Visual Studio MCP Servers](https://learn.microsoft.com/visualstudio/ide/mcp-servers?view=vs-2022).

Dodaj to do pliku konfiguracyjnego MCP w Visual Studio (szczegóły w [dokumentacji Visual Studio](https://learn.microsoft.com/visualstudio/ide/mcp-servers?view=vs-2022)):

```json
{
  "inputs": [],
  "servers": {
    "context7": {
      "type": "http",
      "url": "https://mcp.context7.com/mcp",
      "headers": {
        "CONTEXT7_API_KEY": "YOUR_API_KEY"
      }
    }
  }
}
```

Lub dla serwera lokalnego:

```json
{
  "mcp": {
    "servers": {
      "context7": {
        "type": "stdio",
        "command": "npx",
        "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
      }
    }
  }
}
```

Więcej informacji i rozwiązywanie problemów znajdziesz w [dokumentacji Visual Studio MCP Servers](https://learn.microsoft.com/visualstudio/ide/mcp-servers?view=vs-2022).

</details>

<details>
<summary><b>Instalacja w Crush</b></summary>

Dodaj to do pliku konfiguracyjnego Crush. Zobacz [Crush MCP docs](https://github.com/charmbracelet/crush#mcps), aby uzyskać więcej informacji.

#### Crush – połączenie zdalne (HTTP)

```json
{
  "$schema": "https://charm.land/crush.json",
  "mcp": {
    "context7": {
      "type": "http",
      "url": "https://mcp.context7.com/mcp",
      "headers": {
        "CONTEXT7_API_KEY": "YOUR_API_KEY"
      }
    }
  }
}
```

#### Crush – połączenie lokalne

```json
{
  "$schema": "https://charm.land/crush.json",
  "mcp": {
    "context7": {
      "type": "stdio",
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

</details>

<details>
<summary><b>Instalacja w BoltAI</b></summary>

Otwórz stronę „Settings” aplikacji, przejdź do „Plugins” i wprowadź następujący JSON:

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

Po zapisaniu wpisz na czacie `get-library-docs` wraz z identyfikatorem dokumentacji Context7 (np. `get-library-docs /nuxt/ui`). Więcej informacji znajdziesz w [dokumentacji BoltAI](https://docs.boltai.com/docs/plugins/mcp-servers). Dla BoltAI na iOS [zobacz ten przewodnik](https://docs.boltai.com/docs/boltai-mobile/mcp-servers).

</details>

<details>
<summary><b>Instalacja w Rovo Dev CLI</b></summary>

Edytuj konfigurację MCP Rovo Dev CLI, uruchamiając polecenie -

```bash
acli rovodev mcp
```

Przykładowa konfiguracja -

#### Połączenie zdalne

```json
{
  "mcpServers": {
    "context7": {
      "url": "https://mcp.context7.com/mcp"
    }
  }
}
```

#### Połączenie lokalne

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

</details>

<details>
<summary><b>Instalacja w Zencoder</b></summary>

Aby skonfigurować Context7 MCP w Zencoder, wykonaj następujące kroki:

1. Przejdź do menu Zencoder (...)
2. Z menu rozwijanego wybierz Agent tools
3. Kliknij Add custom MCP
4. Dodaj nazwę i konfigurację serwera z poniższej sekcji i pamiętaj, aby kliknąć przycisk Install

```json
{
  "command": "npx",
  "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
}
```

Po dodaniu serwera MCP możesz z niego wygodnie korzystać.

</details>

<details>
<summary><b>Instalacja w Qodo Gen</b></summary>

Zobacz [Qodo Gen docs](https://docs.qodo.ai/qodo-documentation/qodo-gen/qodo-gen-chat/agentic-mode/agentic-tools-mcps), aby uzyskać więcej informacji.

1. Otwórz panel czatu Qodo Gen w VSCode lub IntelliJ.
2. Kliknij Connect more tools.
3. Kliknij + Add new MCP.
4. Dodaj poniższą konfigurację:

#### Qodo Gen – połączenie lokalne

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

#### Qodo Gen – połączenie zdalne

```json
{
  "mcpServers": {
    "context7": {
      "url": "https://mcp.context7.com/mcp"
    }
  }
}
```

</details>

<details>
<summary><b>Instalacja w Perplexity Desktop</b></summary>

Zobacz [Local and Remote MCPs for Perplexity](https://www.perplexity.ai/help-center/en/articles/11502712-local-and-remote-mcps-for-perplexity), aby uzyskać więcej informacji.

1. Przejdź do `Perplexity` > `Settings`
2. Wybierz `Connectors`.
3. Kliknij `Add Connector`.
4. Wybierz `Advanced`.
5. Wprowadź nazwę serwera: `Context7`
6. Wklej poniższy JSON w pole tekstowe:

```json
{
  "args": ["-y", "@upstash/context7-mcp", "--api-key", "YOUR_API_KEY"],
  "command": "npx",
  "env": {}
}
```

7. Kliknij `Save`.
</details>

## 🔨 Dostępne narzędzia

Context7 MCP udostępnia następujące narzędzia, z których mogą korzystać LLM-y:

- `resolve-library-id`: Rozwiązuje ogólną nazwę biblioteki do kompatybilnego z Context7 identyfikatora biblioteki.
  - `libraryName` (wymagane): Nazwa biblioteki do wyszukania

- `get-library-docs`: Pobiera dokumentację biblioteki przy użyciu kompatybilnego z Context7 identyfikatora.
  - `context7CompatibleLibraryID` (wymagane): Dokładny identyfikator biblioteki kompatybilny z Context7 (np. `/mongodb/docs`, `/vercel/next.js`)
  - `topic` (opcjonalne): Skup dokumentację na konkretnym temacie (np. „routing”, „hooks”)
  - `tokens` (opcjonalne, domyślnie 5000): Maksymalna liczba zwracanych tokenów. Wartości mniejsze niż 1000 są automatycznie zwiększane do 1000.

## 🛟 Wskazówki

### Dodaj regułę

Jeśli nie chcesz dodawać `use context7` do każdego promptu, możesz zdefiniować prostą regułę w sekcji reguł klienta MCP:

- Dla Windsurf w pliku `.windsurfrules`
- Dla Cursor w sekcji `Cursor Settings > Rules`
- Dla Claude Code w pliku `CLAUDE.md`

Lub odpowiednik w Twoim kliencie MCP, aby automatycznie wywoływać Context7 przy każdym pytaniu o kod.

#### Przykładowa reguła

```txt
Always use context7 when I need code generation, setup or configuration steps, or
library/API documentation. This means you should automatically use the Context7 MCP
tools to resolve library id and get library docs without me having to explicitly ask.
```

Od tego momentu będziesz otrzymywać dokumentację Context7 w każdej powiązanej rozmowie bez wpisywania czegokolwiek dodatkowego. Możesz zmodyfikować regułę, aby dopasować ją do swoich przypadków użycia.

### Użyj identyfikatora biblioteki

Jeśli dokładnie wiesz, której biblioteki chcesz użyć, dodaj jej identyfikator Context7 do promptu. Dzięki temu serwer Context7 MCP może pominąć etap dopasowania biblioteki i od razu pobrać dokumentację.

```txt
Implement basic authentication with Supabase. use library /supabase/supabase for API and docs.
```

Składnia ze slashem mówi narzędziu MCP, dla której biblioteki załadować dokumentację.

### Proxy HTTPS

Jeśli korzystasz z proxy HTTP, Context7 używa standardowych zmiennych środowiskowych `https_proxy` / `HTTPS_PROXY`.

## 💻 Rozwój

Sklonuj projekt i zainstaluj zależności:

```bash
bun i
```

Budowanie:

```bash
bun run build
```

Uruchamianie serwera:

```bash
bun run dist/index.js
```

### Argumenty CLI

`context7-mcp` akceptuje następujące flagi CLI:

- `--transport <stdio|http>` – Transport do użycia (domyślnie `stdio`). Zauważ, że transport HTTP automatycznie udostępnia zarówno endpointy HTTP, jak i SSE.
- `--port <number>` – Port nasłuchu przy użyciu transportu `http` (domyślnie `3000`).
- `--api-key <key>` – Klucz API do uwierzytelniania. Klucz możesz uzyskać, tworząc konto na [context7.com/dashboard](https://context7.com/dashboard).

Przykład z transportem HTTP i portem 8080:

```bash
bun run dist/index.js --transport http --port 8080
```

Inny przykład z transportem stdio:

```bash
bun run dist/index.js --transport stdio --api-key YOUR_API_KEY
```

<details>
<summary><b>Przykład konfiguracji lokalnej</b></summary>

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["tsx", "/path/to/folder/context7/src/index.ts", "--api-key", "YOUR_API_KEY"]
    }
  }
}
```

</details>

<details>
<summary><b>Testowanie z MCP Inspector</b></summary>

```bash
npx -y @modelcontextprotocol/inspector npx @upstash/context7-mcp
```

</details>

## 🚨 Rozwiązywanie problemów

<details>
<summary><b>Błędy „Module Not Found”</b></summary>

Jeśli napotkasz `ERR_MODULE_NOT_FOUND`, spróbuj użyć `bunx` zamiast `npx`:

```json
{
  "mcpServers": {
    "context7": {
      "command": "bunx",
      "args": ["-y", "@upstash/context7-mcp"]
    }
  }
}
```

To często rozwiązuje problemy z rozwiązywaniem modułów w środowiskach, w których `npx` nie instaluje lub nie rozwiązuje pakietów poprawnie.

</details>

<details>
<summary><b>Problemy z rozwiązywaniem ESM</b></summary>

Dla błędów typu `Error: Cannot find module 'uriTemplate.js'` spróbuj flagi `--experimental-vm-modules`:

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "--node-options=--experimental-vm-modules", "@upstash/context7-mcp@1.0.6"]
    }
  }
}
```

</details>

<details>
<summary><b>Problemy TLS/Certyfikatów</b></summary>

Użyj flagi `--experimental-fetch`, aby obejść problemy związane z TLS:

```json
{
  "mcpServers": {
    "context7": {
      "command": "npx",
      "args": ["-y", "--node-options=--experimental-fetch", "@upstash/context7-mcp"]
    }
  }
}
```

</details>

<details>
<summary><b>Ogólne błędy klientów MCP</b></summary>

1. Spróbuj dodać `@latest` do nazwy pakietu
2. Użyj alternatywy `bunx` zamiast `npx`
3. Rozważ użycie `deno` jako kolejnej alternatywy
4. Upewnij się, że używasz Node.js v18 lub nowszej dla natywnego wsparcia fetch

</details>

## ⚠️ Zastrzeżenie

Projekty Context7 są współtworzone przez społeczność i chociaż dokładamy starań, aby utrzymać wysoką jakość, nie możemy zagwarantować dokładności, kompletności ani bezpieczeństwa całej dokumentacji bibliotek. Projekty wymienione w Context7 są rozwijane i utrzymywane przez ich odpowiednich właścicieli, a nie przez Context7. Jeśli napotkasz treści podejrzane, nieodpowiednie lub potencjalnie szkodliwe, użyj przycisku „Report” na stronie projektu, aby nas natychmiast powiadomić. Poważnie traktujemy wszystkie zgłoszenia i szybko weryfikujemy oflagowane treści, aby utrzymać integralność i bezpieczeństwo naszej platformy. Korzystając z Context7, potwierdzasz, że robisz to na własną odpowiedzialność i ryzyko.

## 🤝 Skontaktuj się z nami

Bądź na bieżąco i dołącz do naszej społeczności:

- 📢 Obserwuj nas na [X](https://x.com/context7ai) po najnowsze wiadomości i aktualizacje
- 🌐 Odwiedź naszą [stronę](https://context7.com)
- 💬 Dołącz do naszego [Discord Community](https://upstash.com/discord)

## 📺 Context7 w mediach

- [Better Stack: "Free Tool Makes Cursor 10x Smarter"](https://youtu.be/52FC3qObp9E)
- [Cole Medin: "This is Hands Down the BEST MCP Server for AI Coding Assistants"](https://www.youtube.com/watch?v=G7gK8H6u7Rs)
- [Income Stream Surfers: "Context7 + SequentialThinking MCPs: Is This AGI?"](https://www.youtube.com/watch?v=-ggvzyLpK6o)
- [Julian Goldie SEO: "Context7: New MCP AI Agent Update"](https://www.youtube.com/watch?v=CTZm6fBYisc)
- [JeredBlu: "Context 7 MCP: Get Documentation Instantly + VS Code Setup"](https://www.youtube.com/watch?v=-ls0D-rtET4)
- [Income Stream Surfers: "Context7: The New MCP Server That Will CHANGE AI Coding"](https://www.youtube.com/watch?v=PS-2Azb-C3M)
- [AICodeKing: "Context7 + Cline & RooCode: This MCP Server Makes CLINE 100X MORE EFFECTIVE!"](https://www.youtube.com/watch?v=qZfENAPMnyo)
- [Sean Kochel: "5 MCP Servers For Vibe Coding Glory (Just Plug-In & Go)"](https://www.youtube.com/watch?v=LqTQi8qexJM)

## ⭐ Historia gwiazdek

[![Star History Chart](https://api.star-history.com/svg?repos=upstash/context7&type=Date)](https://www.star-history.com/#upstash/context7&Date)

## 📄 Licencja

MIT
