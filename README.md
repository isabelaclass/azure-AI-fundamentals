# Azure AI fundamentals - Azure Machine Learning Service
Azure Machine Learning Service created by Azure AI Fundamentals training.

- Trabalhando com Machine Learning na prática no Azure ML
  
    - Fundamentos dos serviços de IA no Azure
        - Noções básicas do Azure
            - A plataforma de nuvem Azure da Microsoft oferece escalabilidade e confiabilidade: armazenamento de dados, computação e serviços.
              
        - Serviços de IA na Microsoft Azure
            - Aprendizado de máquina Azure: uma plataforma para treinar, implantar e gerenciar modelos de aprendizado de máquina.
            - Serviços de IA do Azure: um conjunto de serviços que abrange visão, fala, linguagem, decisão e IA generativa.
            - Pesquisa cognitiva do Azure: extração, enriquecimento e indexação de dados para pesquisa inteligente e mineração de conhecimento.
            - Recursos de aplicação de IA numa subscrição do Azure:
                - Recursos autônomos para serviços específicos.
                - Recurso geral de serviços de IA do Azure para vários serviços.
                  
            - Consumido por aplicativo via:
                - Um endpoint REST (https://endereço)
                - Uma chave de autenticação ou token de autorização
                  
    - Criando uma conta no Microsoft Azure
        - [Azure.microsoft.com](http://Azure.microsoft.com)
        - Conta experimental - cuidado para não cobrar
        - Machine Learning Studio
        - Os passos podem demorar, então é preciso ter paciência.
          
    - Acessando o serviço do Azure Machine-learning
        - Create a resource → Azure machine learning → Create
        - Subscription: minha conta
            - Resource group: create new → dar um nome (caixa para guardar os recursos)
              
        - Workspace details:
            - Name: nome do workspace (precisa ser exclusivo)
            - Region: East US
            - Storage account (caixa para guardar nosso HD): manter o padrão
            - Key vault (”chaveiro” de segredos, chaves, tokens, certificados): manter padrão
            - Application insight: manter padrão
            - Container registry: none (manter padrão)
              
        - Networking: questão de acesso
        - Encryption: encriptação das chaves
        - Identity: permissionamento
        - Tag: labels
        - Review + create → create
          
    - Configurando modelos e conjuntos de dados
        - Launch Studio → ml.azure.com
        - Ml automatizado → novo trabalho de ML automatizado
          
        - Configurações básicas
            - Nome de trabalho: manter padrão
            - Novo nome do experimento: manter padrão
            - Descrição: escrever para que a sua aplicação será utilizada
            - Marcadores: nenhum
              
        - Tipo de tarefa e dados
            - Selecionar tipo de tarefa: regressão (sugerido pelo Azure)
            - Selecionar os dados → criar
            - Nome: colocar nome que desejar
            - Descrição: descrever dados
            - Tipo: colocar tipo de dados
            - Fontes de dados: selecionar a fonte - > avançar
            - Formato do arquivo: delimitado
            - Delimitador: vírgula
            - Codificação: UTF-8
            - Cabeçalhos de coluna: Somente o primeiro arquivo têm cabeçalhos
            - Ignorar linhas: nenhuma
            - Conjunto de dados com dados de várias linhas: não precisa selecionar → avançar
            - Esquema: não selecionar nada e avançar
            - Examinar → criar
              
        - Configurações de tarefas
            - Coluna de destino: rentals (integer) - tipo de saída dos dados (nesse caso estamos fazendo uma automação para aluguel de bicicletas)
            - Configurações adicionais:
                - métrica primária: NormalizedRootMeanSquaredError
                - Desmarcar seleções
                - Modelos permitidos: RandomForest e LightGBM
                  
            - Limites:
                - Máximo de avaliações: 3
                - Máximo de avaliações simultâneas: 3
                - Máximo de nós: 3
                - Limite de pontuação de métrica: 0.085
                - Tempo limite do experimento (minutos): 15
                - Tempo limite de iteração (minutos): 15
                - Habilitar encerramento antecipado
                - Tipo de validação: divisão de validação de treinamento
                - Validação de percentual de dados: 10
                - Dados de teste: nenhum
                - Avançar
                  
        - Computação
            - Selecione o tipo de computação: Sem servidor
            - Tipo de máquina virtual: CPU
            - Tipo de máquina virtual: Dedicado
            - Tamanho da máquina virtual: Standard_DSE_v2 (4 núcleo(s), 14GB de RAM, 28GB de armazenamento, $0,29/hr)
            - Número de instâncias: 1
            - Avançar
        - Enviar trabalho de treinamento
          
    - Análise e teste do modelo
        - Tarefas (jobs): tarefas executadas pelo Azure
        - ML automatizado:
        - As vezes, no começo, os dados aparecem como não íntegros, mas depois volta ao normal
        - Modelos → informações úteis para ambiente de produção
        - Tarefas (jobs) → Métricas
        - Modelos → Pontos de extremidade
        - Pontos de extremidade → Testar
            - Adicionar código e testar
