@startuml


start

if (il faut au moin un animal au jeu) then (yes)

:ProposeNourirAnimal;
else
:NourirAnimal;



if (Singe?) then (yes)
  :PoidAugmente 3.3 Kilo;
elseif (Tigre?) then (yes)
  :PoidAugmente 4.2 Kilo;
  
elseif (Zebre?) then (yes)
  :PoidAugmente 2.4 Kilo;
elseif (Lion?) then (yes)
  :PoidAugmente 5.2 Kilo;
  
endif

stop
@enduml