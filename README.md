# Generador de Recorridos de Orientación
Última modificación 26-04-2026

Sistema web para crear y exportar recorridos de orientación en formato SVG. Todo en un único archivo HTML autocontenido, sin dependencias externas.

## Características

### 3 modos de visualización
- **3×3**: Campo cuadrado con distribución 3×3 por cuadrante (9 conos por cuadrante)
- **4×4**: Campo cuadrado con distribución 4×4 por cuadrante (16 conos por cuadrante)
- **Campo**: Campo rectangular con conos movibles y lógica de recorrido direccional

### Creación de recorridos
- Clic sobre un cono para añadirlo al recorrido
- Introducción manual de IDs separados por comas
- Generación aleatoria de recorridos
- Borrado y regeneración rápida

### Modo Campo — funcionalidades específicas
- **Plantillas de conos**: 6×6, 7×5 y 8×4 (conos sobrantes van a zona de descarte)
- **Niveles de dificultad**:
  - *Sencillo*: el recorrido siempre avanza hacia el doble círculo (meta), con posibilidad de pasos laterales al mismo nivel (probabilidad fija del 20%, máximo 2 consecutivos)
  - *Avanzado*: sin restricciones de dirección, completamente aleatorio
- **Distribución por filas**: el algoritmo agrupa los conos en filas por proximidad real y distribuye los puntos del recorrido de forma uniforme entre ellas, evitando que se acumulen en una sola fila
- **Detección de anomalías**: aviso antes de generar si la distribución de conos es irregular tras moverlos manualmente
- **Modo edición**: arrastrar conos, excluirlos a zona de descarte, resetear posiciones

### Múltiples recorridos
- Generación de N recorridos en una sola operación
- Vista de miniaturas en modal
- Navegación ◀ ▶ entre recorridos
- Exportación individual o en bloque

### Edición de IDs
- Editor visual con mapa interactivo: los IDs aparecen como campos editables directamente sobre cada cono
- Sincronización bidireccional entre mapa y lista lateral
- Detección de IDs duplicados en tiempo real (fondo rojo)
- Bloqueo del guardado si hay duplicados

### Exportación
- SVG en 3 tamaños
- PDF (A4 portrait)
- Nombre de recorrido configurable antes de exportar

### Configuración avanzada (por módulo)
- Grosor de líneas, bordes y tamaño de conos
- Radio de círculos de recorrido y tamaño de texto
- Número de puntos por recorrido (5–12), sincronizado entre panel principal y múltiples recorridos
- Forma de los conos (círculo o X)
- Tamaño de cuadrícula
- Fondo de imagen personalizable con control de opacidad

## Estructura del proyecto

```
generador-recorridos/
├── Generador_v_B_ultimo.html   # Aplicación completa (único archivo)
├── README.md                   # Este archivo
├── LICENSE.txt                 # Licencia MIT
└── .gitignore                  # Archivos a ignorar
```

## Uso

1. Abre `Generador_v_B_ultimo.html` en tu navegador (no requiere servidor)
2. Selecciona el módulo: 3×3, 4×4 o Campo
3. Crea tu recorrido:
   - Haz clic en los conos para añadirlos al recorrido
   - Usa el botón **Aleatorio** para generar uno automáticamente
   - Introduce IDs manualmente separados por comas
4. En modo Campo, selecciona la dificultad (Sencillo / Avanzado) antes de generar
5. Configura el estilo en **Configuración avanzada**
6. Exporta desde el menú **Exportar** (pon nombre al recorrido primero)

## Tecnologías

- HTML5, CSS3, JavaScript (ES6+)
- SVG para gráficos vectoriales
- Sin dependencias externas — funciona offline

## Licencia

MIT License — ver LICENSE.txt
