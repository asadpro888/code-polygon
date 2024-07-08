
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
}
