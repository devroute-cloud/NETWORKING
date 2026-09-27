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
    2. En la opción Gateway, escribe la puerta de enlace que usaremos 192.168.1.1
    3. En DNS Server déjalo por ahora en 0.0.0.0 (lo veremos en el siguiente día)
    4. En Start IP Address, asegúrate de que inicie en 192.168.1.10 (para que empiece a repartir desde la 10 en adelante)
    5. En Maximum Number of Users, puedes dejarlo en 246
    6. Paso Crucial: Debajo pulsa el botón Guardar (SAVE), y verás que se añade un espacio justo debajo

       <img width="977" height="725" alt="image" src="https://github.com/user-attachments/assets/e05aa98d-01f1-452d-a54a-ec883065f29d" />

- Paso E: (Hacer que las PCs pidan su IP automáticamente):
  - Ahora ve a PC0 > doble clic > Desktop > IP > Configuration
  - ¿Te acuerdas de que antes marcábamos Static?Pues ahora marcaremos la opción que dice DHCP
  - ¡Mira lo un segundo…! ¡Magia! Verás cómo la PC0 le pregunta al servidor y recibe automáticamente su IP (debería asignarse la 192.168.1.10) y su máscara
 
    <img width="1000" height="597" alt="image" src="https://github.com/user-attachments/assets/3779f4bc-6d7d-47c5-9b24-22b580ab106e" />

  - Haz exactamente lo mismo con la PC1: entra a Desktop > IP > Configuration > cámbiala a DHCP, y observa cómo recibe su IP solita (debería ser la 192.168.1.11)
 
    <img width="940" height="653" alt="image" src="https://github.com/user-attachments/assets/af670576-76a7-40da-9fcb-b6acc1c5b383" />

- Paso F: (La prueba de fuego ping):
  - Abre Command Prompt de la PC0
  - Escribe "ipconfig" para verificar que el servidor DHCP le dio su IP correctamente
  - Luego hazle un "ping" a la Pc1 usando la "IP" que le asignó el servidor

    <img width="1122" height="728" alt="image" src="https://github.com/user-attachments/assets/2889d27a-7365-4382-b216-1c1fcee0fcf4" />

    <img width="1122" height="728" alt="image" src="https://github.com/user-attachments/assets/1c9f0654-9f0b-4750-bb66-c8157a25a619" />



¡Qué gran avance! 🎉


