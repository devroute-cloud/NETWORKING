# El Comando "tracert" y la Ruta de los Paquetes 

1. "tracert" (Traceroute): Es una herramienta de diagnóstico de red que muestra la ruta exacta y cada uno de los saltos intermedios,
(como routers) ¿Qué debe incluir un paquete de datos para viajar desde el origen hasta el destino?
Nos ayuda a localizar exactamente dónde se produce un fallo o un retraso en la red.

2. Práctica guiada paso a paso con Cisco Packet Tracer
   -Paso A: Armar la topología de dos redes separadas
    -Coloca 1 router modelo 1941 o 4321
    - 2 switches junto al router
    - 2 Pcs (PC0 conectada al Switch0 y PC1 conectada al Switch1)

   <img width="480" height="490" alt="image" src="https://github.com/user-attachments/assets/cf4ed9b6-3f50-4d74-b9a6-a72c3773ea86" />

   -Paso B: Conectar los dispositivos con los cables correctos
    - Utiliza un cable directo (Copper Straight-Through) de la PC0 al Switch0, y de la PC1 al Switch1
    - Para conectar los switches al router,usa también cables directos desde los puertos del switch hacia las dos interfaces del router.
      Adicional activa el router ( GigabitEthernet0/0 y GigabitEthernet0/1)

   <img width="873" height="748" alt="image" src="https://github.com/user-attachments/assets/74aabfb7-1350-472b-b3ed-76fdd0f5d30b" />

   - Paso C: Configurar las IPs y las puertas de enlace
     -PC0 y su lado del router:
      - IP del router (GigabitEthernet0/0): 192.168.1.1 (Máscara 255.255.255.0) -> ¡Recuerda darle a ON en Port Status!
      - IP de la PC0: 192.168.1.10 (Máscara 255.255.255.0), (Gateway 192.168.1.1)

        <img width="1375" height="985" alt="image" src="https://github.com/user-attachments/assets/0ff6996c-2d3a-46c4-9efd-546a2af6e915" />

     -PC1 y su lado del router:
      -IP del router (GigabitEthernet0/1):192.168.2.1 (Máscara 255.255.255.0) -> ¡Recuerda activar el puerto en ON!
      -IP de la PC1: 192.168.2.10 | Máscara: 255.255.255.0 | Gateway: 192.168.2.1

        <img width="1828" height="987" alt="image" src="https://github.com/user-attachments/assets/21f1306f-61c7-4da3-8a3f-b3782c61caac" />

   - Paso D La prueba del comando "tracert" = El comando "Tracert": rastrea el camino hacia la PC1 ubicada en la otra red
     - PC0 -> Commando Prompt -> tracert 192.168.2.10
     - Observa la magia de la consola: te mostrará el Salto 1 (la IP del router local) 192.168.1.1 que es la puerta de salida y el Salto 2 (la IP final del destino 192.168.2.10)

  <img width="948" height="988" alt="image" src="https://github.com/user-attachments/assets/555afbee-8eef-47e7-b4ad-ae8075a0d37d" />

## Has hecho un trabajo extraordinario el día de hoy
