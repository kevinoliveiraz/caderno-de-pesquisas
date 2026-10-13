# Resumo 

Esta nota apresenta  os principais componentes que formam um computador, suas funções e como trabalham em conjunto.

## Conteúdo a

- Estrutura física do computador (gabinete)
- Funcionamento da placa-mãe
- Papel do processador (CPU)
- Memória RAM e seu funcionamento
- Armazenamento em HDD e SSD
- Placa de vídeo (GPU)
- Fonte de alimentação (PSU)
- Placas de expansão (Wi-Fi e som)
- Portas de conexão do computador
- Periféricos de entrada (teclado e mouse)
- Periféricos de saída (monitor e caixas de som)
- Dispositivos USB (pendrive)
- Identificação dos componentes presentes no seu computador

  <img width="736" height="1104" alt="20260329_224833" src="https://github.com/user-attachments/assets/8d77b5b7-bb84-435a-bacf-e89e3855c0f0" />


# Componentes de um Computador

## COMPUTER CASE (Gabinete)

Caixa que protege e organiza todos os componentes internos. Possui ventilação para **airflow**, espaço para fonte, placa-mãe, unidades de armazenamento e coolers.

**Seu modelo:** AeroCool Mid Tower.

---

## MOTHERBOARD (Placa-mãe)

É o componente central do computador, responsável por conectar todos os demais componentes. CPU, memória RAM, GPU, SSD, fonte e cooler são ligados a ela. Também define quais processadores e memórias são compatíveis.

**Seu modelo:** ASRock A320M-HDV R4.0.

---

## CPU (Processador)

É o cérebro do computador. Executa todos os cálculos e instruções do sistema. Fica instalado no socket da placa-mãe.

Na imagem, o processador aparece sem o cooler, mostrando os pinos na parte inferior.

**Seu modelo:** AMD Ryzen 3 3200G.

---

## RAM (Memória RAM)

Memória temporária utilizada para armazenar os dados que o processador está utilizando no momento. Ao desligar o computador, todo o conteúdo é apagado.

Quanto maior a quantidade de RAM, maior a capacidade de executar vários programas simultaneamente sem perda de desempenho.

**Você possui:** 16 GB DDR4.

---

## HDD (Hard Disk Drive)

Disco rígido mecânico utilizado para armazenamento permanente. Possui discos magnéticos internos giratórios.

- Mais barato por gigabyte.
- Mais lento que um SSD.
- Ideal para armazenar grandes quantidades de arquivos, como filmes e séries.

---

## SSD (Solid State Drive)

Dispositivo de armazenamento eletrônico, sem partes móveis.

É muito mais rápido que um HDD.

Existem dois formatos principais:

- **SSD SATA 2.5"** (retangular)
- **SSD M.2 NVMe** (instalado diretamente na placa-mãe)

**Seu modelo:** SSD SATA de 480 GB.

---

## GPU (Placa de Vídeo)

Responsável pelo processamento gráfico e de vídeo.

Possui seu próprio processador gráfico (GPU) e memória dedicada (VRAM).

Além dos jogos, também pode acelerar tarefas como transcodificação de vídeos no Jellyfin.

**Seu modelo:** NVIDIA GTX 1050 Ti 4 GB.

---

## POWER SUPPLY (Fonte de Alimentação)

Converte a energia elétrica da tomada para as tensões utilizadas pelo computador (+12 V, +5 V e +3,3 V).

É responsável por alimentar todos os componentes do sistema.

**Seu modelo:** Tronos 500 W (sem certificação).

> ⚠️ É o componente mais crítico do seu setup e merece atenção em futuros upgrades.

---

## WIFI CARD (Placa Wi-Fi)

Placa PCI Express responsável por adicionar conectividade Wi-Fi ao computador.

Como a ASRock A320M-HDV R4.0 não possui Wi-Fi integrado, o acesso sem fio depende de uma placa PCI-e ou adaptador USB.

---

## RAM (Representação na imagem)

Na imagem aparecem os módulos (pentes) de memória RAM instalados nos slots da placa-mãe.

**Seu computador possui:**

- 2 módulos DDR4
- Total de 16 GB

---

## PORTS (Painel de Portas)

Conjunto de conexões localizado na parte traseira da placa-mãe.

Normalmente inclui:

- USB
- HDMI
- Ethernet (RJ-45)
- Áudio
- PS/2 (em alguns modelos)

É a região acessível na parte traseira do gabinete.

---

## SPEAKERS (Caixas de Som)

Dispositivo responsável pela reprodução de áudio.

**No seu caso:** Fortrek Black Hawk Soundbar.

---

## KEYBOARD (Teclado)

Dispositivo de entrada utilizado para digitação e comandos.

**Seu modelo:** Fortrek Ranger Rainbow (membrana).

---

## MOUSE

Dispositivo apontador utilizado para controlar o cursor.

**Seu modelo:** Fortrek Ranger RGB.

---

## MONITOR

Tela responsável pela exibição das imagens geradas pelo computador.

**Seu modelo:** Dell P2018Hc 19,5" IPS.

---

## USB DRIVE (Pendrive)

Dispositivo portátil de armazenamento conectado via USB.

Muito utilizado para:

- Instalar sistemas operacionais
- Armazenar arquivos
- Criar mídias bootáveis

**No seu homelab:** utilizado com o Ventoy para instalação de sistemas.

---

## SOUND CARD (Placa de Som)

Responsável pelo processamento de áudio.

Pode ser uma placa dedicada ou integrada à placa-mãe.

