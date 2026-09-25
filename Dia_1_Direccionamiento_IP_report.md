# Direccionamiento IP y Conectividad Básica (PING)

1. Una dirección IP es la dirección de una computadora dentro de una red.
2. El comando PING sirve para comprobar si un dispositivo puede comunicarse con otro a través de una red local.

# Cómo se interconecta:

1. Windows Server 2025 y los equipos con Windows 11: cada máquina necesitará una IP única.
2. Esto permitirá que puedan comunicarse dentro de una red local y con el AD DS.
3. Si una IP está mal configurada, el entorno Windows 11 jamás encontrará el servidor.

# Práctica guiada con capturas de pantalla incluidas paso a paso dentro de Cisco Packet Tracer:

### Paso A: Apertura de Packet Tracer en tu PC. Verás una pantalla en blanco grande (el área de trabajo)

<img width="1841" height="1028" alt="image" src="https://github.com/user-attachments/assets/c20a0930-eff2-4ae6-9dd9-01a781b4fb6e" />

### Paso B: Encuentra los dispositivos.
1. Abajo a la izquierda, encuentra el círculo celeste que dice END DEVICES y haz clic.

<img width="330" height="130" alt="image" src="https://github.com/user-attachments/assets/a8a1c10c-889d-4498-8488-e736b9c6f4bf" />

2. Selecciona el icono que dice PC, luego haz clic en dos partes distintas de la pantalla para que aparezcan la PC0 y la PC1.

<img width="661" height="663" alt="image" src="https://github.com/user-attachments/assets/9cfb0ff2-f75a-42de-a2b6-6e0c33b548a4" />

### Paso C: Conectar las PCs.
1. Localiza el icono que parece un rayo eléctrico (se llama CONNECTIONS). Haz clic en él.
2. Busca el cable llamado COOPER CROSS-OVER (el cable cruzado sirve para conectar dos computadores directamente). Haz clic en él.
3. Haz clic en PCO, selecciona FastEthernet0 y arrastra el cursor hasta PC1 y selecciona FastEthernet0
4. Verás que los foquitos ahora son verdes, indicando que tenemos conexión física.

<img width="661" height="663" alt="image" src="https://github.com/user-attachments/assets/4456ef3e-1295-4d1b-b709-312fba248562" />
<img width="661" height="663" alt="image" src="https://github.com/user-attachments/assets/1542e957-9c9c-48ee-ae03-e16d3285bf55" />
<img width="661" height="663" alt="image" src="https://github.com/user-attachments/assets/ade5ebc5-ff93-47f2-9397-b5d0ead797e2" />

### Paso D: Configurar la IP en la PC0
1. Haz doble clic rápido sobre la PC0. Se abrirá una ventanilla con varias pestañas.
2. Selecciona la pestaña que dice DESKTOP.
3. Dentro de esa pestaña haz clic en el icono que dice IP CONFIGURATION.
4. En la ventana que se abre, debe estar marcado STATIC (estático).

<img width="1031" height="852" alt="image" src="https://github.com/user-attachments/assets/2b106271-2034-481c-8f68-1475c7afbf9e" />

5. En la casilla (IPv4 Address, escribe 192.168.1.10)
6. En la casilla Subnet Mask, verás que sola se completa con 255.255.255.0
7. Luego cierra en la X que está a la derecha justo donde indica el cursor
8. Con esta acción abremos configurado la IP de la PC0

<img width="990" height="843" alt="image" src="https://github.com/user-attachments/assets/5ba4d754-d892-4f37-bb90-62362275129f" />

### Paso E: Configurar la IP en la PC1
1. 


