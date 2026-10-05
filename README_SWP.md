# Mitschrift 4 BHK

## Methoden und Funktionen

sind Codeabschnitte, die bestimmte Aufgaben ausführen. Sie sind wiederverwendbar und können Parameter entgegennehmen, um unterschiedliche Ergebnisse zu liefern. In der Programmierung werden Methoden und Funktionen verwendet, um den Code zu strukturieren, die Lesbarkeit zu verbessern und die Wartung zu erleichtern.

## Unterschied

#### Methoden

gehören meist immer zu einer Klasse oder einem Objekt und werden aufgerufen, um das Verhalten dieses Objekts zu ändern oder Informationen darüber abzurufen. Sie sind in der Regel an die Instanz eines Objekts gebunden und können auf dessen Eigenschaften zugreifen.

#### Funktionen

sind eigenständige Codeblöcke, die unabhängig von Klassen oder Objekten existieren. Sie können überall im Code aufgerufen werden und sind nicht an eine bestimmte Instanz gebunden. Funktionen können Parameter entgegennehmen und Werte zurückgeben, um verschiedene Aufgaben auszuführen.

## CSS Selektoren

sind Muster, die verwendet werden, um HTML-Elemente auf einer Webseite auszuwählen und zu stylen. Sie ermöglichen es Entwicklern, gezielt bestimmte Elemente anzusprechen und deren Darstellung anzupassen. CSS Selektoren können auf verschiedene Arten definiert werden, z.B. durch Klassen, IDs, Attribute oder Pseudoklassen.

## event driven programming

Ereignissteuerung, man kann einen event listener einfügen der überprüft ob ein bestimmtes Ereignis (z.B. ein Klick auf einen Button) stattgefunden hat und daraufhin eine bestimmte Funktion ausführt. Dies ermöglicht eine reaktive Programmierung, bei der das Verhalten einer Anwendung auf Benutzerinteraktionen oder andere Ereignisse reagiert.

JS - Property
HTML - Attribute

## Zuständigkeiten

### HTML

ist der Aufbau einer Webseite. Es definiert die Struktur und den Inhalt der Seite, indem es verschiedene Elemente wie Überschriften, Absätze, Bilder, Links und Formulare verwendet. HTML ist die Grundlage jeder Webseite und wird von Webbrowsern interpretiert, um die Inhalte anzuzeigen.

### JS

ist die Programmiersprache, die das Verhalten und die Interaktivität einer Webseite steuert. Mit JavaScript können Entwickler dynamische Inhalte erstellen, Benutzerinteraktionen verarbeiten, Daten abrufen und manipulieren sowie Animationen und Effekte implementieren. JS wird in der Regel in Verbindung mit HTML und CSS verwendet, um moderne Webanwendungen zu entwickeln.
Das JS-Sheet wird immer einmal am Anfang geladen.

### CSS

ist die Stylesheet-Sprache, die das Aussehen und die Gestaltung einer Webseite definiert. Mit CSS können Entwickler das Layout, die Farben, Schriftarten, Abstände und andere visuelle Aspekte von HTML-Elementen anpassen. CSS ermöglicht es, das Design einer Webseite konsistent zu gestalten und das Erscheinungsbild auf verschiedenen Geräten und Bildschirmgrößen zu optimieren.

## DOM (Document Object Model)

ist die hierachische Struktur von HTML-Elemnten, wobei die Wurzel (Root) das HTML-Tag darstellt. Auch bekannt als DOM-Tree (Document Object Model Tree). -- Ein Model des HTML-Dokuments.
Baum = Dokument
document.body --> body in JS ausgewählt.
DOM Manipulation = das Ändern von HTML-Elemente über JS.

### Json - Key-Value-Pairs

### XML - Tag-Attribute-Pairs

## Frontend Frameworks

versuchen weniger die HTML, CSS und JS zu trennen, sondern sie nehmen z.B. eine Liste machen daraus einen UI-Komponente, diese ist abgeschlossen und beinhaltet JS, CSS und HTML. Template (Vorlage) --> in HTML

Also man nimmt das HTML als Vorlage und greife dann mit JS auf die Daten zu, die man in die Vorlage einfügt.

<ul>  
   for item inlist}
   <li>{item}</li>
</ul>  
  
### So wäre es in Svelte besser
```html
<script>
    let list = $state(["Brot", "Bier"]);
    let newItem = $state("");
    function addItem(){
        list.push(newItem)
    }
    
    let name = $state("Markus"); //nennt man Rune, sorgt dafür, dass es in beide richtungen geht - bind auch wichtig
</script>

<ul>
    {#each list as item}
        <li onlick={deleteItem}>{item}</li>
    {/each}
</ul>

<input type="text" bind:value={newItem}>
<button onclick={addItem}>Add Item</button>

<p>{name}</p>
```
JS --> Daten + Funktionen

let arr = [1, 2, 3, 4, 5]  
arr = [4,5,6] --> Zuweisung  
arr.push(7) --> Mutation

## Svelte

_$state_ in svelte sorgt dafür, dass die Daten in beide Richtungen gebunden sind. Wenn sich die Daten ändern, wird die UI automatisch aktualisiert und umgekehrt. Ist die wichtigste Rune in Svelte, da sie die Reaktivität der Anwendung ermöglicht und sicherstellt, dass die Benutzeroberfläche immer den aktuellen Zustand der Daten widerspiegelt. Gespeichert im RAM am lokalen PC.

_$derived_ in svelte ist eine Möglichkeit, abgeleitete Zustände zu erstellen, die auf anderen Zuständen basieren. Es ermöglicht die Berechnung von Werten, die von einem oder mehreren Zuständen abhängen, und sorgt dafür, dass diese Werte automatisch aktualisiert werden, wenn sich die zugrunde liegenden Zustände ändern. Macht eine Variable von einer anderen abhängig.

_$$effect_ in svelte ist eine Möglichkeit, eine Art Konsturktor zu erstellen, der auf Änderungen von Zuständen reagiert und bestimmte Aktionen ausführt. Es ermöglicht die Ausführung von Code, wenn sich bestimmte Zustände ändern, und kann verwendet werden, um Nebenwirkungen zu handhaben oder asynchrone Operationen durchzuführen. Ist der Konsturktor unserer Komponenten.

### Das Gegenstück von GUI (Graphic User Interface) ist CLI (Command Line Interface)

_$props_ in Svelte sind Eigenschaften, die an eine Komponente übergeben werden, um ihr Verhalten oder ihre Darstellung zu steuern. Sie ermöglichen es, Daten von einer übergeordneten Komponente an eine untergeordnete Komponente weiterzugeben und so die Wiederverwendbarkeit und Modularität des Codes zu verbessern. Props werden in der Regel als Attribute in der HTML-Syntax der Komponente definiert und können verschiedene Datentypen wie Strings, Zahlen, Arrays oder Objekte enthalten.
Props sind custom-Attribute für meine custom-Componente.  
Selbst erstellte Attribute, die man an einen Komponente übergibt, um ihr Verhalten zu steuern.

## Was sind Komponenten?

Komponenten sind eigenständige, wiederverwendbare Bausteine einer Anwendung, die eine spezifische Funktion erfüllen. In Svelte sind Komponenten HTML-Dateien mit eingebettetem JavaScript und CSS. Sie können Props entgegennehmen und Ereignisse auslösen, um mit anderen Komponenten zu kommunizieren.

### Verschachtelung von Komponenten

Parent.svelte

```html
<script>
  import Child from "./Child.svelte";
</script>

<ul>
  <child props="xyz"> </child>
</ul>
```

## Kontrollfunktionen

### bedingte Verzweigungen

sind if, else if, else, switch-case

##### binäre Operatoren gehören aritmetische Operatoren (+, -. \* ,...) dazu

##### ternäre Operatoren haben 3 Operatoren

z.B. (bedingung) ? (wenn wahr) : (wenn falsch) -- (in Klammern Operatoren)

### stack vs queue

stack = LIFO (Last In First Out)
queue = FIFO (First In First Out)

## Eventgesteuerte Programmierung

bind verbindet eine Gabefeld mit einer Variable.
bind und $state sind dafür sehr essentiell.

```html
<script>
  let name = $state("world");
</script>

<input bind:value="{name}" />

<h1>Hello {name}!</h1>
```

In Svelte können wir trotz unterschiedlicher Datentypen einfach die Felder miteinander verbinden.

```html
<script>
  let a = $state(1);
  let b = $state(2);
</script>

<label>
  <input type="number" bind:value="{a}" min="0" max="10" />
  <input type="range" bind:value="{a}" min="0" max="10" />
</label>

<label>
  <input type="number" bind:value="{b}" min="0" max="10" />
  <input type="range" bind:value="{b}" min="0" max="10" />
</label>

<p>{a} + {b} = {a + b}</p>
```

```html
<script>
  let yes = $state(false);
</script>

<label>
  <input type="checkbox" bind:checked="{yes}" />
  Yes! Send me regular email spam
</label>

{#if yes}
<p>Thank you. We will bombard your inbox and sell your personal details.</p>
{:else}
<p>You must opt in to continue. If you're not paying, you're the product.</p>
{/if}

<button disabled="{!yes}">Subscribe</button>
```
