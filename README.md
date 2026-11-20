# Biblioteca Universitaria

Proyecto académico desarrollado con Java y Maven para modelar la gestión básica de libros en una biblioteca universitaria.

## Descripción

La clase `Libro` permite crear libros, consultar sus datos, prestarlos, devolverlos y comparar títulos por contenido.

El proyecto se utiliza para practicar pruebas unitarias y configuración de integración continua con herramientas de calidad de software.

## Tecnologías

- Java 21
- Apache Maven 3.9
- JUnit 5.10.2
- JaCoCo 0.8.14
- Checkstyle 3.3.1
- PMD 3.22.0
- SpotBugs 4.9.8.2
- GitHub Actions

## Funcionalidades

- Crear un libro con título y autor.
- Consultar título, autor y disponibilidad.
- Prestar un libro.
- Impedir prestar un libro que ya no está disponible.
- Devolver un libro.
- Comparar títulos sin utilizar identidad de cadena.

## Estructura

```text
src/
  main/java/Libro.java
  test/java/test/java/LibroTest.java
.github/workflows/ci.yml
pom.xml
```

## Ejecución

Compilar el proyecto:

```powershell
mvn -B clean compile
```

Ejecutar las pruebas:

```powershell
mvn -B test
```

Generar cobertura y construir el proyecto:

```powershell
mvn -B clean verify
```

## Herramientas de calidad

Ejecutar Checkstyle:

```powershell
mvn -B checkstyle:checkstyle
```

Ejecutar PMD:

```powershell
mvn -B pmd:pmd
```

Ejecutar SpotBugs:

```powershell
mvn -B compile spotbugs:spotbugs
```

Los reportes generados se encuentran en `target/`.

## Integración continua

El workflow de GitHub Actions ejecuta seis jobs:

1. Compilación Maven.
2. Pruebas unitarias JUnit.
3. Cobertura JaCoCo.
4. Análisis Checkstyle.
5. Análisis PMD.
6. Análisis SpotBugs.

Todos los jobs finales fueron ejecutados con JDK 21 y finalizaron correctamente:

- [Repositorio en GitHub](https://github.com/Alejandro-Moreira/Biblioteca_Universitaria)
- [Ejecución final de GitHub Actions](https://github.com/Alejandro-Moreira/Biblioteca_Universitaria/actions/runs/44817565656)

## Métricas verificadas

| Herramienta | Resultado |
|---|---|
| JUnit | 6 pruebas, 0 fallos, 0 errores |
| JaCoCo | 100% de instrucciones y ramas cubiertas |
| Checkstyle | 0 advertencias |
| PMD | 0 problemas |
| SpotBugs | 0 defectos |

## Repositorio

Los cambios principales incluyen:

- Estructura estándar para las pruebas JUnit.
- Corrección de formato y Javadoc en `Libro`.
- Prueba adicional para la comparación de títulos nulos.
- Pipeline completo de compilación y calidad.