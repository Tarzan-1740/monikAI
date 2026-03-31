## 📋 GUÍA DE COMPILACIÓN E INSTALACIÓN - MonikAI con LM Studio

### ⚙️ Requisitos Previos

1. **Visual Studio 2019 o superior** (Community Edition es gratis)
   - Descargar desde: https://visualstudio.microsoft.com/vs/
   - Instalar el workload "Desktop development with C++"
   - Instalar ".NET desktop development"

2. **.NET Framework 4.7.2 o superior**
   - Ya viene incluido con Visual Studio

3. **LM Studio** (para la IA)
   - Descargar desde: https://lmstudio.ai/
   - Instalar la aplicación
   - Descargar un modelo (ej: Mistral 7B, Llama 2)

4. **Git (opcional pero recomendado)**
   - Descargar desde: https://git-scm.com/

---

### 🎯 Paso 1: Descargar e Instalar Requisitos

#### 1.1 Instalar Visual Studio
```
1. Descarga Visual Studio Community desde:
   https://visualstudio.microsoft.com/vs/
   
2. Ejecuta el instalador
3. Selecciona:
   - "Desktop development with C++"
   - ".NET desktop development"
4. Click en "Install" y espera a que termine
```

#### 1.2 Instalar LM Studio
```
1. Descarga LM Studio desde: https://lmstudio.ai/
2. Ejecuta el instalador
3. Completa la instalación
4. Abre LM Studio
5. Descarga un modelo (en la sección "Discover"):
   - Recomendado: Mistral 7B (7B tokens, optimizado)
   - Alternativa: Llama 2 13B
6. Una vez descargado, click en "Load Model"
7. Espera a que termine de cargar (verás "Model loaded" al final)
```

---

### 📦 Paso 2: Abrir el Proyecto en Visual Studio

```
1. Abre Visual Studio
2. Click en "File" → "Open" → "Project/Solution"
3. Navega hasta la carpeta: 
   C:\Users\[TuUsuario]\Downloads\MonikAI-0.7-pre\MonikAI-0.7-pre
4. Selecciona el archivo: MonikAI.sln
5. Click en "Open"
6. Espera a que Visual Studio descargue dependencias (puede tardar 2-3 min)
```

---

### ✅ Paso 3: Restaurar Dependencias NuGet

```
1. En Visual Studio, click derecho en "MonikAI" en el Explorador de Soluciones
2. Selecciona "Restore NuGet Packages"
3. O ve a: Tools → NuGet Package Manager → Package Manager Console
4. Escribe: Update-Package -Reinstall
5. Presiona Enter y espera a que termine
```

---

### 🔧 Paso 4: Verificar Configuración de Compilación

```
1. Va a: Build → Configuration Manager
2. En el dropdown "Active solution configuration":
   - Selecciona "Release" (es más rápido que Debug)
3. En "Active solution platform":
   - Selecciona "Any CPU"
4. Click en "Close"
```

---

### 🏗️ Paso 5: Compilar (Build) la Solución

```
1. Click en: Build → Build Solution
   (o presiona Ctrl+Shift+B)
   
2. Espera a que aparezca el mensaje:
   "Build succeeded"
   
3. Si hay errores, mira la ventana "Error List"
   - Si dice algo sobre Newtonsoft.Json:
     * Ve a Tools → NuGet Package Manager → Package Manager Console
     * Escribe: Install-Package Newtonsoft.Json
     * Presiona Enter
     * Intenta compilar de nuevo

4. El ejecutable compilado estará en:
   C:\Users\[TuUsuario]\Downloads\MonikAI-0.7-pre\MonikAI-0.7-pre\MonikAI\bin\Release\MonikAI.exe
```

---

### 🚀 Paso 6: Ejecutar la Aplicación

#### Opción A: Desde Visual Studio
```
1. Presiona F5 o click en: Debug → Start Debugging
2. La aplicación debería abrir
```

#### Opción B: Desde el archivo ejecutable
```
1. Navega a:
   C:\Users\[TuUsuario]\Downloads\MonikAI-0.7-pre\MonikAI-0.7-pre\MonikAI\bin\Release\

2. Haz doble click en: MonikAI.exe

3. La aplicación se abrirá en la esquina inferior derecha de tu pantalla
```

---

### ⚡ Paso 7: Configurar LM Studio Correctamente

**IMPORTANTE**: Necesitas tener LM Studio corriendo ANTES de iniciar MonikAI

```
1. Abre LM Studio
2. Ve a la pestaña "Local Server"
3. Asegúrate de que está en:
   - Host: localhost
   - Port: 1234
   - Status: Running (debería ser verde)
4. Si no está corriendo:
   - Click en el botón verde "Start Server"
   - Espera a que aparezca "Server is now listening..."
5. AHORA puedes iniciar MonikAI
```

---

### 🎨 Paso 8: Configurar Monika (Primera vez)

Cuando abras MonikAI por primera vez, verás:

1. **Ventana de bienvenida** con instrucciones
   - Click en "OK"
   
2. **Ventana de Configuración**:
   - **User Name**: Escribe tu nombre (ej: "Juan")
   - **Language**: Selecciona "Spanish"
   - **Position**: Elige "Automatic" o "Manual" (Manual si necesitas ajustar posición)
   - **Dark Mode**: Elige "Day" o "Night" según prefieras
   - Click en "Save Settings"

3. ¡Monika debería aparecer en la esquina de tu pantalla hablando en español!

---

### 🔍 Solución de Problemas

#### Problema: "No puedo ver a Monika"
**Solución:**
1. Presiona CTRL+SHIFT+F10 para abrir Settings
2. En "Position" selecciona "Manual"
3. Ajusta las coordenadas X e Y manualmente
4. Presiona "Save Settings"

#### Problema: "LM Studio no se conecta"
**Solución:**
1. Verifica que LM Studio esté corriendo
2. En LM Studio, ve a "Local Server"
3. Click en "Start Server" si no está corriendo
4. Espera 5 segundos y reinicia MonikAI
5. Si sigue sin funcionar, reinicia todo

#### Problema: "MonikAI se congela o no responde"
**Solución:**
1. Verifica que tu modelo en LM Studio esté completamente cargado
2. Comprueba que tienes suficiente RAM libre (mínimo 8GB recomendado, 16GB ideal)
3. Cierra otras aplicaciones pesadas
4. Reinicia LM Studio y MonikAI

#### Problema: Error durante la compilación "Project file error"
**Solución:**
1. Cierra Visual Studio
2. Navega a: C:\Users\[TuUsuario]\Downloads\MonikAI-0.7-pre\MonikAI-0.7-pre\
3. Elimina la carpeta ".vs" (carpeta oculta)
4. Abre Visual Studio de nuevo y carga la solución

---

### 📊 Información Técnica

**Especificaciones de tu Setup:**
- GPU: RTX 4080 Super ✅ (Excelente para ejecutar modelos 7B-13B localmente)
- RAM mínima recomendada: 16GB
- Velocidad de respuesta esperada: 1-3 segundos por respuesta

**Modelos recomendados para tu GPU:**
- Mistral 7B (Rápido, buena calidad)
- Llama 2 13B (Mejor calidad, un poco más lento)
- Neural Chat 7B (Optimizado para chat)

---

### 📝 Cambios Realizados

1. ✅ Integración con LM Studio (API OpenAI-compatible)
2. ✅ Traducción de CSV al español de España
3. ✅ Configuración automática de idioma español
4. ✅ Inicialización automática de LM Studio
5. ✅ Sistema de respuestas dinámicas con IA

---

### 🎮 Controles de Teclado

| Atajo | Función |
|-------|---------|
| CTRL+SHIFT+F10 | Abrir configuración |
| CTRL+SHIFT+F12 | Minimizar/Maximizar Monika |
| Click derecho | Menú contextual |

---

### 💡 Tips Útiles

1. **Para mejor rendimiento:**
   - Descarga un modelo más pequeño (7B es suficiente)
   - Cierra navegadores y aplicaciones pesadas
   - Aumenta la RAM si puedes

2. **Para cambiar idioma de nuevo:**
   - Abre los archivos CSV en la carpeta `\docs\`
   - Edita los textos directamente
   - Reinicia MonikAI

3. **Para usar modelos diferentes:**
   - Abre LM Studio
   - Click en "Discover"
   - Descarga otro modelo
   - Carga el modelo deseado
   - MonikAI automáticamente usará el modelo cargado

---

### 📞 Soporte

Si encuentras problemas:
1. Verifica que LM Studio esté corriendo correctamente
2. Comprueba que tienes suficiente RAM
3. Reinicia ambas aplicaciones
4. Revisa los logs en: `C:\Users\[TuUsuario]\AppData\Roaming\MonikAI\`

---

¡Listo! Ahora deberías tener a Monika completamente funcional con IA en español. 🎉

**Hecho por:** GitHub Copilot
**Modelo IA:** Claude Haiku 4.5
**Fecha:** 31 de Marzo de 2026
