# **Daily War**

![Daily War Logo](https://via.placeholder.com/150)

**Daily War** é um aplicativo motivacional e de rastreamento de hábitos que transforma cada dia em uma batalha pessoal. O objetivo é ajudar os usuários a vencerem suas "batalhas diárias" em áreas específicas da vida, como físico, estudos, espiritualidade, família, entre outras, e, assim, conquistar a "guerra" maior de autodesenvolvimento e consistência.

---

## **Índice**
- [Visão Geral](#visão-geral)
- [Funcionalidades](#funcionalidades)
- [Estrutura do Projeto](#estrutura-do-projeto)
- [Tecnologias Utilizadas](#tecnologias-utilizadas)
- [Instalação e Configuração](#instalação-e-configuração)
- [Como Usar](#como-usar)
- [Melhorias Futuras](#melhorias-futuras)
- [Contribuição](#contribuição)
- [Licença](#licença)

---

## **Visão Geral**
O **Daily War** baseia-se na ideia de que cada dia é uma batalha a ser vencida, e a guerra é conquistada ao acumular vitórias diárias consistentes. Os usuários definem áreas personalizadas de foco (como "Físico", "Estudos", "Espiritual", "Família") e avaliam seu desempenho diário em cada uma delas com notas de 0 a 10. O aplicativo fornece feedbacks visuais, como um heatmap de progresso, e relatórios detalhados para ajudar os usuários a identificarem padrões e melhorarem seu desempenho ao longo do tempo.

### **Objetivos Principais**
- Ajudar os usuários a manterem a consistência em suas metas diárias.
- Fornecer uma interface intuitiva e motivadora para o autodesenvolvimento.
- Oferecer insights sobre o desempenho em diferentes áreas da vida.

---

## **Funcionalidades**
O **Daily War** oferece as seguintes funcionalidades principais:

- **Definição de Áreas Personalizadas**: Os usuários podem criar e gerenciar áreas de foco, como "Físico", "Estudos", etc.
- **Registro Diário de Desempenho**: A partir das 19h, o aplicativo envia notificações para que os usuários avaliem seu dia em cada área, atribuindo notas de 0 a 10.
- **Desativação Temporária de Áreas**: Os usuários podem desativar áreas específicas para dias ou semanas em que elas não são relevantes (ex: "Trabalho" durante férias).
- **Heatmap de Progresso**: Um gráfico visual estilo GitHub que exibe o desempenho diário ao longo do tempo, facilitando a visualização de padrões e consistência.
- **Relatórios de Desempenho**: Relatórios detalhados que mostram médias diárias, semanais e por área, ajudando os usuários a identificarem suas forças e pontos de melhoria.
- **Janela de Atualização**: Os usuários têm até 3 dias para atualizar registros esquecidos. Após esse período, as notas são zeradas automaticamente para incentivar a disciplina.
- **Notificações Push**: Lembretes automáticos para garantir que os usuários não esqueçam de registrar seu desempenho diário.

---

## **Estrutura do Projeto**
O projeto está organizado da seguinte forma para garantir modularidade e escalabilidade:

```
daily-war/
├── frontend/               # Código do aplicativo móvel (Flutter)
│   ├── lib/                # Código fonte principal
│   ├── assets/             # Imagens, fontes e outros recursos estáticos
│   └── test/               # Testes unitários e de integração
├── backend/                # Funções serverless (Firebase Functions)
│   ├── functions/          # Código das funções backend
│   └── tests/              # Testes para o backend
├── database/               # Esquemas e scripts de banco de dados (Firestore)
├── docs/                   # Documentação adicional e assets para o README
└── README.md               # Documentação principal do projeto
```

---

## **Tecnologias Utilizadas**
O **Daily War** é construído com tecnologias modernas e escaláveis:

- **Frontend**: [Flutter](https://flutter.dev/) (Dart) - Para uma interface bonita e performática em Android e iOS.
- **Backend**: [Firebase](https://firebase.google.com/) - Para autenticação, banco de dados em tempo real e funções serverless.
- **Banco de Dados**: [Firestore](https://firebase.google.com/docs/firestore) - NoSQL para armazenamento flexível e escalável.
- **Notificações**: [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging) - Para notificações push.
- **Gráficos**: [FL Chart](https://pub.dev/packages/fl_chart) - Biblioteca de gráficos para Flutter.
- **Armazenamento Offline**: [Hive](https://pub.dev/packages/hive) - Para sincronização offline e online.
- **CI/CD**: [GitHub Actions](https://github.com/features/actions) - Para automação de testes e deployments.
- **Monitoramento**: [Sentry](https://sentry.io/) - Para monitoramento de erros e logs.

---

## **Instalação e Configuração**
Para rodar o projeto localmente, siga os passos abaixo:

### **Pré-requisitos**
- [Flutter SDK](https://flutter.dev/docs/get-started/install)
- [Firebase CLI](https://firebase.google.com/docs/cli)
- [Dart](https://dart.dev/get-dart)
- Uma conta no [Firebase](https://firebase.google.com/) para configurar o backend.

### **Passos**
1. **Clone o repositório**:
   ```bash
   git clone https://github.com/seu-usuario/daily-war.git
   cd daily-war
   ```

2. **Instale as dependências do Flutter**:
   ```bash
   cd frontend
   flutter pub get
   ```

3. **Configure o Firebase**:
   - Crie um projeto no Firebase.
   - Adicione o aplicativo Flutter ao projeto Firebase.
   - Baixe o arquivo `google-services.json` (Android) e `GoogleService-Info.plist` (iOS) e coloque-os nas pastas corretas.

4. **Inicie o emulador ou conecte um dispositivo**:
   ```bash
   flutter run
   ```

5. **Configure o backend (se necessário)**:
   - Implemente as funções serverless no Firebase, conforme a estrutura do projeto.

---

## **Como Usar**
1. **Cadastre-se ou faça login** no aplicativo.
2. **Defina suas áreas de foco** (ex: "Físico", "Estudos").
3. **Receba notificações a partir das 19h** para avaliar seu desempenho diário em cada área.
4. **Atribua notas de 0 a 10** para cada área ou desative áreas temporariamente, se necessário.
5. **Visualize seu progresso** através do heatmap e relatórios detalhados.
6. **Atualize registros esquecidos** dentro de 3 dias para evitar que sejam zerados.

---

## **Melhorias Futuras**
O **Daily War** tem um grande potencial de crescimento. Aqui estão algumas melhorias planejadas:

- **Integração com Wearables**: Sincronização com dispositivos como smartwatches para rastrear automaticamente atividades físicas.
- **Gamificação**: Adição de recompensas, badges e níveis para motivar ainda mais os usuários.
- **Comunidade e Desafios**: Funcionalidades sociais onde usuários podem criar desafios em grupo ou compartilhar progresso.
- **Análises Avançadas**: Uso de IA para fornecer insights personalizados sobre padrões de desempenho e sugestões de melhoria.
- **Versão Web e Desktop**: Expansão para outras plataformas usando o Flutter para web e desktop.

---

## **Contribuição**
Contribuições são bem-vindas! Siga os passos abaixo para contribuir:

1. **Fork o repositório**.
2. **Crie uma branch** para sua feature ou correção:
   ```bash
   git checkout -b feature/nova-feature
   ```
3. **Commit suas mudanças**:
   ```bash
   git commit -m "Adiciona nova feature"
   ```
4. **Envie para o repositório remoto**:
   ```bash
   git push origin feature/nova-feature
   ```
5. **Abra um Pull Request** no GitHub.

Por favor, siga as diretrizes de código e adicione testes para suas contribuições.

---

## **Licença**
Este projeto é licenciado sob a [Apache 2.0 License].

---
