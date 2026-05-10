1. How entities are defined and represented in an ERD
Takeaway: An entity is a real‑world object or concept stored in the database, represented as a rectangle in Crow’s Foot notation. 

Entities are the core building blocks of an ERD. They represent nouns in the system—such as Person, Pet, Order, Product, etc.
Key details:

Entities are drawn as rectangles.

The entity name appears at the top, usually singular and uppercase (e.g., PERSON, PET).

A horizontal line separates the name from the attribute list.

Entities represent things the database must track. 

If you want to explore this further, try:

entity definition

entity representation

2. How attributes are defined and associated with entities
Takeaway: Attributes are properties that describe an entity and are listed inside the entity rectangle beneath the name. 

Attributes describe the characteristics of an entity. Examples:

PERSON → PersonID, FirstName, LastName

PET → PetID, Name, Species

Important conventions:

Attributes are written in a single column inside the entity box.

Primary Keys (PK) uniquely identify each record.

Foreign Keys (FK) link to another entity’s PK.

Attributes are not drawn as ovals in Crow’s Foot notation (that is Chen notation). 

Explore more:

entity attributes

primary_key

foreign_key

3. What a relationship is, how it is represented, and how it connects entities
Takeaway: A relationship is a logical connection between two entities, represented by a line with Crow’s Foot symbols indicating cardinality and optionality. 

Relationships show how entities interact.
Representation details:

A line connects two entities.

Symbols at each end indicate:

Maximum cardinality:

One → |

Many → < (crow’s foot)

Minimum cardinality (optionality):

Mandatory → |

Optional → O

Example:

PERSON |—< PET

One person can own many pets.

Each pet must belong to exactly one person (if mandatory).

Explore more:

relationship representation

crow%27s_foot_symbols

4. Types of Relationships (Cardinality)
Takeaway: Cardinality describes how many instances of one entity relate to another—1:1, 1:N, M:N, each with optional/mandatory variations. 

Cardinality Types (Crow’s Foot Notation)
One-to-One (1:1)

Symbol: |—|

Example: Each person has exactly one passport.

One-to-Many (1:N)

Symbol: |—<

Example: One person owns many pets.

Zero-or-One (0..1)

Symbol: O—|

Example: A person may or may not have a driver’s license.

Zero-or-Many (0..N)

Symbol: O—<

Example: A customer may place zero or many orders.

Many-to-Many (M:N)

Not drawn directly; resolved using an associative entity (junction table).

Example: Students enrolled in many classes, classes with many students.

Represented as two 1:N relationships. 

5. ERD: People That Own Pets
Takeaway: The ERD consists of two entities—PERSON and PET—with a 1-to-many relationship: one person can own many pets.

Below is a clean conceptual ERD description you can convert into a diagram for your GitHub submission.

Entities & Attributes
PERSON

PersonID (PK)

FirstName

LastName

Phone

PET

PetID (PK)

Name

Species

PersonID (FK → PERSON.PersonID)

Relationship
PERSON |—< PET

One person can own many pets.

Each pet belongs to exactly one person.
