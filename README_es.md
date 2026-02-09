<div align="center">

![WIP](https://img.shields.io/badge/work%20in%20progress-yellow?style=for-the-badge)
![System & Kernel](https://img.shields.io/badge/System-brown?style=for-the-badge)
![Filesystem](https://img.shields.io/badge/Filesystem-Directory-blue?style=for-the-badge)
![C Language](https://img.shields.io/badge/Language-C-red?style=for-the-badge)

*Una reimplementacion del comando ls clasico*

</div>

<div align="center">
	<img src="/ft_ls.png">
</div>

# ft_ls

[README in English](README.md)

`ft_ls` es una implementacion desde cero del comando Unix `ls`. Este proyecto se centra en el recorrido de directorios, metadatos de archivos, ordenacion y formato de salida, igualando el comportamiento de `ls` lo mas posible.

### Que es ls?

`ls` es la utilidad estandar para:

- Listar archivos y directorios.
- Ver permisos, tamanos, propietarios y fechas.
- Ordenar y filtrar entradas.
- Recorrer directorios de forma recursiva.

### Flujo tecnico

1. Parsear flags y rutas de entrada.
2. Leer entradas con `opendir` y `readdir`.
3. Obtener metadatos con `stat` o `lstat`.
4. Ordenar por nombre o fecha.
5. Formatear salida (long format, ocultos, orden inverso).
6. Si `-R` esta activo, entrar en subdirectorios.

## Instalacion

```bash
git clone https://github.com/Kobayashi82/ft_ls.git
cd ft_ls
make
```

## Uso

```bash
./ft_ls [opciones] [archivo ...]
```

### Opciones
| Opcion | Categoria | Descripcion                          |
|--------|-----------|--------------------------------------|
| `-a`   | Listado   | Incluir archivos ocultos             |
| `-R`   | Listado   | Listado recursivo de subdirectorios  |
| `-t`   | Ordenacion| Ordenar por fecha de modificacion    |
| `-u`   | Ordenacion| Usar access time para ordenar        |
| `-r`   | Ordenacion| Orden inverso                        |
| `-f`   | Ordenacion| No ordenar; habilita `-a`            |
| `-l`   | Visualizacion | Formato largo                    |
| `-g`   | Visualizacion | Formato largo sin propietario    |
| `-d`   | Visualizacion | Lista el directorio en si        |

### Ejemplos

```bash
./ft_ls
./ft_ls -la
./ft_ls -lrt src
./ft_ls -R .
```

## Licencia

Este proyecto esta licenciado bajo la WTFPL – [Do What the Fuck You Want to Public License](http://www.wtfpl.net/about/).

---

<div align="center">

**📂 Desarrollado como parte del curriculum de 42 School 📂**

*"See your system as it really is"*

</div>
