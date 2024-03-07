// import { type } from '@testing-library/user-event/dist/type';
import React, { useReducer} from 'react'

export default function Component2() {
  let intialstate=1;
  const reduc=(state,action)=>{
console.log(state,action)
if(action.shahid==='inc')
{
  return state+1;
}
else if(action.shahid==="dec"){
  return state-1;
}
return state;
// return state;
  }
  const[state,dispatch]=useReducer(reduc,intialstate);
  return (
    <div>
    
    <h1>{state}</h1>
    
    <button onClick={()=>dispatch({shahid:"inc"})}>Change Data</button>
    <button onClick={()=>dispatch({shahid:"dec"})}>Change Data</button>
    </div>
  )
}
