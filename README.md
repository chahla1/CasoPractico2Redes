# CasoPractico2Redes

https://github.com/chahla1/CasoPractico2Redes.git


#OSI/TCP‑IP

El modelo OSI tiene 7 capas (Física, Enlace de datos, Red, Transporte, Sesión, Presentación y Aplicación).
El modelo TCP/IP simplifica este esquema en 4 capas (Acceso a la red, Internet, Transporte y Aplicación). Los dos modelos son útiles para entender y diseñar redes. En este caso, la transferencia de archivos y el streaming multimedia se gestionarán principalmente en las capas de Transporte y Aplicación.

#Capa Física

La fórmula de Shannon es:
C = B × log₂(1 + SNR)
B = 300 MHz (300 × 10⁶ Hz).
SNR = 30 dB.
SNR_{lineal} = 10^{(30/10)} = 1000.
C = 300 × 10⁶ × log₂(1 + 1000).
C = 1.997 Gbps

Para el cableado, se sugiere utilizar QAM (Modulación por Amplitud en Cuadratura) por su alta eficiencia en entornos con poca interferencia. 
Para el Wifi, se sugiere utilizar OFDM (Multiplexación por División de Frecuencia Ortogonal), que es robusto frente a interferencias y multipath.

#Capa de Red

Dirección de red: 172.22.53.0
Máscara: /22 = 255.255.252.0
Rango de direcciones: 172.22.52.0 - 172.22.55.255
Total de direcciones: 2^32-2^22 = 2^10 = 1024
host por subred= 1024 - 2 = 1022

#Capa de Transporte

Se decide el uso de TCP para la transferencia de archivos debido a que el TCP ofrece control de flujo, control de errores y retransmisión en caso de pérdida, lo cual es esencial para archivos grandes donde la integridad es fundamental.
Se decide el uso de  UDP para el streaming multimedia debido a que el UDP es más rápido, con menos sobrecarga. En streaming, una pequeña pérdida de paquetes no es crítica, por lo que se prioriza la fluidez y latencia baja sobre la exactitud.

Formula: Tamaño de Ventana=Ancho de banda×RTT
RTT = 50 ms (0.05 s).
Ancho de banda = 10 Mbps (10 × 10⁶ bps).
MSS = 1460 bytes
Tamaño = 500,000bytes
num segmentos= 500,000/1460 = 342.47

#Capa de Aplicacion

FTP/SFTP para transferencias de archivos.
HTTP/HTTPS para streaming multimedia.
DNS para resolver nombres de dominio.

La multiplexacion explica cómo los servidores gestionan múltiples conexiones simultáneas utilizando técnicas como puertos y hilos.
DASH (Dynamic Adaptive Streaming over HTTP): Describe cómo ajusta la calidad del video en función del ancho de banda disponible.

#Capa de Seguridad

VPN: Configura VPNs para segmentos remotos.
Firewalls (ACLs): Define reglas para permitir o bloquear tráfico.
Cifrado:
Simétrico: AES para velocidad.
Asimétrico: RSA para intercambio seguro de claves.
DNSSEC: Configura firmas digitales para proteger las respuestas de DNS.
