@startuml

	Joueur -> IUJeuZoo : nourrir()
	activate IUJeuZoo
	
	
	IUJeuZoo -> CTRLJeuZoo : nourrir()
	deactivate IUJeuZoo
	activate CTRLJeuZoo
	create Zoo
	
	IUJeuZoo -> Zoo : << create >>
	CTRLJeuZoo -> Zoo : nourrir()
	
	activate Zoo
	create Animal
	CTRLJeuZoo -> Animal : << create >>
	
	activate Animal
	Zoo -> Animal : manger()
	deactivate Animal
	deactivate Zoo

	deactivate CTRLJeuZoo
@enduml