```mermaid
erDiagram
    PERSONATGE {
        string Dni PK
        string Nom
        string Cognoms
    }
    
    Item {
        string Codi 
        string Nom 
        string equipable
        string Comerciable
        string tipus
        float pes
        int qualitat
        int mesures
    }
    
    Habilitat {
        string Codi PK, FK
        string Nom
        float Cost
        string Dany
        string Cooldown
        string tipus
    }

    Mascota {
        string Num_Chip
        string Nom
        String Motxila
    }

    Enemic {
        string codi
        string Nom
        string tipus
        string nivell
        string vida 
        string força
        string agilitat 
        string carisma 
    }

    PERSONATGE ||--|| Item : "és I/I"
    PERSONATGE ||--|| Habilitat : "és I/I"
    PERSONATGE ||--|| Mascota : "és un/I"
    PERSONATGE ||--|| Enemic : "és I/I"
