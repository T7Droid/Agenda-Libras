# Agenda Libras — Documentação Oficial & Conformidade Google

Repositório oficial das páginas web institucionais e de conformidade legal do aplicativo **Agenda Libras**, hospedado no **GitHub Pages**:

🌐 **Endereço Oficial:** [https://t7droid.github.io/Agenda-Libras/](https://t7droid.github.io/Agenda-Libras/)

Projetado em rigorosa consonância com os requisitos de:
- **Verificação de Marca e Verificação OAuth do Google (Google Cloud Platform / OAuth 2.0)**;
- **Política de Dados do Usuário dos Serviços de API do Google (Google API Services User Data Policy / Limited Use Requirements)**;
- **Diretrizes de Conteúdo e Segurança de Dados da Google Play Store (Data Safety Section)**;
- **Política de Padrões de Segurança Infantil da Google Play (CSAE/CSAM)**;
- **LGPD — Lei Geral de Proteção de Dados Pessoais (Lei nº 13.709/2018)** e **ECA (Lei nº 8.069/1990)**.

---

## 📄 Estrutura das Páginas Web

| Página | Arquivo | URL no GitHub Pages | Descrição |
| :--- | :--- | :--- | :--- |
| **Página Inicial** | [`index.html`](./index.html) | `https://t7droid.github.io/Agenda-Libras/` | Landing page institucional do aplicativo. Apresenta funcionalidades, identidade visual, acessibilidade em Libras, princípios de privacidade e links visíveis para todos os documentos legais. |
| **Política de Privacidade** | [`privacy.html`](./privacy.html)<br>[`privacy/index.html`](./privacy/index.html) | `https://t7droid.github.io/Agenda-Libras/privacy` | Documento jurídico exaustivo com detalhamento de permissões, armazenamento local (Room SQLite), integração segura com Google Drive (`drive.appdata`), conformidade com LGPD e exclusão de dados. |
| **Termos de Serviço** | [`terms.html`](./terms.html)<br>[`terms/index.html`](./terms/index.html) | `https://t7droid.github.io/Agenda-Libras/terms` | Condições gerais de uso do aplicativo, regras de direito de imagem e consentimento para vídeos em Libras, isenção de responsabilidade e propriedade intelectual. |
| **Segurança Infantil** | [`seguranca-infantil.html`](./seguranca-infantil.html) | `https://t7droid.github.io/Agenda-Libras/seguranca-infantil.html` | Declaração oficial de Tolerância Zero contra abuso e exploração sexual infantil (CSAE/CSAM), mecanismos de denúncia in-app e compromisso de reporte às autoridades competentes. |

---

## 🔑 Informações para a Verificação OAuth do Google (Google Cloud Console)

Ao submeter a tela de consentimento OAuth do aplicativo para aprovação na Google Cloud Platform:

### 1. Campos da Tela de Consentimento (OAuth Consent Screen)

- **Nome do aplicativo:** `Agenda Libras`
- **E-mail de suporte ao usuário:** `contato.agendalibras@gmail.com`
- **Logotipo do aplicativo:** Ícone oficial do Agenda Libras (mão em Libras).
- **Página inicial do aplicativo (Application Home Page):**  
  `https://t7droid.github.io/Agenda-Libras/`
- **Link da Política de Privacidade (Application Privacy Policy Link):**  
  `https://t7droid.github.io/Agenda-Libras/privacy.html` (ou `https://t7droid.github.io/Agenda-Libras/privacy`)
- **Link dos Termos de Serviço (Application Terms of Service Link):**  
  `https://t7droid.github.io/Agenda-Libras/terms.html` (ou `https://t7droid.github.io/Agenda-Libras/terms`)
- **Domínio autorizado:** `t7droid.github.io`

### 2. Escopo Solicitado e Justificativa

- **Escopo OAuth:** `https://www.googleapis.com/auth/drive.appdata` (*See, create, and delete its own configuration data in your Google Drive*)
- **Por que este escopo é necessário?**  
  O Agenda Libras permite que usuários criem glossários temáticos de sinais em Libras com gravações em vídeo. O aplicativo utiliza a pasta exclusiva de dados de aplicativo no Google Drive (`drive.appdata` / `AppDataFolder`) do próprio usuário para realizar o backup, restauração e sincronização desses vídeos e termos entre dispositivos.
- **Por que o escopo restrito `drive.appdata` é o mais seguro?**  
  Diferente de escopos amplos como `drive` ou `drive.file`, o escopo `drive.appdata` restringe estritamente o acesso do app a uma pasta oculta privativa criada para ele. O aplicativo **não possui permissão** para visualizar, ler, listar, modificar ou apagar nenhum outro arquivo pessoal, fotos ou pastas do usuário no Google Drive.
- **Conformidade com Uso Limitado:**  
  A Política de Privacidade contém a declaração formal de conformidade com a *Google API Services User Data Policy*, garantindo que os dados não são comercializados, não são repassados a terceiros e não são usados para treinar modelos de inteligência artificial.

---

## 🛡️ Preenchimento na Google Play Console (Padrões de Segurança Infantil)

| Campo no Play Console | O que preencher / selecionar |
| :--- | :--- |
| **URL dos padrões de segurança** | `https://t7droid.github.io/Agenda-Libras/seguranca-infantil.html` |
| **Contato designado** | `contato.agendalibras@gmail.com` |
| **Checkbox 1:** *"O app Agenda Libras permite que os usuários denunciem dentro dele os problemas de segurança infantil"* | **Marcar Sim.** (Implemente uma opção em Configurações/Ajuda que abra um e-mail direto para `contato.agendalibras@gmail.com`). |
| **Checkbox 2:** *"Meu app obedece a todas as leis relevantes de segurança infantil e encaminha denúncias para as autoridades regionais e nacionais"* | **Marcar Sim.** (Formalizado na página `seguranca-infantil.html` com a Polícia Federal, SaferNet e NCMEC). |

---

## 🔒 Declarações de Segurança de Dados na Google Play (Data Safety)

| Pergunta no Play Console | Resposta |
| :--- | :--- |
| **O app coleta dados de contatos em servidores do desenvolvedor?** | **Não.** Os contatos permanecem armazenados unicamente no banco local SQLite (Jetpack Room) no aparelho do usuário. |
| **O app utiliza armazenamento em nuvem?** | **Sim, sob demanda e controlado pelo usuário.** Quando o usuário conecta sua Conta Google, os vídeos de glossários são salvos diretamente em sua própria conta Google Drive (pasta `drive.appdata`). O desenvolvedor não retém dados em servidores próprios. |
| **Os dados são transferidos por conexão segura?** | **Sim.** Todo o tráfego com a API oficial do Google Drive é feito via HTTPS/TLS 1.3 criptografado. |
| **O usuário pode solicitar a exclusão dos dados?** | **Sim.** O usuário pode apagar contatos e glossários diretamente no app, apagar os arquivos na pasta do Google Drive, revogar o acesso via `myaccount.google.com/permissions` ou desinstalar o app. |
