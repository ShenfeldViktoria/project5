```mermaid
classDiagram
    direction LR
    class Pizza {
        -price: float
        +get_price(): float
    }
    class PizzaType {
        <<enumeration>>
        MARGARITA
        CARBONARA
        HUNTERS
    }
    class PizzaMargarita {
        +get_price(): float
    }
    class PizzaCarbonara {
        +get_price(): float
    }
    class PizzaHunters {
        +get_price(): float
    }
    Pizza <|-- PizzaMargarita
    Pizza <|-- PizzaCarbonara
    Pizza <|-- PizzaHunters
    create_pizza ..> PizzaType : uses
    create_pizza --> Pizza : returns

