## Per la parte di docker bisognà usare docker swarm e creare tramite compose un esposizione a nginx e treafik

---

## Creare cartella Lanciare il comando 

```
docker swarm init
```

---

## Una volta lanciato possiamo creare il file docker-compose.yaml e avviarlo ricordarsi di creare network (overlay) per far comunicare i due container e nel compose specificarlo:

```
docker network create --driver=overlay web
```

---

## una volta creata la network startiamo il compose cosi:

```
docker stack deploy -c docker-compose.yaml webstack
```