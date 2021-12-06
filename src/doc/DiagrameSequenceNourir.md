@startuml

Joueur -> GestionZooNourir: demandeAficherListeAnimal
GestionZooNourir --> Joueur : ListeAnimal
Joueur -> GestionZooNourir: ChoisitAnimalNourir
GestionZooNourir ->  GestionZooNourir: VerificationSiEstvivantAnimal
GestionZooNourir -->  Joueur: demandeInformationAnimal
Joueur -> GestionZooNourir: sasitInformationAnimalChoisit
GestionZooNourir ->  GestionZooNourir: EnregistreAnimalNourrit

Joueur -> GestionZooNourir: demandeListeAnimalActuel

GestionZooNourir -->  Joueur: afficheListe

	
	
	

@enduml