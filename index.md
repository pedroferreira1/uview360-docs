Documentação UView360
=====================

Opções de configuração do JSON do player (uview.json)
-----

`loop`: Indica se o vídeo deve rodar em loop (recomeçar após o fim).

Uso:

```
loop: true
```

`hlsStream`: Link para o stream HLS, para o caso do vídeo ser live.

Uso:

```
hlsStream: "http://localhost:8080/"
```

`actualDelta`: Indica a posição de rotação inicial do vídeo.

Uso:

```
actualDelta: {
    x: 100,
    y: 0,
}
```

`directionMode`: Parâmetro para auxiliar escolher o `actualDelta`. É adicionado um botão para copiar as coordenadas atuais de X e Y para o clipboard, para ser usado no `actualDelta`. Para ter as coordenadas corretas a rotação deve ser feita utilizando o mouse.

Uso:

```
directionMode: true
```

`uViewLogo`: Caminho para uma imagem do logo da UView360 que irá aparecer ao longo do vídeo (na região de cima e da esquerda do player).

Uso:

```
uViewLogo: "images/uview_logo.png"
```

`uViewLogoMobile`: Caminho para uma imagem do logo da UView360 que irá aparecer ao longo do vídeo, quando visto de uma tela pequena (celular).

Uso:

```
uViewLogoMobile: "images/uview_logo_mobile.png"
```

`uViewLinkLogo`: Link que será acessado ao clicar no logo do UView360.

Uso:

```
uViewLinkLogo: "http://www.uview360.com.br/"
```

`logo`: Caminho para uma imagem do logo de quem está utilizando o player, que irá aparecer ao longo do vídeo (na região de cima e da direita do player).

Uso:

```
logo: "images/logo.png"
```

`logoMobile`: Caminho para uma imagem do logo de quem está utilizando o player, que irá aparecer ao longo do vídeo, quando visto de uma tela pequena (celular).

Uso:

```
logoMobile: "images/logo_mobile.png"
```

`linkLogo`: Link que será acessado ao clicar no logo.

Uso:

```
linkLogo: "http://www.google.com/"
```

`vrDelta`: Rotação inicial para quando está no modo VR.

Uso:

```
vrDelta: 30
```

`backButton`: Indica se deve ser adicionado um botão de 'Voltar' no player. No caso de uso em celular é bom para facilitar a navegação.

Uso:

```
backButton: false
```

`backLink`: Link para ser redirecionado no caso de clique no botão de 'Voltar'.

Uso:

```
backLink: "www.google.com/"
```

`name`: Nome do vídeo para agrupar as informações de analytics

Uso:

```
name: "Video 1"
```

`videoId`: Indicador único do vídeo para ser utilizado na captura de informações do heatmap e informações de analytics.

Uso:

```
videoId: 1
```

`fov`: Field of view inicial do vídeo. Indica o zoom inicial.

Uso:

```
fov: 90
```

`easeRotate`: Objeto que indica a velocidade de rotação do vídeo, para uma rotação suave no teclado

Uso:

```
easeRotate: {
    "keyboardSpeed": 120,
    "velocidadeInicio": 50,
    "velocidadeFim": 50
}
```

`projection`: Projeção do vídeo 360. No momento aceitamos apenas "equiretangular".

Uso:

```
projection: "equiretangular"
```

`spatialAudio`: Indica se o vídeo possui ou não áudio espacial.

Uso:

```
spatialAudio: false
```

`socketAnalytics`: Indica se devemos enviar informações de analytics do heatmap para algum servidor de websocket.

Uso:

```
socketAnalytics: false
```

`socketUrl`: A url do servidor de websocket que irá receber o analytics

Uso:

```
socketUrl: "http://localhost:3000/"
```

`ad`: Objeto para configurar propaganda antes do vídeo. O objeto possui 8 parâmetros:

    `on`: Indica se possui ou não algum vídeo de propaganda.
    `allowSkip`: Indica se pode ou não pular o vídeo de propaganda.
    `is360`: Indica se o vídeo de propaganda é 360.
    `video`: Link para o vídeo de propaganda.
    `audio`: Link para o áudio do vídeo de propaganda.
    `logo`: Link para o logo que irá aparecer nesse vídeo de propaganda.
    `logoMobile`: Link para o logo que irá aparecer nesse vídeo de propaganda, quando visto por telas menores (celular).
    `link`: Link que será direcionado ao clicar no logo.

Uso:

```
ad: {
    "on": true,
    "allowSkip": true,
    "is360": false,
    "video": "video.mp4",
    "audio": "audio.mp3",
    "logo": "",
    "logoMobile": "",
    "link": ""
}
```

`relatedVideos`: Lista de vídeos relacionados para ser apresentado ao final do vídeo. Cada elemento da lista possui 4 parâmetros.

    `image`: Imagem para aparecer nos vídeos relacionados.
    `link`: Link para ser direcionado ao clicar nesse vídeo relacionado.
    `title`: Título do vídeo.
    `time`: Tempo de duração do vídeo.

Uso:

```
relatedVideos: [
    {
        "image": "images/video_relacionado1.png",
        "link": "google.com/",
        "title": "Vídeo relacionado 1",
        "time": "01:33",
    },
    {
        "image": "images/video_relacionado2.png",
        "link": "google.com/",
        "title": "Vídeo relacionado 2",
        "time": "03:03",
    }
]
```

`cameraShare`: Adiciona um ícone para compartilhar uma imagem do vídeo nas redes sociais.

Uso:

```
cameraShare: false
```

`shareTitle`: Título default do compartilhamento da imagem.

Uso:

```
shareTitle: "Radical esse vídeo"
```

`shareDescription`: Descrição default do compartilhamento da image.

Uso:

```
shareDescription: "Muito interessante esse vídeo"
```

`shareLink`: Link default do compartilhamento da image.

Uso:

```
shareLink: "uview360.com.br"
```

`controlButtons`: Indica se o vídeo pode ser controlado por botões remotos, que se comunicam com o player por websocket.

    `on`: Indica se está ligado ou não.
    `socketUrl`: Url do websocket que irá se comunicar para enviar os comandos para movimentar o player.

Uso:

```
controlButtons: {
    "on": true,
    "socketUrl": "http://localhost:3000/"
}
```

`webrtc`: Indica se o link do vídeo é um webrtc.

Uso:

```
webrtc: false
```

`auth`: Indica se para acessar o vídeo é necessário autenticação. Por enquanto temos integração de possível autenticação com o sistema do Cadun.

Uso:

```
auth: false
```

`protectLink`: Indica se o link deve ser protegido para download a partir de um token de acesso, que vem da autenticação.

Uso:

```
protectLink: false
```

Opções de configuração do JSON de mídias do player (uview_media.json)
-----

`video4K`: Caminho para o vídeo na qualidade 4K.

Uso:

```
video4K: "4K.mp4"
```

`videoHQ`: Caminho para o vídeo na qualidade alta.

Uso:

```
videoHQ: "HQ.mp4"
```

`videoMQ`: Caminho para o vídeo na qualidade média.

Uso:

```
videoMQ: "MQ.mp4"
```

`videoLQ`: Caminho para o vídeo na qualidade baixa.

Uso:

```
videoLQ: "LQ.mp4"
```

`audio`: Caminho para o áudio do vídeo. Para versões de iOS menores que a 10 não conseguimos rodar o player inline. Por conta disso rodamos o vídeo e o áudio separadamente.

Uso:

```
audio: "audio.mp3"
```

`desktopDefault`: Caminho do vídeo padrão para iniciar, no caso de estar no desktop.

Uso:

```
desktopDefault: "HQ.mp4"
```

`mobileDefault`: Caminho do vídeo padrão para iniciar, no caso de estar no celular.

Uso:

```
mobileDefault: "MQ.mp4"
```
