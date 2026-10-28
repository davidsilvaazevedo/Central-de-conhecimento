# Central de Conhecimento – SharePoint

Plataforma web de base de conhecimento para equipes de suporte de TI, integrada ao SharePoint Online.

![HTML5](https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white)
![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=000)
![SharePoint](https://img.shields.io/badge/SharePoint-0078D4?style=for-the-badge&logo=microsoftsharepoint&logoColor=white)
![Microsoft Entra ID](https://img.shields.io/badge/Microsoft%20Entra%20ID-0078D4?style=for-the-badge&logo=microsoft&logoColor=white)

---

## 📌 Descrição

A **Central de Conhecimento** reúne em um só lugar as soluções, procedimentos e respostas que a equipe de suporte usa no dia a dia.

O técnico pesquisa um problema, encontra a solução validada, copia respostas prontas e registra novas soluções. O administrador valida o conteúdo, acompanha indicadores e mantém a base organizada.

Os dados ficam em listas do **SharePoint Online (Microsoft Lists)**, e o login é feito com a conta corporativa pelo **Microsoft Entra ID**.

## 🎯 Problema que resolve

- Soluções espalhadas em e-mails, chats e anotações pessoais
- Conhecimento que se perde quando alguém sai de férias ou muda de área
- Respostas aos usuários escritas do zero a cada atendimento
- Falta de clareza sobre qual equipe resolve cada tipo de problema

## ✅ Funcionalidades

### Para técnicos

- 🔎 **Pesquisa de soluções** com resultados enquanto digita e filtros por localidade, categoria, sistema, equipamento, área, criticidade e público
- 📝 **Registro de solução** com template, passo a passo, mais de uma solução por artigo e verificação de duplicados
- 🧭 **Navegação orientada:** trilhas passo a passo para diagnosticar problemas comuns
- 💬 **Respostas padronizadas** prontas para copiar e enviar
- 💻 **Cheats:** scripts de suporte prontos para copiar
- 👥 **Quem resolve:** mapa de qual equipe atende cada assunto
- ⭐ **Favoritos** individuais
- 💡 **Ideias e melhorias** enviadas pela equipe

### Para administradores

- ✔️ **Revisão e validação** de conteúdo, com alertas de artigos incompletos
- 📊 **Painel do administrador** e **indicadores** de uso, validação e resolução
- 🏷️ **Taxonomia** e políticas de publicação
- 🔐 **Controle de acesso** por perfil
- 🧠 **Conhecimento tácito:** captura de conhecimento antes de férias, mudança de área ou desligamento
- 🗄️ **Arquivamento** com histórico preservado
- 💾 **Backup e restauração** da base, com exportação em CSV, XLSX e JSON

### Usabilidade e acessibilidade

- 🌗 Tema escuro, tema claro e modo de alto contraste
- 📱 Layout responsivo para diferentes tamanhos de tela
- ♿ Botões de acessibilidade sempre visíveis
- 🚶 Modo visitante, que mostra apenas a Navegação orientada para quem não é técnico

## 🖼️ Screenshots

### Pesquisar soluções

![Pesquisa de soluções](screenshots/pesquisa.png)

### Registrar solução

![Registro de nova solução](screenshots/registrar-solucao.png)

### Navegação orientada

![Trilhas da navegação orientada](screenshots/navegacao-orientada.png)

### Respostas padronizadas

![Modelos de respostas padronizadas](screenshots/respostas-padronizadas.png)

### Painel do administrador

![Painel do administrador](screenshots/painel-administrador.png)

### Indicadores

![Indicadores de uso](screenshots/indicadores.png)

### Outras telas

| Quem resolve | Taxonomia |
|---|---|
| ![Quem resolve](screenshots/quem-resolve.png) | ![Taxonomia](screenshots/taxonomia.png) |

| Controle de acesso | Revisão e validação |
|---|---|
| ![Controle de acesso](screenshots/controle-de-acesso.png) | ![Revisão e validação](screenshots/revisao-validacao.png) |

| Conhecimento tácito | Ideias e melhorias |
|---|---|
| ![Conhecimento tácito](screenshots/conhecimento-tacito.png) | ![Ideias e melhorias](screenshots/ideias.png) |

| Meus favoritos | Arquivados |
|---|---|
| ![Meus favoritos](screenshots/favoritos.png) | ![Arquivados](screenshots/arquivados.png) |

## 🛠️ Tecnologias utilizadas

| Tecnologia | Uso no projeto |
|---|---|
| HTML, CSS e JavaScript | Interface completa em um único arquivo, sem frameworks |
| SharePoint Online (Microsoft Lists) | Armazenamento dos dados |
| Microsoft Entra ID + MSAL.js | Login com a conta corporativa |
| SheetJS | Exportação para Excel |

## 🗄️ Estrutura de dados

Cada área do sistema usa uma lista do SharePoint:

| Lista | Conteúdo |
|---|---|
| Artigos | Problemas documentados (título, sintomas, categoria, sistema, criticidade etc.) |
| Solucoes | Soluções de cada artigo, com passo a passo e área que ajudou |
| Trilhas | Passos da Navegação orientada |
| Respostas padronizadas | Modelos de texto para os usuários |
| Quem resolve | Assunto, equipe responsável e canal de atendimento |
| Ideias | Sugestões de melhoria |
| Favoritos | Artigos favoritos de cada usuário |
| Perfis | E-mail e perfil (Técnico ou Administrador) de cada pessoa |
| Log de Atividades | Registro de criações, edições e exclusões |

## 🔑 Perfis de acesso

| Ação | Técnico | Administrador |
|---|:---:|:---:|
| Pesquisar, ler e avaliar soluções | ✅ | ✅ |
| Registrar e editar soluções | ✅ | ✅ |
| Copiar respostas padronizadas e cheats | ✅ | ✅ |
| Favoritar artigos e enviar ideias | ✅ | ✅ |
| Validar conteúdo | ❌ | ✅ |
| Gerenciar trilhas, respostas e Quem resolve | ❌ | ✅ |
| Arquivar e restaurar conteúdo | ❌ | ✅ |
| Indicadores, painel, backup e restauração | ❌ | ✅ |

O perfil é definido pela lista **Perfis**. Quem não está cadastrado entra como **Técnico**.

## 🔄 Ciclo de vida do conhecimento

1. **Registro:** qualquer técnico cadastra uma solução, que entra como rascunho.
2. **Validação:** um administrador revisa e publica.
3. **Uso:** o técnico informa se a solução resolveu o chamado, o que alimenta os indicadores.
4. **Revisão:** cada artigo é revisado no máximo a cada 6 meses.
5. **Arquivamento:** conteúdos desatualizados saem da pesquisa, mas o histórico é mantido.

## 🚀 Status do projeto

- [x] Interface completa com todos os módulos
- [x] Login com Microsoft Entra ID
- [x] Integração com as listas do SharePoint
- [x] Backup, restauração e exportação
- [ ] Liberação final de permissões junto à equipe de TI
- [ ] Publicação para toda a equipe de suporte

## ⚠️ Observação

Projeto desenvolvido para uso interno de uma equipe de suporte de TI. Este repositório apresenta as telas e a arquitetura da solução; dados reais, endereços internos e credenciais não são publicados.

## 👨‍💻 Autor

**David Azevedo**

[![GitHub](https://img.shields.io/badge/GitHub-davidsilvaazevedo-181717?style=for-the-badge&logo=github&logoColor=white)](https://github.com/davidsilvaazevedo)
