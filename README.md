# Laboratório GitHub e TDD

Este repositório contém oito tarefas independentes para praticar colaboração com GitHub e desenvolvimento orientado a testes (TDD).

## Objetivo

Cada estudante deve implementar uma função em sua própria branch, escrevendo primeiro os testes automatizados e, depois, o código necessário para fazê-los passar.

## Estrutura

```text
.
├── src/       # funções a serem implementadas
└── tests/     # testes criados pelos estudantes
```

## Fluxo de trabalho

1. Clone o repositório e entre na pasta criada.
2. Crie uma branch com seu nome e a tarefa escolhida.
3. Crie o teste da tarefa dentro de `tests/`.
4. Execute `pytest` e confirme que o teste falha.
5. Faça um commit somente do teste.
6. Implemente a função em `src/`.
7. Execute `pytest` novamente e confirme que todos os testes passam.
8. Faça um commit da implementação, envie a branch e abra um Pull Request.

Exemplo de comandos:

```bash
git switch -c feature/temperatura-seu-nome
pytest
git add tests/
git commit -m "test: define regra de temperatura"

# implementar a função

pytest
git add src/temperatura.py
git commit -m "feat: classifica temperatura"
git push -u origin feature/temperatura-seu-nome
```

## Regras

- Cada estudante deve alterar apenas a função atribuída a ele.
- Não faça `push` diretamente para `main`.
- Não altere o código de outro estudante nesta primeira etapa.
- Todo Pull Request deve indicar os testes executados.
- Não use `git push --force`.

## Tarefas

| Arquivo | Função | Regras principais |
|---|---|---|
| `temperatura.py` | `classificar_temperatura` | frio, ameno ou quente |
| `notas.py` | `situacao_aluno` | aprovado ou recuperação |
| `pares.py` | `contar_pares` | quantidade de pares entre 1 e um limite |
| `confianca.py` | `classificar_confianca` | automática, revisão ou nova análise |
| `estudos.py` | `atividade_do_dia` | conteúdo novo ou revisão geral |
| `senha.py` | `tem_acesso` | acesso permitido ou negado |
| `multiplos.py` | `somar_multiplos_de_tres` | soma de múltiplos de 3 |
| `frete.py` | `valor_frete` | frete gratuito ou valor fixo |

## Execução dos testes

Na raiz do projeto:

```bash
pytest
```

