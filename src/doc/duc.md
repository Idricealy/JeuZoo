@startuml
actor Joueur as j
left to right direction

package JeuZoo{
	usecase "Démarrer Jeu" as UC1
	usecase "Quitter Jeu" as UC2
}

j --> UC1
j --> UC2
@enduml