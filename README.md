---
title: 'MusiKing - Bot de áudio totalmente Open Source'
---

MusiKing
===

## Tabela de Conteúdos

1. [Comandos do Bot](#comandos-do-Bot)
2. [Build](#build)
3. [FAQ](#faq)
4. [ToDo](#todo)

## Comandos do Bot

Abaixo seguem todos os comandos possíveis do bot.

* ```-connect```
    Permite a conexão do bot, pura e simplesmente.
* ```-disconnect```
    Desconecta o bot do canal de voz atual
* ```-equalizer [subcommands]``` ou ```-eq [subcommands]```
    Equalizador para as faixas da fila atual.
    Subcomandos:
    - ```flat``` ```boost``` ```metal``` ```piano```
* ```-lyrics [music]``` ou ```-letras [music]``` ou ```-l [music]```
    Letras da música que deve ser passada como parâmetro. Caso a letra não seja encontrada na API, será enviado um match mais próximo ao digitado pelo usuário.
* ```-next``` ou ```-skip``` ou ```-n```
    Passa para a próxima faixa.
* ```-previous``` ou ```-prev```
    Volta para a faixa anterior
* ```-play [optional: music]``` ou ```-p [optional: music]```
    Caso seja executado passando uma música como parâmetro, então dará a opção do usuário escolher a música, caso seja sem nenhum parâmetro, ele volta a tocar a música, caso esteja pausada.
* ```-pause```
    Pausa a música atual.
* ```-playing``` ou ```-now-playing``` ou ```-np```
    Mostra a música atual sendo tocada.
* ```-next``` ou ```-n```
    Passa para a próxima música, caso tenha alguma tocando no momento.
* ```-previous``` ou ```-p```
    Volta para a música que estava tocando anteriormente.
* ```-queue``` ou ```-fila``` ou ```-q```
    Mostra a fila atual de faixas sendo tocadas com dados detalhados para cada uma
* ```-repeat [subcommand]```
    Repete a música atual dado o subcomando passado como parâmetro.
    Subcomandos:
    - ```none``` Desativa a repetição automática
    - ```1``` Ativa a repetição e aplica apenas para a faixa atual
    - ```all``` Ativa a repetição para todas as faixas
* ```-restart```
    Reinicia a faixa do zero.
* ```-shuffle```
    Embaralha as faixas da fila.
* ```-skipto``` ou ```-playindex```
    Pula para posição específica da fila.
* ```-stop```
    Para todas as faixas e esvazia a fila.
* ```-volume [%]```
    Opção de alterar o volume atual da faixa, os valores podem variar de 0 a 150. Caso hajam valores diferentes desses, será mostrado um erro.
* ```-help```
    Mostra os comandos gerais para o bot, contendo esses comandos comentados acima.

## Build
- Necessário possuir Python na versão 3.6.0 ou superior;
- discord.py 1.5.0 ou superior ```pip install discord```
- wavelink 0.9.0 ou superior ```pip install wavelink```
- OpenJDK 13.0.2
- [Lavalink](https://ci.fredboat.com/viewLog.html?buildId=lastSuccessful&buildTypeId=Lavalink_Build&tab=artifacts&guest=1) (Versão mais recente)
É necessário inserir o arquivo baixado do Lavalink dentro do diretório bin do OpenJDK.
- Arquivo de configuração yaml (a base pode ser encontrada no diretório config, desse mesmo repositório, só fazer as alterações necessárias, caso queira);
- Criar arquivo token.0 ou conforme especificar no arquivo bot.py do seu código. Nesse arquivo é necessário ter o Token do seu bot, mas cuidado para que não vase de forma alguma, pois isso pode ser perigoso.
- Depois disso, é necessário que o Lavalink esteja sendo executado, já que ele é o responsável por fazer o player funcionar corretamente, para isso basta apenas rodar o comando:
```java -jar <arquivo_Lavalink.jar>```


## FAQ

**Quer contribuir adicionando funcionalidades ou sugerindo novas funcionalidades para o repositório?** Deixa um comentário ou faça um pull request com as mudanças!<br/>
Qualquer dúvidas, estou à disposição.


## ToDo:
1. Integrar com Spotify;
2. Melhorar documentação interna do bot no discord;
3. Melhorar mensagens de erro ao executar comando errado;
4. Implementar testes;
5. ~~Criar um ícone legal;~~
6. (Caso Possível) Testar métodos de integração com API do radiooooo.com.

###### tags: `Discord` `Documentation` `MusiKing` `Audio`
