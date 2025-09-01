# Variables de Entorno para Python

## 🪟 Windows

Durante la instalación de Python, si marcaste **"Add Python to PATH"**, el instalador agrega automáticamente las variables.

Si no lo hiciste, debés configurarlo manualmente:

### Ruta típica de instalación

Python se instala en:
```
C:\Users\<TU_USUARIO>\AppData\Local\Programs\Python\PythonXX\
```
*(donde XX es la versión, por ejemplo Python311)*

La carpeta Scripts también debe ir en el PATH:
```
C:\Users\<TU_USUARIO>\AppData\Local\Programs\Python\PythonXX\Scripts\
```

### Configurar en variables de entorno

1. Ir a: **Panel de control** → **Sistema y seguridad** → **Sistema** → **Configuración avanzada del sistema** → **Variables de entorno**
2. En **Variables de usuario** o **Variables del sistema** → editar **Path** y agregar esas rutas
3. Guardar y reiniciar la consola

### Verificación

```bash
python --version
pip --version
```

## � Linux

En Linux el PATH generalmente ya apunta a los directorios donde se instala Python.

### Rutas comunes

Python suele estar en:
```
/usr/bin/python3
/usr/local/bin/python3
```

Pip suele estar en:
```
/usr/bin/pip3
/usr/local/bin/pip3
```

### Configurar manualmente (si fuera necesario)

1. Editar el archivo de configuración del shell que uses (`.bashrc`, `.zshrc`, `.profile`, etc.) en tu home:
   ```bash
   nano ~/.bashrc
   ```

2. Agregar:
   ```bash
   export PATH="/usr/local/bin:$PATH"
   ```

3. Guardar, cerrar y recargar:
   ```bash
   source ~/.bashrc
   ```

### Verificación

```bash
python3 --version
pip3 --version
```

## 🍎 macOS

En macOS es muy similar a Linux, pero depende de si es Intel o Apple Silicon.

### Rutas comunes

**Con Homebrew en Intel:**
```
/usr/local/bin/python3
/usr/local/bin/pip3
```

**Con Homebrew en Apple Silicon (M1, M2, M3):**
```
/opt/homebrew/bin/python3
/opt/homebrew/bin/pip3
```

### Configurar manualmente

1. Editar `.zshrc` (ya que macOS usa Zsh por defecto):
   ```bash
   nano ~/.zshrc
   ```

2. Agregar la ruta correspondiente:
   ```bash
   export PATH="/opt/homebrew/bin:$PATH"
   ```

3. Aplicar los cambios:
   ```bash
   source ~/.zshrc
   ```

### Verificación

```bash
python3 --version
pip3 --version
```