# Como contribuir

## Fluxo de trabalho
1. Crie uma branch a partir da `main` com prefixo: `feat/`, `fix/`, `docs/` ou `chore/`.
2. Escreva os commits no padrão [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/), por exemplo `feat(agenda): marca visita presencial`.
3. Abra um Pull Request usando o modelo e peça revisão. Os testes precisam estar verdes antes de mesclar. Se o projeto não tem CI, rode os testes localmente e registre o resultado no PR.
4. Não faça push direto na `main` e nunca faça force-push nela.

## O que não entra no repositório
- Senhas, tokens, chaves de API, `client_secret`, chave JWT, URLs com senha ou webhook com token.
- Arquivos `.env` reais, chaves e certificados (`.pem`, `.key`, `.p12`, `.pfx`).
- Dumps e backups de banco, dados pessoais ou de clientes reais, planilhas e PDFs com dados reais.
- Logs, `node_modules`, pastas de build e arquivos de editor.

Migrações SQL de esquema podem (e devem) ficar no repositório. Migração já aplicada não se edita: corrija com uma migração nova.

## Se um segredo vazar
1. Gire e invalide o segredo imediatamente.
2. Remova do código por Pull Request.
3. Avalie a limpeza do histórico com o time (nunca reescreva a `main` sem combinar).

## Autoria
Commits e Pull Requests são assinados em nome da equipe, sem atribuição a ferramentas.
