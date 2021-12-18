@startuml

class IUJeuZoo{
	+ nourrir()
}

class Zoo{
	- nom : String
	+ nourrir()
	+ getNom()
}

class Animal{
	- nom : String
	- age : int
	- poids : double
	+ manger()
}

class CTRLJeuZoo {
	+nourrir()
}
IUJeuZoo " 1 " -down-> " -CTRLJeuZoo " CTRLJeuZoo
CTRLJeuZoo " 1 " -up-> "-lesAnimaux"Animal
CTRLJeuZoo " 1 " o-- "- zoo "Zoo
@enduml