@startuml

Joueur -> IUJeuZoo : nourrir()
activate IUJeuZoo


IUJeuZoo -> CTRLJeuZoo : nourrir()
deactivate IUJeuZoo
activate CTRLJeuZoo
CTRLJeuZoo -> Zoo : nourrir()

activate Zoo
deactivate Zoo


create Animal
CTRLJeuZoo -> Animal : << create >>
activate Animal
CTRLJeuZoo --> Animal : getCaracteristique()
Animal --> CTRLJeuZoo : caracteristique

deactivate CTRLJeuZoo


Animal -> Animal : manger()
deactivate Animal
Zoo -> Zoo : afficher()
activate Zoo
deactivate Zoo
Joueur -> IUJeuZoo : faireEntrerVisiteur()
activate IUJeuZoo

IUJeuZoo -> CTRLJeuZoo : faireEntrerVisiteur()
activate CTRLJeuZoo 

create Visiteur
CTRLJeuZoo -> Visiteur : << create >>
CTRLJeuZoo -> Visiteur : getCompteurVisiteur()
activate Visiteur
Visiteur --> CTRLJeuZoo : compteurVisiteur
deactivate Visiteur
CTRLJeuZoo --> IUJeuZoo : compteurVisiteur
deactivate CTRLJeuZoo
deactivate IUJeuZoo


IUJeuZoo -> IUJeuZoo : afficherZoo()
activate IUJeuZoo
deactivate IUJeuZoo


@enduml