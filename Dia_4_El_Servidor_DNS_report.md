# El servidor DNS (El directorio de la Red)

1. Servidor DNS (Domain Name System)
   - El DNS se encarga de traducir los nombres legibles a las direcciones IP numéricas que entiende la red
   - Como "servidor-ad-local" o "google.com"

2. Cómo se interconecta con distintas herramientas_
   - Active Directory (AD DS): Depende al 100% de que el DNS funcione bien
   - Windows Server: Cuando creas un dominio los equipos con Windows buscarán el controlador del dominio haciendo preguntas al servidor DNS
   - Si el DNS falla, Active Directory entero se detendrá; por ese motivo, es vital que el DNS esté configurado debidamente.

3. Práctica guiada paso a paso dentro de Cisco Packet Tracer:
   - Paso A: Colocaremos / 1 switch, 2 PCs y 1 Server
      - Clic en Server0 -> Desktop -> IP -> Configuración
      - Escribe IP estática -> 192.168.1.100 -> máscara 255.255.255.0 -> Gateway en blanco por ahora -> cierra esa ventana

     <img width="998" height="551" alt="image" src="https://github.com/user-attachments/assets/367f1d5b-6233-4340-a440-816aaed712f4" />

   - Paso B: Configurar el servicio DNS en el servidor:
     - En esa misma pestaña Server0 -> Services -> DNS -> interruptor de Service en ON
     - Name -> midominio.local
     - Address -> IP 192.168.1.100
     - Presionar Add para que aparezca en la lista de abajo

     <img width="998" height="551" alt="image" src="https://github.com/user-attachments/assets/24209208-fac7-4eb6-a41d-e81345f88dfe" />

   - Paso C: Configurar el DHCP para que reparta la IP del DNS
     - En el mismo Server0 -> DHCP -> ON
     - Default Gateway -> 192.168.1.1
     - ¡Lo más importante de hoy! En la casilla que dice DNS Server,borra 0.0.0.0 y escribe la IP 192.168.1.100
     - Configura el rango: Start IP Address en 192.168.1.10 y máscara 255.255.255.0
     - Save (Guardar) para actualizar el perfil

     <img width="1068" height="690" alt="image" src="https://github.com/user-attachments/assets/7e3b0eee-8449-45aa-98a2-11883dbcd830" />


  - Paso D: Hacer que la PC0 reciba el DNS
    - Clic en PC0 -> Desktop -> IP Configuration
    - Si estaba en Static, cámbiala a DHCP (o si ya estaba en DHCP, cámbiala a Static y vuelve a poner DHCP para que "renueve" su contrato).
    - Verás que ahora la PC0 recibe su IP automática y también recibe la dirección del DNS Server (192.168.1.100)
   
    <img width="995" height="523" alt="image" src="https://github.com/user-attachments/assets/224d38d2-16dd-4e99-afba-15bb6efec7c7" />

    <img width="995" height="523" alt="image" src="https://github.com/user-attachments/assets/362a2dc4-1417-4edd-8ae2-2806dc243f87" />

   - Paso E: La prueba de fuego con "nslookup":
     -En PC0 -> Command Prompt -> Escribe "nslookup midominio.local" -> Tiene que mostrarte la IP "192.168.1.100"

      



      
   
