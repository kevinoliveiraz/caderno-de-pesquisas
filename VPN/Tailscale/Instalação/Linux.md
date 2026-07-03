Tailscale — Instalação no Linux

Objetivo

Instalar o Tailscale em uma distribuição Linux e conectar o dispositivo à sua rede privada.

---

Método recomendado

O Tailscale disponibiliza um script oficial que detecta automaticamente a distribuição Linux e instala os pacotes necessários.

Execute:

```
curl -fsSL https://tailscale.com/install.sh | sh
```

---

Iniciar o serviço

Após a instalação, inicie o serviço e configure-o para iniciar automaticamente junto com o sistema.

sudo systemctl enable --now tailscaled

---

Autenticar o dispositivo

Conecte o computador à sua conta Tailscale.

sudo tailscale up

Será exibido um link no terminal.

1. Abra o link no navegador.
2. Faça login na sua conta.
3. Autorize o dispositivo.

Após a autenticação, o computador fará parte da sua rede privada.

---

Verificar a conexão

Obter o endereço IP do Tailscale:

tailscale ip -4

Listar todos os dispositivos da rede:

tailscale status

Ver informações detalhadas da conexão:

tailscale ip

---

Comandos úteis

Desconectar da rede:

sudo tailscale down

Reconectar:

sudo tailscale up

Verificar o status do serviço:

sudo systemctl status tailscaled

Visualizar os logs do serviço:

journalctl -u tailscaled

---

Resultado esperado

Após a autenticação, o dispositivo receberá um endereço IP da rede Tailscale e poderá se comunicar com os demais dispositivos autorizados na mesma rede privada, sem a necessidade de abrir portas no 
