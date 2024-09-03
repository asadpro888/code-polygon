
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
