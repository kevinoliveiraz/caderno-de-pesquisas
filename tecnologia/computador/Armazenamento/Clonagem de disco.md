
# Resumo

Esta nota apresenta os conceitos fundamentais sobre clonagem de discos, explicando como copiar integralmente um HD ou SSD para outro dispositivo de armazenamento. São abordados os cenários de uso, os tipos de clonagem, ferramentas disponíveis para Windows e Linux, procedimentos básicos, comandos utilizados no terminal e os principais cuidados para evitar perda de dados.

## Tópicos abordados

- O que é clonagem de disco
- Situações em que a clonagem é recomendada
- Tipos de clonagem (HD ↔ HD, HD ↔ SSD, SSD ↔ SSD e SSD ↔ HD)
- Ferramentas de clonagem para Windows
- Tutorial básico com Macrium Reflect
- Ferramentas de clonagem para Linux
- Tutorial básico com Clonezilla
- Clonagem via terminal utilizando `dd`
- Identificação de discos com `lsblk` e `fdisk`
- Cuidados antes de iniciar a clonagem
# Clonagem de Disco (HD ↔ SSD)

A clonagem copia todo o conteúdo de um disco para outro, incluindo:

- Sistema operacional;
- Arquivos;
- Programas;
- Partições;
- Configurações.

Após a clonagem, o novo disco pode substituir o antigo.

---

# Quando Utilizar

- Migrar HD para SSD;
- Trocar SSD antigo por SSD maior;
- Fazer backup completo;
- Substituir disco com defeito;
- Atualizar armazenamento.

---

# Tipos de Clonagem

| Origem | Destino |
|----------|----------|
| HD | HD |
| HD | SSD |
| SSD | SSD |
| SSD | HD |

---

# Windows

## Programa Recomendado

- Macrium Reflect
- AOMEI Backupper
- EaseUS Todo Backup

---

## Tutorial com Macrium Reflect

1. Instale o Macrium Reflect;
2. Conecte o novo disco;
3. Abra o programa;
4. Selecione o disco de origem;
5. Clique em **Clone this disk**;
6. Selecione o disco de destino;
7. Confirme a operação;
8. Aguarde a conclusão;
9. Desligue o computador;
10. Inicie pelo novo disco.

---

# Linux

## Programas Recomendados

- Clonezilla
- Rescuezilla
- dd
- GParted

---

## Tutorial com Clonezilla

1. Baixe a ISO do Clonezilla;
2. Crie um pendrive bootável;
3. Inicialize pelo pendrive;
4. Escolha:

```text
device-device
```

5. Selecione o disco de origem;
6. Selecione o disco de destino;
7. Confirme a clonagem;
8. Aguarde a conclusão;
9. Reinicie o computador.

---

## Clonagem pelo Terminal (dd)

Exemplo:

```bash
sudo dd if=/dev/sda of=/dev/sdb bs=64K status=progress
```

Onde:

```text
sda = disco origem
sdb = disco destino
```

Atenção:

O comando sobrescreve completamente o disco de destino.

---

# Verificando os Discos no Linux

Listar discos:

```bash
lsblk
```

ou

```bash
sudo fdisk -l
```

Exemplo:

```text
sda 500GB
sdb 1TB
```

---


# Cuidados

Antes de clonar:

- Faça backup dos dados importantes;
- Verifique qual é o disco de origem;
- Verifique qual é o disco de destino;
- Certifique-se de que o destino possui espaço suficiente.

