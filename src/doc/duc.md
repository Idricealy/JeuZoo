@startuml
actor Joueur as j
actor "Administrateur Jeu" as aj
left to right direction

package JeuZoo{
	usecase "Démarrer Jeu" as UC1
	usecase "Quitter Jeu" as UC2
	usecase "Gestion du Zoo" as UC3
	usecase "Initialiser Jeu" as UC4
}
j --> UC3
j --> UC1
j --> UC2
aj --> UC4
@enduml