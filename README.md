# HCI-Main-Activity
// Pokemon Game
let myPokemon = {
    name: 'Pikachu',
    level: 3,
    health: 100,
    attack: 50,
    tackle: function() {
        console.log('The pokemon tackle the target pokemon');
        console.log("targetPokemon");
    }
};


let trainer = {
    name: 'Javol',
    age: 69,
    pokemonList: [],

    addPokemon: function(pokemon) {
        this.pokemonList.push(pokemon);
        console.log(${pokemon.name} added to ${this.name}'s team!);
    }
};


function Pokemon(name, level, health, attack) {
    this.name = name;
    this.level = level;
    this.health = health;
    this.attack = attack;
}


Pokemon.prototype.attackOpponent = function(opponent) {
    console.log(${this.name} attacks ${opponent.name}!);
    opponent.health -= this.attack; 
    console.log(${opponent.name}'s health reduced to ${opponent.health});
};


let pikachu = new Pokemon('Pikachu', 3, 100, 50);
let charmander = new Pokemon('Charmander', 3, 100, 50);
let squirtle = new Pokemon('Squirtle', 3, 100, 50);


pikachu.attackOpponent(charmander);
charmander.attackOpponent(squirtle);


console.log(Trainer: ${trainer.name}, Age: ${trainer.age});


console.log(Trainer Name (Dot Notation): ${trainer.name});
console.log(Trainer Age (Bracket Notation): ${trainer['age']});


trainer.addPokemon(pikachu);
trainer.addPokemon(charmander);
trainer.addPokemon(squirtle);
