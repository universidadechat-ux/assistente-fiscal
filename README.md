# Assistente Fiscal PT

PWA de consulta e organização de fontes fiscais portuguesas, preparada para publicação gratuita no **GitHub Pages**.

## Versão 0.1

- Interface adaptada a computador e telemóvel, instalável como PWA.
- Catálogo de ligações oficiais e adição manual de textos dessas fontes.
- Pesquisa **local de excertos**, sem geração de pareceres por inteligência artificial.
- Histórico e documentos guardados no próprio navegador, em IndexedDB.
- Exportação e restauro de backups JSON.
- Interface disponível offline após a primeira visita.

**Ainda não incluído:** importação automática de códigos, atualização legislativa automática, modelo de IA, sincronização entre dispositivos. Não confundir excertos encontrados com respostas fiscais validadas.

## Publicação com domínio GitHub independente

**Não ativar GitHub Pages neste repositório da conta `universidadechat-ux` antes de decidir o domínio.** Se o publicarmos em `https://universidadechat-ux.github.io/assistente-fiscal/`, partilha a origem do navegador com as outras PWAs do mesmo utilizador.

Para obter isolamento de origem **sem sair do GitHub nem comprar domínio**, criar uma organização GitHub exclusiva para esta aplicação. A organização tem o seu próprio domínio `<organizacao>.github.io`, distinto de `universidadechat-ux.github.io`.

1. Criar uma organização gratuita e escolher o seu nome disponível.
2. Criar nessa organização um repositório público chamado `<organizacao>.github.io` e colocar nele os ficheiros desta PWA.
3. No novo repositório, ativar **Settings → Pages → Deploy from a branch → main → / (root)**.
4. Abrir `https://<organizacao>.github.io/` e instalar a PWA a partir desse domínio, sem alterar as aplicações antigas.

O `manifest.webmanifest`, os caminhos dos assets e o Service Worker usam caminhos relativos para funcionar na raiz deste domínio exclusivo. Um repositório separado, por si só, não equivale a um domínio separado.

O repositório é público: não guardar nele chaves de API, dados pessoais ou documentos de clientes. O histórico e os textos adicionados pelo utilizador são locais ao navegador, devendo ser exportados periodicamente.

Não exige Node.js ou instalação de ferramentas de desenvolvimento no computador. O armazenamento fica separado das outras PWAs quando se usa a origem independente `<organizacao>.github.io`.
