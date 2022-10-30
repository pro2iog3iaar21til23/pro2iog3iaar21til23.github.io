# Design Patterns - composition vs. inheritance

Vi har nu prøvet kræfter med at lave et objektorienteret bibliotek - og set fordelene ved at opdele forskellige elementer i klasser så de kan genbruges af andre.

Men objektorienteret programmering kan selvfølgelig ligesom alt andet programmering anvendes på mange forskellige måder.
Både hensigsmæssige og mindre hensigtsmæssige!

Det har vist sig at nogle problemstillinger går igen i mange forskellige programmer derfor er der gennem tiden også opstået hensigtsmæssige oop-design-principper og oop-arkitekturer til at løse disse problemer.

## Design princip - Vælg komposition istedet for nedarvning!

Dette er et meget berømt princip indenfor OOP. Du kan læse om det her:

[https://www.geeksforgeeks.org/favoring-composition-over-inheritance-in-java-with-examples/](https://www.geeksforgeeks.org/favoring-composition-over-inheritance-in-java-with-examples/)

## Design Pattern - Strategy Pattern

Et design pattern er en objektorienteret arkitektur, der løser en bestemt type problemstilling.   
Vi kigger her på en "Strategy Pattern" der direkte udnytter "komposition istedet for nedarvning":

[https://refactoring.guru/design-patterns/strategy](https://refactoring.guru/design-patterns/strategy)

## Opgaven
- Udtænk en knap klasse, der anvender "strategy pattern". Selve den handling som udføres skal pakkes ind i en såkaldt "strategy".
- Tegn et klassediagram over implementationen
- Skriv om både klassen og klassediagrammet i din log-bog
