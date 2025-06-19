# 📦 Backup e Ripristino del Database

Per effettuare il **ripristino** di un database:

1. Aprire SQL Server Management Studio (SSMS).
2. Fare clic con il tasto destro sulla voce `Database`.
3. Selezionare **Ripristina database...**.
4. Seguire la procedura guidata per caricare il file `.bak` del backup.

---

# ❌ Errore nella Creazione del Diagramma del Database

Se compare un errore durante la creazione del diagramma (es. "utente non è owner del database"), è necessario cambiare il proprietario del database.

Eseguire il seguente script SQL:

```sql
USE Autovelox;
GO
EXEC sp_changedbowner 'sa';
```

---

# Ci sarà da creare un utente nuovo e si puo o interfaccia o con script

# Su interfaccia

Tasto destro su sicurezza --> Nuovo --> Account di accesso --> crea nome utente e password

Per mappare i ruoli vedere immagine 1 , selezionare il db corrente e sotto mettere db_owner e lasciare flag public

---

# Con script 

```
USE Autovelox;
CREATE USER swd2325 FOR LOGIN swd2325;
ALTER ROLE db_owner ADD MEMBER swd2325;
```

# Fare prova per vedere se owner messo correttamente

```
USE Treni;
DROP USER swd2325;
```

se non esce niente significa che è configurato correttamente

