# Generador de Recorridos de Orientación
Última modificación 16-01-2026

**** PARA DESCARGAR PRESIONA EN EL BOTÓN VERDE DE CÓDIGO Y DALE A DOWNLOAD ****

Sistema web para crear y exportar recorridos de orientación en formato SVG.

## Características

- **3 tipos de visualizaciones**:
  - **3x3**: Campo cuadrado con distribución 3x3 por cuadrante
  - **4x4**: Campo cuadrado con distribución 4x4 por cuadrante  
  - **Campo**: Campo rectangular con conos movibles

- **Funcionalidades**:
  - Selección manual de conos para generar recorridos
  - Generación de recorridos aleatorios
  - Exportación a SVG en 3 tamaños
  - Configuración avanzada de estilos
  - Modo edición (solo en Campo), donde se pueden cambiar la ubicación de conos y eliminar los que no interesen

## Estructura del Proyecto
generador-recorridos/
├── index.html # Página principal con menú
├── Recorridos 3x3.html # Visualización 3x3
├── Recorridos 4x4.html # Visualización 4x4
├── Recorridos Campo.html # Visualización Campo
├── README.md # Este archivo
└── .gitignore # Archivos a ignorar


## Uso

1. Abre `index.html` en tu navegador
2. Selecciona el tipo de visualización en el menú lateral
3. Crea tu recorrido:
   - Haz clic en los conos para seleccionarlos
   - Usa "Recorrido aleatorio" para generar uno automáticamente
   - Introduce números manualmente separados por comas
4. Configura el estilo en "Configuración avanzada"
5. Exporta a SVG con los botones correspondientes

## Tecnologías

- HTML5
- CSS3
- JavaScript (ES6+)
- SVG

## Licencia

MIT License
