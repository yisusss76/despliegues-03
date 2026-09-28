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

### Captura del fallo original
<img width="1917" height="951" alt="Captura de pantalla 2026-09-28 123012" src="https://github.com/user-attachments/assets/7d1a4960-a3fd-4bdb-b8a9-c0a708e693b2" />

<img width="557" height="22" alt="image" src="https://github.com/user-attachments/assets/f4dc8210-3b01-4952-b5b6-41b747b97b44" />



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

### Resultado corregido
<img width="1917" height="962" alt="Captura de pantalla 2026-09-28 141018" src="https://github.com/user-attachments/assets/0fece1da-8100-4ac2-86f9-b8dcf59cfbf1" />

<img width="632" height="22" alt="image" src="https://github.com/user-attachments/assets/833e8d96-8d86-4e0a-832f-d0ced8425779" />



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

El trabajo posterior siguió este recorrido mediante pull requests:

1. `feature/dev1` → `qa_pending`.
2. `feature/dev2` → `qa_pending`.
3. `qa_pending` → `uat_pending`.
4. `uat_pending` → `main`.

### Revisión y fusión de la documentación

La pull request de `feature/dev1` a `qa_pending` fue aprobada
por daricuake-prog y fusionada por yisusss76.

[Ver pull request #1](https://github.com/yisusss76/despliegues-03/pull/1)

<img width="1917" height="976" alt="image" src="https://github.com/user-attachments/assets/b32b2c9f-b813-497c-a722-a9e6f070489c" />

### Revisión y fusión del plan de pruebas

daricuake-prog incorporó el plan de pruebas desde `feature/dev2`
a `qa_pending`. La pull request fue revisada y aprobada por
yisusss76, y fusionada por daricuake-prog.

[Ver pull request #2](https://github.com/yisusss76/despliegues-03/pull/2)

<img width="1917" height="971" alt="image" src="https://github.com/user-attachments/assets/c6e2d678-113e-4164-93b6-3d0c4f4ccc2d" />

## 6. Pruebas

Los resultados y las evidencias de las comprobaciones se recogen
en PRUEBAS.md. El compañero creó el plan y registró las primeras
pruebas; posteriormente añadí las capturas y completé los resultados.

## 7. Despliegue

La página se ha publicado mediante GitHub Pages.

En Settings → Pages se ha configurado:

- Source: Deploy from a branch.
- Branch: main.
- Carpeta: / (root).

Enlace público:
https://yisusss76.github.io/despliegues-03/

Se ha comprobado en una ventana de incógnito que la página carga
con sus estilos y permite acceder sin iniciar sesión en GitHub.

### Configuración de GitHub Pages
<img width="1917" height="965" alt="image" src="https://github.com/user-attachments/assets/c9e84858-76ce-46af-ba0b-e9f90c8d49cf" />


### Web publicada
<img width="1917" height="1015" alt="Captura de pantalla 2026-09-28 142226" src="https://github.com/user-attachments/assets/895e4d85-4b5a-4721-a4d9-9fc2bbff2a10" />

## 8. Integración final y despliegue

### Paso de QA a UAT

Se fusionó `qa_pending` en `uat_pending` mediante la pull request #6.

[Ver pull request #6](https://github.com/yisusss76/despliegues-03/pull/6)
<img width="1912" height="962" alt="Captura de pantalla 2026-09-28 185404" src="https://github.com/user-attachments/assets/473ac772-8d2b-480c-b93e-5c6da276fe63" />


### Validación y paso a main

yisusss76 comprobó en UAT los documentos, las capturas,
los resultados de las seis pruebas y la corrección del CSS.
Después se fusionó `uat_pending` en `main`.

Estas fusiones finales fueron realizadas por yisusss76 sin
una nueva aprobación del compañero.
<img width="1912" height="962" alt="Captura de pantalla 2026-09-28 185404" src="https://github.com/user-attachments/assets/93f7cb1e-9b18-4bfb-8949-9bea24261758" />


### Comprobación del despliegue

Tras la integración en `main`, la ejecución #2 de
`pages-build-deployment` terminó correctamente.
También se comprobó que la web publicada seguía funcionando.
<img width="1917" height="960" alt="Captura de pantalla 2026-09-28 185011" src="https://github.com/user-attachments/assets/106e9931-814c-4981-ae72-602614df983f" />


https://yisusss76.github.io/despliegues-03/

