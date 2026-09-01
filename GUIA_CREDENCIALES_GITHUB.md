# Restablecer credenciales de GitHub para hacer `push`

Este repositorio usa un remoto HTTPS:

```text
https://github.com/cristian-leon-avila/backend-wms.git
```

## 1. Revisar las cuentas guardadas

```powershell
git credential-manager github list
```

## 2. Eliminar la credencial anterior

Sustituye `<cuenta>` por el nombre mostrado en el paso anterior:

```powershell
git credential-manager github logout <cuenta>
```

En este equipo se ejecutó:

```powershell
git credential-manager github logout cristianleonavila
```

## 3. Autenticarse nuevamente y subir los cambios

Desde la raíz del repositorio, ejecuta:

```powershell
git push origin main
```

Git Credential Manager debería abrir el navegador. Inicia sesión en la cuenta de GitHub que tenga acceso al repositorio y autoriza la operación.

> GitHub no acepta la contraseña normal de la cuenta para operaciones Git por HTTPS. Usa el inicio de sesión del navegador que ofrece Git Credential Manager o un token de acceso personal.

## 4. Comprobar el resultado

```powershell
git status --short --branch
```

Si el `push` terminó correctamente, la rama local ya no debería aparecer adelantada respecto a `origin/main`.

## Si no aparece la ventana de autenticación

Inicia el acceso explícitamente y vuelve a intentar el `push`:

```powershell
git credential-manager github login
git push origin main
```

## Diagnóstico básico

Comprueba el remoto y el gestor configurado:

```powershell
git remote -v
git config --show-origin --get-all credential.helper
```

