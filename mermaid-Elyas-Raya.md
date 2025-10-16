```mermaid
erDiagram
    PERSONATGE {
        string Dni PK
        string Nom
        string Cognom
        string vida
        string força
        string agilitat 
        string carisma 
    }

    Item {
        string Codi "not null"
        string Nom "not null"
        string equipable
        string Comerciable "not null"
        string tipus "not null"
        float pes "not null"
        int qualitat "not null"
        int mesures "not null"
    } 

    Habilitat {
        string Codi PK, FK "not null"
        string Nom "not null"
        float Cost
        string Dany
        string Cooldown
        string tipus "not null"
    }

    Mascota {
        string Num_Chip "not null"
        string Nom "not null"
        String Motxila
    }

    Enemic {
        string codi "not null"
        string Nom "not null"
        string tipus "not null"
        string nivell "not null"
        string vida 
        string força
        string agilitat 
        string carisma 
    }

    PERSONATGE ||--|{ Item : "equipa"  
    PERSONATGE ||--|{ Habilitat : "poseeix"
    PERSONATGE ||--|| Mascota : "acompaña"
    PERSONATGE ||--|{ Enemic : "enfrenta"

    Item |{--|| Mascota : "carrega"  
    Habilitat |{--|{ Enemic: "li dona poders"
