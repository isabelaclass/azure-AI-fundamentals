# Reconhecimento Facial e transformação de imagens em Dados no Azure ML
- Análise de imagem 4.0 com o AI Vision Service
    - Os recursos incluem: personalização do modelo, ler textos de imagens, detecte pessoas em imagens, detecte pessoas em imagens, gerar legendas de imagens, detectar objetos, marcar recursos visuais e corte inteligente.
    - Detectando rostos com o Face Service
      
        - Qualquer pessoa pode usar o serviço Face para detectar:
            - Desfoque: quão desfocado está o rosto
            - Exposição: aspectos como ruído (refere-se ao ruído visual na imagem)
            - Óculos: se a pessoa estiver usando óculos
            - Pose da cabeça: a orientação do rosto em um espaço 3D
            - Ruído: refere-se ao ruído visual da imagem
            - Oclusão: determina se pode haver objetos bloqueando o rosto na imagem
              
        - Somente clientes gerenciados da Microsoft podem acessar recursos de reconhecimento facial:
            - Correspondência de similaridade
            - Verificação de identidade
              
    - Lendo texto com reconhecimento óptico de caracteres (OCR)
        - Detectar a localização do texto:
            - Impresso
            - Escrito à mão
        - Opções para extração rápida de texto de imagens ou análise assíncrona de documentos digitalizados maiores
          
- Configurando o serviço
    - Portal do Azure → criar recursos → Azure AI Service → Create → Configurar informações de forma similar ao ML
    - Portal Vision Cognitive do Azure → View all resources → Selecionar o que criou agora → Selecionar como default
    - Face → Detect faces in an image → Selecionar “Try it out” → Next steps
      
- Análise de documentos
    - Optical character recognition → Extract text from images → Seleciona “try it out”→ Next Steps
      
- Análise de imagem
    - Image analysis → Add captions to images → Selecionar “try it out” → Next steps
