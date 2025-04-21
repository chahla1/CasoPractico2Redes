# CasoPractico2Redes
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
