@startuml

	Joueur -> IUJeuZoo : nourrir()
	activate IUJeuZoo
	
	
	IUJeuZoo -> CTRLJeuZoo : nourrir()
	deactivate IUJeuZoo
	activate CTRLJeuZoo
	create Zoo
	IUJeuZoo -> Zoo : << create >>
	CTRLJeuZoo -> Zoo : nourrir()
	

	
	
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
	
	Joueur -> IUJeuZoo : etapeSuivante()
	activate IUJeuZoo
		activate CTRLJeuZoo
			IUJeuZoo -> CTRLJeuZoo : etapeSuivante()
			activate Animal
				CTRLJeuZoo -> Animal :  viellir()
				CTRLJeuZoo -> Animal :  maigrir()
			deactivate Animal
		deactivate CTRLJeuZoo
	deactivate IUJeuZoo
@enduml