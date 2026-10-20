# Meu Financeiro 1.0

Aplicativo pessoal de controle financeiro, sem backend, sem Firebase e sem API paga.

## Publicar no GitHub Pages

1. Crie um repositório no GitHub (ex.: `meu-financeiro`).
2. Envie **todos os arquivos e a pasta `icons`** para a raiz do repositório.
3. Acesse **Settings → Pages → Build and deployment** e selecione **Deploy from a branch**, branch `main`, pasta `/ (root)`; salve.
4. Abra o endereço HTTPS fornecido pelo GitHub Pages, normalmente `https://SEU-USUARIO.github.io/meu-financeiro/`.
5. No Chrome Android, abra o menu ⋮ e use **Adicionar à tela inicial** ou **Instalar app**.

## Funcionalidades

- Saldo inicial, contas, dívidas, recebimentos e pagamentos parciais.
- Calendário de vencimentos e recebimentos, com recorrência mensal por 12 meses.
- Assistente gratuito por regras: prioriza contas conforme urgência, data e reserva desejada. Não é IA generativa.
- IndexedDB local, exportação e importação de backup JSON.
- PWA com cache offline após primeiro carregamento.

## Observações importantes

- Os dados **não sincronizam** entre aparelhos ou navegadores.
- Limpar dados do site ou desinstalar pode apagar o banco local: exporte backups JSON regularmente.
- Não coloque dados pessoais sensíveis no repositório: apenas o código deve ir para o GitHub.
- O assistente não conhece juros ou consequências contratuais; confirme prazos e acordos antes de adiar pagamentos.
- Para publicar atualizações, substitua os arquivos no repositório e altere a constante `CACHE` em `sw.js` para um nome novo. Reabra o app online para atualizar.
- Para testar localmente, use um servidor HTTP local (ex.: VS Code Live Server), não `file://`.


## Correção v1.0.1
Corrigida a exibição monetária: os dados permanecem em centavos no IndexedDB e agora são convertidos para reais apenas na apresentação. Não é necessário apagar registros. Atualize os arquivos no GitHub Pages e recarregue o aplicativo.
