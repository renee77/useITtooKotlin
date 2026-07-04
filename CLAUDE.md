# KtorKotlinBackendJaar2

Ktor server-side backend voor het schoolproject van Eva (HBO-ICT jaar 2).

## Project context
- **Student**: Eva, HBO-ICT
- **Leermap**: `/home/eva/claude/kotlin` (documentatie, notities, Kotlin Illustrated Guide)
- **Android app**: komt nog (zal verbinding maken met deze backend)

## Tech stack
| Term | Betekenis |
|------|-----------|
| Ktor 3.x | Kotlin server framework (JetBrains) |
| Netty | Engine waarmee Ktor de server draait |
| ContentNegotiation | Ktor plugin voor JSON serialization |
| kotlinx-serialization | JSON library |
| `10.0.2.2` | Localhost-adres vanuit de Android emulator |

## Structuur
```
src/
├── main/
│   ├── kotlin/
│   │   ├── main.kt            # Entry point (EngineMain)
│   │   ├── Routing.kt         # Route definitions (configureRouting)
│   │   └── Serialization.kt   # JSON setup (configureSerialization)
│   └── resources/
│       ├── application.yaml   # Server config (port 8080, modules)
│       └── logback.xml        # Logging config
└── test/
    └── kotlin/
        └── ServerTest.kt      # Integration tests (testApplication)
```

## Huidige routes
| Methode | Pad | Response |
|---------|-----|----------|
| GET | `/` | `"Hello, World!"` (plain text) |
| GET | `/json/kotlinx-serialization` | `{"hello": "world"}` (JSON) |

## Werkwijze & voorkeuren
- Coach-modus bij coderen: plan bedenken, stap voor stap doorlopen
- Op expliciete vraag om code → gewoon code leveren
- Code altijd voorzien van commentaar
- Directe, beknopte antwoorden — geen overbodige uitleg
- Voertaal: Nederlands | Programmeertermen in het Engels
