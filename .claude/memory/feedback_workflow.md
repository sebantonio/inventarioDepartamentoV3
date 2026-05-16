---
name: Preferencias de trabajo
description: Cómo el usuario prefiere que se trabaje en este proyecto
type: feedback
originSessionId: 97fd2f19-db29-4e74-997b-cfdd7054b186
---
Siempre redesplegar el Apps Script después de cambios en `appscript.txt`.

**Why:** Varias veces se asumió que el cambio ya estaba activo y el error persistía porque no se había redesplegalado.

**How to apply:** Al final de cualquier edición en `appscript.txt`, recordar redesplegar (Implementar → Gestionar implementaciones → Nueva versión).

---

El usuario prefiere respuestas cortas y directas, sin explicar el razonamiento salvo que pregunte.

**Why:** Lo demuestra consistentemente — va al grano.

**How to apply:** Una o dos frases de contexto máximo, luego la solución directamente.

---

Cuando el usuario pregunta "¿se puede hacer X?" sin pedir implementación, dar una recomendación breve y preguntar si quiere que se implemente. No implementar sin confirmación.

**Why:** El usuario a veces explora opciones antes de decidir.

**How to apply:** Responder con el enfoque recomendado en 3-5 líneas y terminar con "¿Lo implemento?"

---

Siempre envolver campos de texto en `String(x||'')` antes de llamar a `.localeCompare()` o `.toLowerCase()` en sort/filter.

**Why:** Items creados con campos vacíos/null provocan `TypeError: x.localeCompare is not a function` que rompe todo el modal de préstamos e inventario. Pasó con el campo `item` en 2026-05-16.

**How to apply:** En cualquier `.sort()` o comparación de strings sobre datos del inventario, usar `String(a.campo||'').localeCompare(String(b.campo||''))`.

---

El usuario crea repos y carpetas nuevas externamente antes de pedir a Claude que trabaje en ellas. No intentar crear el repo — solo copiar archivos al directorio indicado y hacer push.

**Why:** Prefiere tener control del nombre y ubicación del repo de GitHub antes de empezar.

**How to apply:** Cuando diga "he creado un repo en github, trabaja en X carpeta", copiar archivos allí y hacer push directamente sin crear el repo.
