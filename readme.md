PASSO A PASSO DO PROJETO BARCOS(ATÉ AGORA):

instalação do YOLO:
pip install ultralytics

baixei os datasets de imagems no roboflow separados em:
    lixo na água(1k)
    agua limpa(se não o modelo vai achar que a água é suja)(2k)
    troncos(2k)
    
manipulei o dataset pra judar todos os modelos gerados em:train, valid e test em cada imagem.

Reduzi o número de imagems dos troncos em inferência(pois no dataset original tinha 10mil reduzi em 2mil)
Configurei o arquivo data.yaml do train para:
    train: train/images
    val: valid/images
    test: test/images

    nc: 1
    names: ['0']
Esse arquivo diz pro yolo onde estão as imagem, quantas classes existem e os nomes das classes.

Criação do script de treino:
    Modelo yolo26n
    Vai fazer o treinamento em 50 epocas
    passei o dataset


