
# Tailscale — VPN Mesh Privada

## O que é

Tailscale é uma solução de rede privada baseada em WireGuard que cria uma VPN em malha (mesh) entre dispositivos.

Cada dispositivo se conecta diretamente aos outros sempre que possível, reduzindo latência e eliminando a necessidade de um servidor VPN central tradicional.

A autenticação e coordenação da rede são feitas por um controlador externo (login), mas o tráfego de dados é ponto a ponto e criptografado.

Sua principal vantagem é:
- Acesso remoto a servidores sem abrir portas no roteador
- Conexão segura entre máquinas pessoais e homelab
- Rede privada entre dispositivos em diferentes locais
- Substituição de VPNs tradicionais complexas
- Acesso seguro a serviços internos (SSH, HTTP, dashboards)

---

## Arquitetura

- Base: WireGuard
- Modelo: Mesh VPN
- Endereços internos: 100.x.x.x
- Conexões diretas sempre que possível (NAT traversal automático)
- Relay (DERP) apenas quando P2P não é possível

---


