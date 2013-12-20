# Contador aleatorio de 4 bits
Puedes ver cómo funciona [aquí](http://emiliocobos.net/demos/contador4bits/)

# Hacer cambios de estado manual
Si por ejemplo hay un bucle entre valores fuera de los que debería tomar el contador, se pueden obtener las nuevas tablas así:
```php
// Supongamos que el 5 se queda dando vueltas él sólo, por lo que queremos que vaya al 13
$counter->states["0101"] = "1101";

// Si ya habíamos generado las tablas hay que refrescarlas

// Tabla de transiciones
$counter->getTransitionData(true);
// Mapas de Karnaugh
$counter->getKarnaugTables(true);
```