# GUIDb

Creare Cartella di Destinazione del Progetto

Creare Progetto MAUI nella cartella desiderata

Eseguire la linea di comando " dotnet add package sqlite-net-pcl " per installare il pacchetto di SQLite

Includere la libreria di SQLite usando "using SQLite" nel codice

SQLite.SQLiteOpenFlags Flags = SQLite.SQLiteOpenFlags.ReadWrite | SQLite.SQLiteOpenFlags.SharedCache;

Codice per puntare la directory : 

if (!File.Exists(targetFile))

se il file non esiste l'if viene ignorato altrimenti viene eseguito il seguente codice : 

 {
 
            using (Stream fileStream = await FileSystem.Current.OpenAppPackageFileAsync("chinook.db"))
            
            {
            
                using (MemoryStream memoryStream = new MemoryStream())
                
                {
                
                    fileStream.CopyTo(memoryStream);
                    
                    File.WriteAllBytes(targetFile, memoryStream.ToArray());
                    
                }
                
            }
            
        }
        

Database di Riferimento : https://www.sqlitetutorial.net/wp-content/uploads/2018/03/chinook.zip
