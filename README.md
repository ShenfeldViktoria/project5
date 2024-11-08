```mermaid
classDiagram
    direction TB
    class PizzaSystem

    class Context

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

    PizzaSystem --> Context : composition
    Context ..> PizzaType : uses
    Context --> Pizza : factory_method
    Pizza <|-- PizzaMargarita : inheritance
    Pizza <|-- PizzaCarbonara : inheritance
    Pizza <|-- PizzaHunters : inheritance

