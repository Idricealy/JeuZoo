@startuml

class IUJeuZoo{
	- nbEtape : int  
	+ nourrir()
	+ etapeSuivante()
	+ getNbEtape() : int
}

class CTRLJeuZoo{
	- lesAnimaux : ArrayList<Animal>
	- lesVisisteurs : Visiteur
	+ nourrir()
}

class Zoo{
	- nom : String
	+ getNom()
}

class Animal{
	- nom : String
	- age : int
	- poids : double
	+ getCaracteristique() : String
	+ getNom() : String
	+ getAge() : int
	+ getPoids() : double
	+ estVieux() : boolean
	+ estMaigre() : boolean
}

class Visiteur{
	- static int compteurVisiteur
	+ getCompteurVisiteur()
}


IUJeuZoo " 1 " -down-> " -CTRLJeuZoo " CTRLJeuZoo

CTRLJeuZoo " 1 " -up-> "-lesAnimaux"Animal

CTRLJeuZoo " 1 " -up-> "-lesVisiteurs" Visiteur

CTRLJeuZoo " 1 " o-- "- zoo "Zoo

@enduml