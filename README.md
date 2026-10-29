# 🚚 Rotas — Oficinas e Costureiras (versão demo)

App que monta a rota diária de coletas e entregas, gera o link do Google Maps e a mensagem pronta para o motorista no **WhatsApp**, com dados vindos do **Google Sheets**.

🌐 **[Abrir a demo](https://lauramazzi.github.io/rotas-demo/)** — funciona com dados fictícios, sem precisar de planilha.

> Esta é uma cópia pública de um projeto feito para um cliente. Nomes, endereços, motoristas e chaves foram substituídos por dados fictícios, e a senha de acesso foi removida. O código do cliente é privado.

## Problema
A logística com oficinas de costura terceirizadas era combinada à mão: alguém olhava a planilha de movimentações, montava a rota no Maps e digitava a mensagem para o motorista todos os dias.

## Solução
- **Carrega as movimentações do dia** direto da planilha (envios e retiradas por oficina) e transforma em paradas
- **Gera o link do Google Maps** com saída, paradas e retorno ao ponto de origem
- **Mensagem pronta para o WhatsApp** do motorista, com tipo de parada, produto, quantidade e observações
- **Salva a rota** no histórico e exporta para a aba "Rotas" da planilha
- **Backend em Google Apps Script** ([`apps-script/Code.gs`](apps-script/Code.gs)) protegido por chave, com leitura por nome de cabeçalho e preenchimento automático de endereço ao escolher a oficina

## Como testar
1. Abra a [demo](https://lauramazzi.github.io/rotas-demo/).
2. Clique em **"Carregar rota de hoje da planilha"** — as paradas fictícias aparecem.
3. Escolha um motorista e abra o link do Maps ou a mensagem do WhatsApp.

## Stack
JavaScript (vanilla), Google Apps Script, Google Sheets, Google Maps URLs, WhatsApp (wa.me) · deploy no GitHub Pages
