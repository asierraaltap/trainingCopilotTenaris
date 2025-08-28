Library App
Description
Library App is a console-based application for managing library patrons, books, loans, and memberships. It uses a layered architecture with clear separation between business logic, infrastructure, and user interface. Data is stored in JSON files and accessed via repository and service patterns.

Project Structure
AccelerateDevGHCopilot.sln
src/
Library.ApplicationCore/
Library.ApplicationCore.csproj
Entities/
Enums/
Interfaces/
Services/
Library.Console/
appSettings.json
CommonActions.cs
ConsoleApp.cs
ConsoleState.cs
Library.Console.csproj
Json/
Program.cs
README.md
Library.Infrastructure/
Library.Infrastructure.csproj
Data/
tests/
UnitTests/
LoanFactory.cs
PatronFactory.cs
UnitTests.csproj
Key Classes and Interfaces
ConsoleApp
Main console application class that manages user interaction and application state.
(src/Library.Console/ConsoleApp.cs)

JsonData
Handles loading, saving, and populating entities from JSON files.
(src/Library.Infrastructure/Data/JsonData.cs)

JsonPatronRepository
Implements IPatronRepository for patron data access.
(src/Library.Infrastructure/Data/JsonPatronRepository.cs)

JsonLoanRepository
Implements ILoanRepository for loan data access.
(src/Library.Infrastructure/Data/JsonLoanRepository.cs)

IPatronRepository, ILoanRepository, ILoanService, IPatronService
Core interfaces for repository and service patterns.
(src/Library.ApplicationCore/Interfaces/)

Entity Classes
Patron, Loan, Book, BookItem, Author
(src/Library.ApplicationCore/Entities/)

Usage
Build the solution using Visual Studio or the .NET CLI:

Run the console application:

Follow the prompts in the console to search for patrons, view details, manage loans, and renew memberships.

License
This project is licensed under the MIT License.3. Follow the prompts in the console to search for patrons, view details, manage loans, and renew memberships.

License
This project is licensed under the MIT License.