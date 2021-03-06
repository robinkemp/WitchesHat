### Bounded Contexts
**[Player]**
**[PlayerAggregate]**
Id (Mongo autogen)
Sub (Indexed, auth provider unique id)
Nickname

**[Campaign]**
**[CampaignAggregate]**
Id (Mongo autogen)
Name
PlayerList (PlayerAggregateIds)
ActiveCharacters (CharacterIds)

**[CampaignCharacterAggregate]**
Id (Mongo autogen)
CharacterId (Indexed)
PlayerId (Indexed)

### Aggregates

### Proposed item grouping
**[CharacterProfile]**

CharacterName |
Class |
Background |
Race |
Alignment |
Age |
Height |
Weight |
Eyes |
Skin |
Hair |
ProfilePicture |

**[CharacterDetails]**

Backgrouhnd | PersonalityTraits | Ideals | Bonds | Flaws | Languages | ExtraProficiencies | Treasure | TreasureDescription | 

**[AlliesAndOrgs]**

AllyName | Relationship | BackgroundInformation

OrganisationName | Relationship | BackgroundInformation

**[TraitsAndFeatures]**

Trait/FeatureName | Description | Passive/Active?

**[CombatStats]**

ArmourClass | Initiative | Speed | HitPointsMax | HitPointsCurrent | TempHitPoints | HitDiceTotal | HitDiceCurrent | DeathSaves

**[EquippedWeapons]**

WeaponName | WeaponType | AttackBonus | DamageDice | DamageType | Ammunition

**[Inventory]**

CopperPieces | SilverPieces | ElectrumPieces | GoldPieces | PlatinumPieces | EquipmentName | AmmountHeld

**[Attributes]**

Strength |
StrengthMod |
Dexterity |
DexterityMod |
Constitution |
ConstitutionMod |
Intelligence |
IntelligenceMod |
Wisdom |
WisdomMod |
Charisma |
CharismaMod |


**[Skills]**

// Should these be KVPs? k: int skillName, v: bool proficient

Acrobatics |
AnimalHandling |
Arcana |
Athletics |
Deception |
History |
Insight |
Intimidation |
Investigation |
Medicine |
Nature |
Perception |
Performance |
Persuasion |
Religion |
SleightOfHand |
Stealth |
Survival |

passivePerception..? 


**[SavingThrows]**

// Should these be KVPs? k: int savingThrow, v: bool proficient

Strength |
Dexterity |
Constitution |
Intelligence |
Wisdom |
Charisma |

**[SpellcastingStats]**

SpellCastingAbility | SpellSaveDc | SpellAttackBonus | LevelOneSpellCount | LevelTwoSpellCount | LevelThreeSpellCount | LevelFourSpellCount | LevelFiveSpellCount | LevelSixSpellCount | LevelSevenSpellCount

**[PreparedMagicks]**

Name | IsCantrip | EffectDescription | SpellLevel | DamageDie

