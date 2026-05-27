# 🤖 NS Bot — Discord Bot Multipropósito

> Bot de Discord profesional con IA, música, moderación, niveles, tickets y más.  
> Creado por **Ninsi** · Hecho con Python + discord.py

---

## ✨ Características

| Módulo | Descripción |
|---|---|
| 🧠 **IA Chat** | Respuestas inteligentes con Groq AI |
| 🛡️ **Moderación** | Ban, kick, mute, warn y más |
| 🤖 **AutoMod** | Filtrado automático de mensajes |
| ⭐ **Niveles** | Sistema de XP y ranking por servidor |
| 👋 **Bienvenida** | Mensajes personalizados al unirse |
| 🎫 **Tickets** | Sistema de soporte con tickets |
| ⏰ **Recordatorios** | Programa recordatorios personales |
| 🎵 **Música** | Reproduce música en canales de voz |
| 🎮 **Entretenimiento** | Comandos divertidos y juegos |
| 📋 **Logs** | Registro de eventos del servidor |
| ⚙️ **Configuración** | Prefijo y ajustes por servidor |
| 📊 **Dashboard** | Panel web de administración |

---

## 📁 Estructura del proyecto

```
discordninsibot/
├── bot.py                 # Punto de entrada principal
├── run.py                 # Script de inicio alternativo
├── cogs/
│   ├── ai_chat.py
│   ├── automod.py
│   ├── config.py
│   ├── entertainment.py
│   ├── levels.py
│   ├── logs.py
│   ├── moderation.py
│   ├── music.py
│   ├── reminders.py
│   ├── tickets.py
│   └── welcome.py
├── dashboard/
│   └── app.py             # Panel web
├── database/
│   └── db.py              # Base de datos SQLite
├── utils/
│   ├── groq_client.py     # Cliente de Groq AI
│   └── helpers.py         # Funciones auxiliares
├── data/
│   ├── bot.db             # Base de datos (auto-generada)
│   └── bot.log            # Logs (auto-generado)
├── .env                   # Variables de entorno (NO subir)
├── requirements.txt
└── docker-compose.yml
```

---

## 🚀 Instalación

### Requisitos
- Python 3.10 o superior
- Una cuenta de Discord con un bot creado en el [Portal de Desarrolladores](https://discord.com/developers/applications)

### 1. Clona el repositorio

```bash
git clone https://github.com/TuUsuario/ns-bot.git
cd ns-bot
```

### 2. Instala las dependencias

```bash
pip install -r requirements.txt
```

### 3. Configura el `.env`

Crea un archivo `.env` en la raíz del proyecto basándote en `.env.example`:

```bash
cp .env.example .env
```

Edita el `.env` con tus datos:

```env
DISCORD_TOKEN=tu_token_aqui
GROQ_API_KEY=tu_api_key_de_groq  # Opcional, para IA
LOG_LEVEL=INFO
```

### 4. Ejecuta el bot

```bash
python bot.py
```

o usando el script de inicio:

```bash
python run.py
```

---

## ⚙️ Configuración

El prefijo por defecto es `!`. Puedes cambiarlo por servidor con:

```
!config prefix <nuevo_prefijo>
```

Para ver todos los comandos disponibles:

```
!help
```

---

## 🐳 Docker (opcional)

```bash
docker-compose up -d
```

---

## 📋 Comandos principales

| Comando | Descripción |
|---|---|
| `!help` | Lista todos los comandos |
| `!ping` | Latencia del bot |
| `!uptime` | Tiempo en línea |
| `!creador` | Información del creador |
| `!config prefix <p>` | Cambia el prefijo del servidor |

---

## 🔑 Variables de entorno

| Variable | Requerida | Descripción |
|---|---|---|
| `DISCORD_TOKEN` | ✅ Sí | Token del bot de Discord |
| `GROQ_API_KEY` | ⚠️ Opcional | API Key de Groq para IA |
| `LOG_LEVEL` | ❌ No | Nivel de logs (`INFO`, `DEBUG`, `WARNING`) |

---

## 📝 Notas

- La base de datos `bot.db` y los logs `bot.log` se generan automáticamente en la carpeta `data/`
- Al apagar el bot con `Ctrl+C`, se envía un mensaje de despedida en cada servidor
- Al unirse a un nuevo servidor, el bot se presenta automáticamente

---

## 👤 Autor

**Ninsi**  
Hecho con ❤️ y Python

---

## 📄 Licencia

Este proyecto está bajo la licencia MIT. Puedes usarlo como plantilla para tu propio bot.
