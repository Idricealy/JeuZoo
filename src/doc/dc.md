@startuml
left 
class Zoo {
-Nom : String 
-<ArrayList> Animal lesAnimaux
-<ArrayList> Cage lesCages

}
abstract class Animal{
-Nom : String 
-Age : int 
-Poids : double
-{static} nbr_Animal : int
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
Zoo o-- Animal
Joueur -- Jeu
Zoo o-- Cage

Joueur "1..1" -- "0..*" Visiteur
Joueur "1..1" -- "0..*" Animal
@enduml

class Zoo
@endmul
