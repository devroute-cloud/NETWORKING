# El servidor DNS (El directorio de la Red)

1. Servidor DNS (Domain Name System)
   - El DNS se encarga de traducir los nombres legibles a las direcciones IP numéricas que entiende la red
   - Como "servidor-ad-local" o "google.com"

2. Cómo se interconecta con distintas herramientas_
   - Active Directory (AD DS): Depende al 100% de que el DNS funcione bien
   - Windows Server: Cuando creas un dominio los equipos con Windows buscarán el controlador del dominio haciendo preguntas al servidor DNS
   - Si el DNS falla, Active Directory entero se detendrá; por ese motivo, es vital que el DNS esté configurado debidamente.

3. Práctica guiada paso a paso dentro de Cisco Packet Tracer:
   1. Paso A: Colocaremos / 1 switch, 2 PCs y 1 Server
      - Clic en Server0 -> Desktop -> IP -> Configuración
   2. Escribe IP estática -> 192.168.1.100 -> máscara 255.255.255.0 -> Gateway en blanco por ahora -> cierra esa ventana

      
   
