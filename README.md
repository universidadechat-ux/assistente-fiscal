# Assistente Fiscal PT

PWA de consulta e organização de fontes fiscais portuguesas, publicada gratuitamente no GitHub Pages.

## Versão 0.1

- Interface adaptada a computador e telemóvel, instalável como PWA.
- Catálogo de ligações oficiais e adição manual de textos dessas fontes.
- Pesquisa **local de excertos**, sem geração de pareceres por inteligência artificial.
- Histórico e documentos guardados no próprio navegador, em IndexedDB.
- Exportação e restauro de backups JSON.
- Interface disponível offline após a primeira visita.

**Ainda não incluído:** importação automática de códigos, atualização legislativa automática, modelo de IA, sincronização entre dispositivos. Não confundir excertos encontrados com respostas fiscais validadas.

## Publicação

No GitHub: **Settings → Pages → Deploy from a branch → main → / (root)**. Endereço esperado: `https://universidadechat-ux.github.io/assistente-fiscal/`.

O repositório é público: não guardar nele chaves de API, dados pessoais ou documentos de clientes. O histórico e os textos adicionados pelo utilizador são locais ao navegador, devendo ser exportados periodicamente.

Não exige Node.js ou instalação de ferramentas de desenvolvimento no computador. O identificador e o âmbito da PWA são exclusivos deste repositório, evitando conflitos com outras aplicações.
