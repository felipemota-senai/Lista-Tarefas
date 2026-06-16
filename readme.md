# ⚡ ATIVIDADE RÁPIDA — Git & GitHub Desktop
### Disciplina: Desenvolvimento de Sistemas | SENAI
### Tempo: 30 minutos | Ferramenta: GitHub Desktop
---

## 🎯 Objetivo

Praticar o fluxo completo do Git em ritmo acelerado:
criar repositório → adicionar código → commitar → push.
Cada função adicionada = 1 commit. Sem enrolação.

---

## 📁 O Projeto

Você vai construir uma **Lista de Tarefas** simples em Python.
O arquivo `lista_tarefas.py` já tem a estrutura base pronta.
Sua missão é adicionar 4 funções, uma de cada vez.

---

## ⏱️ Cronograma sugerido

| Tempo | O que fazer |
|-------|-------------|
| 0–5 min | Criar o repo e commit inicial |
| 5–10 min | Função 2 + commit |
| 10–15 min | Função 3 + commit |
| 15–20 min | Função 4 + commit |
| 20–25 min | Função 5 + commit |
| 25–30 min | Push final + verificar no GitHub |

---

## 🚀 PASSO 1 — Criar o repositório 

1. Abra o **GitHub Desktop**
2. `File` → `New Repository`
3. Nome: `lista-tarefas-git`
4. Marque **Initialize with a README**
5. Clique em `Create Repository`
6. Copie o arquivo `lista_tarefas.py` para a pasta do projeto
7. No GitHub Desktop, campo `Summary`:
   ```
   feat: adiciona estrutura inicial da lista de tarefas
   ```
8. Clique em `Commit to main` → depois `Publish repository` (Public)

---

## 🔨 PASSO 2 — Adicione as funções (1 commit cada)

> **Ritual de cada função:**
> escreve → testa → commit → push

---

### Função 2 — `adicionar_tarefa`
Adiciona uma tarefa à lista global `tarefas`.

```python
def adicionar_tarefa(descricao):
    """Adiciona uma nova tarefa à lista."""
    tarefa = {"descricao": descricao, "concluida": False}
    tarefas.append(tarefa)
    print(f'Tarefa "{descricao}" adicionada!')
```

**Mensagem de commit:**
```
feat: adiciona funcao adicionar_tarefa
```

---

### Função 3 — `listar_tarefas`
Exibe todas as tarefas com número e status.

```python
def listar_tarefas():
    """Lista todas as tarefas com seu status."""
    if len(tarefas) == 0:
        print("Nenhuma tarefa cadastrada.")
        return
    print("\n--- Suas Tarefas ---")
    for i, tarefa in enumerate(tarefas, 1):
        status = "✅" if tarefa["concluida"] else "⬜"
        print(f"{i}. {status} {tarefa['descricao']}")
```

**Mensagem de commit:**
```
feat: adiciona funcao listar_tarefas
```

---

### Função 4 — `concluir_tarefa`
Marca uma tarefa como concluída pelo número.

```python
def concluir_tarefa(numero):
    """Marca a tarefa do número informado como concluída."""
    if numero < 1 or numero > len(tarefas):
        print("Número de tarefa inválido.")
        return
    tarefas[numero - 1]["concluida"] = True
    print(f'Tarefa {numero} marcada como concluída!')
```

**Mensagem de commit:**
```
feat: adiciona funcao concluir_tarefa
```

---

### Função 5 — `contar_pendentes`
Retorna quantas tarefas ainda não foram concluídas.

```python
def contar_pendentes():
    """Retorna o número de tarefas ainda pendentes."""
    pendentes = 0
    for tarefa in tarefas:
        if not tarefa["concluida"]:
            pendentes += 1
    return pendentes
```

**Mensagem de commit:**
```
feat: adiciona funcao contar_pendentes
```

---

## 📤 PASSO 3 — Push final 

1. No GitHub Desktop, clique em **Push origin**
2. Abra o GitHub no navegador
3. Confirme que aparecem **5 commits** no repositório
4. Copie o link e envie para o professor

---

## ✅ Como deve ficar o histórico

No GitHub Desktop → `History`:

```
feat: adiciona funcao contar_pendentes
feat: adiciona funcao concluir_tarefa
feat: adiciona funcao listar_tarefas
feat: adiciona funcao adicionar_tarefa
feat: adiciona estrutura inicial da lista de tarefas
```

5 commits. Limpos. Com mensagem descritiva. Esse é o objetivo.

---

## 📊 Critérios de Avaliação

| Critério | Pontos |
|----------|--------|
| Repositório público no GitHub | 20 pts |
| Commit inicial correto | 15 pts |
| 4 funções com 1 commit cada | 40 pts |
| Mensagens de commit no padrão `feat:` | 25 pts |
| **TOTAL** | **100 pts** |

---

## 📤 Entrega

Link do repositório público no GitHub.
Prazo: fim da aula — ___/___/______

---

*Sem tempo a perder — bora codar! 🚀*
