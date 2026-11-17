# Prompt Definitivo de DepuraÃ§Ã£o para Claude

![DALLÂ·E 2024-07-24 17 14 32 - A sleek, modern 16x9 image representing a debugging prompt for GitHub  The image features a dark theme with code snippets, a magnifying glass focusing](https://github.com/user-attachments/assets/bf48c21a-7200-441d-b18b-57bf81255627)

Bem-vindo ao Prompt Definitivo de DepuraÃ§Ã£o para Claude! Este prompt sofisticado e cuidadosamente projetado foi desenvolvido para otimizar e aprimorar seu processo de depuraÃ§Ã£o ao trabalhar com Claude 3.5 Sonnet.

## Estrutura do Prompt

O Prompt Definitivo de DepuraÃ§Ã£o para Claude consiste nas seguintes seÃ§Ãµes principais:

1. **VariÃ¡veis**: Um conjunto de variÃ¡veis predefinidas usadas para armazenar informaÃ§Ãµes especÃ­ficas sobre o cenÃ¡rio de depuraÃ§Ã£o, como o cÃ³digo do projeto anexado, mensagem de erro e tarefa do usuÃ¡rio.
2. **EspaÃ§os Reservados**: Ãreas designadas dentro do prompt onde os usuÃ¡rios inserem as informaÃ§Ãµes necessÃ¡rias para seu caso especÃ­fico de depuraÃ§Ã£o.
3. **Blocos de CÃ³digo**: SeÃ§Ãµes do prompt onde os usuÃ¡rios anexam os arquivos relevantes do projeto, incluindo cÃ³digo-fonte, logs e arquivos de configuraÃ§Ã£o.
4. **RaciocÃ­nio e AnÃ¡lise**: SeÃ§Ãµes estruturadas que guiam o processo de pensamento do Claude, desde a geraÃ§Ã£o de previsÃµes atÃ© a identificaÃ§Ã£o da causa raiz do erro.
5. **ExplicaÃ§Ãµes e InstruÃ§Ãµes**: Ãreas onde o Claude fornece explicaÃ§Ãµes detalhadas do problema identificado e instruÃ§Ãµes passo a passo para resolvÃª-lo.

## ExplicaÃ§Ã£o das VariÃ¡veis

A tabela a seguir descreve as variÃ¡veis inseridas pelo usuÃ¡rio no Prompt Definitivo de DepuraÃ§Ã£o para Claude:

| VariÃ¡vel | DescriÃ§Ã£o | Formato de Entrada |
|----------|-----------|-------------------|
| `ATTACHED_PROJECT_CODE` | Os blocos de cÃ³digo representam seus arquivos de cÃ³digo anexados. Se os arquivos forem pequenos o suficiente, vocÃª pode copiar e colar o cÃ³digo dentro. Recomendo que vocÃª exporte todo o seu repositÃ³rio de cÃ³digo em um Ãºnico arquivo anexado usando minha ferramenta [Code-Repository-to-Text-File](https://github.com/PixelPoser/Code-Repository-to-Text-File) para contornar a restriÃ§Ã£o de upload de 5 arquivos. | `<SEU_ARQUIVO_1.py>`, `<SEU_ARQUIVO_2.py>`, `<SEU_ARQUIVO_3.log>` e assim por diante |
| `APP_USE_CASE` | Uma breve descriÃ§Ã£o do propÃ³sito e funcionalidade da aplicaÃ§Ã£o. | Texto em linguagem natural |
| `USER_TASK` | Uma descriÃ§Ã£o da tarefa especÃ­fica que o usuÃ¡rio estava realizando quando o erro ocorreu. | Texto em linguagem natural |
| `ERROR` | A mensagem de erro ou exceÃ§Ã£o encontrada durante o cenÃ¡rio de depuraÃ§Ã£o. | Texto em linguagem natural ou trecho de cÃ³digo |

A tabela a seguir descreve as variÃ¡veis de saÃ­da do Claude. Deixe-as como estÃ£o:

| VariÃ¡vel | DescriÃ§Ã£o |
|----------|-----------|
| `PREDICTIONS` | SuposiÃ§Ãµes fundamentadas do Claude para possÃ­veis causas do erro. |
| `SCRATCHPAD` | Uma Ã¡rea designada para o Claude documentar o processo de raciocÃ­nio e anÃ¡lise durante a depuraÃ§Ã£o. |
| `PROBLEMATIC_CODE` | O segmento de cÃ³digo especÃ­fico identificado como a causa raiz do erro. |
| `STEP_BY_STEP_REASONING` | A explicaÃ§Ã£o detalhada do Claude sobre o processo de depuraÃ§Ã£o, desde a avaliaÃ§Ã£o inicial atÃ© a identificaÃ§Ã£o da causa raiz. |
| `EXPLANATION` | A explicaÃ§Ã£o detalhada do Claude sobre por que o segmento de cÃ³digo identificado Ã© a provÃ¡vel causa raiz do erro. |
| `DEBUG_INSTRUCTIONS` | InstruÃ§Ãµes passo a passo fornecidas pelo Claude para resolver o problema identificado. |

## Formato do Bloco de CÃ³digo

Ao anexar arquivos do projeto ao prompt de depuraÃ§Ã£o, basta renomear 'YOUR_FILE_1.py' e assim por diante com o nome do seu arquivo. VocÃª deve ter um para cada arquivo.

DICA PRO: Tire uma captura de tela ou capturas de tela de toda a pasta do seu repositÃ³rio e use o seguinte prompt no ChatGPT ou em outra conversa do Claude para automatizar a nomeaÃ§Ã£o das tags XML dos arquivos:

Exemplo de nomes de arquivos reais para serem usados no prompt principal
```
<attached_project_code>

 <business_consulting_chatbot.py>
 {{Anexado Ã  conversa}}
</business_consulting_chatbot.py>

  <business_interviewer.py>
{{Anexado Ã  conversa}}
</business_interviewer.py>

<index.html>
{{Anexado Ã  conversa}}
</index.html>

<pdf_conversion.py>
 {{Anexado Ã  conversa}}
</pdf_conversion.py>

<prompts.py>
 {{Anexado Ã  conversa}}
</prompts.py>

 </attached_project_code>

```

### Prompt para nomeaÃ§Ã£o automatizada rÃ¡pida de tags XML de arquivos:

1. Primeiro anexe a captura de tela do repositÃ³rio:

![Screenshot 2024-07-24 at 3 52 39 PM](https://github.com/user-attachments/assets/4b3336d8-61a8-4ed5-b636-f13c072de92e)


3. Use o seguinte prompt no ChatGPT ou em outra conversa do Claude para nomeaÃ§Ã£o automatizada:
```
Analise o repositÃ³rio na foto e use o seguinte modelo para criar tags XML para cada arquivo. Deixe o interior intacto. Escreva em bloco de cÃ³digo.
"""
<attached_project_code>
  <SEU_ARQUIVO_1.py>
 {{Anexado Ã  conversa}}
</SEU_ARQUIVO_1.py>

  <SEU_ARQUIVO_2.py>
{{Anexado Ã  conversa}}
</SEU_ARQUIVO_2.py>

<SEU_ARQUIVO_3.log>
{{Anexado Ã  conversa}}
</SEU_ARQUIVO_3.log>

 </attached_project_code>
"""

```


Certifique-se de que os blocos de cÃ³digo estejam formatados corretamente e incluÃ­dos dentro das tags `<attached_project_code>`. ForneÃ§a as extensÃµes de arquivo necessÃ¡rias e destaque de sintaxe especÃ­fico da linguagem para melhor legibilidade.

## RaciocÃ­nio e AnÃ¡lise

O Prompt Definitivo de DepuraÃ§Ã£o para Claude emprega uma abordagem estruturada para guiar o processo de raciocÃ­nio e anÃ¡lise do Claude. O prompt divide a tarefa de depuraÃ§Ã£o nas seguintes etapas:

1. **AvaliaÃ§Ã£o do Erro**: O Claude examina a mensagem de erro fornecida e a tarefa do usuÃ¡rio para obter uma compreensÃ£o inicial do problema.
2. **GeraÃ§Ã£o de PrevisÃµes**: Com base na avaliaÃ§Ã£o inicial, o Claude gera previsÃµes fundamentadas para possÃ­veis causas do erro.
3. **InvestigaÃ§Ã£o do CÃ³digo**: O Claude revisa meticulosamente o cÃ³digo do projeto anexado, focando nos segmentos relacionados Ã  tarefa do usuÃ¡rio e ao erro.
4. **Refinamento das PrevisÃµes**: Usando um processo de eliminaÃ§Ã£o, o Claude refina as previsÃµes verificando ou refutando cada uma com base na anÃ¡lise do cÃ³digo e raciocÃ­nio lÃ³gico.
5. **IdentificaÃ§Ã£o da Causa Raiz**: O Claude seleciona a causa raiz mais provÃ¡vel das previsÃµes restantes e fornece uma explicaÃ§Ã£o detalhada de por que ela Ã© a culpada.
6. **InstruÃ§Ãµes de DepuraÃ§Ã£o**: O Claude gera instruÃ§Ãµes claras e acionÃ¡veis passo a passo para resolver o problema identificado.

Esta abordagem estruturada garante que o Claude siga um processo de depuraÃ§Ã£o lÃ³gico e sistemÃ¡tico, levando a uma resoluÃ§Ã£o de erros precisa e eficiente.

## IntegraÃ§Ã£o e Fluxo de Trabalho

O Prompt Definitivo de DepuraÃ§Ã£o para Claude pode ser integrado perfeitamente ao seu fluxo de trabalho de desenvolvimento existente. Aqui estÃ£o algumas dicas para uma integraÃ§Ã£o eficaz:

1. **Controle de VersÃ£o**: Certifique-se de que os arquivos do seu projeto estejam versionados corretamente usando um sistema de controle de versÃ£o como o Git. Isso permite que vocÃª anexe facilmente os arquivos relevantes ao prompt de depuraÃ§Ã£o.
2. **IntegraÃ§Ã£o ContÃ­nua**: Incorpore o prompt de depuraÃ§Ã£o no seu pipeline de integraÃ§Ã£o contÃ­nua (CI). Acione automaticamente o prompt quando uma compilaÃ§Ã£o falhar ou quando padrÃµes de erro especÃ­ficos forem detectados.
3. **Rastreamento de Problemas**: Use o prompt de depuraÃ§Ã£o em conjunto com seu sistema de rastreamento de problemas. Anexe a saÃ­da do prompt, incluindo o raciocÃ­nio passo a passo e as instruÃ§Ãµes de depuraÃ§Ã£o, ao problema relevante para fÃ¡cil referÃªncia e colaboraÃ§Ã£o.
4. **RevisÃ£o de CÃ³digo**: Utilize o prompt de depuraÃ§Ã£o durante as revisÃµes de cÃ³digo. Anexe o prompt Ã  solicitaÃ§Ã£o de revisÃ£o e use a anÃ¡lise do Claude para facilitar discussÃµes e identificar problemas potenciais no inÃ­cio do processo de desenvolvimento.

Lembre-se de adaptar a abordagem de integraÃ§Ã£o com base no seu ambiente de desenvolvimento especÃ­fico, ferramentas e prÃ¡ticas da equipe.

## PersonalizaÃ§Ã£o e Extensibilidade

O Prompt Definitivo de DepuraÃ§Ã£o para Claude foi projetado para ser personalizÃ¡vel e extensÃ­vel para atender Ã s suas necessidades especÃ­ficas. Considere as seguintes opÃ§Ãµes de personalizaÃ§Ã£o:

1. **ModificaÃ§Ãµes de VariÃ¡veis**: Ajuste as variÃ¡veis predefinidas para melhor alinhar com a terminologia do seu projeto ou adicione novas variÃ¡veis para capturar informaÃ§Ãµes adicionais de depuraÃ§Ã£o.
2. **Estrutura do Prompt**: Modifique a estrutura do prompt para enfatizar aspectos especÃ­ficos do processo de depuraÃ§Ã£o ou para incorporar etapas de anÃ¡lise adicionais.
3. **AdaptaÃ§Ã£o de Linguagem**: Adapte o prompt para trabalhar com diferentes linguagens de programaÃ§Ã£o, modificando o formato do bloco de cÃ³digo e fornecendo exemplos especÃ­ficos da linguagem.
4. **IntegraÃ§Ã£o com Outras Ferramentas**: Estenda o prompt para integrar com outras ferramentas de depuraÃ§Ã£o ou anÃ¡lise, como linters, profilers ou frameworks de teste.

Sinta-se Ã  vontade para experimentar com o prompt e compartilhar suas modificaÃ§Ãµes ou melhorias com a comunidade. Juntos, podemos aprimorar continuamente a experiÃªncia de depuraÃ§Ã£o com o Claude.


## ConclusÃ£o

O Prompt Definitivo de DepuraÃ§Ã£o para Claude Ã© uma ferramenta poderosa que aproveita as capacidades avanÃ§adas de compreensÃ£o de linguagem e raciocÃ­nio do Claude para revolucionar seu fluxo de trabalho de depuraÃ§Ã£o. Seguindo a abordagem estruturada e utilizando as opÃ§Ãµes de personalizaÃ§Ã£o, vocÃª pode identificar e resolver erros rapidamente, economizando um tempo de desenvolvimento valioso.

Encorajamos vocÃª a experimentar o Prompt Definitivo de DepuraÃ§Ã£o para Claude e vivenciar os benefÃ­cios em primeira mÃ£o. Se vocÃª tiver dÃºvidas, sugestÃµes ou feedback, por favor nÃ£o hesite em entrar em contato. Sua opiniÃ£o Ã© valiosa para moldar o futuro desta soluÃ§Ã£o de depuraÃ§Ã£o.

Boa depuraÃ§Ã£o com o Claude!

---

Projeto adaptado da comunidade INEMA TDS - Marca Arckhe