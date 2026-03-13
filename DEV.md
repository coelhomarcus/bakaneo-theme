# Dev Guide

## Requisitos

- [Node.js](https://nodejs.org)
- [vsce](https://github.com/microsoft/vscode-vsce) — ferramenta de build de extensões VSCode

```bash
npm install -g @vscode/vsce
```

---

## Testar em modo dev (sem build)

Abra a pasta do projeto no VSCode e pressione **F5**.

Isso abre uma nova janela do VSCode com a extensão carregada. Para aplicar o tema nessa janela, vá em `Ctrl+K Ctrl+T` e selecione **BakaNeo**.

Toda vez que editar o arquivo `themes/bakaneo-color-theme.json`, recarregue a janela dev com `Ctrl+Shift+P` → `Developer: Reload Window`.

---

## Build (.vsix)

```bash
vsce package
```

Gera um arquivo `bakaneo-x.x.x.vsix` na raiz do projeto.

---

## Instalar o .vsix localmente

```bash
code --install-extension bakaneo-x.x.x.vsix
```

Ou pelo VSCode: `Ctrl+Shift+P` → `Extensions: Install from VSIX...`

---

## Publicar no Marketplace

```bash
vsce publish
```

> Requer um Personal Access Token configurado. Veja: https://code.visualstudio.com/api/working-with-extensions/publishing-extension
