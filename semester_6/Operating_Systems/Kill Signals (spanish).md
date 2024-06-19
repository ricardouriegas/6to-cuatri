### Señales del KILL explicadas una por una

1. **SIGHUP (1)**
   - **Descripción:** Señal de "hangup" (colgar). Se envía cuando la terminal a la que está conectado un proceso se cierra.
   - **Uso común:** Reiniciar demonios sin detenerlos.

2. **SIGINT (2)**
   - **Descripción:** Señal de interrupción. Se envía cuando el usuario presiona `Ctrl+C` en la terminal.
   - **Uso común:** Interrumpir y detener procesos interactivos.

3. **SIGQUIT (3)**
   - **Descripción:** Señal de "quit" (salida). Similar a `SIGINT`, pero genera un volcado de núcleo.
   - **Uso común:** Terminar procesos con un volcado de núcleo para diagnóstico.

4. **SIGILL (4)**
   - **Descripción:** Señal de instrucción ilegal. Se envía cuando un proceso intenta ejecutar una instrucción no permitida.
   - **Uso común:** Detectar errores graves en el código.

5. **SIGTRAP (5)**
   - **Descripción:** Señal de trampa. Utilizada por los depuradores para detener un proceso en un punto específico.
   - **Uso común:** Depuración de programas.

6. **SIGABRT (6)**
   - **Descripción:** Señal de aborto. Se envía cuando un proceso llama a la función `abort()`.
   - **Uso común:** Terminar un proceso debido a un error crítico.

7. **SIGBUS (7)**
   - **Descripción:** Señal de error de bus. Se produce cuando un proceso causa un error de acceso a la memoria.
   - **Uso común:** Detectar errores de acceso a la memoria.

8. **SIGFPE (8)**
   - **Descripción:** Señal de error de coma flotante. Se envía cuando ocurre una excepción aritmética, como una división por cero.
   - **Uso común:** Detectar errores matemáticos en programas.

9. **SIGKILL (9)**
   - **Descripción:** Señal de matar. Termina un proceso de forma inmediata y no puede ser manejada ni ignorada.
   - **Uso común:** Forzar la terminación de un proceso problemático.

10. **SIGUSR1 (10)**
    - **Descripción:** Señal de usuario 1. Reservada para uso por el usuario.
    - **Uso común:** Señales definidas por el usuario para interacciones específicas.

11. **SIGSEGV (11)**
    - **Descripción:** Señal de violación de segmento. Se produce cuando un proceso intenta acceder a una memoria no permitida.
    - **Uso común:** Detectar errores de acceso a la memoria.

12. **SIGUSR2 (12)**
    - **Descripción:** Señal de usuario 2. Otra señal reservada para el usuario.
    - **Uso común:** Señales definidas por el usuario para interacciones específicas.

13. **SIGPIPE (13)**
    - **Descripción:** Señal de tubería rota. Se envía cuando un proceso escribe en una tubería sin lectores.
    - **Uso común:** Gestionar errores de escritura en tuberías.

14. **SIGALRM (14)**
    - **Descripción:** Señal de alarma. Se envía cuando una alarma establecida por `alarm()` o `setitimer()` expira.
    - **Uso común:** Temporizadores y gestión de tiempos de espera.

15. **SIGTERM (15)**
    - **Descripción:** Señal de terminación. Solicita la terminación de un proceso de manera ordenada.
    - **Uso común:** Terminar procesos de forma ordenada y controlada.

16. **SIGSTKFLT (16)**
    - **Descripción:** Señal de falla en la pila del coprocesador.
    - **Uso común:** Diagnóstico de errores específicos en el coprocesador.

17. **SIGCHLD (17)**
    - **Descripción:** Señal de hijo. Se envía a un proceso padre cuando un proceso hijo termina o se detiene.
    - **Uso común:** Gestionar la terminación de procesos hijo.

18. **SIGCONT (18)**
    - **Descripción:** Señal de continuar. Continúa un proceso que estaba detenido.
    - **Uso común:** Reanudar procesos detenidos.

19. **SIGSTOP (19)**
    - **Descripción:** Señal de detener. Detiene un proceso de forma inmediata y no puede ser manejada ni ignorada.
    - **Uso común:** Detener procesos temporalmente.

20. **SIGTSTP (20)**
    - **Descripción:** Señal de parada de terminal. Se envía cuando el usuario presiona `Ctrl+Z` en la terminal.
    - **Uso común:** Detener procesos interactivos.

21. **SIGTTIN (21)**
    - **Descripción:** Señal de entrada de terminal. Se envía cuando un proceso en segundo plano intenta leer de la terminal.
    - **Uso común:** Gestionar accesos no permitidos a la terminal.

22. **SIGTTOU (22)**
    - **Descripción:** Señal de salida de terminal. Se envía cuando un proceso en segundo plano intenta escribir en la terminal.
    - **Uso común:** Gestionar accesos no permitidos a la terminal.

23. **SIGURG (23)**
    - **Descripción:** Señal de datos urgentes. Se envía cuando hay datos urgentes disponibles en un socket.
    - **Uso común:** Gestionar comunicaciones de red urgentes.

24. **SIGXCPU (24)**
    - **Descripción:** Señal de límite de CPU. Se envía cuando un proceso excede su límite de tiempo de CPU.
    - **Uso común:** Gestionar procesos que consumen demasiados recursos.

25. **SIGXFSZ (25)**
    - **Descripción:** Señal de límite de tamaño de archivo. Se envía cuando un proceso intenta expandir un archivo más allá de su límite.
    - **Uso común:** Gestionar procesos que exceden los límites de tamaño de archivo.

26. **SIGVTALRM (26)**
    - **Descripción:** Señal de alarma virtual. Se envía cuando un temporizador virtual expira.
    - **Uso común:** Temporizadores específicos de procesos.

27. **SIGPROF (27)**
    - **Descripción:** Señal de perfil. Se envía cuando un temporizador de perfil expira.
    - **Uso común:** Herramientas de perfilado y análisis de rendimiento.

28. **SIGWINCH (28)**
    - **Descripción:** Señal de cambio de ventana. Se envía cuando el tamaño de la ventana de terminal cambia.
    - **Uso común:** Gestionar redimensionamientos de la terminal.

29. **SIGIO (29)**
    - **Descripción:** Señal de E/S asíncrona. Se envía cuando una operación de E/S asíncrona se completa.
    - **Uso común:** Gestionar E/S asíncronas.

30. **SIGPWR (30)**
    - **Descripción:** Señal de fallo de energía. Se envía cuando hay una condición de fallo de energía.
    - **Uso común:** Gestionar condiciones críticas de energía.

31. **SIGSYS (31)**
    - **Descripción:** Señal de llamada de sistema inválida.
    - **Uso común:** Detectar llamadas al sistema no válidas.

### Señales en tiempo real

Además de las señales estándar, existen señales en tiempo real (real-time signals) que pueden ser utilizadas para aplicaciones específicas y permiten mayor flexibilidad en el manejo de procesos. Estas señales son:

32. **SIGRTMIN (34) a SIGRTMAX (64)**
    - **Descripción:** Señales en tiempo real desde SIGRTMIN hasta SIGRTMAX. Estas señales se utilizan para aplicaciones específicas del usuario y pueden ser definidas y gestionadas según las necesidades.
    - **Uso común:** Comunicación avanzada entre procesos y manejo de eventos en tiempo real.
