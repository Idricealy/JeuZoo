@startuml

Joueur -> IUJeuZoo : nourrir()
activate IUJeuZoo

IUJeuZoo -> CTRLJeuZoo : nourrir()
activate CTRLJeuZoo
CTRLJeuZoo -> Zoo : nourrir()
activate Zoo
create Animal
CTRLJeuZoo -> Animal
activate Animal
CTRLJeuZoo --> Animal : getCaracteristique()
Animal --> CTRLJeuZoo : caracteristique
CTRLJeuZoo --> IUJeuZoo : caracteristique


activate Animal
Animal -> Animal : manger()


Joueur -> IUJeuZoo : faireEntrerVisiteur()
activate IUJeuZoo

IUJeuZoo -> CTRLJeuZoo : faireEntrerVisiteur()
activate CTRLJeuZoo 


IUJeuZoo -> IUJeuZoo : afficherZoo()
activate IUJeuZoo


@enduml