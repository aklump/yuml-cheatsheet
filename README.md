# yUML Syntax Cheatsheet
Summarized from: <http://yuml.me/diagram/scruffy/class/samples>

## Class Diagrams

### Association `-`
"Client and Project are somehow related."

    [Client]-[Project]

![Association schema](http://yuml.me/diagram/scruffy/class/[Client]-[Project])

### Directed Association `->`
"A Client can have a Project."

    [Client]->[Project]

![Directed Association schema](http://yuml.me/diagram/scruffy/class/[Client]->[Project])

### Multiplicity `1-0..*`
"A Client can zero or more Projects." Any one of these will work.

    [Client]1-0..*[Project]

![Multiplicity schema](http://yuml.me/diagram/scruffy/class/[Client]1-0..*[Project])

    [Client]-0..*[Project]

![Multiplicity schema](http://yuml.me/diagram/scruffy/class/[Client]-0..*[Project])

    [Client]1->0..*[Project]

![Multiplicity schema](http://yuml.me/diagram/scruffy/class/[Client]1->0..*[Project])

    [Client]->0..*[Project]

![Multiplicity schema](http://yuml.me/diagram/scruffy/class/[Client]->0..*[Project])

### Aggregation `+`
"Client contains Projects; but Projects may exist without Client." Either will work.

    [Client]+-[Project]

![Aggregation schema](http://yuml.me/diagram/scruffy/class/[Client]+-[Project])

    [Client]<>-[Project]

![Aggregation schema](http://yuml.me/diagram/scruffy/class/[Client]<>-[Project])

### Composition `++`
"Projects can only exist within a Client." Second shows Directinoal.

    [Client]++-[Project]

![Composition schema](http://yuml.me/diagram/scruffy/class/[Client]++-[Project])

    [Client]++->[Project]

![Composition schema](http://yuml.me/diagram/scruffy/class/[Client]++->[Project])

### Notes `[note:bla]`

    [note: How is this{bg:yellow}]

![Notes schema](http://yuml.me/diagram/scruffy/class/[note: How is this{bg:yellow}])

### Interface `[<<Name>>;method]`

    [<<TodoInterface>>;complete;uncomplete;isComplete;getDuration;getCarryover]uses-.->[Todo]

![Interface schema](http://yuml.me/diagram/scruffy/class/[<<TodoInterface>>;complete;uncomplete;isComplete;getDuration;getCarryover]uses-.->[Todo])

### Class/Scope `=, #, -`

    +	Public
    #	Protected
    -	Private

    [Class|-privateVar:string|#protectedMethod($arg);+publicMethod($arg)]

![Class Scope schema](http://yuml.me/diagram/scruffy/class/[Class|-privateVar:string|protectedMethod($arg);+publicMethod($arg)])

## Combos
### Interface -> Abstract Class -> Class

    [<<ObjectInterface>>;config]uses-.->[Object],[Object]^-.-[Todo]

![Combos schema](http://yuml.me/diagram/scruffy/class/[<<ObjectInterface>>;config]uses-.->[Object],[Object]^-.-[Todo])
