# Resumo

Esta nota apresenta os conceitos fundamentais sobre BIOS e UEFI, explicando seu papel na inicialização do computador, as diferenças entre as duas tecnologias e as principais configurações disponíveis para gerenciamento do hardware antes do carregamento do sistema operacional.

## Tópicos abordados

- O que são BIOS e UEFI
- Processo de inicialização (boot)
- Funções da BIOS
- Limitações da BIOS
- O que é UEFI
- Vantagens do UEFI
- Comparação entre BIOS e UEFI
- MBR e GPT
- Secure Boot
- Como acessar a BIOS/UEFI
- Configurações disponíveis
- Controle de ventoinhas (Fans)
- XMP e EXPO
- Virtualização (Intel VT-x e AMD-V)
- Atualização da BIOS
- Overclock
- Ordem de boot
- Exemplos práticos de uso
- Resumo das diferenças entre BIOS e UEFI

# BIOS e UEFI — O que são?

BIOS e UEFI são sistemas responsáveis por iniciar o computador antes do sistema operacional carregar.

Eles fazem a comunicação inicial entre:

- Processador (CPU)
- Memória RAM
- SSD/HD
- Placa de vídeo (GPU)
- Periféricos
- Sistema operacional

---

# Função principal

Quando você aperta o botão do computador, ocorre a seguinte sequência:

```text
Energia liga
↓
BIOS/UEFI inicia
↓
Verifica o hardware
↓
Encontra o sistema operacional
↓
Windows/Linux inicia
```

---

# O que é BIOS?

BIOS significa **Basic Input/Output System**.

É o sistema tradicional de inicialização dos computadores, responsável por preparar o hardware antes de carregar o sistema operacional.

---

# O que a BIOS faz?

- Detecta o hardware instalado.
- Inicializa os componentes.
- Verifica erros básicos.
- Define a ordem de boot.
- Inicia o sistema operacional.

---

# Limitações da BIOS

A BIOS possui algumas limitações quando comparada ao UEFI:

- Interface simples.
- Suporte limitado para discos grandes.
- Inicialização mais lenta.
- Menos recursos modernos.

---

# O que é UEFI?

UEFI significa **Unified Extensible Firmware Interface**.

É o sucessor moderno da BIOS e está presente na maioria dos computadores atuais.

---

# Vantagens do UEFI

- Interface gráfica.
- Suporte ao mouse.
- Boot mais rápido.
- Maior segurança.
- Compatibilidade com SSDs NVMe.
- Suporte a discos de grande capacidade.
- Secure Boot.
- Melhor gerenciamento do hardware.

---

# BIOS vs UEFI

| BIOS | UEFI |
|------|------|
| Tecnologia antiga | Tecnologia moderna |
| Interface simples | Interface gráfica |
| Boot mais lento | Boot mais rápido |
| Menos recursos | Mais recursos |
| Utiliza MBR | Utiliza GPT |
| Menor segurança | Suporte ao Secure Boot |

---

# MBR e GPT

A BIOS normalmente utiliza o padrão de particionamento **MBR**.

O UEFI utiliza **GPT**, que oferece:

- Suporte a discos maiores.
- Mais partições.
- Maior confiabilidade.

---

# Secure Boot

O Secure Boot é um recurso do UEFI que impede a execução de:

- Malwares de boot.
- Rootkits.
- Sistemas não autorizados.

É amplamente utilizado no Windows 11.

---

# Como acessar a BIOS/UEFI

Durante a inicialização do computador, utilize a tecla correspondente ao fabricante:

| Fabricante | Tecla |
|------------|-------|
| ASUS | DEL / F2 |
| Gigabyte | DEL |
| MSI | DEL |
| Acer | F2 |
| Lenovo | F1 / F2 |
| Dell | F2 |

---

# Configurações disponíveis

Na BIOS/UEFI é possível configurar:

- XMP/EXPO
- Ordem de boot
- Controle das ventoinhas
- Overclock
- Virtualização
- Configuração de SSDs
- Frequência da memória RAM

---

# Controle de ventoinhas

Permite ajustar:

- Velocidade das ventoinhas.
- Curvas de rotação.
- Temperatura alvo.

Essas configurações influenciam:

- Ruído.
- Fluxo de ar (airflow).
- Temperatura do sistema.

---

# XMP / EXPO

Tecnologia utilizada para ativar a velocidade nominal da memória RAM.

Exemplo:

- Memória adquirida: **3200 MHz**
- Sem XMP: **2400 MHz**
- Com XMP: **3200 MHz**

---

# Virtualização

Necessária para:

- Máquinas virtuais.
- Docker.
- WSL.
- Hyper-V.
- Emuladores.

Principais tecnologias:

- Intel VT-x
- AMD-V

---

# Atualização da BIOS

Atualizar a BIOS pode:

- Corrigir falhas.
- Melhorar a compatibilidade.
- Adicionar suporte a novos processadores.
- Aumentar a estabilidade.

**Importante:** interromper a atualização pode inutilizar a placa-mãe.

---

# Overclock

A BIOS/UEFI permite:

- Alterar o clock do processador.
- Ajustar tensões.
- Configurar a memória RAM.
- Modificar limites de energia.

---

# Boot

Boot é o dispositivo utilizado para iniciar o sistema operacional.

Exemplo de prioridade:

1. SSD NVMe
2. Pendrive
3. HD

---

# Exemplos práticos

## Instalar o Windows

Alterar a ordem de boot para iniciar primeiro pelo pendrive.

## Resolver problemas de temperatura

Configurar:

- Ventoinhas.
- Curvas de rotação.
- Fluxo de ar.

## Melhorar o desempenho

Ativar recursos como:

- XMP/EXPO
- Resize BAR
- Precision Boost

---

