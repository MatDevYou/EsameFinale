# Parte di SQL

Bisogna fare il backup di un suo db e per farlo bisogna 

Tasto destro su Database --> ripristina database

# Errore nel creare diagramma

Ci crea owner nuovo e ci permette di creare il diagramma

USE Autovelox;
GO
EXEC sp_changedbowner 'sa';

# Ci sarà da creare un utente nuovo e si puo o interfaccia o con script

# Su interfaccia

Tasto destro su sicurezza --> Nuovo --> Account di accesso --> crea nome utente e password

Per mappare i ruoli vedere immagine 1 , selezionare il db corrente e sotto mettere db_owner e lasciare flag public

# Con script 

USE Autovelox;
CREATE USER swd2325 FOR LOGIN swd2325;
ALTER ROLE db_owner ADD MEMBER swd2325;

# Fare prova

