class Character:

    def __init__(self, name, attack, defense, vida):
        self.name = name
        self.attack = attack
        self.defense = defense
        self.vida = vida
    
    def direck_attack(self, enemy):
        return self.attack - enemy.defense
    
    def esta_vivo(self):
        if self.vida > 0:
            print(f"esta vivo, sus puntos de vida son {self.vida}")
    
    def morir(self):
        if self.vida <= 0:
            self.vida == 0
            print(f"{self.name} a muerto")

    def effect_increase_attack(self, attack=100):
        self.attack += attack
        print(f"{self.name}'s attack has been increased by {attack} points through an effect.\n{self.name} Atk: {self.attack}")

    def effect_increase_defense(self, defense=100):
        self.defense += defense
        print(f"{self.name}'s defense has been increased by {defense} points through an effect.\n{self.name} Def: {self.defense}")

    def show_attributes(self):
        print(f"The attack of {self.name} is {self.attack}")
        print(f"The defense of {self.name} is {self.defense}")


dark_magician = Character("Dark Magician", 2500, 2100, 4000)
flame_swordsman = Character("Flame Swordsman", 1800, 1600, 4000)


flame_swordsman.effect_increase_defense(400)
dark_magician.effect_increase_attack(500)

#dark_magician.show_attributes()
#flame_swordsman.show_attributes()
