# Resumo

Esta nota apresenta os conceitos fundamentais sobre Dual Boot, explicando como instalar e utilizar dois ou mais sistemas operacionais no mesmo computador. São abordados o funcionamento do bootloader, o particionamento do disco, os requisitos para instalação, as vantagens e desvantagens do método e a comparação com máquinas virtuais.

## Tópicos abordados

- O que é Dual Boot
- Funcionamento do Dual Boot
- Bootloader (GRUB e Windows Boot Manager)
- Requisitos para instalação
- Backup antes da instalação
- Verificação do tipo de partição (MBR e GPT)
- Verificação do modo de boot (UEFI e Legacy BIOS)
- Preparação do espaço em disco
- Instalação do segundo sistema operacional
- Exemplo de Dual Boot entre Windows e Linux
- Partição compartilhada
- Vantagens e desvantagens
- Dual Boot vs Máquina Virtual


# Dual Boot — Instalar Mais de Um Sistema Operacional

Dual Boot é a instalação de dois ou mais sistemas operacionais no mesmo computador.

Ao ligar o computador, um menu permite escolher qual sistema iniciar.

Exemplo:

```text
Windows 11
Linux Mint
```

ou

```text
Windows 11
Ubuntu
```

---

# Como Funciona

Cada sistema operacional é instalado em sua própria partição.

Exemplo:

```text
SSD 500 GB

├── Windows 11 (250 GB)
├── Linux Mint (200 GB)
└── Partição Compartilhada (50 GB)
```

Quando o computador inicia:

```text
BIOS/UEFI
↓
Bootloader
↓
Escolha do Sistema
↓
Windows ou Linux
```

---

# O Que é o Bootloader?

Bootloader é o programa responsável por iniciar o sistema operacional.

Exemplos:

- GRUB (Linux)
- Windows Boot Manager

Exemplo:

```text
GNU GRUB

→ Linux Mint
→ Windows 11
```

---

# Requisitos

- Espaço livre em disco;
- Pendrive bootável;
- Backup dos dados importantes;
- BIOS ou UEFI configurada corretamente.

---

# Antes de Começar

## Fazer Backup

Sempre faça backup dos arquivos importantes.

---

## Verificar Tipo de Partição

Windows:

```cmd
diskpart
list disk
```

Verifique se utiliza:

```text
GPT
```

ou

```text
MBR
```

---

## Verificar Modo de Boot

```text
UEFI
```

ou

```text
Legacy BIOS
```

Os sistemas devem utilizar o mesmo modo.

---

# Preparando Espaço

No Windows:

```text
Gerenciamento de Disco
```

ou

```cmd
diskmgmt.msc
```

Reduza a partição do Windows.

Exemplo:

```text
Windows = 500 GB

Reduzir 100 GB

Resultado:

Windows = 400 GB
Espaço Não Alocado = 100 GB
```

---

# Instalação do Segundo Sistema

1. Criar pendrive bootável;
2. Inicializar pelo pendrive;
3. Escolher instalação manual;
4. Utilizar o espaço não alocado;
5. Instalar o sistema.

---

# Exemplo Windows + Linux

```text
SSD 500 GB

Partição EFI
Windows 11
Linux Mint
Swap
```

Após a instalação:

```text
GRUB

Linux Mint
Windows 11
```

---

# Partição Compartilhada

É possível criar uma partição para troca de arquivos.

Exemplo:

```text
NTFS
```

Assim:

```text
Windows
↓
Arquivos
↑
Linux
```

Ambos conseguem acessar.

---

# Vantagens

- Dois sistemas no mesmo computador;
- Aproveitamento do hardware;
- Ambiente para estudos;
- Compatibilidade com diferentes softwares.

---

# Desvantagens

- Menos espaço disponível;
- Instalação mais complexa;
- Atualizações podem afetar o boot.

---

# Dual Boot vs Máquina Virtual

## Dual Boot

```text
Hardware
↓
Sistema Operacional
```

Desempenho total.

---

## Máquina Virtual

```text
Hardware
↓
Sistema Principal
↓
Máquina Virtual
↓
Sistema Convidado


