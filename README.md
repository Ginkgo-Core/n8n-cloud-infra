# Ginkgo n8n Cloud Infrastructure

TRACK = TRACK_INFRA
CURRENT_GATE = DEDICATED_REPO_BOOTSTRAP_CC
CC_ID = CC-20261114-N8N-CLOUD-REPO-BOOTSTRAP-R1

Repositorio privado dedicado a futura plataforma persistente de PREPROD n8n
Cloud da Ginkgo. Este commit inicial C0 contem somente o bootstrap documental.
Nao existe implementacao de infraestrutura, runtime, deploy ou ambiente PROD
neste checkpoint candidato.

## Autoridade e base documental

- [CTO CANONICAL, secoes 182 e 183](https://docs.google.com/document/d/1lRiEfYb2zZqZvNM6OgBD17qDGdI7Ms-JLLMqq2LPm7U/edit): freeze arquitetural e autorizacao condicional deste bootstrap.
- [Cloud SPEC R1](https://docs.google.com/document/d/1GZbpzCwHqEQD4xtt15gug5jfCGYGIFKvU-KjeVfPhps/edit).
- [Corrigenda normativa R1.1, D01-D07](https://docs.google.com/document/d/1uAWNKK5XUlh24TTMWS6UrgQdU5h5i1XLeQdTEBbcvkk/edit).
- [Bootstrap CC aprovado](https://docs.google.com/document/d/1b0DrWL8QIhszRN8R-W_ex1iHWVj75-_MxQ2jg-s7cx0/edit).

A adjudicacao Canonical prevalece; R1.1 sobrepoe os trechos correspondentes da
R1. O freeze e documental. C0 somente sera uma base aceita depois do review
independente e do checkpoint explicito do CTO.

## Ownership e identidades autorizadas

- Writer exclusivo do bootstrap: CODEX.
- Reviewer independente: AGY/GEMINI, STRICT READ-ONLY.
- Aceite ou rejeicao do checkpoint: CTO.
- Remote exclusivo: https://github.com/Ginkgo-Core/n8n-cloud-infra.git
- Branch inicial: main.
- Checkout-base: C:\Ginkgo-CTO\infra\n8n-cloud-infra
- Branch dedicada autorizada para preparacao: codex/infra/n8n-cloud-static-r1
- Worktree dedicado autorizado: C:\Ginkgo-CTO\worktrees\n8n-cloud-static-r1

A branch e o worktree dedicados devem partir exatamente de C0. Sua preparacao
nao autoriza escrever infraestrutura. Nenhum commit, workflow, migration,
fixture, dado ou business logic de outro TRACK e herdado aqui.

## Escopo de C0

Os unicos arquivos de fonte autorizados sao README.md, .gitignore e
.gitattributes, alem dos metadados Git dedicados. Nao ha Compose, manifesto
OCI, configuracao operacional, script, teste, workflow, CI, license template
ou pacote de infraestrutura neste bootstrap.

Os 51 caminhos propostos no harvest permanecem candidatos a um CC estatico
separado. Nao sao autorizados por este CC de bootstrap.

Nao versionar secrets, tokens, credenciais, chaves privadas, certificados de
cliente, arquivos .env reais, dumps, backups ou estado de aplicacao. Regras de
ignore nao substituem a revisao da allowlist nem uma verificacao de conteudo.

## Gates e STOP

A sequencia imediata e: bootstrap C0 -> review AGY read-only -> adjudicacao CTO
-> eventual CC separado de implementacao estatica. Nenhum aceite operacional
ou autorizacao de provisionamento decorre deste repositorio.

Interromper diante de conflito de owner, permissao, remote, caminho, branch,
worktree, privacidade, arquivo inesperado, exposicao de secret ou necessidade
de modificar outro TRACK. Preservar o estado parcial e relatar ao CTO; nao
sobrescrever, apagar ou fazer limpeza agressiva como remediacao automatica.

TRACK_AUTOMATION_N8N permanece HOLD, inclusive viewer, Gate B1 e C09/C10.
Nao definir, importar ou executar workflows, fixtures funcionais ou bindings
de providers neste bootstrap. Nao executar Docker/n8n ou scripts operacionais;
nao contratar VPS, alterar DNS ou acessar secrets.

READY_FOR_STATIC_INFRA_WRITER = NO
READY_TO_BUY_VPS = NO
READY_TO_DEPLOY = NO
READY_TO_EXECUTE_WORKFLOW = NO

STOP apos o relatorio de bootstrap. AGY fara review independente antes do
checkpoint CTO.
