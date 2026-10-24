# PhysicaLab Studio 1.1.1

Laboratorios científicos HTML/JS dentro de notas de Obsidian, con controles, figuras 2D/3D y ecuaciones LaTeX locales.

- [Descargar el plugin completo](PhysicaLab-Studio-1.1.1.zip)
- [Descargar todo el código fuente](PhysicaLab-Studio-1.1.1-source.zip)

## Instalar

Extrae el ZIP del plugin y copia su carpeta `physica-lab-studio` a `.obsidian/plugins/` de tu vault. Conserva `vendor/`, que contiene las bibliotecas y fuentes para trabajar sin conexión. Activa **PhysicaLab Studio** en los complementos de comunidad de Obsidian. Al actualizar, conserva tu `data.json`.

La versión 1.1.1 corrige **Ampliar** en Live Preview mediante pantalla completa nativa. Mantiene el mismo laboratorio y su estado; **Escape** vuelve a la nota. La entrada en pantalla completa se comprobó en Obsidian Windows. Tras actualizar, desactiva y activa el plugin para cargar el código nuevo.

## Crear un laboratorio sencillo

Pide a tu IA que lea `SKILL.md`, `README.md` y `RUNTIME_ARCHITECTURE.md` de la carpeta del plugin. Por ejemplo:

> Crea un péndulo simple para PhysicaLab en `PhysicaLab/labs/pendulo-simple.html`: un diagrama con la masa arrastrable y solo los botones Iniciar/Pausar y Reiniciar. No incluyas fórmulas, teoría ni LaTeX; los escribiré aparte en mi nota. Hazlo offline, conserva el estado con `PhysLab.initialState`/`saveState` y gestiona el ciclo de vida. Entrega el HTML y su bloque physlab.

Abre una nota en modo Edición y ejecuta **PhysicaLab Studio: Insertar laboratorio desde archivo HTML**. Elige el HTML del vault. La guía y los cinco ejemplos editables están incluidos en el ZIP.

## Código fuente

El ZIP de código fuente contiene el proyecto completo y sus pruebas, documentación, fuentes y ejemplos genéricos. Extráelo en una carpeta y ejecuta:

```powershell
npm ci
npm run build
```

La compilación instala el plugin en el `demo-vault` del proyecto. Para preparar un paquete distribuible, usa `npm run dist`. Para copiarlo a otro vault:

```powershell
node scripts/install.mjs "C:\ruta\a\tu\vault"
```

Licencia MIT; las dependencias y fuentes conservan sus licencias incluidas. Android físico sigue pendiente de comprobación.
