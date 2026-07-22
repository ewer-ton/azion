# Azion Consultoria — Landing Page (VMO)

Landing page estática em HTML/CSS/JS puro para a Azion Consultoria em Gestão, Valor & Performance, com foco na apresentação do conceito de **VMO (Value Management Office)**.

Não depende de build, framework ou Node — é só abrir e publicar.

## Estrutura de arquivos

```
azion-site/
├── index.html          → página única (HTML + CSS + JS embutidos)
├── assets/
│   └── logo_azion.png  → logo da Azion
└── README.md            → este guia
```

## Como hospedar no GitHub Pages (passo a passo)

### 1. Crie o repositório no GitHub
1. Acesse [github.com/new](https://github.com/new).
2. Nomeie o repositório, por exemplo `azion-landing` (pode ser público ou privado — Pages funciona nos dois em contas Pro/Org; em contas free precisa ser público).
3. Não marque "Add a README" (já temos um) e clique em **Create repository**.

### 2. Envie os arquivos
Pelo terminal, na pasta `azion-site`:

```bash
cd azion-site
git init
git add .
git commit -m "Landing page Azion — VMO"
git branch -M main
git remote add origin https://github.com/SEU-USUARIO/azion-landing.git
git push -u origin main
```

Ou, se preferir sem linha de comando: acesse a página do repositório no GitHub → **Add file → Upload files** → arraste `index.html`, a pasta `assets` e o `README.md` → **Commit changes**.

### 3. Ative o GitHub Pages
1. No repositório, vá em **Settings → Pages** (menu lateral esquerdo).
2. Em **Build and deployment → Source**, selecione **Deploy from a branch**.
3. Em **Branch**, selecione `main` e a pasta `/ (root)`.
4. Clique em **Save**.

### 4. Acesse o site
Depois de 1–2 minutos, o GitHub mostra a URL no topo da mesma página de **Settings → Pages**, no formato:

```
https://SEU-USUARIO.github.io/azion-landing/
```

Qualquer novo `git push` para `main` atualiza o site automaticamente em cerca de 1 minuto.

### 5. (Opcional) Domínio próprio
Se a Azion tiver um domínio (ex: `azionconsultoria.com.br`):
1. Em **Settings → Pages → Custom domain**, digite o domínio e salve. Isso cria um arquivo `CNAME` no repositório.
2. No painel do seu provedor de DNS, crie:
   - Um registro **CNAME** apontando `www` para `SEU-USUARIO.github.io`; **ou**
   - Registros **A** apontando o domínio raiz para os IPs do GitHub Pages (`185.199.108.153`, `185.199.109.153`, `185.199.110.153`, `185.199.111.153`).
3. Marque **Enforce HTTPS** assim que o certificado for emitido (pode levar até 24h).

## Editar conteúdo

Todo o texto e a estrutura estão em `index.html`, dividido por seções com comentários (`<!-- HERO -->`, `<!-- CONCEITO -->`, `<!-- COMPARATIVO -->`, `<!-- FUNÇÕES -->`, `<!-- ECOSSISTEMA -->`, `<!-- CTA -->`). Basta abrir o arquivo em qualquer editor de texto (VS Code, por exemplo) e alterar diretamente o texto entre as tags.

As cores, fontes e espaçamentos ficam centralizados no bloco `:root { ... }` no topo do `<style>` — mudar uma variável (ex: `--blue`, `--orange`) atualiza a cor em toda a página.

## Trocar o link do LinkedIn

O link `https://www.linkedin.com/company/azion-consultoria/` aparece em 3 lugares no `index.html` (menu, hero e rodapé/CTA final) — todos usando `<a ... target="_blank" rel="noopener">`.
