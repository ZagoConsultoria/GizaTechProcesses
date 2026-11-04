<p align="center">
  <img src="docs/assets/banner.png" alt="GizaTechProcesses" width="100%">
</p>

<p align="center"><b>Processos operacionais da área de tecnologia: estratégia, produto, engenharia e infraestrutura.</b></p>

<p align="center">
  <img src="https://img.shields.io/badge/MkDocs%20Material-0f2d22?style=flat-square" alt="MkDocs Material">
  <img src="https://img.shields.io/badge/Processos-0f2d22?style=flat-square" alt="Processos">
  <img src="https://img.shields.io/badge/Runbooks-0f2d22?style=flat-square" alt="Runbooks">
</p>

**Sumário:** [Visão geral](#visão-geral) · [Estrutura](#estrutura) · [Começando](#começando) · [Deploy e operação](#deploy-e-operação) · [Contribuindo](#contribuindo) · [Segurança](#segurança) · [Mantenedores](#mantenedores)

---

## Visão geral

Biblioteca de processos numerados (POPs) da tecnologia, organizada em quatro áreas: estratégia (ciclos de inovação, OKRs, ROI, custos), produto (discovery, validação, backlog, lançamento), engenharia (auditoria de código, revisão de arquitetura, bugs, monitoramento) e infraestrutura (inventário, segurança de rede, gestão de senhas).

## Estrutura

```
docs/01-estrategia/
docs/02-produto/
docs/03-engenharia/
docs/04-infra/
mkdocs.yml, custom.css
```

## Começando

### Rodar localmente

```bash
pip install mkdocs mkdocs-material
mkdocs serve        # http://127.0.0.1:8000
```

## Deploy e operação

O site é publicado pelo GitHub Pages. Com o renome o endereço passa de `zagoconsultoria.github.io/Processos-TEC` para `zagoconsultoria.github.io/GizaTechProcesses`, e o GitHub não redireciona o endereço antigo.

## Contribuindo

1. Crie uma branch a partir de `main`: `feat/…`, `fix/…`, `docs/…` ou `chore/…`.
2. Use mensagens no padrão [Conventional Commits](https://www.conventionalcommits.org/pt-br/v1.0.0/), por exemplo `feat(auth): adiciona recuperação de senha`.
3. Abra um Pull Request e aguarde revisão e CI verde antes de integrar.
4. Nunca versione chaves, tokens, senhas, certificados ou arquivos `.env`.

## Segurança

Vulnerabilidades e vazamentos devem ser comunicados diretamente à equipe de tecnologia, sem abrir issue pública.

## Mantenedores

Equipe de tecnologia da Zago Consultoria.

Repositório da organização [ZagoConsultoria](https://github.com/ZagoConsultoria). Todos os direitos reservados; não há licença de código aberto definida.
