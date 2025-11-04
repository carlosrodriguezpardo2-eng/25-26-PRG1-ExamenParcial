# Examen parcial Carlos Rodríguez Pardo

Este documento contiene las respuestas a las 5 preguntas del examen, donde se analizan errores en fragmentos de código y se proponen soluciones claras y justificadas.

---

## Pregunta 1

### Código original
```java
System.out.println("Vida Guerrero [" + vidaGuerrero + "] / Vida Vampiro [" + vidaVampiro + "]");
String elGanador = vidaGuerrero > 0 ? "Guerrero" : "Vampiro";
System.out.println("Ganó el" + elGanador);
```

### Errores encontrados
En la última línea del código no existe un espacio entre el texto a mostrar y la variable, lo que provoca que se muestre como "Ganó elGuerrero", suponiendo que haya ganado el guerrero como ejemplo

### Solución propuesta 
```java
System.out.println("Vida Guerrero [" + vidaGuerrero + "] / Vida Vampiro [" + vidaVampiro + "]");
String elGanador = vidaGuerrero > 0 ? "Guerrero" : "Vampiro";
System.out.println("Ganó el " + elGanador);
```

## Pregunta 2

### Código original
```java
System.out.println("Dia " + dia + " - " + hora + ":00  Consumo hora: " + consumoDia);
```

### Errores encontrados
Para empezar, el primer error que veo es que día no lleva tilde en la parte que se utiliza como texto, lo que es un error ortográfico. También he encontrado un espaciado incorrecto entre la hora y el consumo por hora al haber un doble espacio entre el ":00" y el "Consumo hora:". Por último, he encontrado una incongruencia en el nombre de la variable "consumoDia" y lo que representa ya que se supone que dicta el consumo por hora y esta nombrado como si dictase el consumo por día.

## Solución propuesta
```java
System.out.println("Dia " + dia + " - " + hora + ":00. Consumo hora: " + consumoHora);
```

## Pregunta 3

### Código original
```java
for (int piso = PISOS - 1; piso >= 1; piso--) {
    // ...
}
```

### Errores encontrados
El bucle no incluye el piso 0 al estar declarado para piso >= 1 y solo funciona hasta el piso 1.

### Solución propuesta
```java
for (int piso = PISOS - 1; piso >= 0; piso--) {
    // ...
}
```


## Pregunta 4

### Código original
´´´java
System.out.println("Media semanal: " + (consumoTotalSemana / 7));
´´´

### Erorres encontrados
La variable consumoTotalSemana está declarada como un int o entero, lo que lleva a la perdida de decimales al realizar la división y lleva a cierta inexactitud.

### Solución propuesta
Declarar consumoTotalSemana como un double.


## Pregunta 5

### Código original
```java
class batallaExtendida {
    public static void main(String[] args) {
        // ...
    }
}
```

### Errores encontrados
Las clases se deben declarar empezando con mayúscula y la clase "batallaExtendida" no lo está.

### Solución propuesta
```java
class BatallaExtendida {
    public static void main(String[] args) {
        // ...
    }
}
```