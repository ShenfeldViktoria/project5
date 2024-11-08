```PlantUML
@startuml
class PizzaType {
    <<enumeration>>
    +MARGARITA
    +CARBONARA
    +HUNTERS
}

class Pizza {
    -price: float
    +get_price(): float
}

class PizzaMargarita {
}

class PizzaCarbonara {
}

class PizzaHunters {
}

class Factory {
    +create_pizza(pizza_type: PizzaType): Pizza
}

Pizza <|-- PizzaMargarita
Pizza <|-- PizzaCarbonara
Pizza <|-- PizzaHunters
Factory --> PizzaType : uses
Factory --> Pizza : creates
@enduml
