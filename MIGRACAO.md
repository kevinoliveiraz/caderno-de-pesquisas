# Relatório de migração

Data: 2026-10-13.

Os dez repositórios de pesquisas selecionados por Kevin Cardoso foram reunidos neste caderno. Sistemas-de-arquivos- foi colocado dentro de Computador. Agente Letras e os demais projetos continuam independentes.

## Conteúdo e histórico

| Origem | Destino | Documentos | Commits originais |
|---|---|---:|---:|
| [Linux](https://github.com/kevinoliveiraz/Linux) | `tecnologia/linux/` | 4 | 5 |
| [Windows](https://github.com/kevinoliveiraz/Windows) | `tecnologia/windows/` | 2 | 4 |
| [Computador](https://github.com/kevinoliveiraz/Computador) | `tecnologia/computador/` | 11 | 29 |
| [Sistemas-de-arquivos-](https://github.com/kevinoliveiraz/Sistemas-de-arquivos-) | `tecnologia/computador/sistemas-de-arquivos/` | 1 | 3 |
| [Redes](https://github.com/kevinoliveiraz/Redes) | `tecnologia/redes/` | 10 | 15 |
| [Back-end](https://github.com/kevinoliveiraz/Back-end) | `tecnologia/back-end/` | 3 | 4 |
| [Inteligencia-Artificial-](https://github.com/kevinoliveiraz/Inteligencia-Artificial-) | `tecnologia/inteligencia-artificial/` | 4 | 6 |
| [mobile](https://github.com/kevinoliveiraz/mobile) | `tecnologia/mobile/` | 2 | 5 |
| [Docker](https://github.com/kevinoliveiraz/Docker) | `tecnologia/docker/` | 3 | 4 |
| [security](https://github.com/kevinoliveiraz/security) | `tecnologia/security/` | 3 | 6 |

Total: **43 documentos**, **22 imagens versionadas** e **81 commits originais** preservados.

## Como o histórico foi preservado

Cada origem foi obtida como cópia Git completa, sem alterar o repositório de origem. Um commit de importação do caderno tem dois pais: o estado anterior do caderno e o último commit da origem. Assim, os commits antigos continuam alcançáveis, com os mesmos identificadores, autores, datas e textos.

As versões atuais dos arquivos foram colocadas nos diretórios dos temas em novos commits. Os documentos foram importados com os mesmos blobs da origem. Em uma etapa separada, somente os endereços das imagens foram trocados por caminhos relativos para as cópias locais. Não houve resumo ou reescrita dos textos.

As origens auditadas tinham uma única branch, main, e nenhuma tag. Não foi usado squash nem reescrito o histórico. O [manifesto](migracao/manifesto.json) registra os commits de origem, os commits de importação, os blobs e os caminhos de cada arquivo.

## Security: documentos recuperados

Security estava vazio em main. Como o tema foi selecionado após a auditoria, foram recuperadas as últimas versões existentes destes três documentos:

- [DNS/DPS — Dispositivo de Proteção contra Surtos.md](tecnologia/security/DNS/DPS%20%E2%80%94%20Dispositivo%20de%20Prote%C3%A7%C3%A3o%20contra%20Surtos.md) — [versão de origem](https://github.com/kevinoliveiraz/security/blob/8b7482f409fccd6bc04c0e3336e76d5bcd4e38ec/DNS/DPS%20%E2%80%94%20Dispositivo%20de%20Prote%C3%A7%C3%A3o%20contra%20Surtos.md).
- [DNS/O que é DNS?.md](tecnologia/security/DNS/O%20que%20%C3%A9%20DNS.md) — [versão de origem](https://github.com/kevinoliveiraz/security/blob/8b7482f409fccd6bc04c0e3336e76d5bcd4e38ec/DNS/O%20que%20%C3%A9%20DNS%3F.md).
- [DNS/Tailscale.md](tecnologia/security/DNS/Tailscale.md) — [versão de origem](https://github.com/kevinoliveiraz/security/blob/4084f4191d6271392dc185374f5c8d2f4b32d2a9/DNS/Tailscale.md).

Esses documentos permanecem agrupados no tema Security, preservando o contexto da origem. DPS trata de proteção elétrica; DNS e Tailscale também se relacionam às pesquisas de Redes. A recuperação e as referências de origem estão identificadas sem alterar os textos.

## Imagens

Os 22 anexos externos usados pelos estudos foram verificados, copiados sem alteração dos bytes e guardados em assets/imagens. Nomes baseados no conteúdo evitam duplicação e conflitos. O manifesto registra o endereço original, o SHA-256 e os documentos que usam cada imagem.

Os caminhos da versão atual são locais. As versões históricas preservadas mantêm seus endereços originais. Na auditoria, todos os 22 anexos responderam HTTP 200 e puderam ser abertos.

## Ajustes de nomes e caminhos

Foram removidos caracteres incompatíveis com Windows, corrigida uma extensão com espaço e adicionada a extensão Markdown ao arquivo Chipset. Os textos não foram alterados por esses ajustes.

| Origem | Caminho atual |
|---|---|
| `Windows/Por Que o Windows Usa a Unidade C:?.md` | `tecnologia/windows/Por Que o Windows Usa a Unidade C.md` |
| `Computador/Placa mãe/Chipset` | `tecnologia/computador/Placa mãe/Chipset.md` |
| `Redes/Ethernet/O que é Ethernet?.md` | `tecnologia/redes/Ethernet/O que é Ethernet.md` |
| `Redes/VPN/Tailscale/Instalação/Windows. md` | `tecnologia/redes/VPN/Tailscale/Instalação/Windows.md` |
| `Back-end/Supabase/O que é?.md` | `tecnologia/back-end/Supabase/O que é.md` |
| `mobile/Como é uma câmera por dentro?.md` | `tecnologia/mobile/Como é uma câmera por dentro.md` |
| `security/DNS/O que é DNS?.md` | `tecnologia/security/DNS/O que é DNS.md` |

Os commits antigos continuam com os nomes originais. Por isso, abrir algumas versões históricas diretamente no Windows pode falhar por causa de nomes com ? ou :. A versão atual usa caminhos compatíveis.

## Conteúdos em desenvolvimento

Cinco arquivos ainda estão vazios. Eles foram preservados e identificados nos índices:

- [tecnologia/computador/Placa mãe/Chipset.md](tecnologia/computador/Placa%20m%C3%A3e/Chipset.md).
- [tecnologia/computador/fonte de alimentação/resumo.md](tecnologia/computador/fonte%20de%20alimenta%C3%A7%C3%A3o/resumo.md).
- [tecnologia/redes/DNS/O que é nds.md](tecnologia/redes/DNS/O%20que%20%C3%A9%20nds.md).
- [tecnologia/redes/Ethernet/O que é Ethernet.md](tecnologia/redes/Ethernet/O%20que%20%C3%A9%20Ethernet.md).
- [tecnologia/back-end/Supabase/O que é.md](tecnologia/back-end/Supabase/O%20que%20%C3%A9.md).

## Privacidade e escopo

Todas as origens selecionadas são públicas. Kevin confirmou que as senhas escritas como exemplos no tutorial de Nextcloud são fictícias e nunca foram usadas em serviços reais. As capturas de RustDesk já ocultavam os dados de acesso.

Nenhum repositório de origem ou projeto independente foi excluído, arquivado, renomeado ou editado por esta migração. Uma decisão sobre arquivamento deve ser tomada separadamente, depois da validação.

## Validação

Foi verificada a presença de todos os documentos, a igualdade dos blobs na importação, a preservação integral dos textos após descontar apenas as trocas autorizadas de URLs de imagens, a integridade das imagens, os links relativos, o alcance de todos os commits originais e a navegação dos índices.

Os resultados detalhados estão em [validacao.json](migracao/validacao.json). Não foram encontrados arquivos perdidos, conflitos de nomes ou links locais quebrados.
