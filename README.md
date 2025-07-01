# GS | Timer

Un complemento de Office (Office Add-in) profesional diseñado específicamente para OneNote que proporciona un temporizador visual para gestionar tiempo en actividades, reuniones y proyectos.

## 🚀 Características

- **Temporizador Visual**: Interfaz circular con barra de progreso animada
- **Controles Intuitivos**: Botones para iniciar, pausar y reiniciar
- **Configuración Flexible**: Permite establecer minutos y segundos
- **Indicadores Visuales**: Cambios de color según el tiempo restante
- **Integración con OneNote**: Agrega automáticamente notas cuando el temporizador termina
- **Diseño Profesional**: Interfaz moderna y responsive

## 🎯 Compatibilidad

- ✅ OneNote Online
- ✅ OneNote para Windows 10/11 (aplicación moderna)
- ❌ OneNote 2016 (cliente clásico)

## 🛠️ Tecnologías Utilizadas

- **Office.js**: API oficial de Microsoft Office
- **HTML5**: Estructura semántica
- **CSS3**: Estilos modernos con animaciones
- **JavaScript (ES6+)**: Lógica del temporizador
- **Fluent UI**: Componentes de diseño de Microsoft

## 📦 Instalación y Desarrollo

### Prerrequisitos

- Node.js (versión 14 o superior)
- npm o yarn
- OneNote Online o OneNote para Windows 10/11

### 🌐 Uso desde GitHub Pages (Producción)

**¡El más fácil!** El complemento está disponible públicamente en:
```
https://tu-usuario.github.io/gs-timer-onenote/
```

**Para usar el complemento:**
1. Descarga el manifest desde: `https://tu-usuario.github.io/gs-timer-onenote/manifest.xml`
2. En OneNote: **Insertar** → **Complementos** → **Cargar Mi Complemento** → **Subir Mi Complemento**
3. Selecciona el archivo `manifest.xml` descargado
4. ¡Listo! GS | Timer aparecerá en la cinta de OneNote

### 🔧 Desarrollo Local

### Configuración del Entorno

1. **Clonar el repositorio**:
   ```bash
   git clone https://github.com/tu-usuario/gs-timer-onenote.git
   cd gs-timer-onenote
   ```

2. **Instalar dependencias**:
   ```bash
   npm install
   ```

3. **Iniciar servidor de desarrollo**:
   ```bash
   npm run dev-server
   ```

4. **Hacer sideload del complemento**:
   ```bash
   npm start
   ```

### Scripts Disponibles

- `npm run build`: Construir para producción (GitHub Pages)
- `npm run build:dev`: Construir para desarrollo (localhost)
- `npm run build:pages`: Construir específicamente para GitHub Pages
- `npm run dev-server`: Iniciar servidor de desarrollo
- `npm run manifest:dev`: Generar manifest para desarrollo
- `npm run manifest:prod`: Generar manifest para producción
- `npm run deploy`: Build completo para GitHub Pages
- `npm run start`: Hacer sideload en OneNote (desarrollo)
- `npm run stop`: Detener el debugging
- `npm run validate`: Validar el manifest
- `npm run lint`: Verificar código
- `npm run lint:fix`: Corregir errores de linting automáticamente

## 🎨 Interfaz de Usuario

### Panel de Configuración
- **Campo Minutos**: 0-59 minutos
- **Campo Segundos**: 0-59 segundos

### Temporizador Visual
- **Círculo de Progreso**: Muestra el tiempo restante visualmente
- **Display Digital**: Formato MM:SS
- **Estados de Color**:
  - 🔵 Azul: Tiempo normal
  - 🟡 Amarillo: Menos del 25% del tiempo
  - 🔴 Rojo: Menos del 10% del tiempo o terminado

### Controles
- **Iniciar**: Comienza el temporizador
- **Pausar**: Pausa el temporizador (se puede reanudar)
- **Reiniciar**: Vuelve al tiempo inicial configurado

## 🔧 Estructura del Proyecto

```
gs-timer-onenote/
├── .github/workflows/        # 🆕 GitHub Actions para deployment
│   └── deploy.yml           # Workflow de GitHub Pages
├── scripts/                 # 🆕 Scripts de construcción
│   └── generate-manifest.js # Generador de manifest dinámico
├── manifest.xml             # Configuración del complemento (desarrollo)
├── config.json             # 🆕 Configuración de URLs por entorno
├── package.json             # Dependencias y scripts
├── webpack.config.js        # Configuración de build
├── babel.config.json        # Configuración de Babel
├── media/                   # Carpeta para logos personalizados
│   ├── logo.png            # Tu logo personalizado
│   └── README.md           # Guía de diseño
├── src/
│   ├── taskpane/
│   │   ├── taskpane.html   # Interfaz principal
│   │   ├── taskpane.css    # Estilos del temporizador
│   │   └── taskpane.js     # Lógica del temporizador (GSTimer)
│   └── commands/
│       ├── commands.html   # Página de comandos
│       └── commands.js     # Funciones de comandos
├── assets/                 # Iconos del complemento
├── dist/                   # 🆕 Build para GitHub Pages
├── GITHUB_PAGES.md         # 🆕 Documentación de GitHub Pages
└── README.md               # Este archivo
```

## 🚀 Uso del Complemento

1. **Abrir OneNote** (Online o Windows 10/11)
2. **Ir a la pestaña "Inicio"**
3. **Hacer clic en "Abrir Timer"** en el grupo "GS | Timer"
4. **Configurar el tiempo** deseado en minutos y segundos
5. **Hacer clic en "Iniciar"** para comenzar el temporizador
6. **Usar "Pausar"** para pausar temporalmente
7. **Usar "Reiniciar"** para volver a la configuración inicial

## � Casos de Uso

- **Reuniones de trabajo**: Controlar duración de juntas y presentaciones
- **Gestión de tiempo**: Técnica Pomodoro y bloques de tiempo
- **Presentaciones**: Limitar tiempo de exposiciones
- **Actividades de equipo**: Organizar trabajo colaborativo
- **Descansos programados**: Gestionar pausas activas
- **Sesiones de estudio**: Control de tiempo de estudio y revisión

## 🤝 Contribución

1. Fork el proyecto
2. Crear una rama para tu feature (`git checkout -b feature/nueva-funcionalidad`)
3. Commit tus cambios (`git commit -am 'Agregar nueva funcionalidad'`)
4. Push a la rama (`git push origin feature/nueva-funcionalidad`)
5. Crear un Pull Request

## 📝 Licencia

Este proyecto está licenciado bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

## 🐛 Reportar Problemas

Si encuentras algún problema o tienes sugerencias, por favor crea un [issue](https://github.com/tu-usuario/gs-timer-onenote/issues).

## 📚 Recursos Adicionales

- [Documentación de Office Add-ins](https://docs.microsoft.com/office/dev/add-ins/)
- [API de OneNote](https://docs.microsoft.com/office/dev/add-ins/onenote/)
- [Fluent UI](https://developer.microsoft.com/fluentui)
- [Office.js](https://docs.microsoft.com/office/dev/add-ins/reference/javascript-api-for-office)

---

Desarrollado con ❤️ por GS Solutions
