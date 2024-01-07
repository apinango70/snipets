# Uso de diskpart

## Abra el símbolo del sistema como administrador y Ejecute el comando diskpart
    
##  Para ver todos los dispositivos de almacenamiento que están conectados actualmente y que son reconocidos en el sistema.:

```bash
list disk
```

## seleccionar la unidad deseada.​​​​​​ Use el número de índice asociado a la unidad, por ejemplo, select disk 2.

```bash
select disk
```

## eliminar las particiones y los datos de la unidad.

```bash
clean all
```

## crear una partición del tamaño completo de la unidad.

```bash
create partition primary
```

## para establecer el sistema de archivos y la etiqueta de volumen.

```bash
format override fs=NTFS quick label="MicroSD"
```
 
## para ver todos los volúmenes de los Dispositivos de almacenamiento disponibles.

```bash
list volume
```

## seleccionar el volumen recién etiquetado.

```bash
select volume #
```

## asignar una nueva letra al volumen.

```bash
assign letter=#
```

## para ver la nueva letra asignada al nuevo volumen.

```bash
list volume
```
