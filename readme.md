# Procesverslag
**Auteur:** -AnneFleur Frans-

**Het werk:** [opdracht 1](opdracht1/index.html) en [opdracht 2](opdracht2/index.html)


Markdown cheat cheet: [Hulp bij het schrijven van Markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet). Nb. de standaardstructuur en de spartaanse opmaak zijn helemaal prima. Het gaat om de inhoud van je procesverslag. Besteedt de tijd voor pracht en praal aan je website.



## Bronnenlijst
1. -https://codepen.io/goodkatz/pen/LYPGxQz?editors=1100
2. https://www.w3schools.com/css/




## Je 'posts' (je code-dagboek)

Je procesverslag is een soort dagboek.
Bij elk voortgangsgesprek en het eindgesprek voeg je een ‘post’ aan je dagboek toe.

In zo’n ‘post’ neem je op:
- darkmode 
- golven animatie op safari


https://user-images.githubusercontent.com/65559359/117783273-acb41200-b242-11eb-902e-1fa14e4118bd.MOV



https://user-images.githubusercontent.com/65559359/117786401-bf7c1600-b245-11eb-9018-9747a340a5f6.MOV






/* de code */
CSS 

*, *::before, *::after {
  box-sizing: border-box;
}

html, body {
  height:100%;
  width: 100%;
  margin:0;
  display:flex;
    justify-content:center;
    align-items:center;
}

body {
/*    light theme*/
    --backgroundColor1: aliceblue;
    --backgroundColor2: white;
    background-color: var(--RoodLetter);
    --mijnkleur:
    --RoodLetter: red;
    --BlauwLetter: blue;
    --GreenLetter: green;
    --BlackLetter: black;
    --YellowLetter: yellow;

    color: var(--RoodLetter);
    color:var(--textColor);

    background-color: aliceblue;

    @media {
  body:not(.lightMode) {
    /* dark theme */
    --backgroundColor1: midnightblue;
    --backgroundColor2: white;

    --RoodLetter: red;
    --BlauwLetter: blue;
    --GreenLetter: green;
    --BlackLetter: black;
    --YellowLetter: yellow;
  }
}
}

section {
    position: relative;
    text-align: center;
  min-height:5em;
  margin:0;
  padding:5vmin;
  list-style:none;

  display:flex;
  grid-template-columns: repeat( auto-fit, max(15em, 30vmin));
  justify-content:center;
  width: 50%;
  height: 100%;

  background:white;
}

body {
  min-height:100%;
  margin:0;
  padding:0;
  list-style:none;

  grid-template-columns: repeat( auto-fit, max(5em, 2vmin));
}

/*----------------------------------------------------*/
/* TOKOY O 2O2O anitmatie 1*/
section:nth-of-type(1) {
     font-family: 'Black Han Sans', sans-serif;
    font-size: 2em;
    padding: 50% 0;
    background-color: var(--backgroundColor1);
    transform-origin: center bottom;
}

section:nth-of-type(1) h1 {
    position: absolute;
    padding: 0.5em;
    font-size: 0.8em;
    z-index: 100;
    top: 50%;
}

section:nth-of-type(1):hover {
    transform:translate(.1em, -.15em) scale(1);
    text-shadow:.1em 0 0 MidnightBlue, .6em .6em .1875em rgba(0,0,50,.375);
}

section:nth-of-type(1):hover span {
    transform-origin:center bottom;

    animation-name:groterAni, verkleurAni;
    animation-duration: 5s;
    animation-iteration-count: infinite;
    animation-timing-function:ease-in-out;
    display: inline-block;
    padding: 1em .05em;
}


/*TOKYO O 2O2O letters per span*/
span:nth-of-type(1) {
    --mijnkleur:black;
    animation-delay:0s, 0.25s;
}

span:nth-of-type(2) {
    --mijnkleur:blue;
    animation-delay:0.25s, 0.5s;
}

span:nth-of-type(3) {
    --mijnkleur:black;
    animation-delay:0.5s, 0.75s;
}

span:nth-of-type(4) {
    --mijnkleur:black;
    animation-delay:0.75s, 1s;
}

span:nth-of-type(5) {
    --mijnkleur:black;
    animation-delay:1s, 1.25s;
}

span:nth-of-type(6) {
    --mijnkleur:red;
    animation-delay:1.25s, 1.5s;
}

span:nth-of-type(7) {
    --mijnkleur:black;
    animation-delay:1.5s, 1.75s;
}

span:nth-of-type(8) {
    --mijnkleur:yellow;
    animation-delay:1.75s, 2s;
}

span:nth-of-type(9) {
    --mijnkleur:black;
    animation-delay:2s, 2.25s;
}

span:nth-of-type(10) {
    --mijnkleur:green;
    animation-delay:2.25s, 2.5s;
}

/*animatie groter*/
@keyframes groterAni {
    0% {
        transform:scale(1);
    }
    30% {
        transform:scale(1.5);
    }
    50% {
        transform:scale(1.5);
    }
    75% {
        transform:scale(1.5)
    }
    100% {
        transform:scale(1)
    }
}

/*anitmatie verkleuren*/
@keyframes verkleurAni {
    0% {
        color:inherit;
    }
    5%, 80% {
        color:var(--mijnkleur);
    }
    100% {
        color:inherit;
    }
}

/*-----------------------------------------*/
/* duiken inbeeld animatie 2*/
section:nth-of-type(2) {
    display: flex;
    font-family: 'Black Han Sans', sans-serif;
    background-color: var(--backgroundColor2);
    padding: 30em 0;
    position: relative;
    overflow: hidden;
}

section:nth-of-type(2) h1 {
    position: absolute;
    padding: 0;
    font-size: 2.5em;
    z-index: 100;
    top: 50%;
}

.white space {
    padding: 0 0 1em 0;
}

/* de zwarte balk*/
section:nth-of-type(2):before {
    content:"";
    position:absolute;
    width:13em; height:8em;
    border:solid .2em black;
    border-radius:1.5em;

    background-image:radial-gradient(transparent .25em, white .25em .625em, transparent .625em),

    background-size:1.5em 1.5em;
    background-repeat:no-repeat;
    background-position:12em 10em, 11em 20em;
    z-index: 99;
    top: 50%;
}

/* de witte streep op de balk*/
section:nth-of-type(2):after {
    content: "";
    position: absolute;
    width: 2.5em;
    border:solid .25em white;
    left: 36%;
    top: 30em;
    z-index: 110;
}

/*
section:nth-of-type(2):hover {

}
*/

/* de golven*/
.wave placement {
  position: absolute;
    width: 50%;
    height: 100%;
    top: 0em;
    z-index: 1;
}

.waves {
  width: 100%;
  height: 30em;
  margin-bottom:-7px;
  min-height:200px;
  max-height:150px;
}

section:nth-of-type(2):hover {
    animation-iteration-count: infinite;
    animation-fill-mode: both;
}

.bewegen > use{
  animation: move 25s cubic-bezier(.50,.5,.40,.5) infinite;
}
.bewegen:nth-of-type(1) {
  animation-delay: 1s;
  animation-duration: 8s;
}
.bewegen > use:nth-of-type(2) {
  animation-delay: -2s;
  animation-duration: 9s;
}
.bewegen > use:nth-of-type(3) {
  animation-delay: -3s;
  animation-duration: 12s;
}
.bewegen > use:nth-of-type(4) {
  animation-delay: -4s;
  animation-duration: 21s;
}

@keyframes move {
  0% {
   transform: translate3d(-90px,0,0);
  }
  100% {
    transform: translate3d(85px,0,0);
  }
}

/*bellen*/
section:nth-of-type(2) span:nth-of-type(1):before {
    content:"";
    position:absolute;
    width:1.5em; height:1.5em;

    background-color:lightblue;
    border-radius:12em;

    overflow:hidden;
    top: 30em;
    left: 36%;
    z-index: 112;
}

section:nth-of-type(2) span:nth-of-type(1):after {
    content:"";
    position:absolute;
    width:1em; height:1em;

    background-color:lightblue;
    border-radius:12em;

    overflow:hidden;
    top: 29em;
    left: 40%;
    z-index: 113;
}
section:nth-of-type(2).wave placement{
animation-name: golven;
    animation-iteration-count: infinite;
    animation-timing-function:ease-in-out;
}

Shrinking for mobile
@media (max-width: 768em) {
  .waves {
    height: 500em;
    min-height:6em;
  }

