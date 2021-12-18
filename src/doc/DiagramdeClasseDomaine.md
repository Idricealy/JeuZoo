@startuml

class Zoo {
-Nom : String 
-<ArrayList> Animal lesAnimaux


}
abstract class Animal{
-Nom : String 
-Age : int 
-Poids : double
-{static} nbr_Animal : int
-<ArrayList> Cage lesCages
+manger()
+viellir()
}
Class Joueur{    
-Nom : String 
-Age : int 
-sexe : String
+nourrir()
+rentrer()
}
class Jeu{
}
class Cage{
-{static} nbr_Cage : int 
} 
class Visiteur{
-String Nom
}
class Lion{

}
class Singe{

}
class Tigre{

}
class Zebre{

}

Animal <|-- Lion
Animal <|-- Singe
Animal <|-- Tigre
Animal <|-- Zebre
Zoo "1..1" o-- "1..n" Animal

Animal "1..1" o-- "1..1" Cage

Joueur "1..1" -- "0..*" Visiteur
Joueur "1..1" -- "1..*" Zoo

Animal "1..*" -- "1..1" Jeu

@enduml

class Zoo
@endmul
