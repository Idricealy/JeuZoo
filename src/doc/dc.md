@startuml

class Zoo {
-String Nom
-<ArrayList> Animal lesAnimaux
-<ArrayList> Cage lesCages

}
abstract class Animal{
-String Nom
-int Age
-double Poids
-{static} int nbr_Animal
+manger()
+viellir()
}
Class Joueur{    
-String Nom
nourrir()
rentrer()
}
class Jeu{
}
class Cage{
-{static} int nbr_Cage
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
Joueur -- Animal
Joueur -- Visiteur
joueur "1..1" -- "0..*" Visiteur


class Zoo
@endmul
