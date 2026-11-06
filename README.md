# fnlinfo.com.br

Site da FNL Info (Soluções em Informática e Biomedicina). Página única, HTML e CSS puros, sem build e sem dependências além da fonte Plus Jakarta Sans (Google Fonts).

## Arquivos

| Arquivo | O que é |
|---|---|
| `index.html` | O site inteiro (seções: início, informática, biomedicina, diferenciais, contato) |
| `styles.css` | Estilos, com layout responsivo para celular |
| `logo.svg` | Logo completo (símbolo, "fnl", linha e "INFORMÁTICA"), para fundo escuro. Usado no rodapé |
| `logo-compact.svg` | Logo sem a linha e o texto de baixo, para espaços pequenos. Usado no cabeçalho |
| `favicon.svg` | Ícone da aba (só o símbolo) |
| `Informatica.html`, `Biomedicina.html`, `Download.html`, `Fale.html` | Redirecionam os endereços do site antigo para a seção certa da página nova, para links salvos e resultados do Google não quebrarem |

## Editar

Os textos estão todos no `index.html`. Telefones e e-mail aparecem no topo (botões do início) e na seção `#contato`. As cores ficam no começo do `styles.css` (`--navy` e `--gold`, as mesmas do logo).

Para ver localmente, é só abrir o `index.html` no browser.

## Publicar no GitHub Pages

1. Criar o repositório `fnlinfo.github.io` e subir estes arquivos na branch `main`.
2. Settings > Pages > Source: "Deploy from a branch", branch `main`, pasta `/ (root)`.
3. Para usar o domínio `fnlinfo.com.br`: em Settings > Pages > Custom domain, informar `fnlinfo.com.br` (isso cria o arquivo `CNAME`). No DNS do domínio, criar os registros `A` de `fnlinfo.com.br` para os IPs do GitHub Pages (185.199.108.153, 185.199.109.153, 185.199.110.153, 185.199.111.153) e um `CNAME` de `www` para `<usuario>.github.io`. Depois marcar "Enforce HTTPS".

**Cuidado com o e-mail.** Hoje site e e-mail estão na HostGator (DNS em `ns00208/ns00209.hostgator.com.br`, IP `69.6.249.201`). O `MX` aponta para `mail.fnlinfo.com.br`, que resolve para o mesmo IP do site. Ao apontar o site para o GitHub Pages, mude só os registros `A` de `fnlinfo.com.br` e o `www`. O `mail.fnlinfo.com.br` precisa continuar com `A` para `69.6.249.201` (confira se ele é um registro próprio e não um alias do domínio raiz), e o `MX` fica como está. Senão o `tecnico@fnlinfo.com.br` para de receber e-mail.
