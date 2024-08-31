```mermaid
classDiagram
    class Libro {
        +Titulo_libro titulo
        +Autor_libro autores
        +Año_estreno año
    }

    class Miembro {
        +Nombre Nombre
        +Apellido Apellido
        +Libro tomado: fall of titans
    }

    class bibliotecario {
        +Nombre Jorge
        +Ocupacion Librero
        +Estado Ocupado
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
