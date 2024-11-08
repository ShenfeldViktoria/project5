```mermaid
classDiagram
    direction TB
    class PizzaType {
        <<enumeration>>
        MARGARITA
        CARBONARA
        HUNTERS
    }

    class Pizza

    class PizzaMargarita

    class PizzaCarbonara

    class PizzaHunters

    class Factory {
        create_pizza(pizza_type: PizzaType)
    }

    Pizza <|-- PizzaMargarita
    Pizza <|-- PizzaCarbonara
    Pizza <|-- PizzaHunters
    Factory --> PizzaType : uses
    Factory --> Pizza : creates
