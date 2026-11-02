# Temporizador

Temporizador de cuenta regresiva con alerta previa, pensado para charlas, clases, reuniones o exposiciones donde importa saber cuándo queda poco tiempo.

**Pruébalo aquí:** https://illak.github.io/simple-timer-app/

## Qué hace

- Muestra el tiempo restante en formato digital (`MM:SS`), en tamaño grande.
- Permite definir un **tiempo total** (por ejemplo 15 min) y un **aviso de minutos restantes** (por ejemplo 3 min).
- Cuando quedan esos minutos, la pantalla se pone **roja** y suena un **beep** cada segundo.
- Al llegar a cero suena una **bocina tipo airhorn**.
- Modo **claro / oscuro** y modo **pantalla completa**.

## Cómo está hecho

Es una página web estática: un único archivo `index.html` con HTML, CSS y JavaScript, sin librerías, sin servidor y sin archivos de audio (los sonidos se generan en el navegador).
## Uso

1. Ingresa el tiempo total y el aviso (en minutos).
2. Pulsa **Iniciar**. Puedes **Pausar**, **Continuar** o **Reiniciar** cuando quieras.

| Tecla | Acción |
|-------|--------|
| `Espacio` | Iniciar / pausar |
| `R` | Reiniciar |
| `T` | Cambiar tema |
| `F` | Pantalla completa |

## Cosas a considerar

- **Sonido:** los navegadores solo permiten reproducir audio después de que el usuario interactúa con la página. El sonido queda habilitado al pulsar *Iniciar*. Revisa que el volumen del equipo esté activo y haz una prueba corta antes de usarlo en un evento.
- **Aviso menor al total:** el aviso siempre debe ser menor al tiempo total. Si pones un valor mayor, se ajusta automáticamente. Un aviso en `0` desactiva la alerta.
- **Ajustes bloqueados:** no se pueden cambiar los tiempos mientras el timer corre o está en pausa; usa *Reiniciar* para modificarlos.
- **Mantener la pestaña abierta:** el timer funciona con la pestaña en segundo plano, pero si cierras la página o el navegador se detiene.
- **Pantalla encendida:** mientras corre, la app intenta evitar que la pantalla se apague (depende del navegador).
- **Preferencias guardadas:** el tema y los ajustes se recuerdan en el propio navegador. No se envía información a ningún servidor.
- **Precisión:** el tiempo se calcula con el reloj del sistema, por lo que no se desfasa con el uso prolongado. Si el equipo se suspende, el tiempo seguirá contando.
