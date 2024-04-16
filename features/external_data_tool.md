# Ferramenta de Dados Externos

Anteriormente, [Importação de Conhecimento](https://wr2.gitbook.io/jana.ia/features/datasets) permitiu que os desenvolvedores enviassem diretamente textos longos em vários formatos e dados estruturados para criar conhecimento, permitindo que os aplicativos de IA conversassem com base no contexto mais recente carregado pelos usuários. Com essa atualização, a ferramenta de dados externos permite que os desenvolvedores usem seus próprios recursos de pesquisa ou dados externos, como bases de conhecimento internas, como o contexto para LLMs. Isso é conseguido estendendo APIs para buscar dados externos e incorporá-los em Prompts. Em comparação com o upload de conhecimento para a nuvem, o uso de ferramentas de dados externas oferece vantagens significativas para garantir a segurança de dados privados, personalizar pesquisas e obter dados em tempo real.

Quando os usuários finais fazem uma solicitação ao sistema de conversação, o backend da plataforma aciona a ferramenta de dados externos (ou seja, chamando sua própria API), que consulta informações externas relacionadas à pergunta do usuário, tais como perfis de funcionários, registros em tempo real, etc. A ferramenta então retorna através da API as porções relevantes para a solicitação atual. O backend da plataforma reunirá os resultados retornados em texto como contexto injetado no Prompt, a fim de produzir respostas mais personalizadas e atender às necessidades do usuário com mais precisão.

## O que faz? <a href="#what-does-it-do" id="what-does-it-do"></a>

### Início Rápido <a href="#quick-start" id="quick-start"></a>

1. Antes de usar a ferramenta de dados externos, você precisa preparar uma API e uma chave de API para autenticação. Ir para [External\_data\_tool](https://wr2.gitbook.io/jana.ia/features/extension/api\_based\_extension/external\_data\_tool).
2. O Dify oferece gerenciamento centralizado de API; Depois de adicionar configurações de extensão da API na interface de configurações, elas podem ser utilizadas diretamente em vários aplicativos no Dify.

\
Extensão baseada em API

<figure><img src="https://wr2.gitbook.io/~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-18f23579968e226a836a57992c4e239de7fc9ef8%252Fapi_based.png%3Falt=media&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=41f44a078485ed5116f5a3172cb35843319f4418c65a4a8c26fc2a0e8bdedc13" alt=""><figcaption></figcaption></figure>

1. Tomando "Query Weather" como exemplo, insira o nome, o terminal da API e a chave da API na caixa de diálogo "Adicionar nova extensão baseada em API. Depois de salvar, podemos ligar para a API.

Inquérito meteorológico

<figure><img src="https://wr2.gitbook.io/~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-cceb3fa857118c996aff59b2fd41245b4334e76f%252Fapi_based_extension.png%3Falt=media&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=1ae9493c23e2f23d44ffcbf5bc259f93e9c697ef199e319b8ff506e0751b5294" alt=""><figcaption></figcaption></figure>

1. Na página de orquestração rápida, clique no botão "+ Adicionar" à direita de "Ferramentas" e na caixa de diálogo "Adicionar ferramenta" que é aberta, preencha o nome e o nome da variável ( o nome da variável será referenciado no Prompt; portanto, use o inglês ) e selecione a extensão baseada em API adicionada na Etapa 2.

External\_data\_tool

<figure><img src="https://wr2.gitbook.io/~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-62eb07602185035e12d1e37633c6aefa12fa167c%252Fapi_based_extension1.png%3Falt=media&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=4ffc54296b0dcabc404bd875017e8490fe39986c2a16206e9c46ea36b2110dda" alt=""><figcaption></figcaption></figure>

1. Na caixa de orquestração de prompt, podemos montar os dados externos consultados no Prompt. Por exemplo, se quisermos consultar o clima de hoje em Londres, podemos adicionar uma variável chamada `location`, digite "London" e combine-o com o nome da variável de extensão da ferramenta de dados externos `weather_data`. A saída de depuração seria a seguinte:

Weather\_search\_tool

<figure><img src="https://wr2.gitbook.io/~gitbook/image?url=https:%2F%2F987453532-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252FW3pdVn6AztRtyAD0PGfj%252Fuploads%252Fgit-blob-dea5d9af7fd60ac4b7218fa0046fc5ae7aacbd8d%252FWeather_search_tool.jpeg%3Falt=media&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=68d648776af3fef40cadf8a4662dfcfe3151d322db5672dab3aa57b4edde6089" alt=""><figcaption></figcaption></figure>

No Prompt Log, também podemos ver os dados em tempo real retornados pela API:



<figure><img src="../.gitbook/assets/log.jpeg" alt="" width="335"><figcaption><p>Prompt Log</p></figcaption></figure>
