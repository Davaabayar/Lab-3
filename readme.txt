Solutions

*** SOLUTION 1 ***
Sol1.html - Display's grid layout using grid-template-areas & grid-area
-------------
.container {
    display: grid;
    grid-template-columns: 50% 25% 25%;
    grid-template-rows: 200px 200px;
    grid-template-areas: 'item-a item-b item-c''item-a item-d item-e';
}

.item {
    border: 1px solid #ccc;
}

.item-a {
    grid-area: item-a;
}
-------------

*** SOLUTION 2 ***
Sol2.html - used grid-template-columns & defined bigger item as .boxFull using row & column start end line.
-------------

    .wrapper {
        display: grid;
        grid-template-columns: 50% 25% 25%;
        grid-auto-rows: 200px;
        grid-gap: 20px;
    }
    .boxFull {
        grid-column-start: 1;
        grid-column-end: 2;
        grid-row-start: 1;
        grid-row-end: 3;
        position: relative;
    }
  
    <div class="wrapper">
        <div class="box boxFull">One</div>
        <div class="box box2">Two</div>
        <div class="box box3">Three</div>
        <div class="box box4">Four</div>
        <div class="box box5">Five</div>
    </div>
-------------

*** SOLUTION 3 ***
Sol3.html - Used nested grid sol3.html + sol3style.css
-------------

*** SOLUTION 4 ***
Solution 4: Final solution - index.html
Divided column by 2fr 1fr 1fr and defined bigger cell using grid-row property start end row line.
Responsive.
-------------
.container {
    min-height: 100vh;
    width: 1280px;
    margin: 0 auto;
}
.wrapper {
    display: grid;
    grid-template-columns: 2fr 1fr 1fr;
    grid-gap: 1em;
    grid-auto-rows: minmax(170px, auto);
}
.wrapper .big {
    grid-row: 1/3;
}
<div class="wrapper">
    <div class="big"></div>
    <div class="small"></div>
    <div class="small"></div>
    <div class="small"></div>
    <div class="small"></div>
</div>
-------------

Other options:

*** SOLUTION 5 ***
Name bigger cell using grid-area and define the grid content using that name in grid property.

.item1{
    grid-area: A;
}
.container{
    display:grid;
    grid:'A A . .'
    'A A . .';
    grid-gap:10px;
}

*** SOLUTION 6 ***
Name each grid cell items using grid-area property and define grid content using thouse names in grid property

.item1{grid-area: A;}
.item2{grid-area: B;}
.item3{grid-area: C;}
.item4{grid-area: D;}
.item5{grid-area: E;}

.container{
    display:grid;
    grid:'A B C'
    'A A D E';
    grid-gap:10px;
}

*** SOLUTION 7 ***
Define grid area for item1 using row & column start line & span
grid-area: <grid-row-start> / <grid-column-start> / <grid-column-end> / <grid-row-end>

.item1{
    grid-area: 1 / 1 / span 2 / span 2;
}

*** SOLUTION 8 ***
Define grid area for item1 using line number
.item1{
    grid-column-start:1;
    grid-column-end:3;
    grid-row-start:1;
    grid-row-end:3;
}

Solution 9: Short hand definition for Solution 8
.item1{
    grid-column: 1/3;
    grid-row:1/3;
}
