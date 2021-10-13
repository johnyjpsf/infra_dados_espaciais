# infra_dados_espaciais

Infra para dados espaciais baseada em código livre(geoserver, geonetwork, postgresql e docker)

## Configuração

- Copie o arquivo *.env_sample* para um arquivo chamado *.env*
- Termine suas configurações no .env
- Desempacote o arquivo *docker-assets/geoserver/data-2.13.x.zip* no diretório *geoserver_data*
- Se precisar mude as permissões do diretório *geoserver_data/data* para dar permissão de leitura e escrita a todos

## Uso

Na primeira vez que for usar execute, na raiz do projeto, o comando

```bash
docker-compose build
```

Depois, para subir o ambiente, use

```bash
docker-compose up
```

Para conectar ao banco de dados localmente a partir do host use o ip *0.0.0.0*

Se for fazer a conexão no banco de dados entre containers, como no caso de consumir o banco a partir do geoserver, use o nome *postgis* no lugar do ip

O geoserver fica disponível em *http://{seu_ip}:{porta_geoserver}/geoserver* e o geonetwork em *http://{seu_ip}:{porta_geoserver}/geonetwork*, onde *porta_geoserver* e *porta_geoserver* são as configuradas no *.env*
