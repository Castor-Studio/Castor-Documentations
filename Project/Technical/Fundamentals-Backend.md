---
Titre:          Fondamentaux Backend
soustitre:      Castor Application - Desktop Application for video recording/streaming
author:         Castor Application - Castor Team
module:         G-EIP-700
version:        1.0
date de maj:    03/03/2026
---

> Voici les librairies qui vous seront nécessaire pour pouvoir lancer le backend du Projet Castor.
> Ces dernières ont pour but de gérer Vidéo, Audio et Gestion de la logique métiers de l'application.

## 🎬 FFmpeg

> **GitHub** : [github.com/FFmpeg/FFmpeg](https://github.com/FFmpeg/FFmpeg)

|Lib|Rôle|Doc|Install Windows|
|---|---|---|---|
|**avcodec**|Encodage / décodage audio & vidéo|[libavcodec](https://www.ffmpeg.org/libavcodec.html)|`vcpkg install ffmpeg`|
|**avformat**|Muxing / demuxing de containers multimédia|[libavformat](https://ffmpeg.org/libavformat.html)|`vcpkg install ffmpeg`|
|**avutil**|Utilitaires portables (maths, crypto, structures…)|[libavutil](https://www.ffmpeg.org/libavutil.html)|`vcpkg install ffmpeg`|
|**swscale**|Conversion de format pixel & redimensionnement|[libswscale](https://www.ffmpeg.org/libswscale.html)|`vcpkg install ffmpeg[swscale]`|
|**swresample**|Resampling audio & conversion de format de sample|[libswresample](https://www.ffmpeg.org/libswresample.html)|`vcpkg install ffmpeg[swresample]`|

> 💡 Ou via winget pour les binaires CLI : `winget install Gyan.FFmpeg`

---

## 🪟 Windows SDK

> Ces libs sont **incluses nativement** dans le Windows SDK — install : [developer.microsoft.com/windows/downloads/windows-sdk](https://developer.microsoft.com/en-US/windows/downloads/windows-sdk/) ou via Visual Studio Installer.

| Lib            | Rôle                                                  | Doc                                                                                                    | Install Windows                                                                 |
| -------------- | ----------------------------------------------------- | ------------------------------------------------------------------------------------------------------ | ------------------------------------------------------------------------------- |
| **dwmapi**     | Desktop Window Manager (transparence, effets visuels) | [dwmapi.h](https://learn.microsoft.com/en-us/windows/win32/api/dwmapi/)                                | Inclus dans Windows SDK — link : `dwmapi.lib`                                   |
| **windowsapp** | Windows App SDK / WinRT (APIs modernes, WinUI 3)      | [Windows App SDK](https://learn.microsoft.com/en-us/windows/apps/windows-app-sdk/)                     | `winget install Microsoft.WindowsAppSDK` ou NuGet `Microsoft.WindowsAppSDK`     |
| **mmdevapi**   | Core Audio — gestion des périphériques audio          | [MMDevice API](https://learn.microsoft.com/en-us/windows/win32/coreaudio/mmdevice-api)                 | Inclus dans Windows SDK — link : `mmdevapi.lib`                                 |
| **d3d11**      | Direct3D 11 — rendu GPU, shaders, pipeline graphique  | [Direct3D 11](https://learn.microsoft.com/en-us/windows/win32/direct3d11/atoc-dx-graphics-direct3d-11) | Inclus dans Windows SDK — link : `d3d11.lib` ou `vcpkg install directx-headers` |
| **winmm**      | Multimedia legacy (waveXxx, midiXxx, mixerXxx)        | [WinMM](https://learn.microsoft.com/en-us/windows/win32/multimedia/windows-multimedia-start-page)      | Inclus dans Windows SDK — link : `winmm.lib`                                    |
