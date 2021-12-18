@startuml

class Zoo{
- nom : String
+ afficher()
+ nourrir() : void
}

class Cage{
- ouvert : boolean
- numCage : int
+ nourrir()
}

class Animal{
- nom : String
- age : int
- poids : double
- limitePOIDS : double
+ manger()
+ viellir()
}

class Jeu{}

class Visiteur{
+ entrer()
}

class Lion{}

class Singe{}

class Tigre{}

class Zebre{}

Animal <|-- Lion
Animal <|-- Singe
Animal <|-- Tigre
Animal <|-- Zebre



Zoo o-- "1" Cage : - lesCages 
left to right direction
Zoo o-- "1" Animal : - lesAnimaux
Jeu *-- Zoo  : - leZoo
Cage --> "1"Animal : occupant
Zoo o-- Visiteur : - lesVisteurs
@enduml