classDiagram
    direction BT

    class Entity {
        <<abstract>>
        -String id
        +Entity(String id)
        +getId() String
        +setId(String id) void
    }

    class User {
        <<abstract>>
        -String username
        -String password
        -String email
        +User(String id, String username, String password, String email)
        +displayRole()* void
        +getUsername() String
        +setUsername(String username) void
    }

    class Bidder {
        +Bidder(String id, String username, String password, String email)
        +displayRole() void
        +placeBid() void
    }

    class Seller {
        +Seller(String id, String username, String password, String email)
        +displayRole() void
        +manageItems() void
    }

    class Admin {
        +Admin(String id, String username, String password, String email)
        +displayRole() void
        +manageSystem() void
    }

    User --|> Entity : Kế thừa
    Bidder --|> User : Kế thừa
    Seller --|> User : Kế thừa
    Admin --|> User : Kế thừa
