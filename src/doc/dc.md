@startuml

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

<<<<<<< HEAD

=======
Joueur "1..1" -- "0..*" Visiteur
Joueur "1..1" -- "0..*" Animal
@enduml
=======
>>>>>>> branch 'master' of https://github.com/Idricealy/JeuZoo.git
class Zoo
@endmul
