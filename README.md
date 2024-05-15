# Integração da API GPT com Google Sheets

Este repositório demonstra como usar a API GPT da OpenAI dentro do Google Sheets para aprimorar o processamento e a análise de dados. Seguindo o guia passo a passo abaixo, você será capaz de gerar conteúdo dinâmico e automatizar respostas diretamente na sua planilha.

## Pré-requisitos

Antes de começar, certifique-se de ter:
- Uma conta Google
- Acesso ao Google Sheets
- Uma chave de API da OpenAI

## Guia Passo a Passo

### Passo 1: Abra o Google Sheets e Acesse o Editor de Scripts

1. Abra um novo ou existente documento do Google Sheets.
2. Navegue até `Extensões` > `Editor de Apps`. Isso abrirá o editor do Google Apps Script.

### Passo 2: Crie a Função GPTResponse

1. No editor de script, apague qualquer código existente e copie e cole o script fornecido na função GPTResponse.

2. Substitua `"API_KEY"` pela sua chave de API da OpenAI.

### Passo 3: Use a Função GPTResponse na Sua Planilha

1. Volte para o seu documento do Google Sheets.
2. Insira o conteúdo dinâmico e os prompts nas células desejadas.
3. Use a função `GPTResponse` em uma célula. Por exemplo:

```plaintext
=GPTResponse("O resultado da célula [[B2]] será utilizado para calcular [[C3]]." & D4 & D5 & D6)
```

### Exemplo de Uso

Suponha que você tenha os seguintes dados no seu Google Sheets:

- A célula B2 contém o valor `10`.
- A célula C3 contém o valor `5`.
- As células D4, D5 e D6 contêm contexto ou conteúdo adicional a ser anexado ao prompt.

Você deve inserir a seguinte fórmula em uma nova célula para gerar uma resposta do GPT:

```plaintext
=GPTResponse("O resultado da célula [[B2]] será utilizado para calcular [[C3]]." & D4 & D5 & D6)
```

A função substituirá `[[B2]]` e `[[C3]]` pelos seus respectivos valores e enviará o prompt completo para a API GPT. A resposta será exibida na célula onde você inseriu a fórmula.

As mensões a células dentro do prompt são fixas, após o prompt são dinamicas.

### Solução de Problemas

- **Nenhuma resposta do GPT**: Certifique-se de que sua chave de API está correta e possui limites de uso suficientes.
- **Erro ao chamar a API GPT**: Verifique sua conexão com a internet e certifique-se de que a URL da API está correta.

Para qualquer problema, consulte a [documentação da API OpenAI](https://beta.openai.com/docs/api-reference/introduction) para mais detalhes.

## Conclusão

Seguindo estes passos, você pode integrar a GPT-3.5 da OpenAI ao seu Google Sheets para automatizar e aprimorar suas tarefas de análise de dados e geração de conteúdo. Boa codificação!
