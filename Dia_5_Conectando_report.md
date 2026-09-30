# Conectando Redes con el Router y la Puerta de Enlace

1. El router (enrutador): es el encargado de conectar la oficina con el exterior,
como: (otras oficinas, sucursales o internet)
2. El Switch: Es el encargado de conectar todos los equipos físicos dentro de una oficina Red LAN
3. La Puerta de Enlace (Default Gateway): Es la dirección IP del router que ve tu computadora,
En otras palabras: Cuando una PC quiere hablar con otra afuera de su red local, esta le entrega el paquete al Gateway diciendo:"Toma,sácalo de aquí".

# Cómo se interconect con la carrera IT
- En una infraestructura real de Windows Server, las empresas tienen múltiples VLANs (departamentos de recursos humanos, contabilidad y servidores).
- El router o un switch de capa 3 se encarga de enrutar el tráfico entre ellas.
- Además, es la puerta de salida obligatoria para que los equipos con Windows se conecten a servicios en la nube como "M365, Azure o Internet".

# Práctica guiada paso a paso en Cisco Packet Tracer

- Paso A: Armar la topologia del dia
  1. Coloca 1 Router > 1941 o 4321
  2. Coloca 1 Switch > 2960
  3. Coloca 2Pcs > PC0 y PC1 > conéctalas al Switch

     <img width="492" height="570" alt="image" src="https://github.com/user-attachments/assets/54cb5477-3afe-4ea2-9e0e-3bd99b5c2940" />

- Paso B: Conectar los dispositivos
  1. Usa el cable directo (Copper Straight-Through) > PC0 > Switch0 (FastEthernet0/1)
  2. Haz lo mismo con la PC1 > Switch0 (FastEthernet0/2)
  3. Ahora para conectar el Switch al router: cable directo > GigabitEthernet0/0 (o FastEthernet del switch según el modelo) > Switch0 > GigabitEthernet0/0 del Router0 > (Verás que los foquitos tardan unos segundos en ponerse en verde).
  4. Toma en cuenta estos pasos para activar el router ya que por defecto de fábrica viene apagado: Click en el Router > Configuration > menú izquierdo (GigabitEthernet0/0) > Port Status > ON

     <img width="492" height="570" alt="image" src="https://github.com/user-attachments/assets/8a59fa2d-b145-48fc-8b31-56d353d0c97e" />

- Paso C: Configurar la Puerta de Enlace en el Router - !¡De forma visual!
  1. Clic en el router
  2. Selecciona la pestaña Config (arriba)
  3. INTERFACE > clic en GigabitEthernet0/0 (o la interfaz que hayas conectado)
  4. En la parte derecha busca "IP Configuration"
     - En IPv4 Address escribe la que será nuestra puerta de enlace: 192.168.1.1
     - En Subnet Mask,haz clic y aparecerá sola: 255.255.255.0
  5. ¡Paso clave! Arriba a la izquierda de esa misma sección de la interfaz, busca el recuadro que dice "Port Status" y asegúrate de marcar la casilla "ON" (encendido). El foquito de la interfaz en el router se pondrá verde

   <img width="1103" height="823" alt="image" src="https://github.com/user-attachments/assets/ad6ef92f-b939-4546-800b-e595103d844a" />
  
