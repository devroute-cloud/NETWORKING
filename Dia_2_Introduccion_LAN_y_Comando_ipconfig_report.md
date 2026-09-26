# Introducción a las redes locales con Switch (LAN) y el comando "ipconfig"

- Switch:

1. Switch y red LAN (Local Area Network)
2. Switch (conmutador): es el distribuidor central o el corazón de una oficina.
3. En el día 1 conectamos 2 PCs directamente con un solo cable, pero en el mundo real suman casi 50 pcs en una empresa.
4. El switch recibe los datos de una PC y los redirige exactamente a la PC que debe recibirlos.

- El Comando:

1. El comando "ipconfig" es por excelencia en Windows para preguntarle a la PC:
   ¿Quién soy dentro de esta red?
2. Muestra la dirección "IP", "Máscara de Subred" y "Puerto de enlace"

# Práctica guiada junto a capturas de pantalla mostrando el paso a paso dentro de Cisco Packet Tracer

1. Paso A: abrir espacio limpio, File - New y esto abrirá un espacio para empezar a practicar

   <img width="407" height="602" alt="image" src="https://github.com/user-attachments/assets/e8fc0d8e-fb2d-49e1-a525-1f7d5f5c05a3" />

2. Paso B: Colocar el Switch, abajo izquierda - Network Devices - Switch - Modelo 2960 - arrástralo a la pantalla - esta sera nuestra caja que conecta todo.

   <img width="730" height="906" alt="image" src="https://github.com/user-attachments/assets/69a79182-1f73-4074-8388-e1d74054c327" />

3. Paso C: Colocar las PCs, End Devices - coloca 3 PCs alrededor del switch - PC0,PC1 y PC2

   <img width="941" height="942" alt="image" src="https://github.com/user-attachments/assets/36b31006-6174-480d-83b0-f1a2e7048e88" />

4. Paso D: Conectar todo al Switch, Connections (rayo) - Copper Straight-Through (cable directo)
   - Clic en el cable directo,luego clic en PC0 - FastEthernet0 - y luego arrastra el otro extremo hasta el Switch0 - FastEthernet0/1.
   - Haz lo mismo con la PC1 - FastEthernet0 / PC1 - Switch
   - Haz lo mismo con la PC2 - FastEthernet0 / PC2 - Switch
   - "Verás que los foquitos parpadean en ámbar/naranja unos segundos y luego en verde. ¡Esto significa que el switch ya estableció comunicación con las tres PCs!"

     <img width="941" height="942" alt="image" src="https://github.com/user-attachments/assets/04822f0b-ec78-420f-92ad-18151069738d" />

     <img width="941" height="942" alt="image" src="https://github.com/user-attachments/assets/c1c34bd7-a45a-4c8a-8d3b-2edd7b52c2f0" />

5. Paso E: Configurar IPs en la misma red LAN, Asignaremos IPs estáticas a las tres PCs para que formen parte de la misma red.
- PC0: Entra a Desktop > IP Configuration y pon IP: 192.168.10.10 (la máscara se completa sola). Cierra la ventana
- PC1: Entra a Desktop > IP Configuration y pon IP: 192.168.10.11 (la máscara se completa sola). Cierra la ventana
- PC2: Entra a Desktop > IP Configuration y pon IP: 192.168.10.12 (la máscara se completa sola). Cierra la ventana

  <img width="1681" height="632" alt="image" src="https://github.com/user-attachments/assets/11e3734b-19e1-420a-9f2b-cd82afa4ff80" />

6. Paso F: Probar el Switch y usar "ipconfig"
- Abre consola (Command Prompt) de la PC0
- Escribe el comando para ver la configuración de red de la PC: ipconfig.
(Observa cómo muestra la IP 192.168.10.10 que acabamos de configurar)

<img width="610" height="618" alt="image" src="https://github.com/user-attachments/assets/6c8143d3-79db-4870-b751-8d15e29f1488" />

- Ahora, desde esa misma pantalla negra de la PC0, hazle un ping a la PC2 para comprobar que *gracias al switch ahora se comunican*: "ping 192.168.10.12"

<img width="755" height="728" alt="image" src="https://github.com/user-attachments/assets/c3adaa82-0778-48b3-ae89-2a64b2aac560" />

🚀 Has hecho un trabajo excelente hoy
