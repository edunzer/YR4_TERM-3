## ERD EXTRA INFORMATION DOCUMENT

Entities:

  Manuscripts
    Title - varchar
    Author - varchar
    ID - int
    Status - varchar
    Link - varchar

  Authors
    First name - varchar
    Last name - varchar
    Phone - int
    Email - varchar

  Ledger Cards
    Type - varchar
    Name - varchar
    Value - int
    Link - varchar

  Inventory
    Title - varchar
    Amount - int
    Requests - int

  Contracts
    Title - varchar
    Link - varchar

  Illustrations/Artwork
    Title - varchar
    Manuscripts - varchar
    Status - varchar
    Link - varchar

  Printers
    Name - varchar
    Avg Price - int
    Num Previous Jobs - int
    Info - varchar

  Sponsorship
    Name - varchar
    Avg Price - int
    Num Previous Jobs - int
    Info - varchar
