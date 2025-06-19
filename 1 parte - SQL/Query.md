# Visualizzare l'elenco dei comuni che hanno installato almeno un autovelox per la provincia di Teramo

```
Select c.Denomminazione as Comune, m.*
from Mappa m
inner join Comune c on c.IdComune = m.IdComune
inner join Provincia p on p.Id = c.IdProvincia
where p.Denominazione = 'Teramo'
```

---

# Visualizzare l'anno di installazione e il numero di comuni che hanno installato autovelox

```
Select m.AnnoInserimento as Anno, Count(*) as 'Numero Autovelox'
from Mappa m
group by m.AnnoInserimento
order by Anno
```