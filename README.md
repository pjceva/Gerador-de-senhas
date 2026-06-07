# Gerador de Senhas Fortes

Aplicação web minimalista para geração de senhas seguras, rodando 100% no navegador — nenhum dado sai do seu dispositivo.

## Funcionalidades

- **Geração criptograficamente segura** via `crypto.getRandomValues` com rejection sampling para evitar viés de distribuição
- **Comprimento ajustável** de 4 a 32 caracteres
- **Tipos de caracteres configuráveis:** maiúsculas, minúsculas, números e símbolos
- **Medidor de força** com três níveis (Fraca / Média / Forte) e dica contextual
- **Copiar com um clique** para a área de transferência (com fallback para navegadores mais antigos)
- **Configurações salvas** automaticamente via `localStorage`
- **Atalhos de teclado:** `Enter` gera uma nova senha, `Ctrl/Cmd+C` copia quando o campo está focado
- **Responsivo** — funciona em telas pequenas (≥ 320 px)

## Como usar

Abra o arquivo `index.html` diretamente no navegador — não há dependências de servidor ou build.

```bash
open index.html        # macOS
xdg-open index.html    # Linux
start index.html       # Windows
```

## Tecnologias

- HTML5 + CSS3 + JavaScript puro (sem frameworks)
- [Font Awesome 6.5](https://fontawesome.com/) para ícones (CDN)
- Web Crypto API para aleatoriedade segura

## Segurança

A geração usa `crypto.getRandomValues` com rejection sampling, garantindo distribuição uniforme sem viés modular. Nenhuma senha é enviada a servidores ou registrada em logs — tudo acontece localmente no navegador.
