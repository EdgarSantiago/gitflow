
# 🚀 Git Flow — Guia Rápido de Comandos

Este é um guia prático com os principais comandos **Git Flow** para gerenciamento de branches e versões no seu projeto.

---

## ⚙️ 1. Iniciar o Git Flow

```bash
git flow init
```
💡 *Aceite os padrões pressionando Enter em todas as perguntas.*

---

## 🌱 2. Feature (para desenvolver novas funcionalidades)

- ▶️ **Iniciar uma feature:**
```bash
git flow feature start nome-da-feature
```

- ✅ **Finalizar uma feature (mescla com develop):**
```bash
git flow feature finish nome-da-feature
```

---

## 🐞 3. Bugfix (para corrigir bugs ainda na fase de desenvolvimento)

- 🛠 **Iniciar um bugfix:**
```bash
git flow bugfix start nome-do-bugfix
```

- 🔧 **Finalizar um bugfix (mescla com develop):**
```bash
git flow bugfix finish nome-do-bugfix
```

---

## 🔥 4. Hotfix (para corrigir problemas críticos direto em produção)

- 🚨 **Iniciar um hotfix:**
```bash
git flow hotfix start nome-do-hotfix
```

- ✅ **Finalizar um hotfix (mescla com master e develop + tag):**
```bash
git flow hotfix finish nome-do-hotfix
```

---

## 📦 5. Release (para preparar uma nova versão para produção)

- 🎯 **Iniciar uma release a partir da develop (ou homologação):**
```bash
git flow release start nome-da-release
```

- 🧩 **(Opcional) Adicionar commits com `cherry-pick` durante a release:**
```bash
git cherry-pick <commit-id>
```

- 🎉 **Finalizar a release (mescla com master e develop + tag):**
```bash
git flow release finish nome-da-release
```

---

## 💡 Dica Extra: Enviando Apenas o que Está Pronto

Quando você cria uma release a partir da **homologação**, ela **herda todos os commits**.  
Se você quer enviar **somente os que estão prontos**, siga estes passos:

1. 🚀 Crie a release normalmente:
```bash
git flow release start nome-da-release
```

2. ❌ Faça um reset para remover os commits indesejados:
```bash
git reset --hard develop
```

3. 🧠 Adicione apenas os commits aprovados:
```bash
git cherry-pick <commit-id>
```

4. ✅ Finalize a release:
```bash
git flow release finish nome-da-release
```

---
