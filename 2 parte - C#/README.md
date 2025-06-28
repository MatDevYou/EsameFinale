# Collegare database 

su appsettings.json

"Server=.\\SQLEXPRESS;Database=Autovelox;User Id = sa; Password = Orbassano2003; MultipleActiveResultSets=true;TrustServerCertificate=True"

# Installare pacchetti 

Gestione pacchetti NuGet -> cerca quello che devi installare


su terminale per collegare db:

Scaffold-DbContext "Server=localhost\SQLEXPRESS;Database=BikeStores;Trusted_Connection=True;TrustServerCertificate=True;" Microsoft.EntityFrameworkCore.SqlServer -OutputDir Models

# Su program.cs 



# Quando dice crea un servizio intende di creare controller

Tasto destro su controller --> aggiungi --> controller --> controller MVC con visualizzazioni ecc --> scegliere la tabella che si vuole utilizzare

vedere immagine ![alt text](<funzione per vedere autovelox.png>)


