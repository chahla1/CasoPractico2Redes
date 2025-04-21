```mermaid
graph TD
    subgraph Clientes
        Aulas["Aulas (PCs, Tablets)"]
        Bibliotecas["Bibliotecas (PCs, Laptops)"]
        Laboratorios["Laboratorios (PCs)"]
    end

    subgraph Servidores
        ServidorArchivos["Servidor de Archivos"]
        ServidorMultimedia["Servidor de Streaming Multimedia"]
        DNS["Servidor DNS"]
    end

    subgraph RedHeterogenea["Red Heterogénea (Cableado/WiFi)"]
        AP["Puntos de Acceso WiFi"]
        Switches["Switches y Enlaces Cableados"]
        Router["Router Principal"]
    end

    Clientes -->|"Conexión a través de WiFi o Cableado"| RedHeterogenea
    RedHeterogenea -->|"FTP/SFTP (TCP), HTTP/HTTPS (TCP), DNS"| Servidores
    Servidores -->|Respuestas y contenidos (archivos, streaming, nombres de dominio)| RedHeterogenea
    DNS -->|"Resolución de nombres"| RedHeterogenea
```