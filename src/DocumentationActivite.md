@startuml


start

repeat :ProposeNourirAnimal
:NourirAnimal;


backward :Erreur;
note right: VerificationEstVivant Animal
repeat while (ConditionestVivant) not (Yes)
if (Singe?) then (yes)
  :PoidAugmente 3.3 Kilo;
elseif (Tigre?) then (yes)
  :PoidAugmente 4.2 Kilo;
  
elseif (Zebre?) then (yes)
  :PoidAugmente 2.4 Kilo;
elseif (Lion?) then (yes)
  :PoidAugmente 5.2 Kilo;
else (No)
  
endif

stop
@enduml