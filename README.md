# zabbix

## Altera e Insere IP server e Hostmetadata

## Variaveis usadas

| Nome | descrição | obrigatorio | default |
|------|-----------|-------------|---------|
|ipserverused| IP do zabbix-server/proxy já utilizado|yes|127.0.0.1|
|ipserver| IP do zabbix-server/proxy que irá adicionar|yes|[]|
|metadata| Hostmetadata para auto-registro|no|os-linux|

## Modo de Usar 

```
ansible-playbook -i hosts zabbix.yml --extra-vars="ipserverused=127.0.0.1 ipserver=127.0.0.1 metadata=os-linux" --ask-pass
```
## Caso queira adicionar mais de um ip faça

```
ansible-playbook -i hosts zabbix.yml --extra-vars="ipserverused=127.0.0.1 ipserver=127.0.0.1,127.0.0.2 metadata=os-linux" --ask-pass
```