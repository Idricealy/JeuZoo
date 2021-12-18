@startuml

GestionZooNourir--> Joueur: ProposeNourirAnimal
Joueur -> GestionZooNourir : NourirAnimal

GestionZooNourir ->  GestionZooNourir: VerificationSiEstvivantAnimal

GestionZooNourir ->  GestionZooNourir: EnregistreAnimalNourrit

Joueur -> GestionZooNourir: demandeListeInformationAnimal

GestionZooNourir -->  Joueur: afficheListeAnimaux

	
	
	

@enduml