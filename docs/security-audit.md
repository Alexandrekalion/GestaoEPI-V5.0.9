# Auditoria de seguranca preliminar

Data: 2026-07-29

## Achados

| Item | Severidade | Situacao | Acao nesta branch |
|---|---:|---|---|
| Fotos em `backend/uploads/employees` | Alta | Arquivos versionados no repositorio publico | Removidos do conteudo atual da branch |
| Fotos em `backend/uploads/deliveries` | Alta | Arquivos versionados no repositorio publico | Removidos do conteudo atual da branch |
| `SECRET_KEY` com valor padrao no codigo | Alta | Chave JWT previsivel se ambiente nao definir variavel | Removido fallback hardcoded |
| Senha inicial de administrador no seed | Alta | Senha padrao previsivel no codigo | Substituida por `DEFAULT_ADMIN_PASSWORD` |
| Dados de teste com CPF, telefone e email | Media | Dados ficticios, mas semelhantes a dados pessoais | Mantidos por enquanto; revisar se seed deve existir em producao |
| Ausencia de LICENSE | Baixa | Licenciamento indefinido | Adicionado aviso proprietario |

## Pendencias

- Decidir se o repositorio deve continuar publico.
- Avaliar limpeza de historico Git para remover arquivos sensiveis antigos.
- Rotacionar qualquer segredo que possa ter sido usado em ambiente real.
- Validar se dados de seed devem existir fora de ambiente de desenvolvimento.

