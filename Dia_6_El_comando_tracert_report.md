# El Comando "tracert" y la Ruta de los Paquetes 

1. "tracert" (Traceroute): Es una herramienta de diagnóstico de red que muestra la ruta exacta y cada uno de los saltos intermedios,
(como routers) ¿Qué un paquete de datos debe dar para viajar desde el origen hasta el destino?
Nos ayuda a localizar exactamente dónde hay un fallo o un retraso en la red.

2. Práctica guiada paso a paso con Cisco Packet Tracer
   -Paso A: Armar la topología de dos redes separadas
    -Coloca 1 router modelo 1941 o 4321
    - 2 switches junto al router
    - 2 Pcs (PC0 conectada al Switch0 y PC1 conectada al Switch1)

   <img width="480" height="490" alt="image" src="https://github.com/user-attachments/assets/cf4ed9b6-3f50-4d74-b9a6-a72c3773ea86" />

   -Paso B: Conectar los dispositivos con los cables correctos
    - Utiliza un cable directo (Copper Straight-Through) de la PC0 al Switch0, y de la PC1 al Switch1
    - Para conectar los switches al router,usa también cables directos desde los pertos del switch hacia las dos interfaces del router.
      Adicional activa el router ( GigabitEthernet0/0 y GigabitEthernet0/1)

   <img width="873" height="748" alt="image" src="https://github.com/user-attachments/assets/74aabfb7-1350-472b-b3ed-76fdd0f5d30b" />
