# Automatización de Red con el Servidor DHCP

- 🚀 Hoy subiremos de nivel y dejaremos de configurar las IPs a mano una por una,
Y vamos a hacer que un servidor lo haga por nosotros de forma automática

1. Protocolo y Servidor DHCP (Dynamic Host Configuration Protocol)
- El DHCP: es un servicio que vive en un servidor y se encarga de asignar "automáticamente" una 
dirección IP, máscara y puerta de enlace a cada computadora en el preciso instante en que se conecta a la red "JPG"

2. Cómo se interconectan con los diferentes servicios Windows
- Por ejemplo, si estás construyendo en un entorno Windows Server 2025 deberás saber esto:
Una de las primeras tareas obligatorias que harás al levantar tu infraestructura de red será:
Instalar y configurar el rol de DHCP. Es el corazón invisible que alimenta de direcciones IP a todas tus estaciones de trabajo,
Para que puedan comunicarse sin que tengas que configurar nada manualmente.

3. Práctica guiada paso a paso dentro de Cisco Packet Tracer

- Paso A: (Armar la topología del día): abre una ventana en blanco (nueva):
  - Coloca 1 switch (el clásico 2960 del día)
  - Coloca 1 servidor - End Device - Server y ponlo a un lado
  - Coloca 2 PCs (PC0 y PC1) alrededor del switch
    
    <img width="935" height="788" alt="image" src="https://github.com/user-attachments/assets/79d86788-27b5-4f5b-ada3-935222ffcd6b" />

- Paso B: (Conectar todo con cables directos): Selecciona el cable (Copper Straight-Through)
  - Conecta el Server0 (FastEthernet0) - al switch (FastEthernet0/1)
  - Conecta la PC0 (FastEthernet0) - al switch (FastEthernet0/2)
  - Conecta la PC1 (FastEthernet0) - al switch (FastEthernet0/3)
  - Espera a que todos los foquitos estén verdes, ya que eso indica que tiene conexión con el switch.

    <img width="935" height="788" alt="image" src="https://github.com/user-attachments/assets/0ec02261-7ab1-4955-b3cb-70bf801d4824" />

- Paso C: (Asignar IP fija al servidor DHCP): Recuerda "El servidor necesita una IP fija y estática para que las PCs sepan a quién pedirle ayuda"
  - Haz doble clic en Server0,ve a la pestaña Desktop > IP Configuration.
  - En IPv4 Address, escribe: 192.168.1.100 > La máscara se llenará sola 255.255.255.0 > cierra

    <img width="963" height="561" alt="image" src="https://github.com/user-attachments/assets/617781c8-86c0-4dc5-9269-f1c3cdb253ca" />

- Paso D: (Encender el rol de DHCP en el servidor):
  - Dentro de Server0 cambia a la pestaña Services (está arriba, al lado de Desktop)
  - En el menú de la izquierda,busca y haz clic en DHCP
  - Haz lo siguiente
    1. Asegúrate de que el botoncito de Service esté en ON (encendido)
