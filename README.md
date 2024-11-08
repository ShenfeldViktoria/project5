```mermaid
classDiagram
    class PizzaType {
        <<enumeration>>
        MARGARITA
        CARBONARA
        HUNTERS
    }

    class Pizza {
        -float __price
        +get_price() float
    }

    class PizzaMargarita {
        +__init__()
    }
    class PizzaCarbonara {
        +__init__()
    }
    class PizzaHunters {
        +__init__()
    }

    class Client {
        +create_pizza(pizza_type: PizzaType) Pizza
    }

    Pizza <|-- PizzaMargarita
    Pizza <|-- PizzaCarbonara
    Pizza <|-- PizzaHunters
    Client ..> PizzaType : "depends on"
    Client ..> Pizza : "creates"
    Pizza <|-- Client : "uses"

    PizzaType : <<enumeration>>
    Client : create_pizza()
