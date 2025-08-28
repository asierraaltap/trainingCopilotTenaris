# Library App

## Description

Library App is a console-based application for managing library patrons, books, loans, and memberships. It uses a layered architecture with clear separation between business logic, infrastructure, and user interface. Data is stored in JSON files and accessed via repository and service patterns.

---

## Project Structure

```
AccelerateDevGHCopilot.sln
src/
  Library.ApplicationCore/
    Entities/
    Enums/
    Interfaces/
    Services/
  Library.Console/
    appSettings.json
    CommonActions.cs
    ConsoleApp.cs
    ConsoleState.cs
    Json/
    Program.cs
    README.md
  Library.Infrastructure/
    Data/
tests/
  UnitTests/
    LoanFactory.cs
    PatronFactory.cs
    UnitTests.csproj
.gitignore
```

---

## Key Classes and Interfaces

### ConsoleApp

Main console application class that manages user interaction and application state.  
[src/Library.Console/ConsoleApp.cs](src/Library.Console/ConsoleApp.cs)

### CommonActions

Contains reusable actions for the console interface.  
[src/Library.Console/CommonActions.cs](src/Library.Console/CommonActions.cs)

### ConsoleState

Represents the current state of the console application.  
[src/Library.Console/ConsoleState.cs](src/Library.Console/ConsoleState.cs)

### JsonData

Handles loading, saving, and populating entities from JSON files.  
[src/Library.Infrastructure/Data/JsonData.cs](src/Library.Infrastructure/Data/JsonData.cs)

### JsonPatronRepository

Implements `IPatronRepository` for patron data access.  
[src/Library.Infrastructure/Data/JsonPatronRepository.cs](src/Library.Infrastructure/Data/JsonPatronRepository.cs)

### JsonLoanRepository

Implements `ILoanRepository` for loan data access.  
[src/Library.Infrastructure/Data/JsonLoanRepository.cs](src/Library.Infrastructure/Data/JsonLoanRepository.cs)

### Core Interfaces

- `IPatronRepository`
- `ILoanRepository`
- `ILoanService`
- `IPatronService`

Core interfaces for repository and service patterns.  
[src/Library.ApplicationCore/Interfaces/](src/Library.ApplicationCore/Interfaces/)

### Entity Classes

- `Patron`
- `Loan`
- `Book`
- `BookItem`
- `Author`

[src/Library.ApplicationCore/Entities/](src/Library.ApplicationCore/Entities/)

---

## Usage

### Build the Solution

Use Visual Studio or the .NET CLI:

```sh
dotnet build
```

### Run the Console Application

```sh
dotnet run --project src/Library.Console/Library.Console.csproj
```

Follow the prompts in the console to search for patrons, view details, manage loans, and renew memberships.

---

## Testing

Unit tests are located in [tests/UnitTests/](tests/UnitTests/).  
Run tests using:

```sh
dotnet test tests/UnitTests/UnitTests.csproj
```

---

## License

This project is licensed under