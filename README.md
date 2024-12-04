import {useEffect,useState} from 'react'

const App = () => {

  const [count,setCount] = useState(0)
  const [incrimentClicked,setIncrilmentClicked] = useState(false)
  const [decirlmentClicked,setDecirlmentClicked] = useState(false)

  useEffect(() => {setCount(number => number + 10)}, [incrimentClicked])
  useEffect(() => {setCount(number => number - 10)}, [decirlmentClicked])

  return (
    <div className='m-15'>
      <button className='bg-yellow-600' onClick={() => {setIncrilmentClicked(number => !number)}}>+10</button>
      <button className='bg-yellow-300' onClick={() => {setCount(number => number + 1)}}>+1</button> 
      <div className='size-16'>{count}</div>
      <button className='bg-orange-700' onClick={() => {setDecirlmentClicked(number => !number)}}>-10</button> 
      <button className='bg-orange-400' onClick={() => {setCount(number => number - 1)}}>-1</button>      
    </div>
  )
}

export default App
