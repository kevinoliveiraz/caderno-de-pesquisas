# Resumo

Esta nota apresenta os esquemas de particionamento MBR e GPT, explicando como cada um organiza os discos de armazenamento, suas diferenças técnicas, limitações e relação com BIOS e UEFI. Também aborda como identificar o tipo de partição no Windows e no Linux.

## Tópicos abordados

- O que é uma partição
- O que é MBR (Master Boot Record)
- Características do MBR
- Limitações do MBR
- O que é GPT (GUID Partition Table)
- Características do GPT
- Vantagens do GPT
- Comparação entre MBR e GPT
- Relação entre BIOS e UEFI
- Como verificar MBR ou GPT no Windows
- Como verificar MBR ou GPT no Linux


# Partição MBR vs GPT

MBR e GPT são esquemas de particionamento usados para organizar discos de armazenamento.

Eles definem como as partições são criadas e como o sistema operacional encontra os dados armazenados.

---

# O que é uma Partição?

Uma partição é uma divisão lógica de um disco.

Exemplo:

```text
SSD 500 GB
│
├── C: Windows (250 GB)
├── D: Arquivos (200 GB)
└── E: Backup (50 GB)
```

---

# O que é MBR?

MBR significa:

**Master Boot Record**

Foi introduzido em 1983 e durante muitos anos foi o padrão dos computadores.

O MBR armazena:

- Informações das partições;
- Código de inicialização (boot);
- Tabela de partições.

---

# Características do MBR

- Suporta até 2 TB por disco;
- Máximo de 4 partições primárias;
- Compatível com computadores antigos;
- Utilizado principalmente com BIOS.

---

# Limitações do MBR

- Limite de 2 TB por disco;
- Apenas 4 partições primárias;
- Menor tolerância a falhas;
- Tecnologia mais antiga.

---

# O que é GPT?

GPT significa:

**GUID Partition Table**

É o padrão moderno de particionamento e faz parte da especificação UEFI.

---

# Características do GPT

- Suporta discos maiores que 2 TB;
- Permite centenas de partições;
- Possui cópia de segurança da tabela de partições;
- Mais resistente a corrupção de dados;
- Utilizado principalmente com UEFI.

---

# Vantagens do GPT

- Maior capacidade de armazenamento;
- Melhor confiabilidade;
- Recuperação mais fácil em caso de falhas;
- Compatibilidade com hardware moderno.

---

# MBR vs GPT

| Característica | MBR | GPT |
|---------------|------|------|
| Ano de criação | 1983 | 2005 |
| Tamanho máximo do disco | 2 TB | Maior que 2 TB |
| Número de partições | 4 primárias | Até 128 (Windows) |
| BIOS | Sim | Limitado |
| UEFI | Limitado | Sim |
| Cópia de segurança da tabela | Não | Sim |
| Recomendado atualmente | Não | Sim |

---

# Relação com BIOS e UEFI

Geralmente:

```text
BIOS → MBR

UEFI → GPT
```

Embora existam exceções, essa é a combinação mais comum.

---

# Como verificar no Windows

1. Pressione `Win + X`;
2. Abra **Gerenciamento de Disco**;
3. Clique com o botão direito no disco;
4. Selecione **Propriedades**;
5. Abra a aba **Volumes**;
6. Verifique o campo:

```text
Estilo de Partição
```

O resultado será:

```text
GPT (GUID Partition Table)
```

ou

```text
MBR (Master Boot Record)
```

---

# Como verificar no Linux

1. Abra o terminal;
2. digite ``lsblk -d -o NAME,MODEL,PTTYPE
`` ;


O resultado será:

```text
NAME MODEL            PTTYPE
sda  Kingston A400    gpt
sdb  SanDisk SSD      gpt

```



