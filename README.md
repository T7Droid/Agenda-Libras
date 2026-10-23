# Política de Privacidade & Padrões de Segurança Infantil — Agenda Libras

Este repositório contém as páginas web oficiais de conformidade do aplicativo **Agenda Libras**, prontas para homologação na **Google Play Store**, em estrita conformidade com a **LGPD (Lei 13.709/2018)**, o **ECA (Lei 8.069/1990)** e a nova **Política de Padrões de Segurança Infantil da Google Play (CSAE/CSAM)**.

---

## 📄 Arquivos do Projeto

- **[`index.html`](./index.html)**: Página web oficial da **Política de Privacidade**:
  - Declaração da arquitetura **100% Offline (Android Jetpack Room / SQLite local)**.
  - Declaração detalhada das permissões do Android (`READ_CONTACTS`, `CAMERA`, `RECORD_AUDIO`, `READ_MEDIA_*`).
  - Cláusula jurídica robusta de **isenção total de responsabilidade do desenvolvedor** no compartilhamento voluntário de arquivos `.lsbcontact`.
  - Mecanismos de exclusão e retenção de dados locais.
  - Conexão e link direto para a página de segurança infantil.

- **[`seguranca-infantil.html`](./seguranca-infantil.html)**: Página web oficial dos **Padrões de Segurança Infantil (Child Safety Standards)**:
  - Declaração expressa de **Tolerância Zero contra CSAE (Abuso e Exploração Sexual Infantil)** e **CSAM (Material de Abuso Sexual Infantil)**.
  - Definições detalhadas de condutas proibidas (grooming/aliciamento, sextorsão, compartilhamento ilícito).
  - Mecanismos de denúncia dentro do aplicativo e canal direto prioritário.
  - Compromisso formal de notificação e cooperação com as autoridades (Polícia Federal, SaferNet Brasil, Ministério Público e NCMEC).
  - Ponto de contato designado para conformidade (`thyagoneves.sa@gmail.com`).

---

## 🚀 Como publicar gratuitamente via GitHub Pages

A Google Play exige URLs públicas, ativas, mundiais e não editáveis (HTTPS). O **GitHub Pages** é a forma recomendada e gratuita:

### Passo a passo:

1. Crie um repositório no seu GitHub (exemplo: `agenda-libras-privacidade`).
2. Suba os arquivos deste diretório:
   ```bash
   git add .
   git commit -m "docs: adiciona politica de privacidade e padroes de seguranca infantil"
   git branch -M main
   git remote add origin https://github.com/SEU_USUARIO/agenda-libras-privacidade.git
   git push -u origin main
   ```
3. No GitHub:
   - Acesse **Settings** (Configurações) > **Pages** (no menu lateral).
   - Em **Branch**, selecione `main` e a pasta `/ (root)`.
   - Clique em **Save**.
4. Em instantes, o GitHub ativará suas duas páginas:
   - **Política de Privacidade:**
     `https://SEU_USUARIO.github.io/agenda-libras-privacidade/`
   - **Padrões de Segurança Infantil (CSAE/CSAM):**
     `https://SEU_USUARIO.github.io/agenda-libras-privacidade/seguranca-infantil.html`

---

## 🛡️ Como preencher a página "Padrões de segurança infantil" no Google Play Console

Quando o Google Play Console solicitar a seção **Padrões de segurança infantil**:

| Campo no Play Console | O que preencher / selecionar |
| :--- | :--- |
| **URL dos padrões de segurança** | Insira a URL direta: `https://SEU_USUARIO.github.io/agenda-libras-privacidade/seguranca-infantil.html` |
| **Contato** | Selecione `thyagoneves.sa@gmail.com` (o endereço associado à conta de desenvolvedor). |
| **Checkbox 1:** *"O app Agenda Libras permite que os usuários denunciem dentro dele os problemas de segurança infantil"* | **Marque a caixa.** (No app, garanta um botão/opção simples em "Sobre/Configurações" que abra um e-mail de denúncia para `thyagoneves.sa@gmail.com`). |
| **Checkbox 2:** *"Meu app obedece a todas as leis relevantes de segurança infantil e encaminha denúncias para as autoridades regionais e nacionais"* | **Marque a caixa.** (A página `seguranca-infantil.html` já formaliza esse compromisso com a Polícia Federal, SaferNet e NCMEC). |

---

## 🔒 Resumo das Declarações para a Google Play Console (Data Safety)

| Pergunta no Console | Resposta Correta |
| :--- | :--- |
| **O app coleta ou compartilha dados de usuários?** | **Não**, selecione "Não" para coleta em nuvem, pois o app é 100% offline. |
| **Todos os dados coletados são transferidos por conexão segura?** | O app não transfere dados para servidores remotos (funciona offline). |
| **O usuário pode solicitar a exclusão dos dados?** | **Sim**, o usuário pode apagar diretamente no app ou limpando os dados / desinstalando o app. |
