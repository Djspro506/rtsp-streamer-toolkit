# rtsp-streamer-toolkit
Herramienta open source para vMix + OBS con RTSP, SRT, RTMP y NDI
# vMix RTSP Toolkit

**Herramienta open source** para streamers y productores de video que usan **vMix** como principal y **OBS Studio** como secundario.

Permite transmitir con baja latencia usando múltiples protocolos modernos.

![Banner](https://via.placeholder.com/800x200/0066cc/ffffff?text=vMix+RTSP+Toolkit)

## ✨ Características

- **RTSP Server** optimizado para vMix
- **2 salidas RTMP** simultáneas (YouTube, Kick, servidor propio, etc.)
- **SRT** (baja latencia y estable)
- **NDI** support
- **Latencia configurable**: Ultra Low / Low / Medium
- Interfaz gráfica simple y moderna (construido con Tauri)
- Ligero y nativo (no consume mucho recurso como Electron)

## Requisitos

- Windows 10/11 (recomendado)
- [ffmpeg](https://ffmpeg.org/download.html) en el PATH
- NDI Tools (opcional pero recomendado para vMix)
- Plugin [OBS-RTSPServer](https://github.com/iamscottxu/obs-rtspserver) (para modo OBS)

## Cómo usar

1. Descarga y ejecuta la aplicación
2. Configura el **Puerto RTSP**
3. Presiona **Iniciar RTSP Server**
4. En **vMix** agrega la URL como `Stream / IP Camera Input`
5. Configura las URLs RTMP y SRT según necesites
6. ¡Listo para transmitir!

## Protocolos soportados

| Protocolo | Uso principal     | Latencia     |
|-----------|-------------------|--------------|
| RTSP      | vMix              | Baja         |
| RTMP      | Plataformas       | Media        |
| SRT       | Conexiones estables | Muy baja   |
| NDI       | Producción interna| Ultra baja   |

## Desarrollo

Este proyecto fue creado con:
- [Tauri](https://tauri.app) + Rust (backend)
- Svelte (frontend)
- FFmpeg (captura y streaming)

### Compilar desde código

```bash
npm install
npm run tauri build
