# Guia de organização e entrega

## Estrutura

- Criar cada pasta de atividade diretamente na raiz, com o nome indicado pelo professor, por exemplo: `Atividade 2.2`.
- Colocar os arquivos do TF em `Trabalho Final`.
- Manter os arquivos exigidos acessíveis na pasta de entrega. Usar subpastas apenas quando o volume justificar e quando isso for compatível com o enunciado.
- Acrescentar um README local quando forem necessárias instruções de execução ou explicações sobre vários arquivos.
- Usar o histórico do Git para versões anteriores, evitando cópias como `final_v2_corrigido`.

## Notebooks e reprodução

Cada notebook deve permitir entender:

1. O objetivo e sua relação com o enunciado.
2. A fonte, as condições de uso e a forma de obtenção dos dados.
3. As bibliotecas e versões utilizadas.
4. As etapas de preparação e análise.
5. Os resultados, suas limitações e a conclusão.

Antes da entrega:

- Reiniciar o ambiente e executar todas as células em ordem.
- Corrigir erros e remover saídas desnecessárias ou que contenham informações privadas.
- Evitar caminhos absolutos da máquina pessoal; preferir caminhos relativos.
- Documentar downloads ou passos manuais necessários.
- Registrar sementes aleatórias quando aplicável e esclarecer limitações de reprodutibilidade.
- Em aprendizado supervisionado, separar treino, validação e teste conforme o problema; ajustar transformações apenas com os dados de treino.
- Criar um `requirements.txt` por entrega quando houver dependências a instalar, com versões efetivamente verificadas.

## Dados e modelos

- Não publicar senhas, tokens, chaves, dados pessoais ou documentos institucionais restritos.
- Não incluir bases de terceiros sem verificar a permissão de redistribuição. Quando necessário, fornecer a fonte e instruções de obtenção.
- Avaliar tamanho e necessidade antes de versionar bases, modelos e checkpoints. Para arquivos grandes, avaliar Git LFS e seus limites ou disponibilizar uma fonte externa autorizada.
- Não ignorar globalmente arquivos de dados ou modelos que possam ser exigidos na avaliação.

## Histórico de alterações

Usar commits com uma alteração coerente e mensagem descritiva, por exemplo:

- `docs: esclarece metodologia da atividade 2.2`
- `feat: adiciona notebook da atividade 2.2`
- `fix: corrige cálculo da métrica de validação`

Para alterações extensas, usar uma branch e revisar o diff antes de integrar à `main`. Correções documentais pequenas podem ser feitas diretamente na `main`.

## Conferência final

- Conferir o enunciado e os nomes das pastas.
- Verificar se todos os arquivos solicitados estão presentes.
- Confirmar a execução e a coerência entre resultados e conclusão.
- Abrir os arquivos no GitHub para verificar a visualização.
- Conferir se o link aponta para a entrega correta.
- Registrar a entrega no sistema da disciplina quando solicitado: publicar no GitHub não substitui esse envio.
