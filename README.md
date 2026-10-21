# Política de Privacidade — Agenda Libras

Este repositório contém a página web oficial da **Política de Privacidade** do aplicativo **Agenda Libras**, pronta para publicação e homologação na **Google Play Store** e em conformidade com a **LGPD (Lei Geral de Proteção de Dados - Lei 13.709/2018)**.

---

## 📄 Arquivos

- **[`index.html`](./index.html)**: Página web completa, responsiva, moderna e autossuficiente (sem dependências pesadas externas). Inclui:
  - Alternador de tema Claro / Escuro com persistência local.
  - Botão de impressão / exportação em PDF estruturado.
  - Declaração detalhada das permissões do Android (`READ_CONTACTS`, `CAMERA`, `RECORD_AUDIO`, `READ_MEDIA_*`).
  - Destaque da arquitetura **100% Offline (Android Jetpack Room / SQLite local)**.
  - Cláusula jurídica robusta de **isenção total de responsabilidade do desenvolvedor** no compartilhamento voluntário de arquivos `.lsbcontact` (dados de contatos, fotos e vídeos de sinais em Libras).
  - Seções de retenção, controle e eliminação de dados conforme exigências da Google Play Console.
  - Informações de contato e atendimento aos direitos do titular.

---

## 🚀 Como publicar gratuitamente e obter o Link para a Google Play Console

A Google Play exige uma URL pública (com HTTPS) para a política de privacidade. A forma mais fácil e gratuita é usar o **GitHub Pages**:

### Passo a passo com GitHub Pages:

1. Crie um repositório no seu GitHub (exemplo: `agenda-libras-privacidade`).
2. Suba os arquivos deste diretório:
   ```bash
   git remote add origin https://github.com/SEU_USUARIO/agenda-libras-privacidade.git
   git branch -M main
   git push -u origin main
   ```
3. No GitHub, acesse:
   - **Settings** (Configurações do repositório) > **Pages** (no menu lateral esquerdo).
   - Em **Branch**, selecione `main` e a pasta `/ (root)`.
   - Clique em **Save**.
4. Em instantes, o GitHub gerará uma URL como:
   `https://SEU_USUARIO.github.io/agenda-libras-privacidade/`
5. Copie essa URL e cole no campo **"Política de Privacidade"** da sua ficha de aplicativo na **Google Play Console** e na seção **Segurança dos Dados (Data Safety)**.

---

## 🛡️ Resumo das Declarações para a Google Play Console (Data Safety)

Ao preencher a seção de **Segurança dos Dados (Data Safety)** no Google Play Console:

| Pergunta no Console | Resposta Correta |
| :--- | :--- |
| **O app coleta ou compartilha dados de usuários?** | **Não**, selecione "Não" para coleta em nuvem, pois o app é 100% offline. (Se o console perguntar sobre dados manipulados no dispositivo, declare que são processados efemeramente/localmente pelo usuário). |
| **Todos os dados coletados são transferidos por conexão segura?** | O app não transfere dados para servidores remotos (funciona offline). |
| **O usuário pode solicitar a exclusão dos dados?** | **Sim**, o usuário pode apagar diretamente no app ou limpando os dados / desinstalando o app. |
