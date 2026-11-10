# Agenda Libras — Site Institucional & Documentação Legal

Repositório oficial das páginas web institucionais e documentos de conformidade legal do aplicativo **Agenda Libras**, publicado via **GitHub Pages**:

🌐 **Endereço Oficial:** [https://t7droid.github.io/Agenda-Libras/](https://t7droid.github.io/Agenda-Libras/)

Documentação estruturada em conformidade com:
- **LGPD** — Lei Geral de Proteção de Dados Pessoais (Lei nº 13.709/2018);
- **Marco Civil da Internet** (Lei nº 12.965/2014) e **Código de Defesa do Consumidor — CDC** (Lei nº 8.078/1990);
- **ECA** — Estatuto da Criança e do Adolescente (Lei nº 8.069/1990) e **Política de Padrões de Segurança Infantil da Google Play (CSAE/CSAM)**;
- **Lei do Software e Direitos Autorais** (Lei nº 9.609/1998 e Lei nº 9.610/1998);
- **Política de Dados do Usuário dos Serviços de API do Google** (*Google API Services User Data Policy* — *Limited Use Requirements*) e **Políticas da Google Play Store**.

---

## 📄 Páginas Publicadas

| Página | Arquivo(s) | URL no GitHub Pages | Finalidade |
| :--- | :--- | :--- | :--- |
| **Página Inicial** | [`index.html`](./index.html) | `https://t7droid.github.io/Agenda-Libras/` | Apresentação institucional do aplicativo, catálogo visual de contatos, módulo de Glossários em Libras, resumo Plano Gratuito vs. Glossários Premium, transparência da integração Google Drive e links legais. |
| **Política de Privacidade** | [`privacy.html`](./privacy.html)<br>[`privacy/index.html`](./privacy/index.html) | `https://t7droid.github.io/Agenda-Libras/privacy` | Detalhamento de dados manipulados, permissões Android (Câmera, Contatos, Mídia, Bluetooth e Localização técnica para scan de proximidade, Internet), processamento local (Room SQLite, MP4 H.264 sem áudio nos glossários, ML Kit Selfie Segmentation on-device), escopo `drive.appdata`, faturamento via Google Play Billing (cofre `AndroidKeyStore` AES-256-GCM e cache offline de 72h), pacotes `.lsb*` e direitos LGPD. |
| **Termos de Serviço** | [`terms.html`](./terms.html)<br>[`terms/index.html`](./terms/index.html) | `https://t7droid.github.io/Agenda-Libras/terms` | Condições gerais de uso, regras do modelo Freemium e da assinatura `glossarios_premium`, isenção linguística/pedagógica, direitos de imagem e autorais, limites técnicos de bloqueio de tela/expiração, responsabilidade sobre pacotes `.lsb*` e Transferência por Proximidade (Bluetooth). |
| **Segurança Infantil** | [`seguranca-infantil.html`](./seguranca-infantil.html) | `https://t7droid.github.io/Agenda-Libras/seguranca-infantil.html` | Padrões públicos de Tolerância Zero contra CSAE/CSAM abrangendo armazenamento local, nuvem pessoal (`drive.appdata`), Transferência por Proximidade (Bluetooth) e formatos `.lsbcontact`, `.lsbsign`, `.lsbglossary`, `.lsbglossarybackup` e `.lsbbackup`, além de canais prioritários de denúncia e cooperação legal. |

---

## 🔒 Princípios Técnicos de Privacidade & Segurança

- **Arquitetura Offline-First & Sem Servidores Proprietários:** Os dados de contatos, perfil próprio e glossários residem localmente no banco de dados Android Jetpack Room (SQLite), com segmentação de fundo de fotos via **ML Kit Selfie Segmentation** e transcodificação de vídeo (MP4/H.264 até 5s, sem áudio nos glossários) executados **100% no dispositivo**.
- **Integração Opcional com Google Drive (`drive.appdata`):** Mediante conexão voluntária pelo usuário via OAuth 2.0, o aplicativo acessa exclusivamente sua pasta oculta `appDataFolder` (`https://www.googleapis.com/auth/drive.appdata`) na conta Google Drive do próprio usuário — utilizada para vídeos/metadados de Glossários (modos Nuvem e Híbrido) e, conforme opção do usuário, para backup da agenda de contatos, perfil próprio, fotos e vídeos — sem acesso a outros arquivos pessoais do Drive e em cumprimento integral aos requisitos de *Uso Limitado* da Google.
- **Pacotes Criptografados (`AES-256-GCM`):** Exportação e importação protegidas nos formatos `.lsbcontact`, `.lsbsign`, `.lsbglossary`, `.lsbglossarybackup` e `.lsbbackup`, com suporte a **Transferência Direta por Proximidade (Bluetooth)** e Android Sharesheet.
- **Assinatura via Google Play Billing (`glossarios_premium`):** Processamento exclusivo pela Google Play Store, sem coleta de dados bancários pelo desenvolvedor, validação protegida localmente via `AndroidKeyStore` (`AES-256-GCM`) com cache offline de até 72 horas.

---

## 📬 Contato Oficial

- **Desenvolvedor Responsável / Encarregado (DPO):** Thyago Neves da Silva Silvestre
- **E-mail Oficial (Suporte, Privacidade, LGPD, Termos, OAuth & Segurança Infantil):** `thyagoneves.sa@gmail.com`
- **Localidade:** Brasil
