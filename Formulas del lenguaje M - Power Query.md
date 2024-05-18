## LIMPIEZA DE COLUMNA

### Fórmula para eliminar todos los espacios " " conservado solo un carácter de este tipo.

```m
Text.Combine(List.Select(Text.Split(Text.Trim([data]), " "), each _ <> ""), " ")
```

Primera aplicación práctica: REPORTE RESUMEN DE PRESTAMOS POR OFICIAL
![[Pasted image 20240517163651.png]]

---

## COLUMNA PERSONALIZADA

### Fórmula para extraer los dos caracteres de una posición especificada, si el valor es un número conservarlo de lo contrario retornar null

```m
let
    ExtractedText = Text.Middle([nombre_oficial], 5, 2),
    IsNumber = try Number.FromText(ExtractedText) otherwise null,
    Result = if IsNumber <> null then ExtractedText else null
in
    Result
```

Primera aplicación práctica: REPORTE RESUMEN DE PRESTAMOS POR OFICIAL
Se extraer los valores de la oficina.
![[Pasted image 20240517164514.png]]


### Fórmula para comprobar si el registro de una columna es un valor dentro de un rango especificado

```m
let
    // Convertir el valor de la columna cod_of a número entero
    ConvertedValue = try Number.FromText([cod_of]) otherwise null,
    // Verificar si el valor convertido está dentro del rango de 40 a 2000
    Result = if ConvertedValue <> null and ConvertedValue >= 40 and ConvertedValue <= 2000 then "cod" else null
in
    Result

```

