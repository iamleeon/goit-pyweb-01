```mermaid
classDiagram
    ABC <|-- Output
    Output <|-- ConsoleOutput
    Field <|-- Name
    Field <|-- Phone
    Field <|-- Birthday
    Record
    UserDict <| -- AddressBook
    class ABC {
        +display_contact_info(contact)
        +display_all_contacts_info(contacts)
        +show_birthday_info(contacts)
        +birthdays_info(upcoming_birthdays)
        +display_instructions()
    }
    class Field{
        +value
    }
    class Phone{
        +phone_validation(phone)
    }
    class Record{
        +name
        +phones
        +birthday
        +add_phone(phone)
        +remove_phone(phone_to_remove)
        +edit_phone(old_phone, new_phone)
        +find_phone(phone)
        +add_birthday(birthday)

    }
    class AddressBook{
        +add_record(record)
        +find(record)
        +delete(name)
        +get_upcoming_birthdays(days=7)
    }

```