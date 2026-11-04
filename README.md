# Assistente Fiscal PT

PWA de consulta e organização de fontes fiscais portuguesas. Código no GitHub, publicação independente através do **Cloudflare Pages**, no plano gratuito.

## Versão 0.1

- Interface adaptada a computador e telemóvel, instalável como PWA.
- Catálogo de ligações oficiais e adição manual de textos dessas fontes.
- Pesquisa **local de excertos**, sem geração de pareceres por inteligência artificial.
- Histórico e documentos guardados no próprio navegador, em IndexedDB.
- Exportação e restauro de backups JSON.
- Interface disponível offline após a primeira visita.

**Ainda não incluído:** importação automática de códigos, atualização legislativa automática, modelo de IA, sincronização entre dispositivos. Não confundir excertos encontrados com respostas fiscais validadas.

## Publicação isolada (Cloudflare Pages)

**Não ativar GitHub Pages** neste repositório. As outras aplicações de `universidadechat-ux.github.io` partilham a origem do navegador; por isso esta PWA deve ser alojada num domínio `*.pages.dev` dedicado.

1. Iniciar sessão no [Cloudflare Dashboard](https://dash.cloudflare.com/) com uma conta gratuita.
2. Abrir **Workers & Pages → Create application → Pages → Connect to Git**.
3. Autorizar o acesso ao repositório GitHub `universidadechat-ux/assistente-fiscal`.
4. Escolher o nome do projeto, por exemplo `assistente-fiscal-pt` (se estiver disponível), e a branch `main`.
5. **Framework preset:** None; **Build command:** `exit 0` (sem compilação); **Build output directory:** `.`; **Root directory:** deixar a predefinição (raiz do repositório).
6. Publicar. O endereço será comunicado pelo Cloudflare, normalmente `https://<nome-do-projeto>.pages.dev/`.

Os caminhos do manifest, Service Worker e assets são relativos ao alojamento para permitir instalação na raiz de um domínio independente. O ficheiro `_headers` acrescenta proteções e impede a indexação normal pelos motores de pesquisa, mas **não torna a aplicação privada**.

O repositório é público: não guardar nele chaves de API, dados pessoais ou documentos de clientes. O histórico e os textos adicionados pelo utilizador são locais ao navegador, devendo ser exportados periodicamente.

Não exige Node.js ou instalação de ferramentas de desenvolvimento no computador. O armazenamento só fica efetivamente isolado das outras aplicações quando a PWA é aberta no seu domínio `*.pages.dev`, e não em `universidadechat-ux.github.io`.
