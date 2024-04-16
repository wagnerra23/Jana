# Resposta de Anotação

## Resposta de Anotação

### Visão geral do Recurso <a href="#feature-overview" id="feature-overview"></a>

O recurso Resposta de Anotação oferece respostas personalizadas e de alta qualidade para várias aplicações, obtidas por meio de anotação manual.

**Principais Usos:**

1. **Respostas Especializadas para Setores Específicos:** Isto é particularmente valioso no serviço ao cliente ou bases de conhecimento dentro de negócios, governo, etc. Ele permite respostas precisas a perguntas específicas, anotando respostas, como definir "notações padrão" para alguns ou marcar outros como "inrespondíveis."
2. **Adaptação Rápida para Protótipos:** Utilizar a Resposta de Anotação pode melhorar significativamente a qualidade da resposta no rápido desenvolvimento de produtos protótipos, aumentando a satisfação do cliente.

**Como Funciona:**

O recurso fornece um sistema alternativo para melhorar a recuperação, ignorando a fase de geração de Grandes Modelos de Linguagem (LLMs) e evitando as complicações da Geração Aumentada por Recuperação (RAG).

1. Uma vez ativado, você pode anotar as respostas de diálogo LLM. As anotações podem ser respostas de alta qualidade tiradas diretamente do LLM ou suas próprias anotações editadas. Esses conteúdos anotados são salvos para uso futuro.
2. Quando perguntas semelhantes são feitas novamente, o sistema identifica as perguntas anotadas correspondentes.
3. Se uma correspondência for encontrada, a resposta anotada será retornada diretamente, ignorando os processos LLM ou RAG.
4. Sem uma correspondência, a consulta segue o processo LLM ou RAG padrão.
5. Desativar a Resposta de Anotação cessa as respostas correspondentes das anotações.

![](https://wr2.gitbook.io/\~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-090c7766acfb0ee3a498fc8eff83b825f6e678a0%252Fimage%2520%283%29%2520%281%29%2520%281%29.png%3Falt=media\&width=768\&dpr=4\&quality=100\&sign=c51fafb5e7a36f532d14d651656f092e43c4fc9b6186185815de8f18df29242c)Processo de Resposta de Anotação

### Ativação <a href="#activation" id="activation"></a>

Navegue até “Build Apps -> Adicione Feature” para ativar a funcionalidade Resposta de Anotação.

![](https://wr2.gitbook.io/\~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-1acdf479c10bf16e60204dcd0b72396ef7f38e07%252Fscreenshot-20231218-172146%2520%281%29.png%3Falt=media\&width=768\&dpr=4\&quality=100\&sign=e79ee2e46a31c2b92fbfb2d1d6de2cdefe6c86852078da5d964682bd3a53184b)

Start by setting the parameters for Annotation Reply. These include the Score threshold and the Embedding model.

* **Score Threshold:** Sets the minimum similarity score for an annotation to be considered a match and recalled.
* **Embedding Model:** Used for converting annotated text into vectors. Changing the model leads to re-creation of embeddings.

Select 'Save' for immediate application of these settings. The system then creates and stores embeddings for all existing annotations.

![](https://wr2.gitbook.io/\~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-a6c6a10495f0dc2bd1392f1f127f337c8ffca540%252Fscreenshot-20231218-172302.png%3Falt=media\&width=768\&dpr=4\&quality=100\&sign=2cae6dc2c2c69592d3df12d3a2ad85c1828320b770fc7c33851b3cf135d1e810)

### Adding Annotations in Debug Mode <a href="#adding-annotations-in-debug-mode" id="adding-annotations-in-debug-mode"></a>

Annotations can be added or modified directly on the model's replies within the debug and preview interface.

![](https://wr2.gitbook.io/\~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-20d25b53b0a90cdb84002f2e7b02b6769688313f%252Fscreenshot-20231218-175934.png%3Falt=media\&width=768\&dpr=4\&quality=100\&sign=a315aaf026415af0355d64882cc08b56e7233e69b35788d75c0756a53725caea)

Edit and save these replies to ensure high quality.

![](https://wr2.gitbook.io/\~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-3cc1a782ceb6f9d02c18586cc39010629e398389%252Fscreenshot-20231218-180013.png%3Falt=media\&width=768\&dpr=4\&quality=100\&sign=d6accbe2ac2753f1bc077bbd19358e67ee13b7cc0b1b185313bef5c8b7b04c49)

When a user repeats a query, the system uses the relevant saved annotation for a direct reply.

![](https://wr2.gitbook.io/\~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-7a20541c2033ba15f2023d907edf35e04642ce9d%252Fscreenshot-20231218-180135.png%3Falt=media\&width=768\&dpr=4\&quality=100\&sign=156f58bba7c25ef8651d78adfff74fa00a8991a624621898c3c560802a24e21c)

### Enabling Annotations in System Logs <a href="#enabling-annotations-in-system-logs" id="enabling-annotations-in-system-logs"></a>

Ative a funcionalidade Resposta à Anotação em “Build Apps -> Logs e Anotações -> Annotations.”

![](https://wr2.gitbook.io/\~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-9dea8d9aa6119333f8d773fcffb601dcb0e63477%252Fscreenshot-20231218-180233.png%3Falt=media\&width=768\&dpr=4\&quality=100\&sign=954320cd9a728d45413a4e1a1a6f96ec3fc253fb96392bc8e87765cce917b139)

### Ajustando Parâmetros de Backend para Anotações <a href="#adjusting-backend-parameters-for-annotations" id="adjusting-backend-parameters-for-annotations"></a>

**Configurações do Parâmetro:** Estes incluem o limiar de Pontuação e o modelo de Incorporação, assim como na configuração inicial.

![](https://wr2.gitbook.io/\~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-1e5fb4a5dba3b4d0b695010729a90fb680224b77%252Fscreenshot-20231218-180337.png%3Falt=media\&width=768\&dpr=4\&quality=100\&sign=3258199604d21e17001023fff07283325db16f25aaf71f2e0631889643b5af62)

### Importação em massa de Q\&As Anotados <a href="#bulk-importing-annotated-q-and-as" id="bulk-importing-annotated-q-and-as"></a>

**Processo de Importação:** Use o modelo fornecido para formatar pares de perguntas e respostas para anotações e, em seguida, faça o upload em massa.

![](https://wr2.gitbook.io/\~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-2f92e8e5fa2bcde93a10aff80f46e715d5705a08%252Fscreenshot-20231218-180508.png%3Falt=media\&width=768\&dpr=4\&quality=100\&sign=14c9f4657edb311c5fdaeb3151ace1bdee6d41eaefc451019d8edc6b102bffb4)

### Exportação em massa Q\&As Anotados <a href="#bulk-exporting-annotated-q-and-as" id="bulk-exporting-annotated-q-and-as"></a>

**Função de Exportação:** Esse recurso permite uma exportação única de todos os pares de Q\&A anotados armazenados no sistema.

![](https://wr2.gitbook.io/\~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-7c98a2cedb8b78f44f7fe40184f1278f81fa8d02%252Fscreenshot-20231218-180611.png%3Falt=media\&width=768\&dpr=4\&quality=100\&sign=1ae18228915c16619a8d3fb9eb6a3f88855b1986b6c10e4bf237c095c5aa6193)

### Revisando a Anotação Hit History <a href="#reviewing-annotation-hit-history" id="reviewing-annotation-hit-history"></a>

Veja o histórico de uso de cada anotação, incluindo edições, consultas, respostas, fontes, pontuações de similaridade e registros de data e hora. Essas informações são valiosas para melhorias contínuas em suas anotações.

![](https://wr2.gitbook.io/\~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-3e50f8fbc032209f8bea66811b2be232f052f496%252Fscreenshot-20231218-180737.png%3Falt=media\&width=768\&dpr=4\&quality=100\&sign=441d944c68d4f64f273186f4f9f79d36113c2bdfadad995b865d46dcdb5c9429)
