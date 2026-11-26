?# Prompt Definitivo de Depuraçêo para Claude

![DALL·E 2024-07-24 17 14 32 - A sleek, modern 16x9 image representing a debugging prompt for GitHub  The image features a dark theme with code snippets, a magnifying glass focusing](https://github.com/user-attachments/assets/bf48c21a-7200-441d-b18b-57bf81255627)

Bem-vindo ao Prompt Definitivo de Depuraçêo para Claude! Este prompt sofisticado e cuidadosamente projetado foi desenvolvido para otimizar e aprimorar seu processo de depuraçêo ao trabalhar com Claude 3.5 Sonnet.

## Estrutura do Prompt

O Prompt Definitivo de Depuraçêo para Claude consiste nas seguintes seções principais:

1. **Variáveis**: Um conjunto de variáveis predefinidas usadas para armazenar informações específicas sobre o cenário de depuraçêo, como o código do projeto anexado, mensagem de erro e tarefa do usuário.
2. **Espaços Reservados**: Áreas designadas dentro do prompt onde os usuários inserem as informações necessárias para seu caso específico de depuraçêo.
3. **Blocos de Código**: Seções do prompt onde os usuários anexam os arquivos relevantes do projeto, incluindo código-fonte, logs e arquivos de configuraçêo.
4. **Raciocínio e Análise**: Seções estruturadas que guiam o processo de pensamento do Claude, desde a geraçêo de previsões até a identificaçêo da causa raiz do erro.
5. **Explicações e Instruções**: Áreas onde o Claude fornece explicações detalhadas do problema identificado e instruções passo a passo para resolvê-lo.

## Explicaçêo das Variáveis

A tabela a seguir descreve as variáveis inseridas pelo usuário no Prompt Definitivo de Depuraçêo para Claude:

| Variável | Descriçêo | Formato de Entrada |
|----------|-----------|-------------------|
| `ATTACHED_PROJECT_CODE` | Os blocos de código representam seus arquivos de código anexados. Se os arquivos forem pequenos o suficiente, você pode copiar e colar o código dentro. Recomendo que você exporte todo o seu repositório de código em um único arquivo anexado usando minha ferramenta [Code-Repository-to-Text-File](https://github.com/PixelPoser/Code-Repository-to-Text-File) para contornar a restriçêo de upload de 5 arquivos. | `<SEU_ARQUIVO_1.py>`, `<SEU_ARQUIVO_2.py>`, `<SEU_ARQUIVO_3.log>` e assim por diante |
| `APP_USE_CASE` | Uma breve descriçêo do propósito e funcionalidade da aplicaçêo. | Texto em linguagem natural |
| `USER_TASK` | Uma descriçêo da tarefa específica que o usuário estava realizando quando o erro ocorreu. | Texto em linguagem natural |
| `ERROR` | A mensagem de erro ou exceçêo encontrada durante o cenário de depuraçêo. | Texto em linguagem natural ou trecho de código |

A tabela a seguir descreve as variáveis de saída do Claude. Deixe-as como estêo:

| Variável | Descriçêo |
|----------|-----------|
| `PREDICTIONS` | Suposições fundamentadas do Claude para possíveis causas do erro. |
| `SCRATCHPAD` | Uma área designada para o Claude documentar o processo de raciocínio e análise durante a depuraçêo. |
| `PROBLEMATIC_CODE` | O segmento de código específico identificado como a causa raiz do erro. |
| `STEP_BY_STEP_REASONING` | A explicaçêo detalhada do Claude sobre o processo de depuraçêo, desde a avaliaçêo inicial até a identificaçêo da causa raiz. |
| `EXPLANATION` | A explicaçêo detalhada do Claude sobre por que o segmento de código identificado é a provável causa raiz do erro. |
| `DEBUG_INSTRUCTIONS` | Instruções passo a passo fornecidas pelo Claude para resolver o problema identificado. |

## Formato do Bloco de Código

Ao anexar arquivos do projeto ao prompt de depuraçêo, basta renomear 'YOUR_FILE_1.py' e assim por diante com o nome do seu arquivo. Você deve ter um para cada arquivo.

DICA PRO: Tire uma captura de tela ou capturas de tela de toda a pasta do seu repositório e use o seguinte prompt no ChatGPT ou em outra conversa do Claude para automatizar a nomeaçêo das tags XML dos arquivos:

Exemplo de nomes de arquivos reais para serem usados no prompt principal
```
<attached_project_code>

 <business_consulting_chatbot.py>
 {{Anexado à conversa}}
</business_consulting_chatbot.py>

  <business_interviewer.py>
{{Anexado à conversa}}
</business_interviewer.py>

<index.html>
{{Anexado à conversa}}
</index.html>

<pdf_conversion.py>
 {{Anexado à conversa}}
</pdf_conversion.py>

<prompts.py>
 {{Anexado à conversa}}
</prompts.py>

 </attached_project_code>

```

### Prompt para nomeaçêo automatizada rápida de tags XML de arquivos:

1. Primeiro anexe a captura de tela do repositório:

![Screenshot 2024-07-24 at 3 52 39 PM](https://github.com/user-attachments/assets/4b3336d8-61a8-4ed5-b636-f13c072de92e)


3. Use o seguinte prompt no ChatGPT ou em outra conversa do Claude para nomeaçêo automatizada:
```
Analise o repositório na foto e use o seguinte modelo para criar tags XML para cada arquivo. Deixe o interior intacto. Escreva em bloco de código.
"""
<attached_project_code>
  <SEU_ARQUIVO_1.py>
 {{Anexado à conversa}}
</SEU_ARQUIVO_1.py>

  <SEU_ARQUIVO_2.py>
{{Anexado à conversa}}
</SEU_ARQUIVO_2.py>

<SEU_ARQUIVO_3.log>
{{Anexado à conversa}}
</SEU_ARQUIVO_3.log>

 </attached_project_code>
"""

```


Certifique-se de que os blocos de código estejam formatados corretamente e incluídos dentro das tags `<attached_project_code>`. Forneça as extensões de arquivo necessárias e destaque de sintaxe específico da linguagem para melhor legibilidade.

## Raciocínio e Análise

O Prompt Definitivo de Depuraçêo para Claude emprega uma abordagem estruturada para guiar o processo de raciocínio e análise do Claude. O prompt divide a tarefa de depuraçêo nas seguintes etapas:

1. **Avaliaçêo do Erro**: O Claude examina a mensagem de erro fornecida e a tarefa do usuário para obter uma compreensêo inicial do problema.
2. **Geraçêo de Previsões**: Com base na avaliaçêo inicial, o Claude gera previsões fundamentadas para possíveis causas do erro.
3. **Investigaçêo do Código**: O Claude revisa meticulosamente o código do projeto anexado, focando nos segmentos relacionados à tarefa do usuário e ao erro.
4. **Refinamento das Previsões**: Usando um processo de eliminaçêo, o Claude refina as previsões verificando ou refutando cada uma com base na análise do código e raciocínio lógico.
5. **Identificaçêo da Causa Raiz**: O Claude seleciona a causa raiz mais provável das previsões restantes e fornece uma explicaçêo detalhada de por que ela é a culpada.
6. **Instruções de Depuraçêo**: O Claude gera instruções claras e acionáveis passo a passo para resolver o problema identificado.

Esta abordagem estruturada garante que o Claude siga um processo de depuraçêo lógico e sistemático, levando a uma resoluçêo de erros precisa e eficiente.

## Integraçêo e Fluxo de Trabalho

O Prompt Definitivo de Depuraçêo para Claude pode ser integrado perfeitamente ao seu fluxo de trabalho de desenvolvimento existente. Aqui estêo algumas dicas para uma integraçêo eficaz:

1. **Controle de Versêo**: Certifique-se de que os arquivos do seu projeto estejam versionados corretamente usando um sistema de controle de versêo como o Git. Isso permite que você anexe facilmente os arquivos relevantes ao prompt de depuraçêo.
2. **Integraçêo Contínua**: Incorpore o prompt de depuraçêo no seu pipeline de integraçêo contínua (CI). Acione automaticamente o prompt quando uma compilaçêo falhar ou quando padrões de erro específicos forem detectados.
3. **Rastreamento de Problemas**: Use o prompt de depuraçêo em conjunto com seu sistema de rastreamento de problemas. Anexe a saída do prompt, incluindo o raciocínio passo a passo e as instruções de depuraçêo, ao problema relevante para fácil referência e colaboraçêo.
4. **Revisêo de Código**: Utilize o prompt de depuraçêo durante as revisões de código. Anexe o prompt à solicitaçêo de revisêo e use a análise do Claude para facilitar discussões e identificar problemas potenciais no início do processo de desenvolvimento.

Lembre-se de adaptar a abordagem de integraçêo com base no seu ambiente de desenvolvimento específico, ferramentas e práticas da equipe.

## Personalizaçêo e Extensibilidade

O Prompt Definitivo de Depuraçêo para Claude foi projetado para ser personalizável e extensível para atender às suas necessidades específicas. Considere as seguintes opções de personalizaçêo:

1. **Modificações de Variáveis**: Ajuste as variáveis predefinidas para melhor alinhar com a terminologia do seu projeto ou adicione novas variáveis para capturar informações adicionais de depuraçêo.
2. **Estrutura do Prompt**: Modifique a estrutura do prompt para enfatizar aspectos específicos do processo de depuraçêo ou para incorporar etapas de análise adicionais.
3. **Adaptaçêo de Linguagem**: Adapte o prompt para trabalhar com diferentes linguagens de programaçêo, modificando o formato do bloco de código e fornecendo exemplos específicos da linguagem.
4. **Integraçêo com Outras Ferramentas**: Estenda o prompt para integrar com outras ferramentas de depuraçêo ou análise, como linters, profilers ou frameworks de teste.

Sinta-se à vontade para experimentar com o prompt e compartilhar suas modificações ou melhorias com a comunidade. Juntos, podemos aprimorar continuamente a experiência de depuraçêo com o Claude.


## Conclusêo

O Prompt Definitivo de Depuraçêo para Claude é uma ferramenta poderosa que aproveita as capacidades avançadas de compreensêo de linguagem e raciocínio do Claude para revolucionar seu fluxo de trabalho de depuraçêo. Seguindo a abordagem estruturada e utilizando as opções de personalizaçêo, você pode identificar e resolver erros rapidamente, economizando um tempo de desenvolvimento valioso.

Encorajamos você a experimentar o Prompt Definitivo de Depuraçêo para Claude e vivenciar os benefícios em primeira mêo. Se você tiver dúvidas, sugestões ou feedback, por favor nêo hesite em entrar em contato. Sua opiniêo é valiosa para moldar o futuro desta soluçêo de depuraçêo.

Boa depuraçêo com o Claude!

---

Projeto  - ARCKHÉe