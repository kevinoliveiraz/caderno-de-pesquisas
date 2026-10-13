# Resumo

Esta nota apresenta o sistema de arquivos NTFS (New Technology File System), explicando sua função na organização e gerenciamento de dados em dispositivos de armazenamento. Também aborda seus principais recursos, comparações com outros sistemas de arquivos, formas de identificação no Windows e Linux e os cenários mais indicados para sua utilização.

## Tópicos abordados

- O que é NTFS
- Função de um sistema de arquivos
- Onde o NTFS é utilizado
- Suporte a arquivos grandes
- Permissões de acesso
- Journaling
- Compressão de arquivos
- Criptografia (EFS)
- Como verificar se um disco utiliza NTFS no Windows
- Como verificar se um disco utiliza NTFS no Linux
- Comparação entre NTFS e FAT32
- Comparação entre NTFS e EXT4
- Quando utilizar NTFS
- Quando não utilizar NTFS
- Exemplo de uso em um ambiente com Dual Boot




# NTFS — New Technology File System

## O que é NTFS?

NTFS (New Technology File System) é o sistema de arquivos padrão utilizado pelo Windows desde o Windows NT.

Ele é responsável por organizar e armazenar arquivos dentro de discos, SSDs, pendrives e outras unidades de armazenamento.

Sem um sistema de arquivos, o sistema operacional não saberia onde os dados estão armazenados.

---

# Função do Sistema de Arquivos

Imagine um disco vazio:

```text
SSD
└── Espaço em Branco
```

O sistema de arquivos cria uma estrutura para organizar:

```text
SSD
├── Documentos
├── Fotos
├── Vídeos
└── Sistema Operacional
```

---

# Onde o NTFS é Utilizado?

- Windows 11
- Windows 10
- Windows Server
- HDs externos
- SSDs
- Alguns pendrives

---

# Principais Recursos

## Arquivos Grandes

O NTFS suporta arquivos muito maiores que o FAT32.

Exemplo:

```text
FAT32 → Máximo 4 GB por arquivo

NTFS → Vários terabytes
```

---

## Permissões

Permite definir quem pode:

- Ler;
- Modificar;
- Executar;
- Excluir arquivos.

Muito utilizado em empresas e servidores.

---

## Journaling

O NTFS registra alterações antes de gravá-las.

Isso ajuda a recuperar o sistema após:

- Quedas de energia;
- Travamentos;
- Reinicializações inesperadas.

---

## Compressão

Pode armazenar arquivos comprimidos automaticamente.

---

## Criptografia

Suporta EFS (Encrypting File System).

Permite proteger arquivos contra acesso não autorizado.

---

# Como Verificar se um Disco é NTFS?

## Windows

Prompt de Comando:

```cmd
fsutil fsinfo volumeinfo C:
```

ou

```cmd
diskpart
list volume
```

---

## Linux

```bash
lsblk -f
```

Exemplo:

```text
sda1   ntfs
sda2   ext4
```

---

# NTFS vs FAT32

| Característica | NTFS | FAT32 |
|---------------|------|--------|
| Arquivos maiores que 4 GB | Sim | Não |
| Permissões | Sim | Não |
| Journaling | Sim | Não |
| Segurança | Melhor | Básica |
| Windows | Excelente | Excelente |
| Linux | Boa | Excelente |

---

# NTFS vs EXT4

| Característica | NTFS | EXT4 |
|---------------|------|------|
| Sistema Principal | Windows | Linux |
| Journaling | Sim | Sim |
| Permissões Linux | Limitadas | Completas |
| Desempenho no Linux | Menor | Maior |
| Compatibilidade Windows | Excelente | Não nativa |

---

# Quando Utilizar NTFS?

Recomendado para:

- Instalações Windows;
- HDs externos usados principalmente no Windows;
- Compartilhamento entre versões do Windows;
- Arquivos grandes.

---

# Quando Não Utilizar?

Não é a melhor escolha para:

- Partição principal de Linux;
- Servidores Linux;
- Sistemas embarcados.

Nestes casos normalmente utiliza-se:

```text
EXT4
XFS
BTRFS
```

---

# Exemplo Prático

Computador com Dual Boot:

```text
SSD
├── Windows (NTFS)
├── Linux (EXT4)
└── Partição Compartilhada (NTFS)
```

Nesse cenário o Linux e o Windows conseguem acessar a partição NTFS compartilhada.




