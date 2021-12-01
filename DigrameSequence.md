@startuml




  Joueur -> GestionZoo : DeamndeAfficherListeAnimaux
  GestionZoo -->  Joueur : AffichagelisteAnimaux
  Joueur -> GestionZoo : ChoixAnimalNourir
   GestionZoo -->   GestionZoo : VerificationAnimalEstPresent
   GestionZoo -->  Joueur : InformationanimalChoisit
   Joueur -> GestionZoo : NourirAnimal
   GestionZoo -->  GestionZoo : EnregistrementAnimaux
   Joueur -> GestionZoo : DemandeEtatactuelAnimaux
    GestionZoo -->  Joueur : AfficherListeAnimauxActuel
  
  
  
  


@enduml