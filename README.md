# PokemonExampleAPI

This project is a simple Pokémon management system built using C# and ASP.NET Core. It provides an API for managing Pokémon with their attributes, including their moves, abilities, and other key details. The system allows for CRUD (Create, Read, Update, Delete) operations for managing Pokémon records.

## Features

- **Pokemon Class**: Defines the structure of a Pokémon with properties such as ID, name, type, level, stats (HP, attack, defense, etc.), abilities, nature, gender, region, and moves.
- **API Endpoints**: A set of endpoints for performing CRUD operations on Pokémon:
  - Create a Pokémon (`POST`).
  - Get a list of Pokémon (`GET`).
  - Update a Pokémon (`PUT`).
  - Delete a Pokémon (`DELETE`).
- **Move List Validation**: Ensures that each Pokémon can have no more than 4 moves in the list during creation.

## Setup and Installation

### Prerequisites

- **.NET SDK** (5.0 or higher) installed on your machine.
- A development environment such as **Visual Studio** or **Visual Studio Code**.

### Installation Steps

1. Clone the repository:

   ```bash
   git clone https://github.com/your-repository-url.git
   ```

2. Navigate to the project directory:

   ```bash
   cd your-project-directory
   ```

3. Install dependencies:

   ```bash
   dotnet restore
   ```

4. Run the application:

   ```bash
   dotnet run
   ```

   The API should now be running at `http://localhost:5000`.

## API Endpoints

### 1. Create a Pokémon

**URL**: `/api/pokemon`

**Method**: `POST`

**Request Body**: 
```json
{
  "name": "Pikachu",
  "type": "Electric",
  "level": 5,
  "hp": 35,
  "attack": 55,
  "defense": 40,
  "speed": 90,
  "specialAttack": 50,
  "specialDefense": 50,
  "specialAttackSpeed": 80,
  "specialDefenseSpeed": 80,
  "ability": "Static",
  "nature": "Jolly",
  "heldItem": "Thunder Stone",
  "gender": "Male",
  "moves": ["Thunderbolt", "Quick Attack", "Electro Ball", "Iron Tail"],
  "region": "Kanto"
}
```

### 2. Get a List of Pokémon

**URL**: `/api/pokemon`

**Method**: `GET`

**Response**:
```json
[
  {
    "id": 1,
    "name": "Pikachu",
    "type": "Electric",
    "level": 5,
    "hp": 35,
    "attack": 55,
    "defense": 40,
    "speed": 90,
    "specialAttack": 50,
    "specialDefense": 50,
    "specialAttackSpeed": 80,
    "specialDefenseSpeed": 80,
    "ability": "Static",
    "nature": "Jolly",
    "heldItem": "Thunder Stone",
    "gender": "Male",
    "moves": ["Thunderbolt", "Quick Attack", "Electro Ball", "Iron Tail"],
    "region": "Kanto"
  }
]
```

### 3. Update a Pokémon

**URL**: `/api/pokemon/{id}`

**Method**: `PUT`

**Request Body**: Same as the `POST` request but with updated values for the existing Pokémon.

### 4. Delete a Pokémon

**URL**: `/api/pokemon/{id}`

**Method**: `DELETE`

---

## Validation

The Pokémon management system includes the following validation:

- **Moves Validation**: A Pokémon can have a maximum of 4 moves. Any attempt to add more than 4 will be blocked.
- **Mandatory Fields**: The `name`, `type`, `level`, and other basic fields are required when creating a new Pokémon.

---

## Contributing

1. Fork the repository.
2. Create a new branch (`git checkout -b feature-new-feature`).
3. Commit your changes (`git commit -am 'Add new feature'`).
4. Push to the branch (`git push origin feature-new-feature`).
5. Create a new Pull Request.

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
