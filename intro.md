```mermaid
classDiagram
    class Libro {
        +String titulo
        +String autores
        +String año
    }

    class Miembro {
        +String Nombre
        +String Apellido
        +String Libro prestado
    }

    class bibliotecario {
        +String Jorge
        +String Librero
        +String Ocupado
    }

    class biblioteca {
        +String name
        +List<Book> books
        +List<Member> members
        +List<Librarian> librarians
        +addMember(Member member)
        +removeMember(Member member)
    }

    Libro --> biblioteca : contiene
    Miembro --> biblioteca : registra
    bibliotecario --> biblioteca : administra
