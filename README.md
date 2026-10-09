# Cajero automático — Spring Core e inyección de dependencias

**Autor:** Maria del Carmen Chavez Conde

## Cómo correrlo

    ./correr.sh App final-app
    ./probar.sh final

## Las piezas

| Bean | Clase | Cómo lo declara Spring (`@Component` o `@Bean`) | Singleton o prototype |
|configuracionBanco|configuracionBanco|@componenet|---|
|repositorio   |antifraudePorMonto|@componenet    
|antifraude   | cajeroAutomatico|@componenet
|notificador   |notificadorConsola|@componenet
|reloj|reloj|
| cajero| CajeroAutomatico | … | … |


## Boleto de salida

1. ¿Qué es la inyección de dependencias? Explícalo con el cajero, en tus palabras.
La case no crea los objetos que va a usar, la inyeccion de dependencias inyecta por medio del constructor lo que necesita
2. En la MP-1, ¿quién decidía qué antifraude usaba el cajero? ¿Y desde la MP-2?
main el la primera, el contenedor
3. ¿Cuándo usarías `@Bean` en vez de `@Component`? Da el ejemplo de hoy.
Bean es para clases escritas por terceros, y Component cuando yo soy el autor del código
4. ¿Qué gana: `@Primary` o `@Qualifier`? ¿Por qué tiene sentido?
En Spring, la anotación @Qualifier tiene mayor prioridad porque es una instrucción explícita y directa, mientras que @Primary actúa simplemente como una opción por defecto ("fallback") cuando hay ambigüedad y no se ha especificado nada.
5. En tu proyecto de Empleados de la Semana 3 nunca escribiste `@ComponentScan`. ¿Quién lo hace? (Pista: abre la
   anotación `@SpringBootApplication` con `Ctrl+clic` y busca las anotaciones que tiene arriba.)
   @ComponentScan
