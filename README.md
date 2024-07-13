
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
