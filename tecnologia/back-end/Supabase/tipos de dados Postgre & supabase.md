| Tipo de Dado | Nome Técnico | Descrição Técnica | Exemplo de Uso Ideal |
| :--- | :--- | :--- | :--- |
| **int2** | `smallint` | Número inteiro pequeno de 2 bytes (-32.768 a 32.767). | Idade, dias do mês, quantidade de parcelas. |
| **int4** | `integer` | Número inteiro padrão de 4 bytes (-2,1 bilhões a 2,1 bilhões). | IDs numéricos simples, estoque de produtos, contagem de acessos. |
| **int8** | `bigint` | Número inteiro grande de 8 bytes (valores extremamente altos). | Visualizações de vídeos gigantes, números de telefone, transações financeiras em centavos. |
| **float4** | `real` | Número com vírgula de precisão simples (4 bytes). | Dados de sensores, notas de avaliações simples onde pequenas variações decimais não impactam. |
| **float8** | `double precision` | Número com vírgula de precisão dupla (8 bytes). | Coordenadas geográficas (latitude/longitude), cálculos científicos complexos. |
| **numeric** | `decimal` | Número decimal de precisão exata definida pelo usuário. | Preços de produtos, saldos financeiros e valores monetários (evita erros de arredondamento). |
| **json** | `json` | Dados no formato JSON em formato de texto simples. | Logs de sistema, configurações da conta do usuário ou estruturas de dados dinâmicas. |
| **jsonb** | `jsonb` | Dados JSON em formato binário otimizado para consultas e índices. | Metadados de arquivos, respostas de APIs externas e atributos dinâmicos de produtos. |
| **text** | `text` | Texto de tamanho ilimitado (string). | Nomes, descrições, e-mails, URLs e conteúdos de artigos/postagens. |
| **bool** | `boolean` | Valor lógico (*verdadeiro* ou *falso* / `true` ou `false`). | Indicadores de status como `is_admin`, `ativo`, `pago` ou `deletado`. |
| **uuid** | `uuid` | Identificador Único Universal (código alfanumérico único de 128 bits). | Chave primária (`id`) de tabelas para garantir IDs exclusivos em qualquer sistema. |
| **timestamptz** | `timestamp with time zone` | Data e hora exatas com fuso horário incluído. | Campos como `created_at`, `updated_at` e `ultimo_login`. |
