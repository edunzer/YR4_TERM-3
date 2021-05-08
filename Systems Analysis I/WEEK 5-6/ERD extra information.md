## ERD EXTRA INFORMATION DOCUMENT

Entities:

  Manuscripts
    Title - varchar
    Author - varchar
    ID - int
    Status - varchar
    ISBN - varchar
    Link - varchar

  Authors
    First name - varchar
    Last name - varchar
    Phone - int
    Email - varchar
    Ledger link - varchar

  Ledger Cards
    Name - varchar
    Type - varchar
    ID - int
    Value - int
    Spreadsheet link - varchar

  Accounts
    Name - varchar
    Type - varchar
    ID - int
    Value - int
    Spreadsheet link - varchar

  Inventory
    Title - varchar
    Amount - int
    Requests - int
    Status - varchar

  Orders
    Title - varchar
    ISBN - varchar
    Amount - int
    Info - varchar
    Status - varchar

  Contracts
    Title - varchar
    Contract Link - varchar

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

  Employee's
    First name - varchar
    Last name - varchar
    Email - varchar
    Phone - int
    ID - int
    Type - varchar
    Access level - int
