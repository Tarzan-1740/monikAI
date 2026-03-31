## ⚡ CONFIGURACIÓN RÁPIDA - MonikAI con LM Studio

### 🚀 TL;DR (Resumen Rápido)

```
1. Instala Visual Studio Community (descarga, sigue pasos)
2. Instala LM Studio desde https://lmstudio.ai/
3. En LM Studio: "Discover" → Descarga "Mistral 7B"
4. Abre LM Studio, carga el modelo
5. Abre MonikAI.sln en Visual Studio
6. Ctrl+Shift+B para compilar
7. F5 para ejecutar
8. ¡Monika habla en español! 🎉
```

---

### 🔍 Checklist de Verificación

Antes de compilar, verifica esto:

```
✓ Visual Studio 2019+ instalado
✓ .NET Framework 4.7.2+ instalado
✓ LM Studio instalado
✓ Modelo IA descargado en LM Studio
✓ Git (opcional, pero útil)
✓ Al menos 16GB RAM libre
✓ RTX 4080 Super disponible
```

---

### 📦 Instalación Visual Studio (5 minutos)

1. Descarga: https://visualstudio.microsoft.com/vs/
2. Ejecuta el instalador
3. Click en "Desktop development with C#"
4. Espera... espera... ✅

---

### 🤖 Instalación LM Studio (10 minutos)

1. Descarga: https://lmstudio.ai/
2. Instala
3. Abre → "Discover"
4. Busca "Mistral 7B"
5. Click en descargar
6. Espera (depende de tu internet)
7. Una vez descargado → "Load Model"
8. **IMPORTANTE**: Espera a que diga "Model loaded"

---

### 💻 Compilación (5 minutos)

```powershell
1. Abre Visual Studio
2. File → Open → Project/Solution
3. Selecciona: MonikAI-0.7-pre\MonikAI.sln
4. Espera a que termine de cargar los paquetes NuGet
5. Click derecho en "MonikAI" → "Restore NuGet Packages"
6. Presiona Ctrl+Shift+B
7. Espera el mensaje "Build succeeded"
```

---

### ▶️ Ejecución

**Opción A - Desde Visual Studio:**
```
Presiona F5 → Espera → ¡Monika aparece!
```

**Opción B - Desde Explorador Windows:**
```
Ve a: MonikAI-0.7-pre\MonikAI\bin\Release\
Doble click en: MonikAI.exe
```

---

### ⚠️ Problema: No aparece Monika

**Solución:**
```
1. Presiona CTRL+SHIFT+F10
2. En "Position" selecciona "Manual"
3. Cambia X e Y (ej: X=1000, Y=700)
4. Click "Save Settings"
5. Reinicia MonikAI
```

---

### ⚠️ Problema: La IA no responde

**Verificación:**
```
1. ¿LM Studio está corriendo? 
   → Si no, ábrelo

2. En LM Studio, ¿el servidor de local está activo?
   → "Local Server" debe estar verde (Running)
   → Si no, click en el botón verde "Start Server"

3. ¿El modelo está cargado?
   → Debe decir "Model loaded" en LM Studio
   → Si no, click en "Load Model"

4. Si aún no funciona:
   → Cierra todo
   → Espera 10 segundos
   → Abre LM Studio primero
   → Luego abre MonikAI
```

---

### 🎮 Controles Útiles

| Atajo | Qué hace |
|-------|----------|
| CTRL+SHIFT+F10 | Abre configuración |
| CTRL+SHIFT+F12 | Minimiza/Maximiza Monika |
| Click derecho | Menú |

---

### 📊 Especificaciones Verificadas

- **Compilador:** C# .NET Framework 4.8
- **GPU:** RTX 4080 Super ✅ (Excelente)
- **Memoria mínima:** 16GB RAM
- **Espacio disco:** 5GB para MonikAI + 30GB para LM Studio

---

### 🎯 Pasos Finales

Una vez compilado y funcionando:

1. **Primer inicio:** Monika te hablará
2. **Configuración:** Selecciona "Spanish" en settings
3. **¡Listo!** Monika en tu escritorio, en español, con IA

---

### 📞 Si Algo Falla

**Paso 1:** Reinicia todo
```
1. Cierra MonikAI
2. Cierra LM Studio
3. Cierra Visual Studio
4. Espera 5 segundos
5. Abre LM Studio
6. Abre MonikAI
```

**Paso 2:** Verifica conexión
```
1. Abre navegador
2. Ve a: http://localhost:1234/v1/models
3. Debe mostrar JSON con el modelo cargado
4. Si no funciona, LM Studio no está corriendo
```

**Paso 3:** Recompila
```
1. Abre Visual Studio
2. Ctrl+Shift+B
3. Espera "Build succeeded"
4. F5
```

---

### 🎉 Éxito

Si ves a Monika en la esquina de tu pantalla hablando en español, ¡**FELICIDADES!** 🎊

Está completamente funcional con:
- ✅ LM Studio integrado
- ✅ Respuestas de IA dinámicas
- ✅ Español de España
- ✅ RTX 4080 Super optimizada

---

### 💡 Tips Pro

**Para mejor rendimiento:**
- Usa Mistral 7B (rápido, buena calidad)
- Evita Q2 cuantización (usa Q4 como mínimo)
- Cierra otros programas mientras usas Monika

**For respuestas más personalizadas:**
- Edita el archivo `LMStudioService.cs`
- En `SYSTEM_PROMPT`, personaliza el carácter de Monika
- Recompila (Ctrl+Shift+B)

---

### 📚 Archivos Importantes

```
GUIA_COMPILACION.md → Instrucciones detalladas
CAMBIOS_REALIZADOS.md → Lista de cambios
LMStudioService.cs → Conexión con IA
idle_dialogue_Spanish.csv → Diálogos en español
startup_Spanish.csv → Discurso de inicio
application_Spanish.csv → Reacciones a apps
```

---

## 🚀 ¡AHORA SÍ, A COMPILAR Y DISFRUTAR! 🎉

---

**Autor:** GitHub Copilot (Claude Haiku 4.5)
**Versión:** 1.0
**Fecha:** 31 de Marzo de 2026
**Estado:** ✅ Listo para usar
