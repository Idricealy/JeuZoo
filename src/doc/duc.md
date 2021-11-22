@startuml
actor Joueur as j

left to right direction

package JeuZoo{
	usecase "Démarrer Jeu" as UC1
	usecase "Quitter Jeu" as UC2
	usecase "Gestion du Zoo" as UC3
}
j --> UC3
j --> UC1
j --> UC2
@enduml