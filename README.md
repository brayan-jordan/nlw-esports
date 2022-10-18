# nlw-esports
Projeto completo, desenvolvido uma API em NodeJS, utilizando Prisma + Sqlite para persistir os dados e também um projeto front-end em ReactJS para consumir os end-points da api

-- TODO: como startar os projetos...

## front-end screen's:

![home screen](https://github.com/brayan-jordan/nlw-esports/blob/master/screenshots/home.PNG)

![create ad modal](https://github.com/brayan-jordan/nlw-esports/blob/master/screenshots/create_ad.PNG)

## api routes:

- (GET) localhost:3333/games - listar os games:

exemplo de retorno da consulta:
[
	{
		"id": "fecc3dc1-b0e5-41b9-8ce2-bd0635476071",
		"title": "League of Leagends",
		"bannerUrl": "https://static-cdn.jtvnw.net/ttv-boxart/21779-285x380.jpg",
		"_count": {
			"ads": 1
		}
	},
]

- (GET) localhost:3333/games/:gameId/ads - listar os anúncios de um game

exemplo de retorno da consulta:
[
	{
		"id": "86517081-34e4-42a9-99c3-76be716ecf72",
		"name": "Brendin",
		"weekDays": [
			"0",
			"5",
			"6"
		],
		"useVoiceChannel": false,
		"yearsPlaying": 1,
		"hourStart": "18:00",
		"hourEnd": "22:00"
	}
]

- (POST) localhost:3333/games/:gameId/ads - criar anúncio para um game

example payload:
{
	"name": "Brayan",
	"yearsPlaying": 1,
	"discord": "brayan#0000",
	"weekDays": [0,5,6],
	"hourStart": "18:00",
	"hourEnd": "22:00",
	"useVoiceChannel": false
}
