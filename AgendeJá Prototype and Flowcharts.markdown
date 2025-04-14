# AgendeJá: Protótipo de Telas e Fluxogramas

## Protótipo de Telas

Abaixo estão descritas as principais telas do protótipo para a plataforma **AgendeJá**, considerando uma interface responsiva para PC e dispositivos móveis. As telas são projetadas para serem intuitivas, com foco na usabilidade para empresas e consumidores finais.

### 1. Tela de Login/Cadastro (Usuário e Empresa)
- **Descrição**: Tela inicial com opções de login ou cadastro para usuários e empresas.
- **Elementos**:
  - Botões: "Entrar como Usuário", "Entrar como Empresa", "Cadastrar Usuário", "Cadastrar Empresa".
  - Campos: E-mail, senha (para login); Nome, e-mail, senha, telefone (para cadastro).
  - Design: Layout minimalista com logo "AgendeJá" centralizado e fundo com gradiente suave.
- **Responsividade**: No mobile, os botões são empilhados verticalmente; no PC, dispostos em grade.

### 2. Cadastro de Empresa
- **Descrição**: Formulário para empresas se cadastrarem na plataforma.
- **Elementos**:
  - Campos: Nome da empresa, CNPJ, endereço, telefone, e-mail, descrição.
  - Botão: "Enviar para Validação".
  - Nota informativa: "Seu cadastro será revisado em até 48 horas."
- **Responsividade**: No mobile, campos em uma única coluna; no PC, em duas colunas para melhor aproveitamento de espaço.

### 3. Configuração de Serviços (Empresa)
- **Descrição**: Interface para empresas adicionarem serviços oferecidos (ex.: salão de beleza).
- **Elementos**:
  - Lista de serviços: Ex.: Corte de cabelo, manicure, tintura.
  - Campos por serviço: Nome, duração, preço, descrição.
  - Botão: "Adicionar Serviço", "Salvar Alterações".
- **Responsividade**: No mobile, lista com botões expansíveis; no PC, tabela com opções de edição inline.

### 4. Tela de Busca de Serviços (Usuário)
- **Descrição**: Tela principal para usuários buscarem serviços com base em geolocalização.
- **Elementos**:
  - Campo de busca: Filtro por categoria (ex.: Beleza, Saúde, Reparos).
  - Mapa integrado: Exibe empresas próximas com pins.
  - Lista de resultados: Nome da empresa, distância, serviços oferecidos.
  - Botão: "Filtrar por raio" (ex.: 5 km, 10 km).
- **Responsividade**: No mobile, mapa ocupa a parte superior, com lista rolável abaixo; no PC, mapa à esquerda e lista à direita.

### 5. Tela de Agendamento (Usuário)
- **Descrição**: Interface para selecionar data e horário para um serviço.
- **Elementos**:
  - Calendário: Seleção de data (dia atual ou futuro).
  - Horários disponíveis: Ex.: 10:00, 11:00, 14:00.
  - Resumo do serviço: Nome do serviço, preço, duração.
  - Botão: "Confirmar Agendamento".
- **Responsividade**: No mobile, calendário e horários em seções roláveis; no PC, calendário fixo com horários em grade.

### 6. Gerenciamento de Agendamentos (Empresa)
- **Descrição**: Painel para empresas visualizarem e confirmarem agendamentos.
- **Elementos**:
  - Lista de agendamentos: Data, horário, cliente, serviço.
  - Botões: "Confirmar", "Cancelar" por agendamento.
  - Filtro: Por data ou status (pendente, confirmado, concluído).
- **Responsividade**: No mobile, lista com botões expansíveis; no PC, tabela com ações rápidas.

### 7. Confirmação de Agendamento (Usuário)
- **Descrição**: Tela exibida após o agendamento ser confirmado pela empresa.
- **Elementos**:
  - Detalhes: Empresa, serviço, data, horário.
  - Botão: "Adicionar ao Calendário", "Ver Detalhes".
  - Mensagem: "Aguardando confirmação" ou "Agendamento confirmado!".
- **Responsividade**: No mobile, informações em uma coluna; no PC, com layout mais espaçado.

## Fluxogramas

Os fluxogramas descrevem os processos principais da plataforma: cadastro, busca de serviços e agendamento.

### 1. Fluxograma: Cadastro de Empresa
```mermaid
graph TD
    A[Início: Empresa acessa plataforma] --> B[Clica em 'Cadastrar Empresa']
    B --> C[Preenche formulário: Nome, CNPJ, Endereço, etc.]
    C --> D[Envia cadastro para validação]
    D --> E{Validação por equipe}
    E -->|Aprovado| F[Empresa ativa: Configura serviços]
    E -->|Rejeitado| G[Notificação com motivo]
    F --> H[Fim: Empresa pronta para uso]
```

### 2. Fluxograma: Busca de Serviços
```mermaid
graph TD
    A[Início: Usuário logado] --> B[Ativa geolocalização]
    B --> C[Seleciona categoria de serviço]
    C --> D[Define raio de busca]
    D --> E[Plataforma exibe empresas próximas]
    E --> F[Usuário seleciona empresa]
    F --> G[Visualiza serviços disponíveis]
    G --> H[Fim: Prossegue para agendamento]
```

### 3. Fluxograma: Agendamento
```mermaid
graph TD
    A[Início: Usuário seleciona serviço] --> B[Escolhe data no calendário]
    B --> C[Seleciona horário disponível]
    C --> D[Confirma agendamento]
    D --> E[Notificação enviada à empresa]
    E --> F{Empresa revisa agendamento}
    F -->|Confirmado| G[Usuário recebe confirmação]
    F -->|Recusado| H[Usuário notificado para reagendar]
    G --> I[Fim: Agendamento concluído]
```

## Observações
- **Ferramentas sugeridas para prototipagem**: Figma ou Adobe XD para telas interativas, com exportação para formatos responsivos.
- **Estilo visual**: Paleta de cores moderna (ex.: azul e branco com tons de verde para confirmações), fontes legíveis (ex.: Roboto, Open Sans).
- **Testes iniciais**: Validar fluxos com usuários reais para garantir clareza e eficiência.