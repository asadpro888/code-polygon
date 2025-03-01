.
import './App.css'
import styled, {css} from 'styled-components';

const Wrapper = styled.section`
  padding: 4rem;
  margin: 2rem;
  background-color: ${({ color }) => color ? color : 'black'};
  ${({ is3D }) => is3D && css`
  background-color: yellow;
  transform: rotateY(180deg);
  box-shadow: 1rem 1rem black;
  `}
`

const Title = styled.h1`
  font-size: 36px;
  color: white;
  text-align: center;
  font-family: cursive;
`
function App() {
 

  return (
    <>
      <Wrapper>
        <Title>Styled Components</Title>
      </Wrapper>
      <Wrapper color={'pink'}>
        <Title>Styled Components</Title>
      </Wrapper>
      <Wrapper is3D={true}>
        <Title>Styled Components</Title>
      </Wrapper>
    </>
  )
}

export default App
import React from 'react';
import { useState } from 'react';

const ComponentsWithUseState = () => {
    const [count, setCount] = useState(0);
    const renderBar = () => {
        const bars = [];
        for (let i = 0; i < count; i++) { 
            bars.push( < div
                 style={{
                  backgroundColor: 'rgba(212, 113, 211, 0.3)',
                  width: '10%',
                  height: '100%',
              }}
                  
              ></div>)
    }
    return bars;
   }
  return (
    <div>
          <h1>useState</h1>
          <div style={{
              border: '0.1rem solid rgba(0,0,0,0.3)',
              height: '100px',
              width: '80%',
              display: 'flex',
              margin: '2rem auto',
          }}>
              {renderBar()}
          </div>
          <button onClick={() => setCount(count - 1)}>Subtract bar</button>
          <button onClick={() => setCount(count + 1)}>Add Bar</button>
    </div>
  )
}

export default ComponentsWithUseState

////////////////////////////////////////////////
import { useState } from 'react'
const UseContext = () => {
    const [count, setCount] = useState(0)
  return (
    <div>
          <h1>{ count}</h1>
          <button onClick={() => setCount(count + 1)}>Add</button>
          <button onClick={()=> setCount(count - 1)}>sub</button>
    </div>
  )////////////////////////////////////////////
   <script>
        gsap.to(".box", {opacity: 0, duration: 4, y: -50, x: -100, ease: 'elastic(1, 0.3)', delay:1.1})
        gsap.from(".box1", { opacity: 0, duration: 1, y: -50, x: -100, delay: 1.4, stagger: 0.6 })
     // //////animation with gsap
      const myText = new SplitType('#my-text')
        gsap.to('.char', {
            y: 0,
            stagger: 0.05,
            delay:0.2,
            duration: 1,
        })
    </script>
    /////////////////////////////////////////////
    <script>
       TweenMax.staggerTo('.img', 1, {y:100}, 0.2);
        
    </script>
    //routing lesson//

    import { BrowserRouter } from 'react-router-dom';
    import {Route,  Routes} from 'react-router-dom'
     <Routes>
        <Route exact path='/' component={<Home/>} />
      </Routes>  

    /////routing lesson/////
}
////algoritmes///
const studentDatabase = ['jordan', 'erick', 'john', 'michel'];

const findStudent = (allStudents, studentName) => {
    for (let i = 0; i < allStudents.length; i++){
        if (allStudents[i] === studentName) { 
            console.log(`Found ${studentName}`);
        }
    }
}

findStudent(studentDatabase, "erick");
console.log(findStudent);
-----------------------------------------------
const groceries = ['milk', 'bread', 'eggs', 'flour', 'choose', 'sugar'];

const searchForItem = (item) => {
    for (let i = 0; i < groceries.length; i++){
        if (groceries[i] === item) { 
            console.log(`Found: ${item}`);
        }
    }
 for (let j = 0; j < groceries.length; j++){
        if (groceries[j] === item) { 
            console.log(`Found: ${item} 2`);
        }
    }    
}
searchForItem('eggs');
----------------------------------------------
const numbers = [1, 2, 3, 4, 5];

const getElement = (arr, index) => arr[index];
console.log(getElement(numbers, 0));
---------------------------------------------
function findPairs(arr) {
    for (let i = 0; i < arr.length; i++){
        for (let j = i + 1; j < arr.length; j++) { 
            console.log(`Pair: ${arr[i]}, ${arr[j]}`);
        }
    }
}

const numbers = [1, 2, 3, 4, 5];
findPairs(numbers);
-------------------------------------------
for (let a = 0; a < 100; a++){
    if (a % 3 == 0 && a % 5 == 0) { }
    else if (a % 3 == 0) { }
    else if (a % 5 == 0) { }
    else { }
    console.log([a]);
}
-----------------------------------------
const text = 'i am sorry'

for (let a = 1; a < text.length; a++){
    console.log(text, [a]*100);
}
----------------------------------------
class Node {
    constructor(value) {
        this.val = value;
        this.left = null;
        this.right = null;
    }
}
const a = new Node('a');
const b = new Node('b');
const c = new Node('c');
const d = new Node('d');
const e = new Node('e');
const f = new Node('f');


a.left = b;
a.right = c;
b.left = d;
b.right = e;
c.right = f;


// a -> b -> d -> e -> c -> f
------------------------------------
let text1 = 'ass';
let text2 = 'love';
let text3 = 'hate';
let text4 = 'forgotten';
let text5 = ',love';
let text6 = ',hate';
let text7 = ',love';
let text8 = ',hate';
class Mates{
    constructor(val) {
        this.val = val;
        this.K = text1+text5;
        this.L = text2+text6;
        this.M = text3+text7;
        this.S = text4+text8;
    }
}

const a = new Mates('K');
const b = new Mates('L');
const c = new Mates('M');
const d = new Mates('S');

a.K = c;
b.L = d;
c.M = a;
d.S = b;

console.log( new Mates)
// a -> b -> d -> e -> c -> f
------------------------------------
class Node{
    constructor(val) { 
        this.val = val;
        this.left = null;
        this.right = null;
    }
}


const depthFirstValues = (root) => {
    const values = [root];
    while (values.length > 0) {
        const current = values.pop();
        console.log(current.val);
        if (current.left) values.push(current.left);
        if (current.right) values.push(current.right);
    }
};
const a = new Node('a');
const b = new Node('b');
const c = new Node('c');
const d = new Node('d');
const e = new Node('e');
const f = new Node('f');

a.left = b;
a.right = c;
b.left = d;
b.right = e;
c.right = f;
depthFirstValues(a)
-------------------------------------------
const net = new brain.NeuralNetwork()

const data = [{"input":{"r":0,"g":0,"b":0},"output":[1]},{"input":{"r":1,"g":1,"b":1},"output":[0]},{"input":{"r":0.944808294257035,"g":0.6674782369918966,"b":0.5766399840934922},"output":[0]},{"input":{"r":0.5639948440377565,"g":0.7176485901155334,"b":0.09089889404108642},"output":[1]},{"input":{"r":0.1735805927844496,"g":0.055394078147760206,"b":0.5718893632998685},"output":[1]},{"input":{"r":0.9981576669053267,"g":0.5599753720355853,"b":0.14004222444100312},"output":[0]},{"input":{"r":0.19516320408209298,"g":0.19675137123292608,"b":0.6611291964504313},"output":[1]},{"input":{"r":0.6164834530502397,"g":0.8040215937551165,"b":0.8850111600872357},"output":[0]},{"input":{"r":0.3041418057844665,"g":0.44672594827873735,"b":0.2457621104163552},"output":[1]},{"input":{"r":0.9700762875730256,"g":0.04347977676242154,"b":0.48983830868727063},"output":[0]},{"input":{"r":0.5208315789104343,"g":0.7362065633265635,"b":0.7122939301003071},"output":[0]},{"input":{"r":0.23520758286480792,"g":0.9557008141546155,"b":0.11014352211423728},"output":[0]},{"input":{"r":0.589232622786013,"g":0.6262382467772079,"b":0.22068417769342719},"output":[1]},{"input":{"r":0.4974235182026916,"g":0.06800405227377082,"b":0.6991588905288477},"output":[1]},{"input":{"r":0.014012292032445028,"g":0.8366939310719097,"b":0.7852317228157895},"output":[0]},{"input":{"r":0.6034691954439091,"g":0.995582899847562,"b":0.07976036555452626},"output":[0]},{"input":{"r":0.3954203797322433,"g":0.9691389246293933,"b":0.5340578656677233},"output":[0]},{"input":{"r":0.597573150116294,"g":0.6469698799143129,"b":0.14327503451373547},"output":[0]},{"input":{"r":0.03137390761585168,"g":0.6714730771317701,"b":0.526269930102498},"output":[1]},{"input":{"r":0.4060610880542337,"g":0.8395520707830146,"b":0.9519617868006716},"output":[0]},{"input":{"r":0.09937849463297255,"g":0.998567114295779,"b":0.7305857380072192},"output":[0]},{"input":{"r":0.19658225353968817,"g":0.34243367565320626,"b":0.6907903948687992},"output":[1]},{"input":{"r":0.14183816462521293,"g":0.5768425498165213,"b":0.20904833189001226},"output":[1]},{"input":{"r":0.1304525766950142,"g":0.15770748106098176,"b":0.1513780578868713},"output":[1]},{"input":{"r":0.08233178944743225,"g":0.13330341221297903,"b":0.9740919835995931},"output":[1]},{"input":{"r":0.6679568819262076,"g":0.2572629537807716,"b":0.056641327982522194},"output":[1]},{"input":{"r":0.9775544056225354,"g":0.6484034439721735,"b":0.35002088833074785},"output":[0]},{"input":{"r":0.4379821477793624,"g":0.8012236229142786,"b":0.9807309238569026},"output":[0]},{"input":{"r":0.1903408797077648,"g":0.8217165591038438,"b":0.7168542544342942},"output":[1]},{"input":{"r":0.3493291422243354,"g":0.7156906546326169,"b":0.8432935745081787},"output":[1]},{"input":{"r":0.9105963156497519,"g":0.9959716499017874,"b":0.38457267991993893},"output":[0]},{"input":{"r":0.5939915201365638,"g":0.2869215845407964,"b":0.6197160854239552},"output":[1]},{"input":{"r":0.8855809221913826,"g":0.7989923584284897,"b":0.0923202306111528},"output":[0]}]

net.train(data)

const colorEl = document.getElementById('color')
const guessEl = document.getElementById('guess')
const whiteButton = document.getElementById('white-button')
const blackButton = document.getElementById('black-button')
const printButton = document.getElementById('print-button')
let color
setRandomColor()

whiteButton.addEventListener('click', () => {
  chooseColor(1)
})

blackButton.addEventListener('click', () => {
  chooseColor(0)
})

printButton.addEventListener('click', print)

function chooseColor(value) {
  data.push({
    input: color,
    output: [value]
  })
  setRandomColor()
}

function print() {
  console.log(JSON.stringify(data))
}

function setRandomColor() {
  color = {
    r: Math.random(),
    g: Math.random(),
    b: Math.random()
  }
  const guess = net.run(color)[0]
  guessEl.style.color = guess > .5 ? '#FFF' : '#000'
  colorEl.style.backgroundColor = 
    `rgba(${color.r * 255}, ${color.g * 255}, ${color.b * 255})`
}
--------------------------------------------
function bubbleSort(arr) {
    for (let i = arr.length - 1; i > 0; i--){
        for (let j = 0; j < i; j++) { 
            if (arr[j] > arr[j + 1]) { 
                let temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }
    return arr;
}

const myArr = [4, 2, 6, 5, 1, 3];
const res = bubbleSort(myArr);
console.log(res);
--------------------------------------
function selectionSort(arr) {
    for (let i = 0; i < arr.lenght; i++){
        let minIndex = i;

        for (let j = i + 1; j < arr.lenght; j++){
            if (arr[j] < arr[minIndex]) { 
                minIndex = j;
            }
        }
        if (i === minIndex) {
            let temp = arr[i];
            arr[i] = arr[minIndex];
            arr[minIndex] = temp;
        }
        return arr;
    }
}

const myArr = [4, 2, 6, 5, 1, 3];
const res = selectionSort(myArr);
console.log(res);
------------------------------let text1 = 'i'
let text2 = 'love'
let text3 = 'you'
class Text{
    constructor(value) {
        this.value = value;
        this.a = text1;
        this.b = text2;
        this.c = text3;
    } 

}

const a = new Text('fuck you');
const b = new Text('is dogshit');
const c = new Text('suck');

a.a = a+a;
b.b = b+b;
c.c = c+c;

console.log(a,b,c);
-----------python----------
user_input = input("enter something: ")
print('you entered', user_input)
----------------------------------
const person = {
    name: 'John',
    age: 30,
    greet: function () {
        console.log('Hi, I am ' + this.name + ' and I am ' + this)

    }
}
const person2 = {
    name: 'Jane',
    age: 30,
    greet: function () {
        console.log('Hi, I am ' + this.name + ' and I am ' + this
        )
    }
}

console.log(person.age)
person.greet()

-----way to ask "i am sorry" by javascript----
function MyFavoriteKdrams() {
    for (let i = 1; i < 100; i++){
        let i = 'i am sorry'
        console.log([i]);
    }
}

MyFavoriteKdrams()

--------------d3.js--------------------------
d3.select();
d3.selectAll();

d3.select('h1').style('color', 'red')
d3.select('h1').style('font-size', '50px')
    .attr('class', 'heading')
    .text('something');

d3.select('body').append('p').text('first paragrah')
    d3.select('body').append('p').text('first paragrah')    
    d3.select('body').append('p').text('first paragrah')
d3.select('body').append('p').text('first paragrah')
    
d3.selectAll('p').style('color', 'blue')
--------------d3.js----------------------
let dataset = [1, 2, 3, 4, 5];

d3.select('body')
    .selectAll('p')
    .data(dataset)
    .enter()
    .append('p')
    .text('D3 is extremly awesome')
    -

--------------simple barchart utilizing d3.js-------
let dataset = [80, 100, 56, 120, 180, 30, 40, 120, 160];

let svgWidth = 500, svgHeight = 300, barPadding = 5;
let barWidth = (svgWidth / dataset.length);

let svg = d3.select('svg')
    .attr("width", svgWidth)
    .attr('height', svgHeight);


let barChart = svg.selectAll('rect')
    .data(dataset)
    .enter()
    .append('rect')
    .attr('y', function (d) {
        return svgHeight - d;
    })
    .attr('height', function (d) {
        return d;
    })
    .attr('width', barWidth - barPadding)
    .attr('transform', function (d, i) {
        let translate = [barWidth * i, 0];
        return 'translate(' + translate + ')';
    })

------------string length in py---------
string_len = 'python'
my_lenght = len(string_len)
print(my_lenght)

print(len('asadprox'))
---------------------------------------
text = 'python'
first_char = text[4]
substring = text[1:2]
print(first_char)
---------string formatting------
name = 'asad'
age = 16

formatted_string = f'my name is {name} i am {age} years old'
print(formatted_string)
-----bg alterer whenever mouse enter------
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.6.0/css/all.min.css" integrity="sha512-Kc323vGBEqzTmouAECnVceyQqyqdsSiqLQISBL29aUW4U/M7pSPA/gEUZQqv1cwx4OnYxTxve5UMg5GT6L4JJg==" crossorigin="anonymous" referrerpolicy="no-referrer" />
    <link rel="stylesheet" href="main.css">
</head>
<body>
    <ul class="sci">
        <li style="--clr:#ff0000"><a href=""><i class="fa-brands fa-youtube"></i></a></li>
         <li style="--clr:#333333"><a href=""><i class="fa-brands fa-x-twitter"></i></a></li>
          <li style="--clr:#00a783"><a href=""><i class="fa-brands fa-whatsapp"></i></a></li>
    </ul>
<script src="https://cdnjs.cloudflare.com/ajax/libs/vanilla-tilt/1.8.1/vanilla-tilt.min.js" integrity="sha512-wC/cunGGDjXSl9OHUH0RuqSyW4YNLlsPwhcLxwWW1CR4OeC2E1xpcdZz2DeQkEmums41laI+eGMw95IJ15SS3g==" crossorigin="anonymous" referrerpolicy="no-referrer"></script>
    <script>
        VanillaTilt.init(document.querySelectorAll(".sci li a"), {
		max: 25,
		speed: 400,
        glare: true
	});
        let list = document.querySelectorAll('.sci li');
        let bg  = document.querySelector('body')
        list.forEach(element => {
            element.addEventListener('mouseenter', () => {
                let color = event.target.style.getPropertyValue('--clr');
                bg.style.backgroundColor = color;
            })
            element.addEventListener('mouseleave', () => {
                bg.style.backgroundColor = '#fff';
            })
        })
    </script>
</body>
</html>
*{
    box-sizing: border-box;
    margin: 0;
    padding: 0;    
}

body{
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    transition: 0.5s;
}

.sci{
    position: relative;
    display: flex;  
    gap: 30px;
}
.sci li{
    list-style: none;
}

.sci li a{
    border-radius: 10px;
    position: relative;
    display: flex;
    justify-content: center;
    align-items: center;
    width: 150px;
    height: 150px;
    background: #fff;
    color: #333;
    font-size: 4rem;
    text-decoration: none;
    box-shadow: 0 25px 35px ;
    transform-style: preserve-3d;
    transition: background 0.25s;
}

.sci li a:hover{
    background: var(--clr);
    box-shadow: 0 25px 35px rgba(0,0,0,0.25);
    border: 5px solid var(--clr)
}

.sci li a i{
    transition: 0.5s;
    pointer-events: none;
}
.sci li a:hover i{
    transform: scale(1.5) translateZ(50px);
    color: #fff;
}
--------------------------------------------
let text = document.querySelector('#text');
let light = document.querySelector('#light');

document.addEventListener('mousemove', (evt) => {
  let mouseX = evt.clientX;
  let mouseY = evt.clientY;
  light.style.left = mouseX + 'px';
  light.style.top = mouseY + 'px';

  let distanceX = mouseX - text.offsetLeft - text.offsetWidth / 2;
  let distanceY = mouseY - text.offsetTop - text.offsetHeight / 2;


  let newShadow = "";
  for (let i = 0; i < 200; i++){
    let shadowX = -distanceX * (i / 200);
    let shadowY = -distanceY * (i / 200);
    newShadow += (newShadow ? ',' : "") + shadowX + 'px' + shadowY + 'px 0 rgba(33,33,33,1';
  }
   text.style.textShadow = newShadow;
})
-------------materialize icons----------------
 <i class="material-icons red-text">warning</i>
     <i class="material-icons black-text">search</i>
     <i class="material-icons black-text">cloud</i>
     <i class="material-icons black-text">desktop</i>
--------------python quiz game----------------------
print("welcome to my computer quiz!")

playing = input('Do you want to play? ')

if playing != "yes":
    quit()
print("okay! Let's play: )")

answer = input("what does CPU stand for? ")
if answer == "central processing unit":
    print("correct! ")
else: 
    print('incorrect')

    answer = input("what does NATO stand for? ")
if answer == "NORTH ATLANTIC TREATY ORGANIZATION":
    print("correct! ")
else:
    print("incorrect")

answer = input("what does sco stand for? ")
if answer == "shanhai treaty organization":
    print("correct! ")
else:
    print("incorrect")

answer = input("what does Brics stand for? ")
if answer == "Brazil, Russia, India, China, South Africa":
    print("correct! ")
else:
    print("incorrect")
-------------------drag & drop-----------------
const draggableElements = document.querySelectorAll('.draggable');
const dropZone = document.getElementById('right');

// Function to handle the beginning of a drag operation
function handleDragStart(event) {
  event.dataTransfer.setData('text/plain', event.target.id);
}

// Function to handle when a draggable element hovers over the drop zone
function handleDragOver(event) {
  event.preventDefault(); // Allow dropping
}

// Function to handle when a draggable element is dropped on the drop zone
function handleDrop(event) {
  event.preventDefault(); // Prevent default behavior (like opening the element)

  const droppedElementId = event.dataTransfer.getData('text/plain');
  const droppedElement = document.getElementById(droppedElementId);

  // Safety check to prevent adding the same element multiple times
  if (droppedElement !== dropZone && !dropZone.contains(droppedElement)) {
    dropZone.appendChild(droppedElement);
  }
}

// Attach event listeners
draggableElements.forEach(element => {
  element.addEventListener('dragstart', handleDragStart);
});

dropZone.addEventListener('dragover', handleDragOver);
dropZone.addEventListener('drop', handleDrop);
--------------------svelte.js---------
<script>
    import Nested from "./Nested.svelte";
    
     let count = 1;
     function Handleclick(){
        count += 1
     }
     function ChangeColor(e){
        document.body.style.backgroundColor = e.target.value;
     }
</script>
<input type="color" on:input={ChangeColor}>
----------------async await-----------
async function getUserCountry() {
    const username = document.getElementById('usernameGet').value;

    if (!username) {
        alert('Please enter a username.');
        return;
    }

    try {
        const response = await fetch(`https://api.github.com/users/${username}`);
    }
    catch (error) {
        alert('Error fetching user data. Please check your internet connection.');
        return;
    }
    
    const userData = await response.json();
    const country = userData.location;
    document.getElementById('countryGet').textContent = `Country: ${country}`;
    
    const commitsResponse = await fetch(`https://api.github.com/users/${username}/commits`);
    const commitsData = await commitsResponse.json();
    const commitsCount = commitsData.length;
    document.getElementById('commitsCount').textContent = `Commits: ${commitsCount}`;
    
    const repositoriesResponse = await fetch(`https://api.github.com/users/${username}/repos`);
    const repositoriesData = await repositoriesResponse.json();
    const repositoriesCount = repositoriesData.length;

    document.getElementById('repositoriesCount').textContent = `Repositories: ${repositoriesCount}`;
    
    const followersResponse = await fetch(`https://api.github.com/users/${username}/followers`);
    const followersData = await followersResponse.json();
    const followersCount = followersData.length;
    document.getElementById('followersCount').textContent = `Followers: ${followersCount}`;

    const followingResponse = await fetch(`https://api.github.com/users/${username}/following`);
    const followingData = await followingResponse.json();
    const followingCount = followingData.length;
    document.getElementById('followingCount').textContent = `Following: ${followingCount}`;
    
    document.getElementById('userDetails').style.display = 'block';
    document.getElementById('error').style.display = 'none';
    document.getElementById('loading').style.display = 'none';
    document.getElementById('usernameGet').value = '';
}
----------------------------------------FETCH API --------
fetch('https://reqres.in/api/users')
    .then(res => res.json())
    .then(data => console.log(data))
    .catch(error => console.log('ERROR'))
---------------------module----------
const hour = 12;

console.log(hour % 12 || 12);
--------------flatMap------------
const offices = [
    {
        name: 'west bank',
        employees: ['john', 'sarah'],
    },
    {
        name: 'east bank',
        employees: ['ban', 'hope'],
    },
    {
        name: 'north bank',
        employees: ['johny', 'kenny'],
    },
];

const employees = offices.flatMap(office => office.employees).flat();
console.log(employees)
--------------------------------js project-------------
let input = document.querySelector('#inp')
let div = document.querySelector('.hh1');

------------------entries---------------
const params = {
    search: 'javascript tutorials',
    page: 2,
    limit: 10,
    order: 'desc',
    sort: 'relevance'
};


const result = Object.entries(params);


for (const [key, value] of result) {
    console.log(`${key}: ${value}`);
}


input.addEventListener('input', function () {
    div.textContent = this.value;
});
----------------------------------------------
const str = "john works from home and jane works from office";
const result = str.match(/([a-z]+ works from [a-z]+)/ig);

console.log( result );
---------------Math.random----------------
const min = 50;
const max = 100;


let random = Math.floor(Math.random() * max) + min;
console.log(random);
---------------Random number generator------
const myButton = document.getElementById('myButton');
const myLabel = document.getElementById('myLabel');
const min = 10;
const max = 60;
let randomNum;

myButton.addEventListener('click', () => {
  randomNum = Math.floor(Math.random() * (max - min + 1)) + min;
  myLabel.textContent = `Random number: ${randomNum}`;
});
---------------ternary operator------------
let age = 21;

 let age >= 18 ? "you're an adult" : "you're a minor";
 ----------------switch cases------------------
 let day = 1;

switch () {
    case day === 1:
        console.log('Today is Monday');
        break;
    case day === 2:
        console.log('Today is Tuesday');
        break;
    case day === 3:
        console.log('Today is Wednesday');
        break;
    case day === 4:
        console.log('Today is Thursday');
        break;
    case day === 5:
        console.log('Today is Friday');
        break;
    case day === 6:
        console.log('Today is Saturday');
        break;
    case day === 7:
        console.log('Today is Sunday');
        break;
    default:
        console.log('Invalid day');
}
-------------JSON----------------
const users = {
    id: 1,
    username: "dcde",
    memberSince: 2017,
};

const json = JSON.stringify(users, null, '\t');

console.log(json);
const records = `[
{"id":1, "username": "dcode", "memberSince": 2017},
  {"id":2, "username": "jdoe", "memberSince": 2019},
  {"id":3, "username": "admin", "memberSince": 2015}
]`;

const users = JSON.parse(records);

for(const u of users){
    console.log(u.username)
}
------------includes----------------------
const numbers = [1, 4, 9, 16, 25, 36, 49, 64];


console.log(numbers.includes(25, -5))
-----------------from-----------------
const username = 'dcode';
const usernameAsArray = Array.from(username, character =>{
    return character.toUpperCase();
});

console.log(usernameAsArray)
--------------with---------------------------
const hobbies = ['tennis', 'reading', 'gym'];
const newHobbies = hobbies.with(1, 'coding');
console.log(hobbies)
console.log(newHobbies)
----------------------flat---------------
const keyValuePairs = [
    ["username", "dcode"],
    ['memberSince', '2017'],
];

console.log(keyValuePairs.flat())
/3darray.flat()
const array3d = [
    1,
    2,
    [
        3,
        [
            4,
            5,
        ]
    ]
];

console.log(array3d.flat(2))
------------freeze--------
let user = {
    username: "dcode",
    memberSince: "2017",
}
Object.freeze(user)
user.memberSince = '2018';
user.active = true;
delete user.username
console.log(user)
---------failed weather app code-----
const api = {
    key: '0683eb0606334b98c7f51d904ff7e81f',
    baseURL: 'https://api.openweathermap.org/data/3.0/',
};

const searchBox = document.querySelector('.search-box');

searchBox.addEventListener('keypress', setQuery)

function setQuery(e){
    if(e.keyCode == 13){
        getResults(searchBox.value)
        console.log(searchBox.value);
        
    }
}

function getResults(query){
    fetch(`${api.baseURL}.weather?q=${query}&units=metric&APPID=${api.key}`)
    .then(weather =>{
        return weather.json();
    }).then(displayResults)
}
function displayResults(weather) {
    console.log(weather);
    let city = document.querySelector(".location .city")
    city.innerHTML = `${weather.name}, ${weather.sys.country}`;

    let now = new Date();
    let date = document.querySelector('.location .date')
    date.innerHTML = dateBuilder(now)
}
function dateBuilder(s){
    let months = ['January', 'february', 'march', 'april', 'may', 'june', 'july', 'august', 'september', 'october', 'november', 'december'];
    let days = ['sunday', 'monday', 'thuesday', 'wednesday', 'thursday', 'friday', 'saturday'];


    let day = days[s.geyDay()];
    let date = s.getDate();
    let month = months[s.getMonth]
    let year = s.getFullYear();

    return `${day} ${date} ${month} ${year}`;
};
----------------failed face detection codes------------------
const video = document.getElementById('video')

Promise.all([
  faceapi.nets.tinyFaceDetector.loadFromUri('/models'),
  faceapi.nets.faceLandmark68Net.loadFromUri('/models'),
  faceapi.nets.faceRecognitionNet.loadFromUri('/models'),
  faceapi.nets.faceExpressionNet.loadFromUri('/models')
]).then(startVideo)

function startVideo() {
  navigator.getUserMedia(
    { video: {} },
    stream => video.srcObject = stream,
    err => console.error(err)
  )
}

video.addEventListener('play', () => {
  const canvas = faceapi.createCanvasFromMedia(video)
  document.body.append(canvas)
  const displaySize = { width: video.width, height: video.height }
  faceapi.matchDimensions(canvas, displaySize)
  setInterval(async () => {
    const detections = await faceapi.detectAllFaces(video, new faceapi.TinyFaceDetectorOptions()).withFaceLandmarks().withFaceExpressions()
    const resizedDetections = faceapi.resizeResults(detections, displaySize)
    canvas.getContext('2d').clearRect(0, 0, canvas.width, canvas.height)
    faceapi.draw.drawDetections(canvas, resizedDetections)
    faceapi.draw.drawFaceLandmarks(canvas, resizedDetections)
    faceapi.draw.drawFaceExpressions(canvas, resizedDetections)
  }, 100)
})
-----------simple redux counter---------------
import { createSlice } from "@reduxjs/toolkit";


export const counterSlice = createSlice({
    name: 'counter',
    initialState: {count: 0},
    reducers:{
        increment: (state) => {
            state.count += 1;
        },
        decrement: (state) => {
            state.count -= 1;
        }
    }
});

export const {increment, decrement} = counterSlice.actions;

export default counterSlice.reducer;
--------stack algoritmes-------
class Stack{
    constructor(){
        this.items = []
        this.count = 0
    }

    push(element){
        this.items[this.count] = element
        console.log(`${element} added to ${this.count}`);
        this.count += 1
        
        
        return this.count - 1
    }
    pop(){
        if(this.count == 0) return undefined
        let deleteItem = this.items[this.count - 1]
        this.count -= 1
        console.log(`${deleteItem} removed`);
        
        return deleteItem;
    }
}

const stack = new Stack()

stack.push(100)
stack.push(200)
stack.push(300)

stack.pop()
stack.pop()
stack.pop()
stack.pop()
--------------function------------

const array = [1, 3, 5, 7, 5, 3, 9, 4, 7]

function sum(arr){
    let sum = 0;
    for(const val of arr){
        sum += val;
    }
    return sum;
}
sum([1, 3, 5,7]);
-------reducer function------------
const array = [1, 3, 5, 7, 5, 3, 9, 4, 7]

function sum(arr){
    const reducer = (total, value) => total + value;
    const initialvalue = 0;
    return arr.reduce(reducer, initialvalue);
}

sum(array)/
const array = [
    {item: 'imac', price: 100}, 
    {item: 'ipad', price: 500}
]

const sum = array.reduce((total, item) => total + item, 0)

sum
console.log(sum);/
const dates = [
    '01/08/2022',
    '02/08/2022',
    '04/08/2022',
    '04/07/2022'
].map(v => new Date(v))
dates
const maxDate = dates.reduce((max,d) => d > max ? d : max, dates[0]);

maxDate
------------js debugging methods------
const button = document.querySelector('.button')
const inputs = document.querySelectorAll('.input')
const result = document.querySelector('.result')

const getUsername =()=>{
    return inputs[0].value;
};

const getAge = () => {
    return inputs[1].value;
}


button.addEventListener('click', ()=>{
    // debugger;
    const username = getUsername()
    const age = getAge()

    result.textContent = `${username} is ${age} years old`
})
------------map---------------------
const numberArray = [2, 3, 4, 5, 35]
const doubleArra = numberArray.map(numberArray =>{
    return numberArray * 2
})
console.log(doubleArra);
/////////////
const makeDouble = numberItem => numberItem * 2

const numberArray = [2, 3, 4, 5,35];
const doubleArray = numberArray.map(makeDouble);


const doubleArray2 = numberArray.map(n => n * 2);

console.log(doubleArray);
//////////////////////////////
const myName = 'Asadprox'
const nameArray = myName.split('');
const newName = myName.split('').map(l => `${l}${l}`)

console.log(newName);

const joinedNewName = newName.join('')

joinedNewName
////////////////////////
const count = true;

let countValu = new Promise(function(resolve, reject){
    if(count){
        resolve('there is a count value');
    }else{
        reject('there is no count value')
    }
});
console.log(countValu);
---------------promise----------

//////////////////
let promise = new Promise(function(resolve, reject){
    setTimeout(() => resolve('done'), 5000)
})

promise.then((success)=> console.log(success))

-------------react use state-----------------
import { useState } from 'react'

import './App.css'

function App() {
  const [count, setCount] = useState(0)
    const increment = () =>{
        setCount(count+1)
    }
    const decrement = () =>{
        setCount(count-1)

    }
  return (
    <>
      <div>
      <h1>counter app</h1>
        <p>the count is: {count}</p>
        <button onClick={decrement}>+</button>
        <button onClick={increment}>-</button>
      </div>
    </>
  )
}

export default App
-----error handling--------------

try{
    console.log(asad);
    console.log('try block will throw you error');
    
}catch(err){
    console.log(err.name);
    console.log(err.message);
    console.log('catch block will caught it');
}finally{
    console.log('this is finally block');
    
}
-------------------stopwatch project-------------
import React, { useEffect, useState } from 'react'
import './App.css'
 const App = () => {
  const [time, setTime] = useState(0)
  const [running, setRunning] = useState(false)

  useEffect(()=> {
    let interval;
    if(running){
      interval = setInterval(() => {
        setTime((prevTime) => prevTime + 10)
      }, 10)
    }else if(!running){
      clearInterval(interval)
    }
    return () => clearInterval(interval)
  }, [running])
  return (
    <>
      <h1>01-StopWatch</h1>
      <div>
        <span>{('0' + Math.floor((time / 60000) % 60)).slice(-2)}</span>
        <span>{('0' + Math.floor((time / 1000) % 60)).slice(-2)}:</span>
        <span>{('0' + Math.floor((time / 10) % 60)).slice(-2)}</span>
      </div>
      <div>
        <button onClick={()=>{setRunning(true)}}>Start</button>
        <button onClick={()=>{setRunning(false)}}>Stop</button>
        <button onClick={()=>{setRunning(0)}}>Reset</button>
      </div>
    </>
  )
}
export default App;
---------------JSON---------------
{
    "key": "value",
    "favoritenumber": 3,
    "isprogrammer": true,
    "hobbies": ["Weigth lifting", "Bowling"],
    "friends": [{
        "name": "Joey",
        "Surname": "Adamson",
        "typeofGame": true
    }]

}
------------while loop in JS---------
let i = 0;
while(i < 10){
    i++;
    if (i === 5) continue;
    console.log(i);

}
------------------do while loop------
let i = 0;
do{
    i++;
    if (i === 5) continue;
    console.log(i);

}while(i < 10)
-----charAt method---------
let myVar = 'Matmatics';

console.log(myVar.charAt(7));
/this methos defines a number of string which is located
--------nested functions in js-----------------
let x = 1

const parent =() =>{
    let myValue = 2;
    console.log(x)
    console.log(myValue)

    const child = () => {
        console.log(x += 5)
        console.log(myValue += 1)

    }

    child()
}

parent()
---------------------------------------
const arr = [23,45,64,78,96,34]
console.log(met1(arr))

function met1(arr){
    let sum = 0;
    let i = 0;
    while(i < arr.length){
        sum += arr [i]
        i++
    }
    return sum;
}
--------------annotating in typescript------------
let me: number = 2;
let python: string = 'programming language';
-------------any type------------------------
let tech = 'Typescript';

console.log( typeof tech);

tech = 'javascript';

let isHard: boolean = true;
let matter: any = 'ggggg';

matter = 3;
matter = null;
matter = false;
-------------------------------------------
let numbers: number[] = [1,2,3,4,5,6]
--------------Objects in Typescript--------
function print(): {name:string, age:number, loc:string}{
    return{
        name: 'asadprox',
        age: 16,
        loc: 'Uzb'
    }
}
-----------getting a date in react-------------
      <article>{date.getDate()}</article>

const ValidPassword = () => <h1>valid ValidPasswrd</h1>
const InvalidPassword = () => <h1>invalid ValidPasswrd</h1>


const Password = ({ isValid }) => {
  // if(isValid){
  //   return <ValidPassword/>
  // }
  // return <InvalidPassword/>

  return isvalid ? <ValidPassword/> : <InvalidPassword/>
}


const App = () => {
  return (
    <div>
      <Password isValid={false}/>
    </div>
  )
}

export default App
------------------------------------
const Cart = () => {
  const items: string[] = ['Wireless Earbuds', 'New SSD', 'Hoddie', 'Laptop'];



  return(
    <div>
    <h1>Cart</h1>
      {items.length > 0 && <h2>You have {items.length} items in your cart</h2>}
    </div>

  )
}


const App = () => {
  return (
    <div>
      <Cart/>
    </div>
  )
}

export default App
// let baseSalary = 30_000;
// let overtime = 10;
// let rate = 20;

// function getWage(baseSalary, overtime, rate){
//     return baseSalary + (overtime * rate);
// }

// let employee = {
//     baseSalary: 30_000,
//     overtime: 10,
//     rate: 20,
//     getWage: function(){
//         return this.baseSalary + (overtime * rate);
//     }
// }

// employee.getWage();

// -------------------------------------

// function createCircle(radius){
//     return {
//         radius,
//         draw: function(){
//             console.log('draw')
//         }
//     }
// }

// const circle = createCircle(1)



// function Circle(radius){
//     console.log('this', this);
//     this.radius = radius;
//     this.draw = function(){
//         console.log('draw')
//     }
// }
// const another = new Circle(1)


// class Pent{
//     constructor(){
//         radiusY = 20;
//         radiusX = 20;
//         Space = {
//             x = 30,
//             y = 30,
//         }
//     }
// }
// const other  = new Pent();

new Number();
new String()
-----------------fiter--------
const number = [1, -1, 2, 3];

const filtered = number.filter(function(value){
    return value >= 0
})

console.log(filtered)

----------------ts seris-------------
'use strict'

console.log('typescript')
interface someValue{
    name: string,
    id: number
}

let obj: someValue ={
    name: 'ffff',
    id: 234,
}
console.log(obj)

let awesome:string = 'ddhdhdhdhdhd'
awesome = 'something'
awesome = awesome.toUpperCase()
console.log(awesome)

let amount:number = 20;
amount = 12 - 3;

let aws:boolean = false;

aws = true;
let greeting:string = 'hello';
greeting = greeting.toUpperCase();

let age:number = 45;
age = age = 5

let isAdult: boolean = age >= 18;
isAdult = !isAdult;
console.log(isAdult)
let tax:number | string | boolean = true;
tax = false;
tax = '$10'


let requestStatus: 'pending' | 'succes' | 'error' = 'pending';

requestStatus = 'error'
let books = ['1994', 'Brave new worls', 'fehrenheit 451'];

let foundBook:string | undefined;

for(let book of books){
    if(book === '1994'){
        foundBook = book;
        break;
    }
}
-----------failed fetchdata----------------

const App = () => {
  const url = 'https://www.course-api.com/react-tours-project'

  async function fetchData(url:string){
    try{
      const response = await fetch(url)
      if(!response.ok){
        throw new Error(`HTTP error! status: ${response.status}`)
      }
      const data = await response.json()
      console.log(data)
      return data
    }catch (error){
      const erroMsg = error instanceof Error? error.message: 'there was an error...'
      console.log(erroMsg);
      return [];
    }
  }
 const tour = await fetchData(url)
 tour.map((t:any)=> {
  console.log(tour.name)
 })
  return (
    <div>App</div>
  )
}

export default App
---------useState challenge----------
import React from 'react'
import { useState, useEffect } from 'react'
const App = () => {
  const [name, setName] = useState(() =>{
    const saveName = localStorage.getItem('name')
    return saveName ? JSON.parse(saveName) : '';
  })
  useEffect(() => {
    localStorage.setItem('name', JSON.stringify(name))
  }, [name])
  const handleChange = (event) => {
    setName(event.target.value)
  }
  const handleClear = () => setName('')
  return (
    <div>
      <h1>your name : {name}</h1>
      <input type="text" value={name} onChange={handleChange} placeholder='enter your name'/>
      <button onClick={handleClear}>Clear</button>
    </div>
  )
}

export default App
import React from 'react'
import { useState } from 'react'

const App = () => {
  const [todos, setTodos] = useState([])
  const [inputValue, setInputValue] = useState('')
  const handleSubmit = (e) => {
    e.preventDefault()
    if(inputValue.trim()){
      setTodos([...todos, inputValue]);
      setInputValue('')
    }
  }
  const handleChange = (e) => {
    setInputValue(e.target.value)
  }
  return (
    <div>
      <h1>Todo list</h1>
      <form onSubmit={handleSubmit}>
        <input type="text" onChange={handleChange} value={inputValue} placeholder='Add todo'/>
        <button type='submit'>add todo</button>
      </form>
      <ul>
        {todos.map((todo, index) => (
          <li key={index}>{todo}</li>
        ))}
      </ul>
    </div>
  )
}

export default App
let age = 15
let name = age > 10 ? 'asad'
let names = ['pedro', 'jessica', 'carol', 'pedro', 'pedro'];

names.filter((name)=> {
    return name !== 'pedro'
    console.log(names)
})

const number = [1, -2, 4, 5]
const sum = number.reduce((accumulator, currentvalue)=>{
    return accumulator + currentvalue
})
console.log(sum)
let money = '50.67';
// money = parseInt(money)
// money = +money
// money = Number(money)
// money = money.toString()
// money = String(money)
money = parseFloat(money)
console.log(money)
console.log( typeof money)
import React from 'react'
import {useState} from 'react'
const App = () => {
  const[count, setCount] = useState(1)
  const [names, setNames] = useState([
    'jphn',
    'joe',
    'asad'
  ])
  const[input, setInput] = useState("")
  return (
    <div>
      <h1>{count}</h1>
      <button onClick={()=> setCount(count + 1)}>+</button>
      <ul>
        {names.map((name)=>(
          <li key={Math.random() * 2}>{name}</li>
        ))}
      </ul>
      <input type='text' value={input} onChange={(e)=> setInput(e.target.value)}/>
      <button onClick={()=> setInput(e.push(name))}>add</button>
    </div>
  )
}

export default App

import React from 'react'
import { useState, useEffect} from 'react'
const App = () => {
  const[screen, setScreen] = useState(window.innerWidth)
  useEffect(()=> {
    window.addEventListener('resize', () => {
      setScreen(window.innerWidth)
    })
    
  }, [screen])
  return (
    <div>
      <section>{screen}</section>
    </div>
  )
}

export default App
let name = '            asad             ';
// let surname = 'ismoilov';
// let fullname = name.concat(surname)
// console.log(fullname)
// name += 'something else'
// console.log(name.length)
// console.log(name.toUpperCase())
// console.log(name.slice(1, 2))
// console.log(name.split('').join('-'))
    // console.log(name.includes('f'))
// console.log(name.trim())
// let plus = 9;
// let inus = 9
// let backtic = `${plus} + ${inus}`
// console.log(backtic)
// let fullname = 'robert';
// let lastname = 'rattinson'
// let overall = fullname + '' + lastname;
// console.log(overall.toLocaleUpperCase())
// let favactor = `my favorite actor is ${overall}`
// console.log(favactor)
// let money  = 50.9;
// money = +money
// money = parseInt(money)
// money = Number(money)
// console.log(money)
// console.log( typeof money)
// money = parseFloat(money)
// console.log(money)
// let a = 20
// let b = 20
// if(a > b){
//     console.log('a is greater then b')
// }else if (a < b){
//     console.log('a is less then b')
// }else{
//     console.log('first')
// }
// let time = 30;
// let greeting;
// if(time < 10){
//     greeting = 'good morning'
//     console.log(greeting)
// }else if(time < 20){
//     greeting = 'good day'
//     console.log(greeting)
// }else{
//     greeting = 'good evening'
//     console.log(greeting)
// }
// let password = 9;
// if(password <= 8){
//     console.log('welcome')
// }else if(password >= 8){
//     console.log('password is too short')
// }
// else if(password <= 8){
//     console.log('password should be 8 characters')
// }else{
//     console.log('please provide password')
// }
// let day = 'friday';
// switch(day){
//     case 'monday':
//         console.log('today is monday')
//         break;
//     case 'thuesday':
//         console.log('today is tuesday')
//         break;
//     case 'sunday':
//         console.log('today is sunday')
//         break;
//     case 'saturday':
//         console.log('today is saturday')
//         break;
//     default:
//         console.log('dont know what is today')                
// }
// let fruit = 'kiwi'
//  switch(fruit){
//     case 'orange':
//         console.log('i am not fan of orange')
//         break;
//     case 'apple':
//         console.log('how you like them apples')
//         break;       
//      default:
//         console.log('i never heard of that fruit')   
//  }
// function Loop(){
//     for (let i = 0; i < 100; i++){
//         console.log('asad', i)
//     }
// }
// Loop()
// for(let i = 1; i < 1000; i++){
//     console.log('asad', i)
// }
// let i = 0;
// while(i <= 5){
//     console.log('hello world')
//     i++;
// }
// let i = 10;
// while(i <= 100){
// console.log('asadprox', i)
// i++
// }
// let i = 1;
// do{
//     console.log('hello world')
//     i++;
// }while(i <= 5);
// let i = 20;
// do{
//     console.log('asad', i)
//     i++
// }while(i <= 400)
// let i = 2
// while(i < 100){
//     console.log('asadprox888', i)
//     i++
// }
// const a = true;
// const b = false;
// const c = 3;
// console.log(a > 2 && c < 2)
// console.log(a || b)
// console.log(b || b)
// console.log(!a)
// console.log(!b)
// let password = 'asadpox'
// if(password.length >= 8 || password.includes('pro')){
//     console.log('valid password')
// }else{
//     console.log('invalid password')
// }
// const myList = ['sum', 'some', 'beach', 'witch']
// console.log(myList)
// let num = [1,2,3,44,5,5,6,6,65,3,3,23,32,3]
// console.log(num)
// console.clear()
// const nested = [1, 2, 2,34,5,5 ['one', 'two'], 2,45,]
// console.log(nested[5])
// const letter = ['s', 'd', 't']
// const favSinger = ['alanwalker', 'john doe', 'rose']
// console.log(favSinger[0])
// const fruits = ['apples',
//     'banana',
//     'grape',
//     'strawberry'
// ]
// fruits.push('berry') add
// fruits.pop() remove
// fruits.shift() remove
// fruits.unshift('berry') add
// const fruits = ['apples', 'pomefranates', 'mongo']
// const moreFruits = ['strawberry', 'pineapple', 'grapefruite']
// const tatal = fruits.concat(moreFruits)
// console.log(tatal)
// const pl = ['javascript', 'golang', 'python', 'php']
// const numbers = [1,2,34,54,3,3,3,33]
// console.log(pl.includes('java'))
// console.log(pl.join('|'))
// console.log(pl.reverse())
// console.log(pl.slice(1, 3))
// console.log(numbers)
// console.log(numbers.sort())
// const person = {
//     name: 'asad',
//     lastName: 'ismoilov',
//     age: 16,
//     planet: 'earth',
//     isprogrammer: true,
// }
// delete person.age
// console.log(person.lastName)
// console.log(person.age)
// console.log(person.isprogrammer)
// console.log(person.name)
// const Toyota = {
//     type: 'B',
//     model: 'S class',
//     color: 'red',
// }
// console.log(typeof Toyota)
// car.wheels = 4;
// console.log(car)
// function greet( x, y){
// return x + y;

// }

// const res = greet(5, 9)
// console.log(res)
// function myFunc(p1, p2){
//     return p1 * p2
// }
// let x = myFunc(3, 8);
// console.log(x)
// function show(fn){
//     const value = 10;
//     fn(value)
// }
// show(function(value){
//     console.log(value)
// })
// function greet(name, cb){
//     console.log(`hello ${name}`)
//     cb()
// }
// function cb(){
//     console.log('i am callback')
// }
// greet('John', cb)
// function showCallFunction(fn){
//     const val = 10;
//     fn(val)
// }
// function fn(){
//     console.log(val)
// }
// let textMes = 'hey'
// console.log(textMes)
// function showMes(){
//     let textMessage = 'hello';
//     console.log(textMessage)
// }
// showMes()
// for(let i = 0; i < 5; i++){
//     console.log(i)
// }
// console.log(i)
// let phones = ['Appwrite', false, 'Samsung', 'Nokia', 'OPPO', ]
// phone.find((item, index, array)=> item.id == 3)
// console.log()
// console.log(phones.includes('Sumsung'))
// phones.forEach((item, index, array)=> console.log(item, index))
// let evanMorePhones = ['iphone 12', 'iphone 33']
// let CombineThem = phones.concat(evanMorePhones)
// console.log(CombineThem)
// console.log(phones.splice('Techno'))
// let Copy = phones.slice(1, 3)
// console.log(Copy)
// phones.unshift('Techno')
// phones.shift()
// phones.push('fuck')
// phones.pop()
// for(let phone of phones){
    // console.log(phone)
// }
// let nums = [1,2,3]
// let digits = nums
// console.log(nums === digits)
// function Read(){
//     return `hello my name is ${person.name} & i am ${person.age} years old`
// }
// const person ={
//     name: 'John',
//     age: 12,
//     Read,
// }
// console.log(person.Read())
// const person = {
//     name: 'asad',
//     age: 16,
//     greet: function(){
//         return `hello my name is ${person.name} & i am ${person.age}years old`
//     }
// }
// console.log(person.greet())
// const person = {
//     name: 'John Doe',
//     age: 23,
//     email: 'johnDoe234@gmail.com',
//     isSubscribed: true,
//     hobbies: ["Reading", "Running", "Cooking"],
//     address: {
//     city: "New York",
//         idk: true
//     },
// }
// const jsonStringify = JSON.stringify(person)
// const parsed = JSON.parse(jsonStringify)
// console.log(parsed)
// const currentDate = new Date(2024, 2, 24, 12, 20, 0, 0);
// console.log(currentDate)
// const date = new Date()
// const year = date.getFullYear()
// const month = new getMonth()
// const day = new getDay()
// console.log(`year ${year}`)
// console.log(`moth ${month}`)
// console.log(`day ${day}`)
// date.setDate(date.getDate() + 1)
// console.log(date.toDateString())
// console.log(date.toISOString())
// console.log(date)
// console.log(date.toLocaleDateString())
// setInterval(()=> console.log('this func will be executed in every 2 second'),
// 2000
// )
// setTimeout(function (){
//     console.log(`this  func tion will be exucuted after 3 seconds`)
// }, 3000)
// const intervalId = setInterval(function(){
//     console.log(`this is being executing in the interval`)
// },1000)
// console.log(intervalId)
// setTimeout(function(){
//     clearInterval(intervalId)
//     console.log(`interval stopping`)
// },10000)
// console.log('gggjjjjjjjjjjj\
//     hhhhhhhhhhhhhhh')
// console.log(`${['hh', 'hggg', 'hgg', 'jbg']}`)
// console.log(`
//     the quick
//     brown fox
//     jumps over
//     the lazy dog
//     `)
//     let name = 'asad'
//     let lastName = 'ismoilov'
//     console.log(`${name} my surname is ${lastName}`)
// const greet = (username) => `hello ${username}`
// console.log(greet('asad'))
// const double = (number)=> number * 2
// console.log(double(100))
// setTimeout(()=>{
//     console.log('hello')
//     setTimeout( () => {
//         console.log('hey')
//         setTimeout( ()=> {
//             console.log('namaste')
//             setInterval(()=> {
//                 console.log('hi')
//                 setTimeout(()=> {
//                     console.log('bonjour')
//                 },2000)
//             },2000)
//         }, 2000)
//     }, 2000)
// },2000)
// function user(name, age, work){
//     return{
//         name,
//         age,
//         work,
//         intro:() =>{
//             console.log(`my anem is ${name} i am ${age} years old i am ${work}`)
//         }
//     }
// }
// const asad = user('asad', 16, 'programmer')
// const alex = ('alex', 34, 'designer')
// console.log(asad.intro())
// const lib = {
//     sum: (a, b)=> {
//         return a + b
//     },
//     mult: (a, b)=> {
//         return a * b
//     },
// }
// console.log(lib.sum(2,4))
// console.log(lib.mult(2,4))
// const gertPersionES5 = (name, age, height) => {
//     return{
//         name,
//         age,
//         height,
//     }
// }
// const res = gertPersionES5('asad', 16, 1.82)
// console.log(res)
// function name(name = true){
//     if(name === true){
//         for(let i = 0; i <= 5; i++){
//             console.log(`${i}`)
//         }
//     }
// }
// name()
// function rating(rate){
//     if(rate === 5){
//         console.log(`hih ratings :)`)
//     }else if(rate === 0){
//         console.log('low Ratings :(')
//     }
// }
// rating(0)
// function multiply(a,b = 1){
//     return a * b
// }
// console.log(multiply(4)) 
// function giveMe4(a,b,c,d){
//     console.log('a', a)
//     console.log('b', b)
//     console.log('c', c)
//     console.log('d', d)
// }
// const colors = ['red', 'green', 'blue', 'teal']
// giveMe4(...colors)
// const strnums = ['one', 'two', 'three']
// const other = ['four', 'five', 'six']
// const concat = [...strnums, ...other]
// console.log(concat)
// let peoples = ['asad', 'alex', 'jordan']
// console.log(['kumar' ...peoples])
// 
// let person = {
//     name: 'asad',
//     age: 16,
//     gender: 'male'
// }
// const clone = {...person, work: 'Programmer', location: 'idk'}
// console.log(clone)
// let arr = [1,2,3];
// let arr2 = [4,5];
// let arr3 = [...arr, ...arr2]
// console.log(arr3)
// const user = {
//     name: 'jen',
//     age: 22,
// }
// const data = {...user, location: 'Termiz'}
// console.log(data)
// function user(x, ...userDate){
//     console.log(x)
//     console.log(userDate)
// }
// user('asad',15, 'programming')
// function person(name, lastname, ...hobbies){
//     console.log(name)
//     console.log(lastname)
//     console.log(hobbies)
// }
// person('asad', 'ismoilov', 'politics', 'geoghraphy')
// function variadic(...params){
//     console.log(params)
// }
// console.log('asad', 'ismoilov', 'go')
// const foo = ['one', 'two', 'three']
// const [one, two, three] = foo
// console.log(one)
// console.log(two)
// console.log(three)
// const [red, yellow, green, blue] = foo;
// console.log(green)
// let a,b 
// [a = 5, b = 8] = [1, 'two']
// console.log(b)
// function f(){
//     return [1, 2]
// }
// let a,b 
// [a, b] = f()
// console.log(a)
// console.log(b)
// function f(){
//     return [1,2,3]
// }
// const [a, , b] = f()
// console.log(a)
// console.log(b)
// const [a, ...b] = ['one', 'two', 'three']
// console.log(b)
// const colors = ['red', 'green', 'blue', 'yellow', 'orange']
// const [a, ...b] = colors
// console.log(b)
// const student = {name: 'asad', position: 'first', rollNumber: 23}
// const {name, position, rollNumber} = student;
// console.log(name)
// console.log(position)
// console.log(rollNumber)
// const person = {
//     name: 'asadpro888',
//     age: 16,
//     gender: 'male',
//     country: 'USA'
// }
// const {name, age, gender, country}  = person
// console.log(country)
// console.log(gender)
// console.log(name)
// console.log(age)
// const num = {x: 100, y: 200}
// console.log(x: new1, y: new2) = num
// console.log(new1)
// console.log(new2)
// let {a, b, ...rest} = {a: 100, b: 200, c: 300, d:400}
// console.log(a)
// console.log(b)
// console.log(rest)
// let name = 'asadprox8888'
// console.log(name.trim(''))
// class Track {
//     constructor(parama){
//         this.name = parama.name;
//         this.url = parama.url;
//     }
//     playTrack(){
//         console.log(`we started playing ${this.name}`)
//     }
// }
// class YoutubeTrack extends Track{
//     constructor(params){
//         super(params);
//         console.log('constructor youtube', params)
//         this.image = params.image
//     }
//     playTrack(){
//         console.log('hello youtube')
//     }
// }
// const track01 = new Track({
//     name: 'track01',
//     url: 'track01.mp3'
// })
// const track02 = new Track({
//     name: 'track02',
//     url: 'track02.mp3'
// })
// console.log(track01.name, 'track01')
// console.log(track02.name, 'track02')
// track01.playTrack()
// track02.playTrack()
// const youtubeTrack01 = new YoutubeTrack({
//     name: 'youtubetrack01',
//     url: 'youtubetrack01.mp3',
//     image: 'youtubetrack01.jpg'
// })
// const youtubeTrack02 = new YoutubeTrack({
//     name: 'youtubetrack02',
//     url: 'youtubetrack02.mp3',
//     image: 'youtubetrack02.jpg'
// })
// console.log(youtubeTrack01.playTrack)
// console.log(youtubeTrack02.playTrack)
// const Track = function(params){
//     console.log(params)
//     this.name = params.name;
//     this.url = params.url;
//     this.playTrack = function(){
//         console.log(`we started playing ${params.name}`)
//     }
// }
// const track01 = new Track({
//     name: 'track01',
//     url:'track01.mp3'
// })
// const track02 = new Track({
//     name: 'track02',
//     url:'track02.mp3'
// })
// track01.playTrack()
// track02.playTrack()
// ---------------------------------------
// console.log(getLanguages)
// function getLanguages(){
//     return ['javascript', 'python']
// }
// const person  = {
//     name: 'asadprox888',
//     age: 16,
//     country: 'USA'
// }
// function printPersonInfo({name, age, country}){
//     console.log(`Name: ${name}`)
//     console.log(`Age: ${age}`)
//     console.log(`Country: ${country}`)
// }
// printPersonInfo(person)
// let optioans = {
//     title: 'my menu',
//     items: ['item', 'item2']
// }
// function showMenu({title, width: w = 100, height: h = 200, items: [item, item2]}){
//     console.log(`${title} ${w} ${h}`)
//     console.log(item)
//     console.log(item2)
// }
// showMenu(optioans)
// const songs = [
//     {name: 'Houdini', singer: 'Eminem', duration: 4.34},
//     {name: 'I was nver there', singer: 'Weeknd', duration: 3.34},
//     {name: 'old town road', singer: 'Lil Nas X', duration: 2.34},
//     {name: 'Legit', singer: 'weeknd', duration: 4.24},
//     {name: 'Wake up', singer: 'Moondiety', duration: 1.34},
//     {name: 'Neon Blade', singer: 'Moondeity', duration: 2.34},
// ]
// const [, , , {singer: s}] = songs;
// console.log(singer)
const data = {
    user: {
        id: 123,
        name: 'asadprox',
        age: 16,
        email: 'asilbekismoilov220@gmail.com',
        address: {
            city: 'New York',
            country: 'USA',
        },
        hobbies: ['Reading', 'Painting', 'Cooking'],
        scores: {
            math: 95,
            science: 88,
            history: 75,
        },
    },
    products: [
        {id: 1, name: 'Laptop', price: 1000},
        {id: 2, name: 'Phone', price: 800},
        {id: 3, name: 'Tablet', price: 500},
    ],
    settings: {
        darkMode: true,
        notifications: {
            email: true,
            sms: false,
            push: true
        },
        language: 'English'
    },
};
const {
    user: {
        name, age, address: {city, country},
        hobbies,
        scores: {math, science, history},
        email,
    },
    products: [product1, product2, product3],
    settings: {
        darkMode,
        notifications: {
            email: emailNotification,
            sms: smsNotification,
            push: pushNotification,
        },
        language,
    },
}= data
