# Validación de Levantamiento de Flota | Milwaukee Tool & Hangcha México 🚜⚡

Aplicación web estática, interactiva y responsiva desarrollada a partir del archivo de levantamiento de planta (`Levantamiento Planta Hangcha.xlsx`). Permite al cliente revisar y validar individual o masivamente los **85 equipos de montacargas**, confirmando especificaciones de modelos, capacidades de carga, alturas de mástil, tipos de energía, voltajes de cargador y ubicaciones por planta.

---

## 🚀 Características Principales

1. **Catálogo Completo (85 Equipos)**:
   - Vista en **Tarjetas visuales** o en **Tabla compacta** tipo Excel.
   - Buscador universal en tiempo real (# de equipo, modelo, tipo, depto, planta).
   - Filtros instantáneos por:
     - **Planta**: Golden, Planta 1, Planta 2.
     - **Modelo**: DR16LI, BT45LI, FPG25 (Gas), FBT20LI, FBE25LI, OPM02LI, CBD20-WD, MJ20 (Mima).
     - **Departamento**: Warehouse, CI, Shipping, Test Lab, Relevo, EHS.
     - **Estado de Validación**: Pendientes, Aprobados, Con Cambios.

2. **Sistema de Validación con Paloma y Tacha**:
   - 🟢 **Paloma (Aprobar)**: Marca el equipo con visto bueno.
   - 🔴 **Tacha (Requiere Cambio / Rechazar)**: Abre un panel desplegable de observaciones para que el cliente especifique:
     - Etiquetas rápidas: `Capacidad Carga`, `Altura Mástil`, `Voltaje/Cargador`, `Modelo Incorrecto`, `Reubicar Planta`, `Tipo de Equipo`.
     - Campo de texto libre para detallar el requerimiento exacto (ej. *"Se requiere capacidad de 2.5T en vez de 1.6T"*).
   - Botón de **Aprobación Masiva**: Permite aprobar con un solo clic todos los equipos filtrados (ej. todas las unidades de un modelo o planta homogénea).

3. **Vista Agrupada por Familia de Modelos (8 Modelos)**:
   - Resumen consolidado de especificaciones técnicas por modelo.
   - Posibilidad de validar familias completas en un solo clic.

4. **Persistencia Automática (LocalStorage)**:
   - El cliente puede recargar la página o cerrar el navegador sin perder su avance.

5. **Múltiples Opciones de Entrega de Resultados a Hangcha**:
   - 📊 **Descargar Excel Oficial (.xlsx)**: Genera un archivo con las columnas originales del levantamiento más:
     - `ESTADO DE VALIDACIÓN` (`APROBADO (PALOMA) ✓`, `REQUIERE CAMBIO (TACHA) ✕`, `PENDIENTE`)
     - `OBSERVACIONES / CAMBIOS SOLICITADOS`
     - `MOTIVOS SELECCIONADOS`
     - `FECHA DE VALIDACIÓN`
     - `VALIDADO POR`
     - Hoja adicional con **Resumen Ejecutivo** y métricas.
   - 💬 **Enviar por WhatsApp**: Permite ingresar cualquier número de WhatsApp de destino (o dejar en blanco para elegir el contacto) con el desglose preformateado.
   - ✉️ **Enviar por Correo**: Dirigido automáticamente a **projectmilwhang@gmail.com** con el informe técnico completo redactado.
   - 📋 **Copiar Resumen**: Copia el reporte ejecutivo al portapapeles.
   - 💾 **Respaldos JSON**: Guardar y cargar sesiones en archivo `.json`.

---

## 💻 Cómo Probar la Aplicación en Local

Simplemente haz doble clic sobre el archivo `index.html` o ábrelo en cualquier navegador web moderno (Google Chrome, Safari, Microsoft Edge, Firefox). **No requiere servidor, ni instalación de software, ni conexión de base de datos.**

---

## 🌐 Cómo Subir a GitHub y Activar GitHub Pages (Paso a Paso)

Puedes publicar la aplicación en GitHub de dos maneras:

### Opción A: Desde la Terminal (Recomendado)

1. Abre tu terminal en la carpeta del proyecto:
   ```bash
   cd "/Users/flavioberlanga/Desktop/Proyecto Milwaukee-Hangcha"
   ```

2. Inicializa el repositorio Git (si aún no está inicializado):
   ```bash
   git init
   git add .
   git commit -m "feat: Aplicacion web de Hojas de Datos y Validacion Milwaukee-Hangcha con fichas tecnicas PDF"
   ```

3. Crea un nuevo repositorio en [GitHub.com](https://github.com/new) (por ejemplo llamado `validacion-milwaukee-hangcha`).

4. Conecta tu repositorio local y sube los cambios:
   ```bash
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/validacion-milwaukee-hangcha.git
   git push -u origin main
   ```

5. **Activa GitHub Pages**:
   - En tu repositorio de GitHub, ve a **Settings** (Configuración) > **Pages**.
   - En **Build and deployment** > **Source**, selecciona `Deploy from a branch`.
   - En **Branch**, selecciona `main` y carpeta `/ (root)`.
   - Haz clic en **Save** (Guardar).
   - En 1 o 2 minutos, GitHub te dará un enlace público como:
     `https://TU_USUARIO.github.io/validacion-milwaukee-hangcha/`

---

### Opción B: Directamente desde la Web de GitHub (Sin Terminal)

1. Ve a [GitHub.com](https://github.com/new) y crea un repositorio público (ej. `validacion-milwaukee-hangcha`).
2. Haz clic en **"uploading an existing file"** (subir archivos existentes).
3. Arrastra todos los archivos de esta carpeta (`index.html`, los archivos `.png`, `.pdf` y este `README.md`).
4. Haz clic en **Commit changes**.
5. Ve a **Settings** > **Pages** > selecciona rama `main` y guarda.
6. ¡Listo! Comparte el enlace generado con el cliente.

---

## 📋 Estructura de Archivos

```
Proyecto Milwaukee-Hangcha/
├── index.html                        # PÁGINA 1: Aplicación web interactiva de Levantamiento & Validación (85 Equipos)
├── propuesta-comercial.html          # PÁGINA 2: Propuesta Comercial & Programa de Mantenimiento a 60 Meses (83 Equipos)
├── pagina2.html                      # Acceso directo alternativo a la Página 2
├── Levantamiento Planta Hangcha.xlsx  # Archivo Excel original de referencia
├── logo-milwaukee.png                # Logotipo oficial de Milwaukee Tool
├── logo-hangcha.png                  # Logotipo oficial de Hangcha México
├── *.png                             # Fotografías oficiales de estudio por modelo (DR16LI, FBT20LI, etc.)
├── *.pdf                             # Fichas técnicas oficiales descargables en PDF
└── README.md                         # Guía técnica, comercial y despliegue a GitHub
```

---

## 💼 Resumen de la Página 2: Propuesta Comercial & Mantenimiento

La **Página 2 (`propuesta-comercial.html`)** es una cotización formal y ejecutiva orientada a la toma de decisión para la Dirección de Compras, Supply Chain y Finanzas de **Milwaukee Tool**, integrando los datos de la cotización a 60 meses:

1. **Dashboard Financiero de KPIs**:
   - **83 Unidades en Contrato de Arrendamiento** (+2 unidades de relevo dedicadas).
   - **Renta Mensual Base**: `USD 75,661.80`.
   - **Deducción Comercial Propuesta (-10%)**: `-USD 7,566.18/mes`.
   - **Renta Mensual Ajustada**: `USD 68,095.62/mes`.
   - **Mantenimiento Integral In-Situ (METRIKA / Hangcha)**: `USD 18,650.00/mes`.
   - **Costo Mensual Combinado (Renta + Mtto)**: `USD 86,745.62/mes` (antes de IVA).
   - **Total Acumulado a 60 Meses**: `USD 5,204,737.20` (antes de IVA).

2. **Comparativa de Mantenimiento (Ahorro del 54.4%)**:
   - METRIKA / Hangcha: `USD 18,650.00/mes` | `USD 1,119,000.00` a 5 años.
   - Proveedor Directo: `USD 40,925.50/mes` | `USD 2,455,530.00` a 5 años.
   - **Ahorro Neto Directo para Milwaukee**: **`USD 22,275.50/mes`** y **`USD 1,336,530.00 USD`** durante los 60 meses.

3. **Desglose de Renta por Modelo (8 Modelos)**:
   - Tabla oficial con unidades, renta base, renta con -10%, costo total a 60 meses, costo unitario por modelo, fotos y fichas técnicas descargables en PDF.

4. **Estructura de Operación y Continuidad Operativa**:
   - **Capital Humano**: 1 Coordinador de Servicio, 1 Administradora / Agente de cuenta, 2 Técnicos residentes certificados en tecnología de litio Hangcha.
   - **Infraestructura**: Taller en sitio, unidad móvil para traslados/contingencias, y opción de oficina satélite cercana contigua a planta.
   - **Refacciones & Consumibles**: Stock local de alta rotación (1 kit de ruedas rudomáticas por modelo, mangueras hidráulicas de carro portacuchillas y pistones de levante, filtros y consumibles preventivos).
   - **Respaldo de Marca**: Almacén Central Hangcha en Pachuca, Hidalgo para suministro exprés de componentes mayores y soporte directo de planta armadora en China (Ingeniería Hangcha).
   - **Garantía Cero Paros**: 2 Equipos de Relevo dedicados (1 Double Reach DR16LI + 1 FBEE25LI de 2.5T) sin costo adicional por inactividad.
   - **Garantía de Fábrica & Mantenimiento**: 12 meses de garantía de fábrica en unidades nuevas, garantía extendida en celdas LiFePO4, control semanal de horómetros y programa de mantenimiento mensual.

5. **Herramientas de Exportación**:
   - Botón directo de **Impresión / Guardar PDF Formal** (`@media print` optimizado).
