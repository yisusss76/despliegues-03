# Documentación de la práctica: corrección y despliegue

## 1. Objetivo

Identificar y corregir un error visual en la página de EIG Campus,
registrar el cambio con Git y publicar la web mediante GitHub Pages.

La práctica se realiza en pareja, trabajando en un mismo repositorio
con ramas individuales y pull requests.

## 2. Repositorio

https://github.com/yisusss76/despliegues-03

Se ha creado un fork del repositorio del profesor y se ha añadido
al compañero como colaborador.

## 3. Error identificado

Los enlaces «Servicios» y «Contacto» del menú tenían el texto blanco.
Como el fondo de la cabecera también era blanco, los enlaces no se veían.

La regla responsable estaba en el archivo `styles.css`:

```css
.nav__menu a {
  text-decoration: none;
  color: white;
}
```

**Captura del error y del inspector:** pendiente de incorporar.

## 4. Corrección realizada

Se ha sustituido el color blanco por la variable `--color-text`,
definida en el CSS con el valor `#1f2933`.

```css
.nav__menu a {
  text-decoration: none;
  color: var(--color-text);
}
```

El cambio afecta únicamente al color de los enlaces del menú.

**Captura del resultado:** pendiente de incorporar.

## 5. Organización del trabajo en pareja

| Rama | Finalidad |
|---|---|
| `feature/dev1` | Elaboración de esta documentación |
| `feature/dev2` | Documentación de pruebas y sus resultados |
| `qa_pending` | Integración y revisión de las aportaciones |
| `uat_pending` | Validación previa a la publicación |
| `main` | Versión final publicada |

Cada integrante realiza sus commits desde su propia cuenta de GitHub.

La corrección inicial del CSS se guardó directamente en `main`,
antes de incorporar al proceso el requisito de trabajo por ramas.
Las ramas de desarrollo se crearon a partir de esa versión.

El trabajo posterior seguirá este recorrido mediante pull requests:

1. `feature/dev1` → `qa_pending`.
2. `feature/dev2` → `qa_pending`.
3. `qa_pending` → `uat_pending`.
4. `uat_pending` → `main`.

**Enlaces y capturas de commits, revisiones y pull requests:**
pendientes de incorporar conforme se realicen.

## 6. Pruebas

Los resultados y las evidencias de las comprobaciones se recogerán
en `PRUEBAS.md`, elaborado por el compañero.

## 7. Despliegue

La publicación se realizará con GitHub Pages utilizando la rama
`main` y la carpeta raíz `/ (root)`.

**Enlace público y capturas del despliegue:**
pendientes de incorporar y verificar.
