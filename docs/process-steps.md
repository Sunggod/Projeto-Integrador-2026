# Sequência de Desenvolvimento do Projeto

## 1. Cronograma geral

1. **Planejamento:** documentação e regras de negócio.
2. **Identidade visual:** nome, logotipo e cores.
3. **Site institucional:** apresentação do serviço.
4. **Planos:** página comercial.
5. **Autenticação:** cadastro e login.
6. **Área do jogador:** busca de quadras e vídeos.
7. **Área do contratante:** cadastro e contratação.
8. **Dashboards:** painéis de gerenciamento.
9. **Backend:** banco de dados e integrações.
10. **Inteligência artificial:** processamento e identificação de momentos.
11. **Testes:** validação do sistema.
12. **Apresentação:** demonstração final no SENAC.

## 2. Sequência detalhada por fases

### Fase 1 — Fundação do sistema

#### Etapa 1: Planejamento técnico e regras de negócio

- Definir os tipos de usuários e as permissões de cada perfil.
- Definir os dados cadastrais de cada usuário.
- Definir as regras de publicação de conteúdos e interação.
- Definir a organização das quadras e regiões.

**Entrega:** documento de requisitos funcionais e regras de negócio.

#### Etapa 2: Banco de dados

- Estruturar o banco relacional com PostgreSQL e Prisma ORM.
- Criar as tabelas centrais: `usuarios`, `perfis`, `estabelecimentos`, `quadras`, `modalidades`, `planos`, `assinaturas`, `partidas` e `momentos`.
- Evoluir o modelo com tabelas sociais: `publicacoes`, `curtidas`, `comentarios`, `compartilhamentos`, `amizades`, `grupos`, `grupo_membros`, `localizacoes` e `notificacoes`.

#### Etapa 3: Sistema de cadastro e login

- Implementar autenticação unificada para usuário comum, contratante e administrador.
- Criar os fluxos de cadastro, validação de e-mail, recuperação de senha e gerenciamento de sessão.

#### Etapa 4: Página inicial e navegação

- Construir a interface principal e o menu de navegação: Início, Explorar, Mapa, Grupos, Notificações e Perfil.
- Exibir a estrutura inicial do feed, quadras em destaque, momentos recentes, grupos e modalidades.

### Fase 2 — Rede social e marketplace

#### Etapa 5: Sistema de publicações e feed

- Implementar a criação de publicações vinculadas às quadras, incluindo vídeos de melhores momentos, fotos, eventos e textos.
- Desenvolver as interações: curtir, comentar, compartilhar, salvar, acessar perfil e acessar a página da quadra.

#### Etapa 6: Marketplace de quadras

- Criar a busca de quadras com filtros por modalidade, cidade e região.
- Desenvolver a página pública de cada estabelecimento, com fotos, endereço, modalidades, lista de quadras, vídeos e status de gravação inteligente.

#### Etapa 7: Geolocalização

- Implementar o modo **Próximo de mim**, solicitando permissão de GPS para listar quadras, eventos e conteúdos próximos.
- Implementar o modo **Explorar todas as regiões**, permitindo busca manual por cidade e estado sem depender do GPS.

#### Etapa 8: Perfil, amizades e grupos

- Desenvolver o perfil do jogador com bio, modalidades, histórico, amigos e grupos.
- Implementar o sistema de amizades: enviar, aceitar, recusar, remover e seguir.
- Criar grupos e comunidades esportivas com criação, regras, administração e publicações internas.

### Fase 3 — Contratantes e gestão comercial

#### Etapa 9: Dashboard do contratante

- Construir o painel administrativo do estabelecimento com: Visão geral, Meu estabelecimento, Minhas quadras, Câmeras, Partidas, Melhores momentos, Armazenamento, Meu plano e Configurações.
- Implementar operações CRUD para estabelecimentos, quadras e fotos, além da gestão de vídeos publicados.

#### Etapa 10: Planos e pagamentos

- Criar uma vitrine comparativa dos planos START, PRO e PREMIUM.
- Implementar o fluxo demonstrativo de solicitação e contratação, consulta de assinatura, alteração e cancelamento.

### Fase 4 — Inteligência artificial e vídeos

#### Etapa 11: Integração com câmeras

- Desenvolver o cadastro de equipamentos e sua vinculação às quadras.
- Criar o pipeline de recebimento e armazenamento dos fluxos de vídeo, com monitoramento da conexão.

#### Etapa 12: Implementação da inteligência artificial

- Configurar a análise de vídeo com visão computacional.
- Implementar a detecção de eventos esportivos, como gols, cestas e pontos, e o recorte automático dos melhores momentos.
- Armazenar os clipes gerados.

#### Etapa 13: Integração da IA com a rede social

- Conectar os recortes gerados ao dashboard do contratante para aprovação.
- Implementar a publicação automática na página da quadra e no feed.

### Fase 5 — Testes e publicação

#### Etapa 14: Testes funcionais

- Validar cadastro, login, permissões, publicações, interações sociais, geolocalização, cadastro de quadras, planos e fluxo de vídeos.

#### Etapa 15: Segurança e desempenho

- Aplicar validação de dados, controle de acesso, proteção de arquivos e backup do banco.
- Definir regras de privacidade, incluindo LGPD e proteção de menores de idade, e implementar moderação.

#### Etapa 16: Apresentação final no SENAC

- Executar a demonstração ponta a ponta: visão do jogador, interação social, visão do contratante e simulação ou demonstração da IA.

## 3. Roadmap por ciclos de execução

1. **Ciclo 01 — Planejamento e banco de dados:** modelagem, requisitos e arquitetura.
2. **Ciclo 02 — Login e usuários:** cadastro, autenticação e permissões.
3. **Ciclo 03 — Interface e página inicial:** navegação e dashboards iniciais.
4. **Ciclo 04 — Marketplace e localização:** quadras, filtros e mapas.
5. **Ciclo 05 — Rede social:** feed, vídeos e interações.
6. **Ciclo 06 — Grupos e amizades:** conexões e comunidades.
7. **Ciclo 07 — Área do contratante:** gestão de quadras e planos.
8. **Ciclo 08 — Inteligência artificial:** câmeras e processamento de vídeos.
9. **Ciclo 09 — Testes e apresentação:** segurança, correções e demonstração.

## 4. Checklist inicial de implementação

- [ ] Documentar os requisitos funcionais.
- [ ] Definir os tipos de usuários e permissões.
- [ ] Modelar o banco de dados.
- [ ] Criar o projeto e configurar o GitHub.
- [ ] Desenvolver o backend inicial.
- [ ] Implementar cadastro e login.
- [ ] Criar a página inicial.
- [ ] Criar a navegação entre áreas.

