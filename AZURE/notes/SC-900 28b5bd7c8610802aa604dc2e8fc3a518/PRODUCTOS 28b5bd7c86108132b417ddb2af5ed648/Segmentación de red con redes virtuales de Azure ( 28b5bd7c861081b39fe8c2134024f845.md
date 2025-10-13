# Segmentación de red con redes virtuales de Azure (Azure Virtual Networks)

- **¿Qué es?** Las redes virtuales (VNets) son el bloque fundamental de construcción para tu red privada en Azure. Te permiten aislar lógicamente tus recursos de Azure.
- **¿Cómo funciona?** Cuando creas una VNet, defines tu propio espacio de direcciones IP privado. Dentro de una VNet, puedes crear **subredes**, que son segmentos lógicos más pequeños.

**Aislamiento:** Las VNets están aisladas entre sí por defecto. El tráfico no puede fluir directamente entre ellas a menos que configures específicamente el emparejamiento de VNets (VNet Peering) o uses un gateway.