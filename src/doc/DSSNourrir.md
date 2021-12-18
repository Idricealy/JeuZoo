@startuml

JeuZoo --> Joueur : ProposeNourrirAnimaux
Joueur -> JeuZoo : ChoisiNourrirAnimaux
JeuZoo --> Animaux : NourritAnimaux
@enduml