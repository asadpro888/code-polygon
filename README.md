
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
