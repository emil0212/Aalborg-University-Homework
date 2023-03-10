# Imperative Programming

Imperative programming is a paradigm of computer programming where the program describes steps that change the state of the computer.

### Language

Doing this course we used the C Programming Language

### IDE

For this project, the 'Clion' Integrated Development Environment (IDE) by JetBrains was utilized. 'Clion' is a cross-platform IDE that is specifically designed for C and C++ development. It offers a range of features including code navigation, code refactoring, debugging, and code completion, which make it a powerful tool for developing C and C++ applications. 'Clion' also integrates with popular build systems such as CMake and Gradle, allowing for easy compilation and execution of projects. Overall, 'Clion' proved to be a reliable and efficient choice for this project.

### Literature

Problem Solving and Program Design in C - Eigth Edition

### C History

C was developed by Dennis Tichie in 1972 at AT&T Bell Labs in the USA. Historically it's connected to the UNIX operating system. Many other programming languages are inspired by C.

### Top-Down Design with Functions

In software development, top-down design is a method of designing and building a program by breaking it down into smaller, more manageable pieces. This approach allows you to build a program incrementally, starting with the big picture and then working your way down to the details.

Top-down design involves breaking the program into smaller functions, each of which performs a specific task. This allows you to reuse code and make your program more modular and easier to maintain.

### Prototypes

In C, a prototype is a declaration of a function that specifies the function's name, return type, and parameter list. Prototypes are used to inform the compiler about the functions that are used in a program, so that the compiler can check that the function calls are valid and generate the correct code.

Prototypes are typically placed in a header file or at the top of a source file before the main function.

Handin3.c:

```c
//Prototype at the top of the program
double trap(double, double, int, binary_f, function_flag);
...
double trap(double a, double b, int n, binary_f f, function_flag flag)
{
    //h = (b-a)/n
    double h = (b-a)/n, area;

    //Function pointer to the sum function
    double (*sum_ptr)(double, double, int, binary_f, function_flag) = &sum;

    //Invoking the function pointer and assigning its result to a variable
    double sum = (*sum_ptr)(a, h, n, f, flag);

    //T=(h/2)*(f(a) + f(b) + 2 * (sum [i=1 ... n] f(x_i) )
    area = (h/2) * (f(a, flag) + f(b, flag) + 2 * sum);

    return area;
}
```

### Library Functions

"Predefined Functions and Code Reuse: A primary goal of software engineering is to write error-free code. Code reuse, reusing program fragments that have already been written and tested whenever possible, is one way to accomplish this goal. Stated more simply, ???Why reinvent the wheel???? C promotes reuse by providing many predefined functions that can be used to perform mathematical computations. C???s standard math library defines a function named sqrt that performs the square root computation. The function call in the assignment statement" -??*Problem Solving and Program Design in C*

### Examples:

- math.h
- stdio.h
- stdlib.h
- stdbool.h etc..

## Danish Notes from Lectures

### **Lektion 2: Introduktion til C (9.9.2022)**

Lektion 2 er en introduktion til C programmering. Emnerne, der vil blive d??kket, inkluderer variable, erkl??ringer og initialisering.

Variabler er steder i computerhukommelsen, hvor data kan gemmes og tilg??s. For at kunne bruge en variabel i et C-program, skal den f??rst erkl??res. Erkl??ringen giver information om, hvad slags data variablen vil indeholde, og hvad den skal hedde. For eksempel kan en variabel erkl??res som en int (heltal) med navnet "a".

Initialisering er at give en variabel en startv??rdi, n??r den erkl??res. Dette kan g??res ved at tildele en v??rdi til variablen i erkl??ringen. For eksempel kan variablen "a" initialiseres med v??rdien 5 ved at skrive "int a = 5;".

Assignments er brugt til at tildele en v??rdi til en eksisterende variabel. For eksempel kan v??rdien af variablen "a" ??ndres til 10 ved at skrive "a = 10;".

I C-programmer findes der flere forskellige datatyper, som kan bruges til at erkl??re variable med. Nogle almindelige eksempler er int (heltal), float (decimal), char (karakter) og andre. Hver datatype har sine egne specifikationer og begr??nsninger.

Udtryk og operatorer bruges til at udf??re beregninger og sammenligninger i et program. Operatorerne kan v??re matematiske (+, -, *, /) eller logiske (==, !=, >, <). Operator prioritering bestemmer r??kkef??lgen af operationerne i et udtryk. For eksempel vil multiplikation og division normalt blive udf??rt f??r addition og subtraktion. Associering bestemmer hvordan operatorerne samarbejder i et udtryk. For eksempel vil operatorerne i et udtryk normalt blive evalueret fra venstre mod h??jre.

S?? til sidst, printf og scanf er bibliotekfunktioner, der bruges til at udskrive og indl??se data fra brugeren. printf bruges til at udskrive en tekststreng eller en variabel p?? sk??rmen, mens scanf bruges til at l??se input fra brugeren og gemme det i en variabel. Disse funktioner er vigtige for at lave interaktive programmer, der kan kommunikere med brugeren.

### **Lektion 3: Selektive kontrolstrukturer (14.9.2022)**

I denne lektion har vi studeret selektive kontrolstrukturer i C-programmering. Vi har set p?? logiske udtryk og boolean datatypen, som kan evalueres til enten sandt eller falsk. Vi har set p?? if-statements, som giver mulighed for at udf??re en bestemt handling, hvis en bestemt betingelse er opfyldt.

```c
int a = 5;
if (a > 3) {
    printf("a is greater than 3\n");
}
```

Her vil det udskrive "a is greater than 3" fordi a er st??rre end 3.

Vi har ogs?? set p?? switch-statements, som giver mulighed for at udf??re forskellige handlinger baseret p?? forskellige v??rdier af en bestemt variabel.

```c
char grade = 'B';
switch(grade) {
    case 'A':
        printf("Excellent!\n");
        break;
    case 'B':
        printf("Good job!\n");
        break;
    case 'C':
        printf("You passed!\n");
        break;
    default:
        printf("Invalid grade\n");
}
```

Her vil det udskrive "Good job!" fordi grade er sat til 'B'.

Vi har ogs?? introduceret begrebet blokke og scoperegler. En blok er en sektion af koden, der er omsluttet af kr??llede parenteser "{}". Scoperegler bestemmer, hvilke variable og funktioner, der er tilg??ngelige i en bestemt blok eller sektion af koden.

```c
int x = 10;
{
    int y = 5;
    printf("x + y = %d\n", x + y);
}
printf("x = %d\n", x);
```

Her vil det f??rste printf udskrive "x + y = 15" og det andet udskrive "x = 10" fordi x er tilg??ngelig i hele programmet, men y kun er tilg??ngelig i den f??rste blok.

Alt i alt har vi set p?? de forskellige selektive kontrolstrukturer, der er tilg??ngelige i C, og hvordan de kan anvendes i koden for at g??re det mere interaktivt og effektivt.

### **Lektion 4: Iterative kontrolstrukturer?? (16.9.2022)**

I denne lektion har vi studeret iterative kontrolstrukturer i C-programmering. Disse strukturer giver mulighed for at gentage en sektion af koden, indtil en bestemt betingelse er opfyldt.

Vi har set p?? while-l??kker, som giver mulighed for at udf??re en handling, s?? l??nge en bestemt betingelse er opfyldt.

```c
int i = 0;
while (i < 10) {
    printf("%d ", i);
    i++;
}
```

Her vil det udskrive tal fra 0 til 9 fordi i starter fra 0 og ??ges med 1 indtil det er 10.

Vi har ogs?? set p?? for-l??kker, som giver mulighed for at definere start- og stop-betingelser, samt hvordan t??lleren skal ??ndres efter hver iteration.

```c
for (int i = 0; i < 10; i++) {
    printf("%d ", i);
}
```

Her vil det ogs?? udskrive tal fra 0 til 9 fordi i starter fra 0, stopper ved 9 og ??ges med 1 efter hver iteration.

Vi har set p?? do-while-l??kker, som er ens i forhold til while-l??kker, men forskellen er at do-while-l??kken mindst k??rer 1 gang, uanset om betingelsen er opfyldt eller ej.

```c
int i = 0;
do {
    printf("%d ", i);
    i++;
} while (i < 10);
```

Her vil det ogs?? udskrive tal fra 0 til 9 fordi i starter fra 0 og ??ges med 1 indtil det er 10.

Vi har ogs?? set p?? Euclids algoritme, som er en metode til at finde den st??rste f??lles divisor (GCD) mellem to tal.

```c
int gcd(int a, int b) {
    if (b == 0)
        return a;
    return gcd(b, a % b);
}
```

Her kan man bruge den ved at skrive:

```c
printf("GCD of 60 and 48 is %d", gcd(60, 48));
```

Her vil det udskrive GCD of 60 and 48 is 12, da 12 er den st??rste f??lles divisor mellem 60 og 48.

Vi har ogs?? set p?? kommaoperatoren, som kan anvendes i for-l??kker for at udf??re flere handlinger i en enkelt iteration.

Vi har ogs?? set p?? klassificeringen af gentagelser, som kan v??re enten definite eller udefinerede. Definite gentagelser ved, hvor mange gange de skal k??re, mens udefinerede gentagelser k??rer, indtil en bestemt betingelse er opfyldt.

Vi har ogs?? set p?? hop med break og continue. Break bruges til at bryde ud af en l??kke eller et switch-statement tidligere end normalt, mens continue bruges til at springe over en iteration og g?? direkte til den n??ste.

```c
for (int i = 0; i < 10; i++) {
    if (i == 5) {
        break;
    }
    printf("%d ", i);
}
```

Her vil det udskrive tal fra 0 til 4, fordi break bryder ud af l??kken, n??r i n??r 5.

```c
for (int i = 0; i < 10; i++) {
    if (i % 2 == 0) {
        continue;
    }
    printf("%d ", i);
}
```

Her vil det udskrive tal fra 1 til 9, fordi continue springer over alle lige tal, s?? kun ulige tal bliver udskrevet.

Alt i alt har vi set p?? de forskellige iterative kontrolstrukturer, der er tilg??ngelige i C, og hvordan de kan anvendes i koden for at g??re det mere effektivt og automatisere Gentagende opgaver. Vi har ogs?? set p?? Euclids algoritme, komma operatoren, klassificering af gentagelser, hop med break og continue, som er nyttige v??rkt??jer for at skrive komplekse og effektive programmer.

### **Lektion 5: Funktioner og top-down programmering (21.9.2022)**

I denne lektion har vi studeret brugen af funktioner og top-down programmering i C-programmering. Funktioner giver mulighed for at opdele et program i mindre, genanvendelige dele, hvilket g??r det nemmere at forst?? og vedligeholde.

Vi har set p?? procedurer og funktioner, som er to former for funktioner i C. Procedurer er funktioner, der ikke returnerer nogen v??rdi, mens funktioner returnerer en v??rdi.

Vi har ogs?? set p?? abstraktion, som er evnen til at se bort fra detaljer og koncentrere sig om de vigtigste aspekter af et problem. Dette g??r det nemmere at forst?? og l??se komplekse problemer ved at bryde dem ned i mindre dele.

Vi har set p?? call by value parametre, som er en metode til at sende input parametre til en funktion. Dette giver mulighed for at sende kopier af variable i stedet for originalerne, s?? funktionen ikke ??ndrer v??rdien af de originale variable.

Vi har ogs?? set p?? top-down programudvikling ved trinvis forfinelse. Dette er en metode, hvor et program er opdelt i mindre dele og hver del er skrevet og testet separat, f??r de samles til det f??rdige program. Dette g??r det nemmere at identificere og l??se fejl i koden.

Vi har ogs?? set p?? del og hersk (del og kombiner) metoden, som er en m??de at l??se komplekse problemer p?? ved at bryde dem ned i mindre dele og derefter l??se hver del separat, f??r de kombineres til den endelige l??sning.

Alt i alt har vi i denne lektion set p??, hvordan funktioner kan anvendes til at g??re koden mere overskuelig og effektiv, ved at opdele den i mindre, genanvendelige dele. Vi har ogs?? set p?? metoder til at l??se komplekse problemer ved hj??lp af abstraktion, top-down programmering og del og hersk metoden.

### **Lektion 6: Funktioner og parametre (7.10.2022)**

I denne lektion har vi introduceret begrebet pointere i C-programmering. Pointere er variable, der gemmer en adresse i hukommelsen og giver mulighed for at referere til en anden variable.

Vi har set p?? call by reference parametre, som er en metode til at sende output parametre til en funktion. Dette giver mulighed for at ??ndre v??rdien af de originale variable inde i funktionen. 

```c
void add(int *x, int *y) {
    *x = *x + *y;
}
```

Her kan man bruge den ved at skrive:

```c
int a = 3, b = 4;
add(&a, &b);
printf("%d", a);
```

Her vil det udskrive 7, fordi funktionen adder b til x og gemmer det i x.

Vi har ogs?? set p?? pointere til funktioner, som giver mulighed for at gemme adressen p?? en funktion i en pointervariabel, og derefter bruge den til at kalde funktionen. Dette kan v??re nyttigt i situationer, hvor man ??nsker at gemme en funktion i en variabel og derefter kalde den senere eller v??lge en funktion baseret p?? en bestemt betingelse.

Alt i alt har vi i denne lektion set p??, hvordan pointere og call by reference parametre kan anvendes i C-programmering for at g??re koden mere fleksibel og effektiv. Pointere giver mulighed for at referere til andre variable, mens call by reference parametre giver mulighed for at ??ndre v??rdien af de originale variable inde i funktionen og pointere til funktioner giver mulighed for at gemme en funktion i en variabel og derefter kalde den senere eller v??lge en funktion baseret p?? en bestemt betingelse.

### **Lektion 7: Arrays og Pointere??(3.10.2022)**

I denne lektion har vi set p?? brugen af arrays og pointere i C-programmering, med b??de eksempler og forklaringer.

Vi har set p?? arrays i ??n og flere dimensioner. En en-dimensional array er en liste af variable af samme datatype, der er organiseret som en r??kke. En multi-dimensional array er en liste af variable organiseret som en matrice. For eksempel:

```c
int oneDimensionalArray[5] = {1, 2, 3, 4, 5}; // En en-dimensional array med plads til 5 integer
int twoDimensionalArray[3][3] = {{1, 2, 3}, {4, 5, 6}, {7, 8, 9}}; // En to-dimensional array med plads til 3x3 integer
```

Vi har ogs?? set p?? forholdet mellem pointere og arrays. Et array kan betragtes som en type pointer, da et arraynavn i C-programmering er en pointer til den f??rste element i arrayet. Dette giver mulighed for at bruge pointere til at referere til og manipulere data i arrays. For eksempel:

```c
int array[5] = {1, 2, 3, 4, 5};
int *p = array; // p er en pointer variabel, som peger p?? f??rste element i arrayet
printf("%d", *p); // udskriver 1, som er v??rdien af det f??rste element i arrayet
```

Vi har set p?? pointeraritmetik, som er metoderne til at navigere og manipulere data i arrays ved hj??lp af pointere. Dette inkluderer, at bruge pointere til at f?? adgang til en bestemt element i et array og til at navigere gennem et array. For eksempel:

```c
int array[5] = {1, 2, 3, 4, 5};
int *p = array; // p peger p?? f??rste element i arrayet
p = p + 2; // p peger nu p?? 3. element i arrayet
printf("%d", *p); // udskriver 3
```

Vi har ogs?? set p?? sortering af arrays, som er metoder til at organisere data i et array i en bestemt r??kkef??lge. Der er flere algoritmer til at sortere arrays, som kan v??lges afh??ngigt af det specifikke problem. For eksempel ved at bruge en algoritme som Bubblesort:

```c
void bubbleSort(int arr[], int n)
{
    int i, j;
    for (i = 0; i < n-1; i++)

       // Last i elements are already in place
       for (j = 0; j < n-i-1; j++)
           if (arr[j] > arr[j+1])
              swap(&arr[j], &arr[j+1]);
}
```

Vi har ogs?? set p?? b??de statisk og dynamisk allokering af lager, hvor statisk allokering er allokering af lager p?? forh??nd, mens dynamisk allokering er allokering af lager under k??rselstiden. For eksempel, statisk allokering:

```c
int array[5];
```

Dynamisk allokering:

```c
int *array = (int *) malloc(5 * sizeof(int));
```

Alt i alt har vi i denne lektion set p??, hvordan arrays og pointere kan anvendes i C-programmering for at gemme og organisere data. Vi har set p?? forholdet mellem pointere og arrays, pointeraritmetik, sortering af arrays, og forskellige metoder til allokering af lager. Dette er vigtige v??rkt??jer for at skrive effektive og organiseret kode, som kan h??ndtere store m??ngder data.
Dynamisk allokering giver mulighed for at allokere lager efter behov, men det kr??ver ogs?? at frig??re lager manuelt n??r det ikke l??ngere er brugt med free() funktionen.

```c
free(array);
```

Dette er vigtigt at huske for at undg?? memory leaks og for at optimere brugen af hukommelsen i programmet.

### **Lektion 8: Datatyper og Test (26.10.2022)**

I denne lektion har vi set p?? datatyper og test i C-programmering.
Vi har set p?? en oversigt over de forskellige datatyper i C, herunder de primitive datatyper som int, char, og float, samt de mere avancerede datatyper som pointers, arrays, og structs.
Vi har ogs?? set p?? enumeration typer, som giver mulighed for at give navne til konstanter og g??re koden mere l??sbar. 

```c
enum Weekday {Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday};
```

Vi har set p?? typedefinitioner, som giver mulighed for at give et alias til en eksisterende datatype.

```c
typedef unsigned int uint;
```

Vi har ogs?? set p?? type casts, som giver mulighed for at konvertere en variabel fra en datatype til en anden.

```c
int a = 5;
float b = (float) a;
```

Vi har set p?? scope, som er omr??det hvor en variabel eller funktion er synlig.
Vi har set p?? tilf??ldige tal, som giver mulighed for at generere tilf??ldige tal i koden.

```c
#include <stdlib.h>
#include <time.h>

srand(time(0));
int randomNumber = rand() % 100;
```

Vi har set p?? systematisk programtest og introduktion til debugging. Dette inkluderer metoder til at teste programmet for fejl og metoder til at finde og rette fejl i koden.

Vi har set p?? systematisk programtest og introduktion til debugging. Dette inkluderer metoder til at teste programmet for fejl og metoder til at finde og rette fejl i koden. En af metoderne, som er at bruge tilf??ldige tal i testen, kan v??re ved at generere tilf??ldige tal og bruge dem som input til programmet for at teste hvordan det reagerer p?? forskellige input.
Ved at bruge rand() funktionen i kombination med modulus operatoren kan vi begr??nse den tilf??ldige tal til et bestemt interval. I eksemplet ovenfor er tallet begr??nset til intervallet 0-99, ved at tage resten efter division med 100. Det er vigtigt at seede rand() funktionen med srand() og give den et unikt seed value (i eksemplet ovenfor er seedet current time) for at undg?? at f?? samme tilf??ldige tal hver gang programmet k??res.

Vi har ogs?? set p?? debugging v??rkt??jer som breakpoints, stepping through code, og print statements for at hj??lpe med at finde fejl i koden.
Vi har set p?? testing teknikker som unit testing, integration testing, og system testing for at sikre at programmet fungerer som forventet.
Alt i alt, har vi i denne lektion set p?? v??sentlige emner som datatyper og test, som er vigtige for at skrive korrekt og robust kode i C-programmering.

### **Lektion 9: Tegn og Tekststrenge (28.10.2022)**

I denne lektion har vi set p?? datatypen char og tekststrenge i C-programmering.

Vi har diskuteret v??sentlige funktioner fra string.h standard library, som giver mulighed for at arbejde med tekststrenge i C. Dette inkluderer funktioner til at kopiere, sammenligne, og manipulere tekststrenge, s??som strcpy, strcmp, og strcat.

```c
char destination[20];
char source[] = "Hello, World!";
strcpy(destination, source);
```

Vi har ogs?? set p?? eksempler p?? programmer, der behandler tekst, som kan omfatte at l??se tekst fra en fil, manipulere tekststrenge for at ??ndre deres format eller indhold, og udskrive tekst til en sk??rm eller en fil.

Vi har set p?? konceptet omkring tekststrenges null-terminerings karakter, som indikerer enden af en tekststreng. 

Det er vigtigt at have dette i mente n??r man arbejder med tekststrenge i C, da det kan f??re til fejl i programmet hvis det ikke h??ndteres korrekt. For eksempel, hvis man allokerer for lidt lager til en tekststreng, kan det f??re til buffer overflow fejl, hvis den overskrider det allokerede lager.

Vi har ogs?? set p?? andre funktioner fra string.h biblioteket, s??som strlen, strcat, strstr, som giver mulighed for at finde l??ngden af en tekststreng, kombinere to tekststrenge og finde en understreng i en tekststreng, og mange andre. Disse funktioner g??r det nemmere at arbejde med tekststrenge i C og kan spare tid og kode.

Vi har ogs?? set p?? eksempler p?? programmer, der behandler tekst, som kan omfatte at l??se tekst fra en fil, manipulere tekststrenge for at ??ndre deres format eller indhold, og udskrive tekst til en sk??rm eller en fil. Dette kan omfatte at l??se en fil linje for linje, at s??ge efter specifikke ord i en tekstfil, eller at ??ndre formatteringen af tekst i en fil.

Alt i alt, har vi i denne lektion set p?? v??sentlige emner som datatypen char og tekststrenge i C-programmering, samt de funktioner og metoder, der er tilg??ngelige for at arbejde med tekst i C. Det er vigtigt at have en grundig forst??else af disse emner for at skrive effektiv og robust kode, der kan h??ndtere tekst data.

### **Lektion 10: Datastrukturer - Structs??(2.11.2022)**

I denne lektion har vi set p?? datastrukturer, specifikt structs, i C-programmering.

Vi har set p?? hvordan structs kan bruges til at gemme og organisere data i C ved at definere en datatype, der best??r af flere felter, hver med deres egen datatype.

```c
struct Person {
    char name[20];
    int age;
    char address[100];
};
```

Vi har ogs?? set p?? varianter af structs, s??som unions og structs med bitfelter. Unions giver mulighed for at gemme forskellige datatyper i samme variabel, mens structs med bitfelter giver mulighed for at spare lager ved at gemme data i mindre bit-felter.

Vi har set p?? arrays af structs og structs med arrays, som giver mulighed for at gemme flere instanser af en struct eller en array i en struct. Dette kan v??re nyttigt for at organisere og h??ndtere data i store eller komplekse programmer.

Vi har ogs?? kort n??vnt forholdet mellem structs og classes i objekt-orienterede programmeringssprog. Structs er en form for simpel datastruktur, mens classes er en avanceret datastruktur med funktioner og metoder, der kan arbejde p?? dataene.

Alt i alt, har vi i denne lektion set p?? v??sentlige emner som datastrukturer og structs i C-programmering, samt varianterne af structs og deres anvendelser i at organisere og h??ndtere data i C. Det er vigtigt at have en grundig forst??else af disse emner for at skrive effektiv og organiseret kode i C.

### **Lektion 11: Rekursion (4.11.2022)**

I denne lektion har vi set p?? rekursive procedurer og funktioner i C-programmering.

Rekursion er en metode, hvor en funktion kalder sig selv, indtil et bestemt stop-vilk??r er opfyldt. Dette kan v??re en effektiv metode til at l??se problemer, der kan deles op i mindre dele af samme type. For eksempel kan en rekursiv funktion til at beregne factorial af et tal n defineres som:

```c
int factorial(int n) {
    if (n == 1) {
        return 1;
    }
    return n * factorial(n - 1);
}
```

Vi har ogs?? set p?? rekursive del og hersk algoritmer, som er en metode til at l??se problemer ved at opdele dem i mindre dele og l??se dem individuelt. En kendt eksempel p?? en rekursiv del og hersk algoritme er quicksort.

Vi har set p?? eksempler p?? meget hurtige og meget langsomme rekursive algoritmer, og hvordan valget af rekursion kan p??virke ydeevnen af programmet. Det er vigtigt at v??lge den rigtige rekursive metode og at afslutte rekursionen korrekt for at undg?? at programmet g??r i en evig loop og utilstr??kkelig hukommelse.

Alt i alt, har vi i denne lektion set p?? v??sentlige emner som rekursive procedurer og funktioner i C-programmering, samt metoder til at l??se problemer ved hj??lp af rekursion og deres p??virkning p?? ydeevnen af programmet. Det er vigtigt at have en grundig forst??else af rekursion og dens brug for at skrive effektiv og organiseret kode i C.

### **Lektion 12: Input/output og Filer (9.11.2022)**

I denne lektion har vi set p?? filbegreber. Vi l??rte om forskellen mellem tekstfiler og bin??re filer, og hvordan de h??ndteres forskelligt. Vi l??rte ogs?? om sekventielle filer og random access filer og hvordan de kan bruges til forskellige form??l.

Vi gennemgik ogs?? hvordan filer h??ndteres i C-programmering, herunder brugen af funktionerne fopen, fclose, fread og fwrite for at ??bne, lukke, l??se fra og skrive til filer.

Vi ??vede ogs?? mere p?? input og output ved hj??lp af funktionerne scanf og printf. Eksempelvis kan vi bruge scanf til at indtaste data fra brugeren og gemme det i en variabel, fx:

```c
int alder;
printf("Indtast din alder: ");
scanf("%d", &alder);
```

Og vi kan bruge printf til at udskrive data til sk??rmen, fx:

```c
printf("Din alder er: %d", alder);
```

Vi l??rte ogs?? om formatering af output ved hj??lp af placeholders i printf-funktionen, fx:

```c
printf("Din alder er: %d ??r", alder);
```

Alt i alt, var det en informativ lektion hvor vi fordybede os i filbegreber, input/output og C-programmering.

### **Lektion 13: Dynamiske datastrukturer - lister og tr??er (11.11.2022)**

I denne lektion, den 11. november 2022, har vi set p?? dynamiske datastrukturer, som er datastrukturer, der kan ??ndre st??rrelse og form under k??rslen. Vi har fokuseret p?? lister og tr??er, som er to af de mest almindelige dynamiske datastrukturer.

Vi startede med at se p?? k??dede lister, som er en simpel form for datastruktur, der best??r af en r??kke elementer, hvor hvert element har en reference til det n??ste element i listen. Hvert element i en k??de liste er kendt som en node, og kan indeholde en v??rdi og en reference til det n??ste element.

For eksempel kan vi bruge en k??de liste til at implementere en stak, hvor det nyeste element tilf??jes til toppen og det ??ldste element fjernes fra toppen.

```c
struct Node {
    int data;
    Node* next;
};
```

Her er et eksempel p?? en node i en k??de liste.

Vi s?? ogs?? p?? varianter af k??dede lister, s??som dobbeltek??dede lister og cirkul??re lister. En dobbeltek??det liste har referencer til b??de det n??ste og det forrige element i listen, mens en cirkul??r liste har en reference til det f??rste element i listen som sidste element.

Derefter gik vi videre til at se p?? bin??re tr??er, som er en mere avanceret form for datastruktur. Et bin??rt tr?? best??r af elementer kendt som noder, hvor hver node kan have op til to under-elementer. Det kan bruges til at implementere en r??kke forskellige algoritmer og datastrukturer. Et eksempel er bin??re s??getr??er, hvor hvert element er sorteret i en bestemt orden, s?? det kan bruges til hurtigt at s??ge efter et bestemt element.

```c
struct Node {
    int key;
    Node *left, *right;
};
```

Her er et eksempel p?? en node i et bin??rt tr??.

Vi l??rte ogs?? om traversering af tr??er, s??som pre-order, in-order, og post-order traversering. Pre-order traversering bes??ger f??rst roden, derefter venstre side og til sidst h??jre side. In-order traversering bes??ger venstre side f??rst, derefter roden og til sidst h??jre side. Post-order traversering bes??ger f??rst venstre side, derefter h??jre side og til sidst roden. Det er is??r nyttigt n??r man skal slette et element i et bin??rt tr??, da det sikrer at elementet f??rst slettes efter at dets under-elementer er blevet slettet.

Vi har ogs?? set p?? hvordan pointere kan bruges til at implementere dynamiske datastrukturer. Pointere er variabler, der indeholder en reference til en anden variabel, og kan bruges til at ??ndre st??rrelsen og formen af en datastruktur under k??rslen. Pointere er is??r nyttige i kombination med dynamiske datastrukturer som lister og tr??er, da de giver mulighed for at ??ndre st??rrelsen og formen af datastrukturen under k??rslen.

Eksempel p?? brug af pointer i k??dede lister:

```c
Node* head = NULL;
head = (Node*)malloc(sizeof(Node));
```

Her er et eksempel p?? hvordan pointere kan bruges til at oprette en ny node i en k??de liste og allokere plads i hukommelsen til denne node.

Alt i alt var det en detaljeret og informativ lektion, hvor vi dykkede dybt ned i dynamiske datastrukturer og hvordan de kan bruges til at implementere avancerede algoritmer og datastrukturer i programmering. Vi s?? p?? k??dede lister, varianter af k??dede lister, bin??re tr??er og bin??re s??getr??er, og hvordan pointere kan bruges i forbindelse med disse datastrukturer.
