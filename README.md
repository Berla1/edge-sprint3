# Transmitindo dados entre dispositivos conectados 

<img src="https://miro.medium.com/v2/resize:fit:720/format:webp/1*J-xFM5IGIsRwBvpDXbqjJQ.png" alt="Logo formulaE" width = "1000"/>

## Descrição do projeto 

O projeto consiste em um servo motor que se movimenta de maneira independente e envia dados para um servidor externo, no caso desse projeto foi utilizado o Node-red para receber as informações de rotação do servo. Futuramente essa funcionalidade será implementada em um projeto de um carrinho de Formula E com ESP32.

## Requisitos

- Conexão WiFi
- Node-red
- Bibliotecas:
  - PubSubClient
  - WiFi
  - ESP32Servo
 
## Utilizando Node-red

<img src="https://cdn.xingosoftware.com/elektor/images/fetch/dpr_1,w_800,h_460,c_fit/https%3A%2F%2Fwww.elektormagazine.com%2Fassets%2Fupload%2Fimages%2F42%2F20200612144414_Node-Red-official-logo.png" alt="Logo formulaE" width = "1000"/>

1. Instale o Node.js através do link https://nodejs.org/pt
   
2. Com o Node instalado o comando `npm install -g --unsafe-perm node-red` pode ser utilizado no terminal para instalar o Node-red.
  
3. Se tudo ocorrer bem na instalação a saída esperada é algo similar a isso:
```
+ node-red@1.1.0
added 332 packages from 341 contributors in 18.494s
found 0 vulnerabilities
```
4. Com a instalação feita, o comando `node-red` deve ser ulitizado para rodar o servidor do Node-red, e se tudo ocorrer como esperado a saída esperada é algo similar a isso:
   ```
   Welcome to Node-RED
    ===================
    
    30 Jun 23:43:39 - [info] Node-RED version: v1.3.5
    30 Jun 23:43:39 - [info] Node.js  version: v14.7.2
    30 Jun 23:43:39 - [info] Darwin 19.6.0 x64 LE
    30 Jun 23:43:39 - [info] Loading palette nodes
    30 Jun 23:43:44 - [warn] rpi-gpio : Raspberry Pi specific node set inactive
    30 Jun 23:43:44 - [info] Settings file  : /Users/nol/.node-red/settings.js
    30 Jun 23:43:44 - [info] HTTP Static    : /Users/nol/node-red/web
    30 Jun 23:43:44 - [info] Context store  : 'default' [module=localfilesystem]
    30 Jun 23:43:44 - [info] User directory : /Users/nol/.node-red
    30 Jun 23:43:44 - [warn] Projects disabled : set editorTheme.projects.enabled=true to enable
    30 Jun 23:43:44 - [info] Creating new flows file : flows_noltop.json
    30 Jun 23:43:44 - [info] Starting flows
    30 Jun 23:43:44 - [info] Started flows
    30 Jun 23:43:44 - [info] Server now running at http://127.0.0.1:1880/red/
    ```
5. Agora você já pode acessar a aplicação através do endereço `http://127.0.0.1:1880/red/` no seu navegador.

## Utilizando simulação no Wokwi

A simulação pode ser acessada através do link: https://wokwi.com/projects/409891028149852161

Para rodar o projeto, basca clicar no botão de 'play' em verde na simulação do Wokwi, se tudo ocorrer bem as informações serão publicadas no tópico especificado e o servo irá se movimentar de maneira independente.

## Conexão entre Wokwi e Node-red



