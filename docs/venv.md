
# 🐍 Como usar ambientes virtuais (venv) no Python

Ambientes virtuais são usados para **isolar dependências** de projetos Python.  
Assim, você evita conflitos entre versões de pacotes em diferentes projetos.

---

## ✅ Por que usar um ambiente virtual?

- Evita que pacotes de um projeto afetem outro.
- Permite versões específicas para cada projeto.
- Facilita o deploy e organização.

---

## 💻 Como criar e ativar ambiente virtual no Python

> Funciona com Python 3.3 ou superior

---

## 🪟 Windows

### Criar o ambiente virtual

```bash
python -m venv nome_do_ambiente
```

### Ativar o ambiente virtual

```bash
nome_do_ambiente\Scripts\activate
```

### Desativar o ambiente

```bash
deactivate
```

---

## 🐧 Linux

### Criar o ambiente virtual

```bash
python3 -m venv nome_do_ambiente
```

### Ativar o ambiente virtual

```bash
source nome_do_ambiente/bin/activate
```

### Desativar o ambiente

```bash
deactivate
```

---

## 🍎 macOS

### Criar o ambiente virtual

```bash
python3 -m venv nome_do_ambiente
```

### Ativar o ambiente virtual

```bash
source nome_do_ambiente/bin/activate
```

### Desativar o ambiente

```bash
deactivate
```

---

## 🧪 Teste rápido (depois de ativar)

```bash
pip install requests
pip freeze
```

Você verá algo como:

```
requests==2.31.0
```

Esse pacote foi instalado **só dentro do ambiente virtual**.

---

## 📝 Dica: Adicione no .gitignore

Se for usar Git, adicione essa linha no seu `.gitignore`:

```
nome_do_ambiente/
```

Isso evita que o ambiente virtual seja enviado para o repositório.

---

Pronto! Agora você já pode trabalhar com seus projetos de forma isolada e organizada 🚀
