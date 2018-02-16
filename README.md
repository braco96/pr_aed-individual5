# AED — Entrega Individual 5: Disk Usage
**Autor:** Luis Bravo  
**Curso:** 2017–2018 — Algoritmos y Estructuras de Datos (UPM)

Proyecto **Maven** organizado para la práctica sobre árboles y cálculo de uso de disco.

## Estructura
```
src/
  main/java/aed/diskusage/
    DiskUsage.java
    FileNode.java
    AEDTree.java
    Printer.java
    Ejemplo.java
  test/java/aed/diskusage/
    TesterInd5.java
    BuildSmokeTest.java
docs/guia.pdf
libs/net-datastructures-5.0.jar   # añadir manualmente
```

## Uso
```bash
# 1) Copia la librería net-datastructures-5.0.jar en la carpeta libs/
# 2) Compila y ejecuta los tests
mvn -q -DskipTests=false test

# Ejecuta el main de ejemplo
mvn -q -Dexec.mainClass=aed.diskusage.Ejemplo exec:java
```

### Descripción del ejercicio
Implementar el método `printDiskUsage(Tree<FileNode> tree)` que:
- Recorre el árbol de directorios/ficheros en **profundidad**.
- Calcula el **tamaño total** de cada subárbol (directorio o fichero).
- Imprime con `Printer.print` una línea con el tamaño y la ruta completa.
- No modifica el árbol original.

**Ejemplo esperado:**
```
10 /home/dir1/f1
20 /home/dir1/f2
29 /home/dir1/f3
59 /home/dir1/
10 /home/dir2/f4
20 /home/dir2/dir3/f5
20 /home/dir2/dir3/
30 /home/dir2/
89 /home/
```

Consulta *docs/guia.pdf* para más detalles.

— *Luis Bravo*