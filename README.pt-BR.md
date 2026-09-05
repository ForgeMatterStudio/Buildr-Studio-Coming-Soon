<p align="center">
  <img src="assets/banner-pt-br.png" alt="Buildr Studio" width="100%">
</p>

<p align="center">
  <a href="README.md">English</a>
  •
  <a href="README.pt-BR.md"><strong>Português</strong></a>
</p>

---

# Buildr Studio

### Desenvolvimento Android. Reinventado para o mobile.

Buildr Studio é um ambiente de desenvolvimento Android mobile-first criado pela **ForgeMatter** para permitir desenvolvimento Android real diretamente em celulares e tablets.

Ele não foi pensado como um simples editor de código nem como um complemento de uma IDE de desktop.

O objetivo é oferecer um ambiente completo onde seja possível criar, editar, analisar, compilar, testar, visualizar, gerenciar e preparar aplicativos Android para distribuição usando um único dispositivo.

> **O Buildr Studio está atualmente em desenvolvimento privado ativo.**

---

## Desenvolva aplicativos Android de qualquer lugar

O Buildr leva as partes essenciais de um fluxo moderno de desenvolvimento Android para uma interface criada desde o início para dispositivos móveis.

Crie um projeto.

Escreva Kotlin ou Java.

Navegue pela estrutura do projeto.

Trabalhe com Git e GitHub.

Execute builds.

Analise erros e diagnósticos.

Use um terminal conectado ao projeto real.

Visualize seu aplicativo.

Prepare releases.

Tudo sem depender de um ambiente tradicional de desktop para o fluxo principal de desenvolvimento.

---

## O que o Buildr Studio está sendo criado para fazer

### Editor de código

Um editor voltado para desenvolvimento real de projetos Android.

Entre as capacidades planejadas e em evolução estão:

- edição de Kotlin e Java
- edição de XML e recursos Android
- destaque de sintaxe
- números de linha
- múltiplos arquivos abertos
- árvore de arquivos do projeto
- busca e substituição
- desfazer e refazer
- salvamento automático
- navegação rápida entre arquivos e símbolos
- diagnósticos por arquivo e linha
- marcadores de erros e warnings diretamente no editor
- Quick Fix quando houver uma correção segura
- navegação otimizada para arquivos extensos
- persistência do estado do projeto e do editor
- painel de arquivos adaptativo para celulares e telas maiores

O objetivo é aproximar progressivamente a experiência do que desenvolvedores esperam de uma IDE real.

---

## Diagnósticos em tempo real

O Buildr está sendo desenvolvido para detectar problemas antes da compilação sempre que possível.

Os diagnósticos podem incluir:

- erros Kotlin
- erros Java
- problemas de sintaxe XML
- erros no AndroidManifest
- problemas de configuração Gradle
- arquivos obrigatórios ausentes ou inválidos
- dependências ou configurações inválidas
- warnings
- diagnósticos informativos

Erros e warnings devem aparecer em diferentes pontos da interface:

- diretamente na linha afetada
- no gutter do editor
- na barra de status
- no painel Problemas/Diagnóstico
- nos detalhes de build quando forem relevantes

Sempre que possível, o Buildr também deverá levar diretamente ao arquivo e à linha afetados.

---

## Compreensão de Android e Gradle

O Buildr não está sendo desenvolvido como um simples editor de texto.

O modelo de projeto é projetado para compreender informações específicas do Android, incluindo:

- módulos
- applicationId e namespace
- configuração do AndroidManifest
- estrutura Gradle
- variantes e tasks
- configuração de SDK
- dependências
- Activities de inicialização
- configuração de build
- informações de versão do projeto

O estado do Gradle e os diagnósticos do projeto devem permanecer sincronizados com o workspace automaticamente.

---

## Builds

O Buildr pode iniciar e acompanhar compilações Android mantendo o ambiente de desenvolvimento separado da infraestrutura que executa a build.

A experiência de build está sendo desenvolvida com:

- preflight antes da compilação
- confirmação explícita
- progresso da build
- estados de fila e execução
- histórico
- etapas detalhadas
- duração
- artefatos resultantes
- logs completos
- extração do erro real do compilador
- navegação direta do erro para o Editor
- acompanhamento de builds em segundo plano
- notificações de mudanças importantes de estado

Sempre que possível, o Buildr deve identificar o erro real do compilador em vez de mostrar apenas mensagens genéricas de falha do Gradle.

---

## Compilação rápida pelo projeto

Projetos que já possuem uma configuração válida poderão iniciar uma build diretamente pelo menu contextual da área Projetos.

Antes de iniciar, o Buildr poderá executar um preflight e identificar bloqueios como:

- Gradle inválido
- arquivos ausentes
- Manifest inválido
- integração GitHub indisponível
- alterações locais relevantes ainda não sincronizadas
- configuração de build ausente
- diagnósticos críticos

Caso alguma intervenção seja necessária, o Buildr deve informar claramente o problema e levar o usuário ao local correto para resolvê-lo.

---

## Terminal integrado

O Terminal do Buildr Studio está sendo desenvolvido como uma ferramenta de primeira classe conectada ao mesmo workspace real utilizado pelo Editor.

O Terminal está planejado para oferecer:

- sessões persistentes
- múltiplas sessões
- histórico de comandos
- autocomplete
- operações de arquivos
- fluxos Git
- links clicáveis no formato `arquivo:linha`
- acesso às ferramentas disponíveis no ambiente
- interação com os mesmos arquivos usados pelo Editor

Alterações feitas no Terminal devem refletir imediatamente em:

- Editor
- árvore de arquivos
- diagnósticos
- estado do Git
- análise do projeto

---

## CLI Buildr

Uma CLI própria chamada `buildr` está planejada para expor capacidades do Buildr diretamente pelo Terminal.

Entre os comandos planejados estão operações como:

- `buildr project`
- `buildr analyze`
- `buildr problems`
- `buildr sync`
- `buildr build`
- `buildr status`
- `buildr logs`
- `buildr artifact`
- `buildr git`

A CLI e a interface gráfica devem operar sobre o mesmo estado do projeto, e não como ambientes separados.

---

## Git e GitHub

O GitHub é parte central do fluxo do Buildr.

O aplicativo está sendo desenvolvido para oferecer:

- importação de projetos do GitHub
- sincronização de repositórios
- branches
- commits
- atualização de projetos
- integração com builds
- status Git
- consciência do estado remoto
- fluxos apoiados por GitHub Actions quando aplicável

O indicador GitHub do Buildr representa o estado real da sincronização e não apenas uma conexão visual.

---

## Atualização inteligente de projetos

Ao importar um ZIP pertencente a um projeto que já existe no Buildr, o aplicativo pode identificar essa relação em vez de simplesmente criar uma duplicata.

O fluxo de atualização foi projetado para:

- identificar o projeto existente
- comparar a identidade do projeto
- mostrar arquivos adicionados
- mostrar arquivos alterados
- mostrar arquivos removidos
- criar um snapshot de segurança
- atualizar o projeto existente
- permitir rollback em caso de falha
- permitir importar como uma cópia separada

O objetivo é tornar a evolução do projeto mais segura sem obrigar o usuário a substituir manualmente pastas completas.

---

## Live View

O Live View está sendo desenvolvido como um sistema real de visualização do aplicativo.

O objetivo não é gerar uma representação visual falsa ou aproximada da aplicação.

O Buildr e seu Preview Host dedicado estão sendo desenvolvidos para:

- identificar a configuração real de inicialização do projeto
- estabelecer um runtime isolado de preview
- exibir o aplicativo em uma superfície dedicada
- reagir a alterações do projeto
- preservar a fidelidade da aplicação real

O Preview Host é um componente complementar distribuído junto de versões compatíveis do Buildr Studio.

O Live View continua em desenvolvimento ativo.

---

## Gerenciamento de projetos

O Buildr oferece um workspace unificado para projetos locais e projetos vinculados ao GitHub.

Os fluxos de projeto estão sendo desenvolvidos para incluir:

- criação de novos projetos Android
- importação de ZIP
- importação do GitHub
- identificação de projetos
- detecção de atualizações
- duplicação de projetos
- ações contextuais
- configuração de build por projeto
- persistência do estado do workspace

---

## Detalhes de build e artefatos

Uma build concluída deve oferecer muito mais do que apenas um indicador verde de sucesso.

O Buildr está sendo desenvolvido para apresentar:

- versão compilada
- versão anterior
- variante
- task
- duração
- etapas individuais da compilação
- informações do artefato gerado
- logs completos
- diagnósticos relevantes do compilador
- opções de salvar e compartilhar quando apropriado

---

## Desenvolvimento assistido por IA

O Buildr Studio está planejado para possuir uma camada de assistência por IA voltada ao desenvolvimento e aos diagnósticos.

Quando houver contexto técnico suficiente, o Buildr poderá oferecer ações como:

- explicar um erro de build
- analisar diagnósticos do compilador
- identificar causas prováveis
- sugerir alterações no código
- gerar um patch proposto
- explicar problemas de Gradle
- auxiliar na configuração do projeto

Alterações geradas pela IA não devem ser aplicadas silenciosamente.

Quando houver uma modificação de código proposta, o Buildr deverá mostrar a mudança e exigir aprovação explícita antes de aplicá-la.

---

## Mobile first

A experiência em celular está sendo projetada para ser autossuficiente.

As funcionalidades essenciais não dependerão de um tablet.

Em telas compactas, o Buildr utiliza superfícies dedicadas para ferramentas como:

- Editor
- Terminal
- Projetos
- Builds
- Home

Painéis e ferramentas contextuais se adaptam ao espaço disponível.

---

## Também pensado para tablets

Telas maiores deverão permitir um workspace mais rico sem criar um produto separado.

Em tablets, o Buildr está planejado para oferecer layouts como:

- árvore de arquivos persistente
- Editor e Terminal simultâneos
- Terminal dockado
- painéis de Problemas e saída
- Live View ao lado das ferramentas de desenvolvimento
- painéis redimensionáveis
- workspace multipainel
- interações otimizadas para teclado e mouse

O mesmo projeto, sessão e estado do Terminal devem acompanhar a transição entre layouts compactos e expandidos.

---

## Vitrine Buildr

Uma futura **Vitrine Buildr** está planejada como um catálogo público de aplicativos criados com o Buildr Studio.

Desenvolvedores poderão apresentar seus aplicativos com informações como:

- nome do aplicativo
- descrição
- imagens
- informações de release
- versão
- informações do desenvolvedor
- links oficiais de distribuição

A Vitrine não será um serviço de hospedagem de APKs.

Cada aplicativo direcionará o usuário para os canais oficiais de distribuição definidos por seu desenvolvedor.

Também está planejada uma área **Minha Vitrine** vinculada à Conta Buildr.

---

## Comunidade Buildr

Uma experiência dedicada de **Comunidade Buildr** está planejada como parte do ecossistema ForgeMatter.

O objetivo é criar um espaço onde usuários do Buildr possam:

- descobrir projetos
- trocar conhecimento
- discutir desenvolvimento Android
- compartilhar fluxos de trabalho
- ajudar outros usuários
- encontrar recursos da comunidade
- acompanhar novidades do ecossistema Buildr

A primeira experiência da comunidade poderá utilizar o GitHub antes de evoluir para uma integração mais profunda com o Buildr.

---

## Assistente de Distribuição

O Buildr está planejado para ajudar desenvolvedores a preparar aplicativos Android para distribuição.

O Assistente de Distribuição deverá auxiliar em tarefas como:

- configuração de release
- preparação de versão
- configuração de assinatura
- validação da release
- preparação de artefatos
- verificações de prontidão para distribuição

O próprio Buildr Studio **não está planejado para distribuição pela Google Play**.

Downloads e disponibilidade oficiais do Buildr serão oferecidos por canais controlados pela ForgeMatter.

---

## Buildr Preview Host

Algumas capacidades avançadas de preview utilizam um componente dedicado chamado Buildr Preview Host.

Versões compatíveis do Host devem ser distribuídas junto com o Buildr Studio, sem exigir que o usuário faça download ou compilação manual de outro componente.

O Buildr verifica a compatibilidade antes de utilizar o Host.

---

## Segurança por arquitetura

O Buildr está sendo desenvolvido partindo do princípio de que qualquer aplicativo Android distribuído pode ser analisado ou submetido a engenharia reversa.

Por isso, decisões críticas de segurança e autorização não devem depender de esconder lógica dentro do APK.

A arquitetura está sendo desenvolvida em torno de princípios como:

- autorização server-side
- credenciais curtas e revogáveis
- tratamento seguro de tokens
- proteção de dados locais sensíveis
- exposição mínima de segredos
- verificações de integridade quando apropriado
- separação entre cliente e infraestrutura privilegiada

---

## O que vem pela frente

O Buildr Studio continua evoluindo.

Algumas funcionalidades mostradas ou descritas neste repositório podem estar:

- já implementadas
- parcialmente implementadas
- em desenvolvimento ativo
- planejadas para versões futuras

A experiência pública continuará mudando conforme o Buildr se aproxima de suas primeiras versões abertas.

---

## Testes beta

Uma beta pública poderá ser disponibilizada antes da versão estável.

Builds beta poderão ser publicadas como pre-releases controladas e poderão ser substituídas ou retiradas conforme o desenvolvimento avançar.

Versões beta podem conter recursos incompletos, limitações de compatibilidade e problemas conhecidos.

A disponibilidade oficial de qualquer beta será sempre anunciada pelos canais controlados pela ForgeMatter.

---

## Status de lançamento

**Status atual:** Desenvolvimento privado

**Download público:** Ainda indisponível

**Beta pública:** Planejada / em avaliação

**Versão estável:** A anunciar

---

## Sobre a ForgeMatter

A ForgeMatter é um estúdio independente de software focado em criar ferramentas ambiciosas para desenvolvedores e criadores.

**Buildr Studio é um produto ForgeMatter.**

---

## Propósito deste repositório

Este é o repositório público informativo oficial do Buildr Studio.

Ele será utilizado para:

- informações sobre o produto
- status de desenvolvimento
- anúncios públicos
- informações sobre beta
- informações de releases
- links oficiais do Buildr Studio

O código-fonte e a infraestrutura interna do Buildr Studio são mantidos separadamente.

---

## Licenciamento

Buildr Studio é um software proprietário.

Este repositório não concede permissão para copiar, modificar, redistribuir ou reutilizar o aplicativo Buildr Studio ou seu código-fonte.

© 2026 ForgeMatter. Todos os direitos reservados.
